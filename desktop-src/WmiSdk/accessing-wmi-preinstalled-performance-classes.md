---
description: O repositório WMI contém classes de desempenho pré-instalado para todos os objetos de biblioteca de desempenho.
ms.assetid: 2158385f-d0dc-4102-84db-ce02d2b0ee53
ms.tgt_platform: multiple
title: Acessando classes de desempenho de WMI pré-instalado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656c3434d2f20bd73ae9ff5273f7e67439fc6caa01ac9ee5bf0283850e64b34a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131889"
---
# <a name="accessing-wmi-preinstalled-performance-classes"></a>Acessando classes de desempenho de WMI pré-instalado

O repositório WMI contém classes de desempenho pré-instalado para todos os objetos de biblioteca de desempenho. Por exemplo, instâncias da classe de desempenho de dados brutos do [**Win32 \_ PerfRawData \_ PerfProc \_ process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) representam processos. Esse objeto de desempenho é visível no monitor do sistema como o objeto de processo.

A propriedade **PageFaultsPerSec** do [**\_ \_ \_ processo Win32 PerfRawData PerfProc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) representa o contador de desempenho falhas de página por segundo para o processo. As [**classes \_ PerfFormattedData do Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contêm os valores de dados calculados exibidos no monitor do sistema (Perfmon.exe). O valor da propriedade **PageFaultsPerSec** do [**processo Win32 \_ PerfFormattedData \_ PerfProc \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) é o mesmo que aparece no monitor do sistema.

Use a [API com para WMI](com-api-for-wmi.md) ou a [API de script para](scripting-api-for-wmi.md) que o WMI acesse dados de desempenho por meio das [classes de contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes). Em ambos os casos, um objeto de [*atualização*](gloss-r.md) é necessário para obter cada exemplo de dados. Para obter mais informações e exemplos de código de script para usar atualizadores e acessar classes de desempenho, consulte [tarefas WMI: monitoramento de desempenho](wmi-tasks--performance-monitoring.md). Para obter mais informações, consulte [acessando dados de desempenho no script](accessing-performance-data-in-script.md).

## <a name="accessing-performance-data-from-c"></a>Acessando dados de desempenho do C++

O exemplo de código C++ a seguir usa o provedor de contador de desempenho para acessar classes de alto desempenho predefinidas. Ele cria um objeto de atualização e adiciona um objeto ao atualizador. O objeto é uma instância de [**processo do Win32 \_ PerfRawData \_ PerfProc \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) que monitora o desempenho de um processo específico. O código lê apenas uma propriedade Counter no objeto Process, a propriedade **VirtualBytes** . O código requer as referências a seguir e **\# inclui** instruções para compilar corretamente.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



O procedimento a seguir mostra como acessar dados de um provedor de alto desempenho em C++.

**Para acessar dados de um provedor de alto desempenho em C++**

1.  Estabeleça uma conexão com o namespace do WMI e defina a segurança do WMI usando uma chamada para [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) e [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

    Esta etapa é uma etapa padrão para a criação de qualquer aplicativo cliente WMI. Para obter mais informações, consulte [criando um aplicativo WMI usando C++](creating-a-wmi-application-using-c-.md).

2.  Crie um objeto de atualização usando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com CLSID \_ WbemRefresher. Solicite uma interface [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher) por meio do método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) . Solicite uma interface [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) por meio do método **QueryInterface** .

    A interface [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) é a interface principal para o objeto [**atualizador**](swbemrefreshableitem-refresher.md) WMI.

    O exemplo de código C++ a seguir mostra como recuperar [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher).

    ```C++
    IWbemRefresher* pRefresher = NULL;

    HRESULT hr = CoCreateInstance(
        CLSID_WbemRefresher,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemRefresher,
        (void**) &pRefresher);

    IWbemConfigureRefresher* pConfig = NULL;

    pRefresher->QueryInterface( 
        IID_IWbemConfigureRefresher,
        (void**) &pConfig
      );
    ```

    

3.  Adicione um objeto ao atualizador por meio de uma chamada para o método [**IWbemConfigureRefresher:: AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath) .

    Quando você adiciona um objeto ao atualizador, o WMI atualiza o objeto sempre que você chama o método [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) . O objeto que você adiciona designa o provedor em seus qualificadores de classe.

    O exemplo de código C++ a seguir mostra como chamar [**AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath).

    ```C++
    IWbemClassObject* pObj = NULL;
    IWbemServices* pNameSpace = NULL;

    // Add the instance to be refreshed.
    hr = pConfig->AddObjectByPath(
         pNameSpace,
         L"Win32_PerfRawData_PerfProc_Process.Name=\"WINWORD\"",
         0L,
         NULL,
         &pObj,
         NULL
    );
    if (FAILED(hr))
    {
       cout << "Could not add object. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       return hr;
    }
    ```

    

4.  Para configurar o acesso mais rápido ao objeto, conecte-se à interface [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) por meio de [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) na interface [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) .

    O exemplo de código C++ a seguir mostra como recuperar um ponteiro para o objeto usando [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) em vez de [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject).

    ```C++
        // For quick property retrieval, use IWbemObjectAccess.
        IWbemObjectAccess* pAcc = NULL;
        pObj->QueryInterface( IID_IWbemObjectAccess, (void**) &pAcc );
        // This is not required.
        pObj->Release();
    ```

    

    A interface [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) aumenta o desempenho porque você pode obter identificadores para propriedades de contador específicas e requer que você bloqueie e desbloqueie o objeto em seu código, que é uma operação que o [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) executa para cada acesso de propriedade.

5.  Obtenha os identificadores das propriedades para examinar usando chamadas para o método [**IWbemObjectAccess:: GetPropertyHandle**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyhandle) .

    As alças de propriedade são as mesmas para todas as instâncias de uma classe, o que significa que use o identificador de propriedade que você recupera de uma instância específica para todas as instâncias de uma classe específica. Você também pode obter um identificador de um objeto de classe para recuperar valores de propriedade de um objeto de instância.

    O exemplo de código C++ a seguir mostra como recuperar um identificador de propriedade.

    ```C++
        // Get a property handle for the VirtualBytes property
        long lVirtualBytesHandle = 0;
        DWORD dwVirtualBytes = 0;
        CIMTYPE variant;

        hr = pAcc->GetPropertyHandle(L"VirtualBytes",
             &variant,
             &lVirtualBytesHandle 
        );
        if (FAILED(hr))
        {
           cout << "Could not get property handle. Error code: 0x"
                << hex << hr << endl;
           return hr;
        }
    ```

    

6.  Crie um loop de programação que execute as seguintes ações:

    -   Atualize o objeto com uma chamada para [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) usando o ponteiro criado na chamada anterior para [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

        Nesta chamada, o atualizador WMI atualiza o objeto de cliente usando os dados que o provedor fornece.

    -   Execute qualquer ação conforme necessário no objeto, como recuperar um nome de propriedade, tipo de dados ou valor.

        Você pode acessar a propriedade por meio do identificador de propriedade obtido anteriormente. Devido à chamada de [**atualização**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) , o WMI atualiza a propriedade a cada vez pelo loop.

O exemplo de C++ a seguir mostra como usar a API de alto desempenho do WMI.


```C++
// Get the local locator object
IWbemServices* pNameSpace = NULL;
IWbemLocator* pWbemLocator = NULL;
CIMTYPE variant;
VARIANT VT;

CoCreateInstance( CLSID_WbemLocator, NULL,
    CLSCTX_INPROC_SERVER, IID_IWbemLocator, (void**) &pWbemLocator
);

// Connect to the desired namespace
BSTR bstrNameSpace = SysAllocString( L"\\\\.\\root\\cimv2" );

HRESULT hr = WBEM_S_NO_ERROR;

hr = pWbemLocator->ConnectServer(
     bstrNameSpace,      // Namespace name
     NULL,               // User name
     NULL,               // Password
     NULL,               // Locale
     0L,                 // Security flags
     NULL,               // Authority
     NULL,               // Wbem context
     &pNameSpace         // Namespace
);

if ( SUCCEEDED( hr ) )
{
    // Set namespace security.
    IUnknown* pUnk = NULL;
    pNameSpace->QueryInterface( IID_IUnknown, (void**) &pUnk );

    hr = CoSetProxyBlanket(
         pNameSpace, 
         RPC_C_AUTHN_WINNT, 
         RPC_C_AUTHZ_NONE, 
         NULL, 
         RPC_C_AUTHN_LEVEL_DEFAULT, 
         RPC_C_IMP_LEVEL_IMPERSONATE,
         NULL, 
         EOAC_NONE 
    );
    if (FAILED(hr))
    {
       cout << "Cannot set proxy blanket. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       return hr;
    }

    hr = CoSetProxyBlanket(pUnk, 
         RPC_C_AUTHN_WINNT, 
         RPC_C_AUTHZ_NONE, 
         NULL, 
         RPC_C_AUTHN_LEVEL_DEFAULT, 
         RPC_C_IMP_LEVEL_IMPERSONATE,
         NULL, 
         EOAC_NONE 
    );
    if (FAILED(hr))
    {
       cout << "Cannot set proxy blanket. Error code: 0x"
            << hex << hr << endl;
       pUnk->Release();
       return hr;
    }

    // Clean up the IUnknown.
    pUnk->Release();

    IWbemRefresher* pRefresher = NULL;
    IWbemConfigureRefresher* pConfig = NULL;

    // Create a WMI Refresher and get a pointer to the
    // IWbemConfigureRefresher interface.
    CoCreateInstance(CLSID_WbemRefresher, 
                     NULL,
                     CLSCTX_INPROC_SERVER, 
                     IID_IWbemRefresher, 
                     (void**) &pRefresher 
    );
    
    pRefresher->QueryInterface(IID_IWbemConfigureRefresher,
                               (void**) &pConfig );

    IWbemClassObject* pObj = NULL;

    // Add the instance to be refreshed.
    pConfig->AddObjectByPath(
       pNameSpace,
       L"Win32_PerfRawData_PerfProc_Process.Name=\"WINWORD\"",
       0L,
       NULL,
       &pObj,
       NULL 
    );
    if (FAILED(hr))
    {
       cout << "Cannot add object. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       
       return hr;
    }

    // For quick property retrieval, use IWbemObjectAccess.
    IWbemObjectAccess* pAcc = NULL;
    pObj->QueryInterface(IID_IWbemObjectAccess, 
                         (void**) &pAcc );

    // This is not required.
    pObj->Release();

    // Get a property handle for the VirtualBytes property.
    long lVirtualBytesHandle = 0;
    DWORD dwVirtualBytes = 0;

    pAcc->GetPropertyHandle(L"VirtualBytes", 
                            &variant, 
                            &lVirtualBytesHandle );

    // Refresh the object ten times and retrieve the value.
    for( int x = 0; x < 10; x++ )
    {
        pRefresher->Refresh( 0L );
        pAcc->ReadDWORD( lVirtualBytesHandle, &dwVirtualBytes );
        printf( "Process is using %lu bytes\n", dwVirtualBytes );
        // Sleep for a second.
        Sleep( 1000 );
    }
    // Clean up all the objects.
    pAcc->Release();
    // Done with these too.
    pConfig->Release();
    pRefresher->Release();
    pNameSpace->Release();
}
SysFreeString( bstrNameSpace );
pWbemLocator->Release();
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Classes de contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Tarefas do WMI: monitoramento de desempenho](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
