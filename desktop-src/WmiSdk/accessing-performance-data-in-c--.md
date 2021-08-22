---
description: A API de alto desempenho do WMI é uma série de interfaces que obtêm dados de classes de contador de desempenho.
ms.assetid: ee0a2ead-f53a-4651-a287-04a62eba3f84
ms.tgt_platform: multiple
title: Acessando dados de desempenho em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e566fb5803e598e42fac06d8f04fe3e71935008668e397a47d0226a96560eec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820323"
---
# <a name="accessing-performance-data-in-c"></a>Acessando dados de desempenho em C++

A API de alto desempenho do WMI é uma série de interfaces que obtêm dados de [classes de contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes). Essas interfaces exigem o uso de um objeto de [*atualização*](gloss-r.md) para aumentar a taxa de amostragem. Para obter mais informações sobre como usar o objeto atualizador no script, consulte [acessando dados de desempenho em](accessing-performance-data-in-script.md) tarefas de script e [WMI: monitoramento de desempenho](wmi-tasks--performance-monitoring.md).

As seções a seguir são discutidas neste tópico:

-   [Atualizando dados de desempenho](#refreshing-performance-data)
-   [Adicionando enumeradores ao atualizador de WMI](#adding-enumerators-to-the-wmi-refresher)
-   [Exemplo](#example)
-   [Tópicos relacionados](#related-topics)

## <a name="refreshing-performance-data"></a>Atualizando dados de desempenho

Um objeto de atualização aumenta o desempenho do cliente e do provedor de dados recuperando os dados sem cruzar os limites do processo. Se o cliente e o servidor estiverem localizados no mesmo computador, um atualizador carregará o provedor de alto desempenho em processo para o cliente e copiará os dados diretamente dos objetos do provedor para os objetos do cliente. Se o cliente e o servidor estiverem localizados em computadores diferentes, o atualizador aumentará o desempenho armazenando em cache objetos no computador remoto e transmitindo conjuntos de dados mínimos ao cliente.

Um atualizador também:

-   Reconecta automaticamente um cliente a um serviço WMI remoto quando ocorre um erro de rede ou o computador remoto é reiniciado.

    Por padrão, um atualizador tenta reconectar seu aplicativo ao provedor de alto desempenho relevante quando uma conexão remota entre os dois computadores falha. Para evitar a reconexão, passe o **\_ sinalizador WBEM \_ atualizar nenhum sinalizador de \_ \_ \_ reconexão automática** na chamada do método de [**atualização**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) . Os clientes de script devem definir a propriedade [**SWbemRefresher. falha**](swbemrefresher-autoreconnect.md) como **false**.

-   Carrega vários objetos e enumeradores fornecidos pelos mesmos ou provedores diferentes.

    Permite adicionar vários objetos, enumeradores ou ambos a um atualizador.

-   Enumera objetos.

    Assim como outros provedores, um provedor de alto desempenho pode enumerar objetos.

Depois de concluir a gravação do cliente de alto desempenho, talvez você queira melhorar o tempo de resposta. Como a interface [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) é otimizada para velocidade, a interface não é threadsafe intrinsecamente. Portanto, durante uma operação de atualização, não acesse o objeto ou a enumeração atualizável. Para proteger objetos entre threads durante chamadas de método **IWbemObjectAccess** , use os métodos [**IWbemObjectAccess:: Lock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-lock) e [**Unlock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-unlock) . Para melhorar o desempenho, sincronize seus threads para que você não precise bloquear threads individuais. A redução de threads e a sincronização de grupos de objetos para operações de atualização proporcionam o melhor desempenho geral.

## <a name="adding-enumerators-to-the-wmi-refresher"></a>Adicionando enumeradores ao atualizador de WMI

O número de instâncias e dados em cada instância são atualizados pela adição de um enumerador ao atualizador para que cada chamada para [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) resulte em uma enumeração completa.

O exemplo de código C++ a seguir requer as referências a seguir e \# inclui instruções para compilar corretamente.


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



O procedimento a seguir mostra como adicionar um enumerador a um atualizador.

**Para adicionar um enumerador a um atualizador**

1.  Chame o método [**IWbemConfigureRefresher:: AddEnum**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum) usando o caminho para o objeto atualizável e a interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .

    O atualizador retorna um ponteiro para uma interface [**IWbemHiPerfEnum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum) . Você pode usar a interface **IWbemHiPerfEnum** para acessar os objetos na enumeração.

    ```C++
    IWbemHiPerfEnum* pEnum = NULL;
    long lID;
    IWbemConfigureRefresher* pConfig;
    IWbemServices* pNameSpace;

    // Add an enumerator to the refresher.
    if (FAILED (hr = pConfig->AddEnum(
        pNameSpace, 
        L"Win32_PerfRawData_PerfProc_Process", 
        0, 
        NULL,
        &pEnum, 
        &lID)))
    {
        goto CLEANUP;
    }
    pConfig->Release();
    pConfig = NULL;
    ```

    

2.  Crie um loop que execute as seguintes ações:

    -   Atualiza o objeto usando uma chamada para [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh).
    -   Fornece uma matriz de ponteiros de interface [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) para o método [**IWbemHiPerfEnum:: GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects) .
    -   Acessa as propriedades do enumerador usando os métodos [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) passados para [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).

        Um identificador de propriedade pode ser passado para cada instância de [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) para recuperar o valor atualizado. O cliente deve chamar [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar os ponteiros **IWbemObjectAccess** retornados por [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).

## <a name="example"></a>Exemplo

O exemplo de código C++ a seguir enumera uma classe de alto desempenho, em que o cliente recupera um identificador de Propriedade do primeiro objeto e reutiliza o identificador para o restante da operação de atualização. Cada chamada para o método [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) atualiza o número de instâncias e os dados da instância.


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int __cdecl wmain(int argc, wchar_t* argv[])
{
    // To add error checking,
    // check returned HRESULT below where collected.
    HRESULT                 hr = S_OK;
    IWbemRefresher          *pRefresher = NULL;
    IWbemConfigureRefresher *pConfig = NULL;
    IWbemHiPerfEnum         *pEnum = NULL;
    IWbemServices           *pNameSpace = NULL;
    IWbemLocator            *pWbemLocator = NULL;
    IWbemObjectAccess       **apEnumAccess = NULL;
    BSTR                    bstrNameSpace = NULL;
    long                    lID = 0;
    long                    lVirtualBytesHandle = 0;
    long                    lIDProcessHandle = 0;
    DWORD                   dwVirtualBytes = 0;
    DWORD                   dwProcessId = 0;
    DWORD                   dwNumObjects = 0;
    DWORD                   dwNumReturned = 0;
    DWORD                   dwIDProcess = 0;
    DWORD                   i=0;
    int                     x=0;

    if (FAILED (hr = CoInitializeEx(NULL,COINIT_MULTITHREADED)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = CoInitializeSecurity(
        NULL,
        -1,
        NULL,
        NULL,
        RPC_C_AUTHN_LEVEL_NONE,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL, EOAC_NONE, 0)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = CoCreateInstance(
        CLSID_WbemLocator, 
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemLocator,
        (void**) &pWbemLocator)))
    {
        goto CLEANUP;
    }

    // Connect to the desired namespace.
    bstrNameSpace = SysAllocString(L"\\\\.\\root\\cimv2");
    if (NULL == bstrNameSpace)
    {
        hr = E_OUTOFMEMORY;
        goto CLEANUP;
    }
    if (FAILED (hr = pWbemLocator->ConnectServer(
        bstrNameSpace,
        NULL, // User name
        NULL, // Password
        NULL, // Locale
        0L,   // Security flags
        NULL, // Authority
        NULL, // Wbem context
        &pNameSpace)))
    {
        goto CLEANUP;
    }
    pWbemLocator->Release();
    pWbemLocator=NULL;
    SysFreeString(bstrNameSpace);
    bstrNameSpace = NULL;

    if (FAILED (hr = CoCreateInstance(
        CLSID_WbemRefresher,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemRefresher, 
        (void**) &pRefresher)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = pRefresher->QueryInterface(
        IID_IWbemConfigureRefresher,
        (void **)&pConfig)))
    {
        goto CLEANUP;
    }

    // Add an enumerator to the refresher.
    if (FAILED (hr = pConfig->AddEnum(
        pNameSpace, 
        L"Win32_PerfRawData_PerfProc_Process", 
        0, 
        NULL, 
        &pEnum, 
        &lID)))
    {
        goto CLEANUP;
    }
    pConfig->Release();
    pConfig = NULL;

    // Get a property handle for the VirtualBytes property.

    // Refresh the object ten times and retrieve the value.
    for(x = 0; x < 10; x++)
    {
        dwNumReturned = 0;
        dwIDProcess = 0;
        dwNumObjects = 0;

        if (FAILED (hr =pRefresher->Refresh(0L)))
        {
            goto CLEANUP;
        }

        hr = pEnum->GetObjects(0L, 
            dwNumObjects, 
            apEnumAccess, 
            &dwNumReturned);
        // If the buffer was not big enough,
        // allocate a bigger buffer and retry.
        if (hr == WBEM_E_BUFFER_TOO_SMALL 
            && dwNumReturned > dwNumObjects)
        {
            apEnumAccess = new IWbemObjectAccess*[dwNumReturned];
            if (NULL == apEnumAccess)
            {
                hr = E_OUTOFMEMORY;
                goto CLEANUP;
            }
            SecureZeroMemory(apEnumAccess,
                dwNumReturned*sizeof(IWbemObjectAccess*));
            dwNumObjects = dwNumReturned;

            if (FAILED (hr = pEnum->GetObjects(0L, 
                dwNumObjects, 
                apEnumAccess, 
                &dwNumReturned)))
            {
                goto CLEANUP;
            }
        }
        else
        {
            if (hr == WBEM_S_NO_ERROR)
            {
                hr = WBEM_E_NOT_FOUND;
                goto CLEANUP;
            }
        }

        // First time through, get the handles.
        if (0 == x)
        {
            CIMTYPE VirtualBytesType;
            CIMTYPE ProcessHandleType;
            if (FAILED (hr = apEnumAccess[0]->GetPropertyHandle(
                L"VirtualBytes",
                &VirtualBytesType,
                &lVirtualBytesHandle)))
            {
                goto CLEANUP;
            }
            if (FAILED (hr = apEnumAccess[0]->GetPropertyHandle(
                L"IDProcess",
                &ProcessHandleType,
                &lIDProcessHandle)))
            {
                goto CLEANUP;
            }
        }
           
        for (i = 0; i < dwNumReturned; i++)
        {
            if (FAILED (hr = apEnumAccess[i]->ReadDWORD(
                lVirtualBytesHandle,
                &dwVirtualBytes)))
            {
                goto CLEANUP;
            }
            if (FAILED (hr = apEnumAccess[i]->ReadDWORD(
                lIDProcessHandle,
                &dwIDProcess)))
            {
                goto CLEANUP;
            }

            wprintf(L"Process ID %lu is using %lu bytes\n",
                dwIDProcess, dwVirtualBytes);

            // Done with the object
            apEnumAccess[i]->Release();
            apEnumAccess[i] = NULL;
        }

        if (NULL != apEnumAccess)
        {
            delete [] apEnumAccess;
            apEnumAccess = NULL;
        }

       // Sleep for a second.
       Sleep(1000);
    }
    // exit loop here
    CLEANUP:

    if (NULL != bstrNameSpace)
    {
        SysFreeString(bstrNameSpace);
    }

    if (NULL != apEnumAccess)
    {
        for (i = 0; i < dwNumReturned; i++)
        {
            if (apEnumAccess[i] != NULL)
            {
                apEnumAccess[i]->Release();
                apEnumAccess[i] = NULL;
            }
        }
        delete [] apEnumAccess;
    }
    if (NULL != pWbemLocator)
    {
        pWbemLocator->Release();
    }
    if (NULL != pNameSpace)
    {
        pNameSpace->Release();
    }
    if (NULL != pEnum)
    {
        pEnum->Release();
    }
    if (NULL != pConfig)
    {
        pConfig->Release();
    }
    if (NULL != pRefresher)
    {
        pRefresher->Release();
    }

    CoUninitialize();

    if (FAILED (hr))
    {
        wprintf (L"Error status=%08x\n",hr);
    }

    return 1;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Classes de contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Acessando dados de desempenho no script](accessing-performance-data-in-script.md)
</dt> <dt>

[Atualizando dados do WMI em scripts](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[Tarefas do WMI: monitoramento de desempenho](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Monitorando dados de desempenho](monitoring-performance-data.md)
</dt> <dt>

[Qualificadores de propriedade para classes de contador de desempenho formatadas](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[Tipos de contador de desempenho WMI](wmi-performance-counter-types.md)
</dt> <dt>

[**Wmiadap.exe**](wmiadap.md)
</dt> <dt>

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> </dl>

 

 
