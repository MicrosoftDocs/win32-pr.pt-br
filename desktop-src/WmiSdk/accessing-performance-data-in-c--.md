---
description: A API de alto desempenho do WMI é uma série de interfaces que obtêm dados de classes de contador de desempenho.
ms.assetid: ee0a2ead-f53a-4651-a287-04a62eba3f84
ms.tgt_platform: multiple
title: Acessando dados de desempenho em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b076e1ab15b934f347ee491711d7d3d1b8fbbe0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813296"
---
# <a name="accessing-performance-data-in-c"></a><span data-ttu-id="1bffa-103">Acessando dados de desempenho em C++</span><span class="sxs-lookup"><span data-stu-id="1bffa-103">Accessing Performance Data in C++</span></span>

<span data-ttu-id="1bffa-104">A API de alto desempenho do WMI é uma série de interfaces que obtêm dados de [classes de contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span><span class="sxs-lookup"><span data-stu-id="1bffa-104">The WMI high-performance API is a series of interfaces that obtain data from [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="1bffa-105">Essas interfaces exigem o uso de um objeto de [*atualização*](gloss-r.md) para aumentar a taxa de amostragem.</span><span class="sxs-lookup"><span data-stu-id="1bffa-105">These interfaces require use of a [*refresher*](gloss-r.md) object to increase the sampling rate.</span></span> <span data-ttu-id="1bffa-106">Para obter mais informações sobre como usar o objeto atualizador no script, consulte [acessando dados de desempenho em](accessing-performance-data-in-script.md) tarefas de script e [WMI: monitoramento de desempenho](wmi-tasks--performance-monitoring.md).</span><span class="sxs-lookup"><span data-stu-id="1bffa-106">For more information about using the refresher object in scripting, see [Accessing Performance Data in Script](accessing-performance-data-in-script.md) and [WMI Tasks: Performance Monitoring](wmi-tasks--performance-monitoring.md).</span></span>

<span data-ttu-id="1bffa-107">As seções a seguir são discutidas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="1bffa-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="1bffa-108">Atualizando dados de desempenho</span><span class="sxs-lookup"><span data-stu-id="1bffa-108">Refreshing Performance Data</span></span>](#refreshing-performance-data)
-   [<span data-ttu-id="1bffa-109">Adicionando enumeradores ao atualizador de WMI</span><span class="sxs-lookup"><span data-stu-id="1bffa-109">Adding Enumerators to the WMI Refresher</span></span>](#adding-enumerators-to-the-wmi-refresher)
-   [<span data-ttu-id="1bffa-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1bffa-110">Example</span></span>](#example)
-   [<span data-ttu-id="1bffa-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1bffa-111">Related topics</span></span>](#related-topics)

## <a name="refreshing-performance-data"></a><span data-ttu-id="1bffa-112">Atualizando dados de desempenho</span><span class="sxs-lookup"><span data-stu-id="1bffa-112">Refreshing Performance Data</span></span>

<span data-ttu-id="1bffa-113">Um objeto de atualização aumenta o desempenho do cliente e do provedor de dados recuperando os dados sem cruzar os limites do processo.</span><span class="sxs-lookup"><span data-stu-id="1bffa-113">A refresher object increases data provider and client performance by retrieving data without crossing process boundaries.</span></span> <span data-ttu-id="1bffa-114">Se o cliente e o servidor estiverem localizados no mesmo computador, um atualizador carregará o provedor de alto desempenho em processo para o cliente e copiará os dados diretamente dos objetos do provedor para os objetos do cliente.</span><span class="sxs-lookup"><span data-stu-id="1bffa-114">If both the client and the server are located on the same computer, a refresher loads the high-performance provider in-process to the client, and copies data directly from provider objects into client objects.</span></span> <span data-ttu-id="1bffa-115">Se o cliente e o servidor estiverem localizados em computadores diferentes, o atualizador aumentará o desempenho armazenando em cache objetos no computador remoto e transmitindo conjuntos de dados mínimos ao cliente.</span><span class="sxs-lookup"><span data-stu-id="1bffa-115">If the client and the server are located on different computers, the refresher increases performance by caching objects on the remote computer, and transmitting minimal data sets to the client.</span></span>

<span data-ttu-id="1bffa-116">Um atualizador também:</span><span class="sxs-lookup"><span data-stu-id="1bffa-116">A refresher also:</span></span>

-   <span data-ttu-id="1bffa-117">Reconecta automaticamente um cliente a um serviço WMI remoto quando ocorre um erro de rede ou o computador remoto é reiniciado.</span><span class="sxs-lookup"><span data-stu-id="1bffa-117">Automatically reconnects a client to a remote WMI service when a network error occurs, or the remote computer is restarted.</span></span>

    <span data-ttu-id="1bffa-118">Por padrão, um atualizador tenta reconectar seu aplicativo ao provedor de alto desempenho relevante quando uma conexão remota entre os dois computadores falha.</span><span class="sxs-lookup"><span data-stu-id="1bffa-118">By default, a refresher attempts to reconnect your application to the relevant high-performance provider when a remote connection between the two computers fails.</span></span> <span data-ttu-id="1bffa-119">Para evitar a reconexão, passe o **\_ sinalizador WBEM \_ atualizar nenhum sinalizador de \_ \_ \_ reconexão automática** na chamada do método de [**atualização**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) .</span><span class="sxs-lookup"><span data-stu-id="1bffa-119">To prevent the reconnection, pass the **WBEM\_FLAG\_REFRESH\_NO\_AUTO\_RECONNECT** flag in the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method call.</span></span> <span data-ttu-id="1bffa-120">Os clientes de script devem definir a propriedade [**SWbemRefresher. falha**](swbemrefresher-autoreconnect.md) como **false**.</span><span class="sxs-lookup"><span data-stu-id="1bffa-120">Scripting clients must set the [**SWbemRefresher.AutoReconnect**](swbemrefresher-autoreconnect.md) property to **FALSE**.</span></span>

-   <span data-ttu-id="1bffa-121">Carrega vários objetos e enumeradores fornecidos pelos mesmos ou provedores diferentes.</span><span class="sxs-lookup"><span data-stu-id="1bffa-121">Loads multiple objects and enumerators that are provided by the same or different providers.</span></span>

    <span data-ttu-id="1bffa-122">Permite adicionar vários objetos, enumeradores ou ambos a um atualizador.</span><span class="sxs-lookup"><span data-stu-id="1bffa-122">Allows you to add multiple objects, enumerators, or both to a refresher.</span></span>

-   <span data-ttu-id="1bffa-123">Enumera objetos.</span><span class="sxs-lookup"><span data-stu-id="1bffa-123">Enumerates objects.</span></span>

    <span data-ttu-id="1bffa-124">Assim como outros provedores, um provedor de alto desempenho pode enumerar objetos.</span><span class="sxs-lookup"><span data-stu-id="1bffa-124">Like other providers, a high-performance provider can enumerate objects.</span></span>

<span data-ttu-id="1bffa-125">Depois de concluir a gravação do cliente de alto desempenho, talvez você queira melhorar o tempo de resposta.</span><span class="sxs-lookup"><span data-stu-id="1bffa-125">After you finish writing your high-performance client, you may want to improve your response time.</span></span> <span data-ttu-id="1bffa-126">Como a interface [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) é otimizada para velocidade, a interface não é threadsafe intrinsecamente.</span><span class="sxs-lookup"><span data-stu-id="1bffa-126">Because the [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface is optimized for speed, the interface is not intrinsically threadsafe.</span></span> <span data-ttu-id="1bffa-127">Portanto, durante uma operação de atualização, não acesse o objeto ou a enumeração atualizável.</span><span class="sxs-lookup"><span data-stu-id="1bffa-127">Therefore, during a refresh operation, do not access the refreshable object or enumeration.</span></span> <span data-ttu-id="1bffa-128">Para proteger objetos entre threads durante chamadas de método **IWbemObjectAccess** , use os métodos [**IWbemObjectAccess:: Lock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-lock) e [**Unlock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-unlock) .</span><span class="sxs-lookup"><span data-stu-id="1bffa-128">To protect objects across threads during **IWbemObjectAccess** method calls, use the [**IWbemObjectAccess::Lock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-lock) and [**Unlock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-unlock) methods.</span></span> <span data-ttu-id="1bffa-129">Para melhorar o desempenho, sincronize seus threads para que você não precise bloquear threads individuais.</span><span class="sxs-lookup"><span data-stu-id="1bffa-129">For improved performance, synchronize your threads so that you do not need to lock individual threads.</span></span> <span data-ttu-id="1bffa-130">A redução de threads e a sincronização de grupos de objetos para operações de atualização proporcionam o melhor desempenho geral.</span><span class="sxs-lookup"><span data-stu-id="1bffa-130">Reducing threads and synchronizing groups of objects for refresh operations provides the best overall performance.</span></span>

## <a name="adding-enumerators-to-the-wmi-refresher"></a><span data-ttu-id="1bffa-131">Adicionando enumeradores ao atualizador de WMI</span><span class="sxs-lookup"><span data-stu-id="1bffa-131">Adding Enumerators to the WMI Refresher</span></span>

<span data-ttu-id="1bffa-132">O número de instâncias e dados em cada instância são atualizados pela adição de um enumerador ao atualizador para que cada chamada para [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) resulte em uma enumeração completa.</span><span class="sxs-lookup"><span data-stu-id="1bffa-132">Both the number of instances and data in each instance are refreshed by adding an enumerator to the refresher so that each call to [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) results in a complete enumeration.</span></span>

<span data-ttu-id="1bffa-133">O exemplo de código C++ a seguir requer as referências a seguir e \# inclui instruções para compilar corretamente.</span><span class="sxs-lookup"><span data-stu-id="1bffa-133">The following C++ code example requires the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="1bffa-134">O procedimento a seguir mostra como adicionar um enumerador a um atualizador.</span><span class="sxs-lookup"><span data-stu-id="1bffa-134">The following procedure shows how to add an enumerator to a refresher.</span></span>

<span data-ttu-id="1bffa-135">**Para adicionar um enumerador a um atualizador**</span><span class="sxs-lookup"><span data-stu-id="1bffa-135">**To add an enumerator to a refresher**</span></span>

1.  <span data-ttu-id="1bffa-136">Chame o método [**IWbemConfigureRefresher:: AddEnum**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum) usando o caminho para o objeto atualizável e a interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="1bffa-136">Call the [**IWbemConfigureRefresher::AddEnum**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum) method using the path to the refreshable object and the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span>

    <span data-ttu-id="1bffa-137">O atualizador retorna um ponteiro para uma interface [**IWbemHiPerfEnum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum) .</span><span class="sxs-lookup"><span data-stu-id="1bffa-137">The refresher returns a pointer to an [**IWbemHiPerfEnum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum) interface.</span></span> <span data-ttu-id="1bffa-138">Você pode usar a interface **IWbemHiPerfEnum** para acessar os objetos na enumeração.</span><span class="sxs-lookup"><span data-stu-id="1bffa-138">You can use the **IWbemHiPerfEnum** interface to access the objects in the enumeration.</span></span>

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

    

2.  <span data-ttu-id="1bffa-139">Crie um loop que execute as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="1bffa-139">Create a loop that performs the following actions:</span></span>

    -   <span data-ttu-id="1bffa-140">Atualiza o objeto usando uma chamada para [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh).</span><span class="sxs-lookup"><span data-stu-id="1bffa-140">Refreshes the object by using a call to [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh).</span></span>
    -   <span data-ttu-id="1bffa-141">Fornece uma matriz de ponteiros de interface [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) para o método [**IWbemHiPerfEnum:: GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects) .</span><span class="sxs-lookup"><span data-stu-id="1bffa-141">Provides an array of [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface pointers to the [**IWbemHiPerfEnum::GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects) method.</span></span>
    -   <span data-ttu-id="1bffa-142">Acessa as propriedades do enumerador usando os métodos [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) passados para [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).</span><span class="sxs-lookup"><span data-stu-id="1bffa-142">Accesses the properties of the enumerator by using the [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) methods passed into [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).</span></span>

        <span data-ttu-id="1bffa-143">Um identificador de propriedade pode ser passado para cada instância de [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) para recuperar o valor atualizado.</span><span class="sxs-lookup"><span data-stu-id="1bffa-143">A property handle can be passed to each [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) instance to retrieve the refreshed value.</span></span> <span data-ttu-id="1bffa-144">O cliente deve chamar [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar os ponteiros **IWbemObjectAccess** retornados por [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).</span><span class="sxs-lookup"><span data-stu-id="1bffa-144">The client must call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release the **IWbemObjectAccess** pointers returned by [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).</span></span>

## <a name="example"></a><span data-ttu-id="1bffa-145">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1bffa-145">Example</span></span>

<span data-ttu-id="1bffa-146">O exemplo de código C++ a seguir enumera uma classe de alto desempenho, em que o cliente recupera um identificador de Propriedade do primeiro objeto e reutiliza o identificador para o restante da operação de atualização.</span><span class="sxs-lookup"><span data-stu-id="1bffa-146">The following C++ code example enumerates a high-performance class, where the client retrieves a property handle from the first object, and reuses the handle for the remainder of the refresh operation.</span></span> <span data-ttu-id="1bffa-147">Cada chamada para o método [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) atualiza o número de instâncias e os dados da instância.</span><span class="sxs-lookup"><span data-stu-id="1bffa-147">Each call to the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method updates the number of instances and the instance data.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="1bffa-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1bffa-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bffa-149">Classes de contador de desempenho</span><span class="sxs-lookup"><span data-stu-id="1bffa-149">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="1bffa-150">Acessando dados de desempenho no script</span><span class="sxs-lookup"><span data-stu-id="1bffa-150">Accessing Performance Data in Script</span></span>](accessing-performance-data-in-script.md)
</dt> <dt>

[<span data-ttu-id="1bffa-151">Atualizando dados do WMI em scripts</span><span class="sxs-lookup"><span data-stu-id="1bffa-151">Refreshing WMI Data in Scripts</span></span>](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[<span data-ttu-id="1bffa-152">Tarefas do WMI: monitoramento de desempenho</span><span class="sxs-lookup"><span data-stu-id="1bffa-152">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="1bffa-153">Monitorando dados de desempenho</span><span class="sxs-lookup"><span data-stu-id="1bffa-153">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="1bffa-154">Qualificadores de propriedade para classes de contador de desempenho formatadas</span><span class="sxs-lookup"><span data-stu-id="1bffa-154">Property Qualifiers for Formatted Performance Counter Classes</span></span>](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="1bffa-155">Tipos de contador de desempenho WMI</span><span class="sxs-lookup"><span data-stu-id="1bffa-155">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> <dt>

[<span data-ttu-id="1bffa-156">**Wmiadap.exe**</span><span class="sxs-lookup"><span data-stu-id="1bffa-156">**Wmiadap.exe**</span></span>](wmiadap.md)
</dt> <dt>

[<span data-ttu-id="1bffa-157">**QueryPerformanceCounter**</span><span class="sxs-lookup"><span data-stu-id="1bffa-157">**QueryPerformanceCounter**</span></span>](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> </dl>

 

 
