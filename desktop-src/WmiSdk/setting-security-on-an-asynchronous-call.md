---
description: As chamadas assíncronas apresentam sérios riscos à segurança porque um retorno de chamada para o coletor pode não ser resultado da chamada assíncrona pelo aplicativo ou script original.
ms.assetid: 2b839ea9-e1e6-4123-a98a-04ebee907b3b
ms.tgt_platform: multiple
title: Definindo a segurança em uma chamada assíncrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39f78315814d3b66c97e60a6b8045d7ea9e7afe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761544"
---
# <a name="setting-security-on-an-asynchronous-call"></a>Definindo a segurança em uma chamada assíncrona

As chamadas assíncronas apresentam sérios riscos à segurança porque um retorno de chamada para o [*coletor*](gloss-s.md) pode não ser resultado da chamada assíncrona pelo aplicativo ou script original. A segurança em conexões remotas é baseada na criptografia da comunicação entre o cliente e o provedor no computador remoto. No C++, você pode definir a criptografia por meio do parâmetro nível de autenticação na chamada para [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). Em script, defina o *AuthenticationLevel* na conexão do moniker ou em um objeto [**SWbemSecurity**](swbemsecurity.md) . Para obter mais informações, consulte [definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md).

Os riscos de segurança para chamadas assíncronas existem porque o WMI reduz o nível de autenticação em um retorno de chamada até que o retorno de chamada seja executado com sucesso. Em uma chamada assíncrona de saída, o cliente pode definir o nível de autenticação na conexão com o WMI. O WMI recupera as configurações de segurança na chamada do cliente e tenta chamar de volta com o mesmo nível de autenticação. O retorno de chamada é sempre iniciado no nível de **privacidade do PCT do \_ nível de \_ autenticação \_ \_ \_ RPC C** . Se o retorno de chamada falhar, o WMI reduzirá o nível de autenticação para um nível em que o retorno de chamada pode ter êxito, se necessário, para **RPC \_ C \_ Authn \_ nível \_ None**. No contexto de chamadas no sistema local em que o serviço de autenticação não é Kerberos, o retorno de chamada é sempre retornado no **\_ \_ \_ nível \_ None do RPC C Authn**.

O nível de autenticação mínimo é **RPC \_ C \_ Authn \_ nível \_ PKT** (**wbemAuthenticationLevelPkt** para scripting). No entanto, você pode especificar um nível mais alto, como a **wbemAuthenticationLevelPktPrivacy**(privacidade do PCT de nível de autenticação) do **RPC \_ C \_ \_ \_ \_** . É recomendável que os aplicativos cliente ou scripts definam o nível de autenticação para o padrão de **\_ \_ \_ nível \_** autentican do RPC C (**wbemAuthenticationLevelDefault**), que permite que o nível de autenticação seja negociado para o nível especificado pelo servidor.

O valor do registro **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault** controla se o WMI verifica um nível de autenticação aceitável em retornos de chamada. Esse é o único mecanismo para proteger a segurança do coletor para chamadas assíncronas feitas em scripts ou Visual Basic. Por padrão, essa chave do registro é definida como zero. Se a chave do registro for zero, o WMI não verificará os níveis de autenticação. Para proteger chamadas assíncronas em scripts, defina a chave do registro como 1. Os clientes C++ podem chamar [**IWbemUnsecuredApartment:: CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) para controlar o acesso ao coletor. O valor é criado em qualquer lugar por padrão.

Os tópicos a seguir fornecem exemplos de configuração de segurança de chamada assíncrona:

-   [Definindo a segurança em uma chamada assíncrona no VBScript](setting-security-on-an-asynchronous-call-in-vbscript.md)
-   Configurando a segurança de chamada assíncrona em C++

## <a name="setting-asynchronous-call-security-in-c"></a>Configurando a segurança de chamada assíncrona em C++

O método [**IWbemUnsecuredApartment:: CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) é semelhante ao método [**IUnsecuredApartment:: CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) e cria um coletor em um processo separado, Unsecapp.exe, para receber retornos de chamada. No entanto, o método **CreateSinkStub** tem um parâmetro *dwFlag* que especifica como o processo separado manipula o controle de acesso.

O parâmetro *dwFlag* especifica uma das seguintes ações para Unsecapp.exe:

-   Use a configuração chave do registro para determinar se deseja ou não verificar o acesso.
-   Ignore a chave do registro e sempre verifique o acesso.
-   Ignore a chave do registro e nunca Verifique o acesso.

O exemplo de código neste tópico requer a seguinte \# instrução include para compilação correta.


```C++
#include <wbemidl.h>
```



O procedimento a seguir descreve como executar uma chamada assíncrona com [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment).

**Para executar uma chamada assíncrona com IWbemUnsecuredApartment**

1.  Crie um processo dedicado com uma chamada para [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    O exemplo de código a seguir chama [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar um processo dedicado.

    ```C++
    CLSID                    CLSID_WbemUnsecuredApartment;
    IWbemUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_WbemUnsecuredApartment, 
                     NULL, 
                     CLSCTX_LOCAL_SERVER, 
                     IID_IWbemUnsecuredApartment, 
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

    O exemplo de código a seguir cria um stub para o coletor.

    ```C++
    LPCWSTR          wszReserved = NULL;           
    IWbemObjectSink* pStubSink   = NULL;
    IUnknown*        pStubUnk    = NULL; 

    pUnsecApp->CreateSinkStub(pSink,
                              WBEM_FLAG_UNSECAPP_CHECK_ACCESS,  //Authenticate callbacks regardless of registry key
                              wszReserved,
                              &pStubSink);
    ```

    

4.  Libere o ponteiro do objeto do coletor.

    Você pode liberar o ponteiro do objeto porque o stub agora possui o ponteiro.

    O exemplo de código a seguir libera o ponteiro do objeto.

    ```C++
    pSink->Release();
    ```

    

5.  Use o stub em qualquer chamada assíncrona.

    Quando terminar com a chamada, libere a contagem de referência local.

    O exemplo de código a seguir usa o stub em uma chamada assíncrona.

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    Às vezes, talvez seja necessário cancelar uma chamada assíncrona depois de fazer a chamada. Se você precisar cancelar a chamada, cancele a chamada com o mesmo ponteiro que originalmente fez a chamada.

    O exemplo de código a seguir descreve como cancelar uma chamada assíncrona.

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

6.  Libere a contagem de referência local quando terminar de usar a chamada assíncrona.

    Certifique-se de liberar o ponteiro *pStubSink* somente depois de confirmar que a chamada assíncrona não deve ser cancelada. Além disso, não libere *pStubSink* depois que o WMI liberar o ponteiro do coletor *pSink* . A liberação de *pStubSink* após o *pSink* cria uma contagem de referência circular na qual o coletor e o stub permanecem na memória para sempre. Em vez disso, um local possível para liberar o ponteiro está na chamada [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) , feita pelo WMI para relatar que a chamada assíncrona original foi concluída.

7.  Quando terminar, não inicializar com com uma chamada para [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

    O exemplo de código a seguir mostra como chamar [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) no ponteiro *pUnsecApp* .

    ```C++
    pUnsecApp->Release();
    ```

    

Para obter mais informações sobre a função [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) e os parâmetros, consulte a documentação [com](../cossdk/component-services-portal.md) .

 

 
