---
description: Instrumentação de Gerenciamento do Windows (WMI) pode criar o coletor para receber retornos de chamada assíncronos para um aplicativo cliente em um processo separado.
ms.assetid: 3d3111ac-7d83-48d6-94e4-36cb46a506fa
ms.tgt_platform: multiple
title: Reduzindo a segurança de um coletor em um processo separado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63aec8bcb451d254961acae8278cb45cb4454f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807199"
---
# <a name="lowering-the-security-for-a-sink-in-a-separate-process"></a>Reduzindo a segurança de um coletor em um processo separado

Instrumentação de Gerenciamento do Windows (WMI) pode criar o coletor para receber retornos de chamada assíncronos para um aplicativo cliente em um processo separado. O processo separado é Unsecapp.exe. Use a interface [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) . **IWbemUnsecuredApartment** permite que você controle se Unsecapp.exe autentica retornos de chamada para o coletor. Para obter mais informações, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).

Você pode reduzir a segurança nesse processo e o WMI pode acessar o coletor sem restrição. Para ajudar com essa técnica, o WMI fornece o Unsecapp.exe processo para funcionar como o processo separado. Você pode hospedar Unsecapp.exe com uma chamada para a interface [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) .

A interface [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) permite que um aplicativo cliente crie um processo dedicado separado executando Unsecapp.exe para hospedar uma implementação [**IWbemObjectSink**](iwbemobjectsink.md) . O processo dedicado pode chamar [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para conceder acesso de WMI ao processo dedicado sem comprometer a segurança do processo principal. Após a inicialização, o processo dedicado atua como um intermediário entre o processo principal e o WMI.

O procedimento a seguir descreve como executar uma chamada assíncrona com [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment).

**Para executar uma chamada assíncrona com IUnsecuredApartment**

1.  Crie um processo dedicado com uma chamada para [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    O exemplo de código a seguir chama [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar um processo dedicado.

    ```C++
    IUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_UnsecuredApartment, NULL, 
      CLSCTX_LOCAL_SERVER, IID_IUnsecuredApartment, 
      (void**)&pUnsecApp);
    ```

    

2.  Crie uma instância do objeto Sink.

    O exemplo de código a seguir cria um novo objeto de coletor.

    ```C++
    CMySink* pSink = new CMySink;
    pSink->AddRef();
    ```

    

3.  Crie um stub para o coletor.

    Um stub é uma função de wrapper produzida do coletor.

    O exemplo de código a seguir chama [**CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) para criar um stub para o coletor.

    ```C++
    IUnknown* pStubUnk = NULL; 
    pUnsecApp->CreateObjectStub(pSink, &pStubUnk);
    ```

    

4.  Chame [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para o wrapper e solicite um ponteiro para a interface [**IWbemObjectSink**](iwbemobjectsink.md) .

    O exemplo de código a seguir chama [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) e solicita um ponteiro para a interface [**IWbemObjectSink**](iwbemobjectsink.md) .

    ```C++
    IWbemObjectSink* pStubSink = NULL;
    pStubUnk->QueryInterface(IID_IWbemObjectSink, (void **)&pStubSink); pStubUnk->Release();
    ```

    

5.  Libere o ponteiro do objeto do coletor.

    Você pode liberar o ponteiro do objeto porque o stub agora possui o ponteiro.

    O exemplo de código a seguir libera o ponteiro do objeto do coletor.

    ```C++
    pSink->Release();
    ```

    

6.  Use o stub em qualquer chamada assíncrona.

    Quando terminar com a chamada, libere a contagem de referência local.

    O exemplo de código a seguir usa o stub em uma chamada assíncrona.

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    Às vezes, talvez seja necessário cancelar uma chamada assíncrona depois de fazer a chamada. Se você precisar cancelar a chamada, cancele a chamada com o mesmo ponteiro que originalmente fez a chamada.

    O exemplo de código a seguir mostra como cancelar uma chamada assíncrona.

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

7.  Libere a contagem de referência local quando terminar de usar a chamada assíncrona.

    Certifique-se de liberar o ponteiro *pStubSink* somente depois de confirmar que a chamada assíncrona não precisa ser cancelada. Além disso, não libere *pStubSink* depois que o WMI liberar o ponteiro do coletor *pSink* . A liberação de *pStubSink* após o *pSink* cria uma contagem de referência circular na qual o coletor e o stub permanecem na memória para sempre. Em vez disso, um local possível para liberar o ponteiro está na chamada [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) , feita pelo WMI para relatar que a chamada assíncrona original foi concluída.

8.  Quando terminar, não inicializar com com uma chamada para [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

    O exemplo de código a seguir mostra como chamar [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) no ponteiro *pUnsecApp* .

    ```C++
    pUnsecApp->Release();
    ```

    

    Os exemplos de código neste tópico exigem a referência a seguir e \# incluem a instrução para compilação correta.

    ```C++
    #include <wbemidl.h>
    #pragma comment(lib, "wbemuuid.lib")
    ```

    

Para obter mais informações sobre a função [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) e os parâmetros, consulte a documentação [com](../cossdk/component-services-portal.md) no SDK (Software Development Kit) da plataforma.

 

 
