---
description: Descreve como incluir o provedor COM WMI como um componente em um aplicativo em vez de em processo para o WMI. Chamado de provedor dissociado, esse é o tipo recomendado de provedor COM WMI a ser criado para o Windows 2000 e sistemas operacionais posteriores.
ms.assetid: a502f0dd-9add-4ebd-bc25-743a55eb78ac
ms.tgt_platform: multiple
title: Incorporando um provedor em um aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb544cd3b04cc75cef026bb2e4d2e579b8dbf135
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104551428"
---
# <a name="incorporating-a-provider-in-an-application"></a>Incorporando um provedor em um aplicativo

Ao criar um aplicativo que deve ser instrumentado, a prática recomendada é incluir o provedor como um componente dentro do próprio aplicativo. Essa prática permite que Instrumentação de Gerenciamento do Windows (WMI) interajam com o provedor de serviços diretamente, em vez de indiretamente por meio da API do programa. O desacoplamento do provedor do WMI também coloca o aplicativo no controle do ciclo de vida do provedor, em vez do WMI. Para obter mais informações sobre como gravar um provedor que é executado no processo WMI, consulte [fornecendo dados ao WMI escrevendo um provedor](supplying-data-to-wmi-by-writing-a-provider.md). Para obter mais informações sobre o modelo de hospedagem e as configurações de segurança para o provedor, consulte [hospedagem e segurança do provedor](provider-hosting-and-security.md).

O diagrama a seguir ilustra a relação entre o WMI, um provedor dissociado e um aplicativo.

![relação entre WMI, provedor dissociado e aplicativo](images/decoupledprov.png)

Para obter mais informações sobre métodos de provedor desacoplados, consulte [**IWbemDecoupledRegistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar) e [**IWbemDecoupledBasicEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider).

> [!Note]  
> O provedor dissociado dá suporte a instâncias, métodos, provedores de eventos e consumidores de eventos. Ele não dá suporte a provedores de propriedades e de classes. Para obter mais informações, consulte [escrevendo um provedor de classe](writing-a-class-provider.md) e [gravando um provedor de propriedades](writing-a-property-provider.md).

 

Os exemplos de código neste tópico exigem as referências a seguir e \# incluem instruções para compilar corretamente.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



O procedimento a seguir usa exemplos de código C++ para descrever como incorporar um provedor dissociado em seu aplicativo. O método de inicialização do aplicativo executa as etapas a seguir para que o WMI interaja apenas com um provedor dissociado registrado.

**Para implementar um provedor dissociado em um aplicativo C++**

1.  Inicialize a biblioteca COM para uso pelo thread de chamada.

    O exemplo de código a seguir mostra como inicializar a biblioteca COM.

    ```C++
    HRESULT hr = S_OK ;
    hr = CoInitializeEx (0, COINIT_MULTITHREADED );
    ```

    

2.  Defina o nível de segurança do processo padrão.

    Esse nível estabelece o nível de segurança necessário para que outros processos acessem as informações do processo do cliente. O nível de autenticação deve ser o padrão de nível da autenticação RPC \_ C \_ \_ \_ . Para obter mais informações, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md).

    O exemplo de código a seguir mostra como definir o nível de segurança padrão.

    ```C++
    hr = CoInitializeSecurity (NULL, 
        -1, 
        NULL, 
        NULL,
        RPC_C_AUTHN_LEVEL_DEFAULT,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL, 
        EOAC_DYNAMIC_CLOAKING, 
        NULL);

    if (FAILED(hr))
    {
      CoUninitialize();
      cout << "Failed to initialize security. Error code = 0x"
           << hex << hr << endl;
      return;
    }
    ```

    

3.  Registre o registrador de provedor dissociado.

    O exemplo de código a seguir mostra como registrar o registrador de provedor dissociado.

    ```C++
    CLSID CLSID_WbemDecoupledRegistrar;
    IID IID_IWbemDecoupledRegistrar;
    IWbemDecoupledRegistrar *myRegistrar = NULL;

    hr = CoCreateInstance(CLSID_WbemDecoupledRegistrar,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IWbemDecoupledRegistrar,
                          (void**)&myRegistrar);
    if (SUCCEEDED(hr))
    {
        IUnknown *pIUnknown = NULL;
        // CMyProv is the class added for WMI instance / event provider
        HRESULT hr = CMyProv::CreateInstance(NULL,&pIUnknown);
        if ( SUCCEEDED(hr))
        {
            hr = myRegistrar->Register(0,
                NULL,
                NULL,
                NULL,
                L"root\\cimv2",
                L"DecoupledInstanceProvider",
                pIUnknown);

                pIUnknown->Release();
        }
    }

    if (FAILED (hr))
    {
        if ( myRegistrar )
        {
            myRegistrar->Release () ;
        }
    }
    ```

    

4.  Registre o provedor de eventos dissociado.

    O exemplo de código a seguir mostra como registrar o provedor de eventos dissociado.

    ```C++
    IWbemDecoupledBasicEventProvider *myEvtRegistrar;

    // -- Create an instance of IWbemDecoupledEventProvider
    hr = CoCreateInstance(CLSID_WbemDecoupledBasicEventProvider,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IWbemDecoupledBasicEventProvider,
                          (void**)&myEvtRegistrar);

    if (SUCCEEDED(hr))
    {
       // -- Register the DecoupledEventProvider
       hr = myEvtRegistrar->Register(0,
                                     NULL,
                                     NULL,
                                     L"root\\cimv2",
                                     L"DecoupledEventProvider",
                                     NULL, NULL);
       if (SUCCEEDED(hr))
       {
          IWbemServices *pService = NULL;
          hr = myEvtRegistrar->GetService (0, NULL, &pService);
          if (SUCCEEDED(hr))
          {
             IWbemObjectSink *pSink = NULL;
             hr = myEvtRegistrar->GetSink ( 0, NULL, &pSink );
             if (SUCCEEDED(hr))
             {
                // Provide events
             }
          }
       } 
    }
    ```

    

5.  Faça as [chamadas para o WMI](making-calls-to-wmi.md) exigidas pela funcionalidade do provedor. Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md). Para obter mais informações se o provedor tiver uma solicitação de dados de um script ou aplicativo, consulte [representando um cliente](impersonating-a-client.md).

Antes de terminar, o aplicativo deve ser limpo após ele mesmo. O procedimento a seguir descreve como cancelar o registro do provedor dissociado para que o WMI não tente consultá-lo para obter informações.

O procedimento a seguir descreve como cancelar o registro do provedor dissociado.

**Para cancelar o registro do provedor dissociado**

1.  Cancelar o registro e liberar o registrador.

    O exemplo de código a seguir mostra como cancelar o registro e liberar o registrador.

    ```C++
    myRegistrar->UnRegister();
    myRegistrar->Release();
    ```

    

2.  Cancelar o registro e liberar o provedor de eventos.

    O exemplo de código a seguir mostra como cancelar o registro e liberar o provedor de eventos.

    ```C++
    myEvtRegistrar->UnRegister();
    myEvtRegistrar->Release();
    ```

    

3.  Limpe o servidor COM.

    O exemplo de código a seguir mostra como cancelar a inicialização da biblioteca COM.

    ```C++
    CoUninitialize();
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protegendo seu provedor](securing-your-provider.md)
</dt> <dt>

[Desenvolvendo um provedor WMI](developing-a-wmi-provider.md)
</dt> </dl>

 

 



