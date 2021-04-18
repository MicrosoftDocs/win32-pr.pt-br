---
description: O repositório WMI contém classes de desempenho pré-instalado para todos os objetos de biblioteca de desempenho.
ms.assetid: 2158385f-d0dc-4102-84db-ce02d2b0ee53
ms.tgt_platform: multiple
title: Acessando classes de desempenho de WMI pré-instalado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0265f9b4008913a463545ed03cd6f1025b58ef5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781370"
---
# <a name="accessing-wmi-preinstalled-performance-classes"></a><span data-ttu-id="e6d10-103">Acessando classes de desempenho de WMI pré-instalado</span><span class="sxs-lookup"><span data-stu-id="e6d10-103">Accessing WMI Preinstalled Performance Classes</span></span>

<span data-ttu-id="e6d10-104">O repositório WMI contém classes de desempenho pré-instalado para todos os objetos de biblioteca de desempenho.</span><span class="sxs-lookup"><span data-stu-id="e6d10-104">The WMI repository contains preinstalled performance classes for all the performance library objects.</span></span> <span data-ttu-id="e6d10-105">Por exemplo, instâncias da classe de desempenho de dados brutos do [**Win32 \_ PerfRawData \_ PerfProc \_ process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) representam processos.</span><span class="sxs-lookup"><span data-stu-id="e6d10-105">For example, instances of the raw data performance class [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) represent processes.</span></span> <span data-ttu-id="e6d10-106">Esse objeto de desempenho é visível no monitor do sistema como o objeto de processo.</span><span class="sxs-lookup"><span data-stu-id="e6d10-106">This performance object is visible in System Monitor as the Process object.</span></span>

<span data-ttu-id="e6d10-107">A propriedade **PageFaultsPerSec** do [**\_ \_ \_ processo Win32 PerfRawData PerfProc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) representa o contador de desempenho falhas de página por segundo para o processo.</span><span class="sxs-lookup"><span data-stu-id="e6d10-107">The **PageFaultsPerSec** property of [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) represents the Page Faults per second performance counter for the process.</span></span> <span data-ttu-id="e6d10-108">As [**classes \_ PerfFormattedData do Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contêm os valores de dados calculados exibidos no monitor do sistema (Perfmon.exe).</span><span class="sxs-lookup"><span data-stu-id="e6d10-108">The [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes contain the calculated data values displayed in System Monitor (Perfmon.exe).</span></span> <span data-ttu-id="e6d10-109">O valor da propriedade **PageFaultsPerSec** do [**processo Win32 \_ PerfFormattedData \_ PerfProc \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) é o mesmo que aparece no monitor do sistema.</span><span class="sxs-lookup"><span data-stu-id="e6d10-109">The value of the **PageFaultsPerSec** property of [**Win32\_PerfFormattedData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) is the same as when it appears in System Monitor.</span></span>

<span data-ttu-id="e6d10-110">Use a [API com para WMI](com-api-for-wmi.md) ou a [API de script para](scripting-api-for-wmi.md) que o WMI acesse dados de desempenho por meio das [classes de contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span><span class="sxs-lookup"><span data-stu-id="e6d10-110">Use either the [COM API for WMI](com-api-for-wmi.md) or the [Scripting API for WMI](scripting-api-for-wmi.md) to access performance data through the [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="e6d10-111">Em ambos os casos, um objeto de [*atualização*](gloss-r.md) é necessário para obter cada exemplo de dados.</span><span class="sxs-lookup"><span data-stu-id="e6d10-111">In both cases a [*refresher*](gloss-r.md) object is required to obtain each data sample.</span></span> <span data-ttu-id="e6d10-112">Para obter mais informações e exemplos de código de script para usar atualizadores e acessar classes de desempenho, consulte [tarefas WMI: monitoramento de desempenho](wmi-tasks--performance-monitoring.md).</span><span class="sxs-lookup"><span data-stu-id="e6d10-112">For more information and script code examples for using refreshers and accessing performance classes, see [WMI Tasks: Performance Monitoring](wmi-tasks--performance-monitoring.md).</span></span> <span data-ttu-id="e6d10-113">Para obter mais informações, consulte [acessando dados de desempenho no script](accessing-performance-data-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="e6d10-113">For more information, see [Accessing Performance Data in Script](accessing-performance-data-in-script.md).</span></span>

## <a name="accessing-performance-data-from-c"></a><span data-ttu-id="e6d10-114">Acessando dados de desempenho do C++</span><span class="sxs-lookup"><span data-stu-id="e6d10-114">Accessing Performance Data from C++</span></span>

<span data-ttu-id="e6d10-115">O exemplo de código C++ a seguir usa o provedor de contador de desempenho para acessar classes de alto desempenho predefinidas.</span><span class="sxs-lookup"><span data-stu-id="e6d10-115">The following C++ code example uses the Performance Counter provider to access predefined high-performance classes.</span></span> <span data-ttu-id="e6d10-116">Ele cria um objeto de atualização e adiciona um objeto ao atualizador.</span><span class="sxs-lookup"><span data-stu-id="e6d10-116">It creates a refresher object and adds an object to the refresher.</span></span> <span data-ttu-id="e6d10-117">O objeto é uma instância de [**processo do Win32 \_ PerfRawData \_ PerfProc \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) que monitora o desempenho de um processo específico.</span><span class="sxs-lookup"><span data-stu-id="e6d10-117">The object is a [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) instance that monitors the performance of a specific process.</span></span> <span data-ttu-id="e6d10-118">O código lê apenas uma propriedade Counter no objeto Process, a propriedade **VirtualBytes** .</span><span class="sxs-lookup"><span data-stu-id="e6d10-118">The code only reads one counter property in the process object, the **VirtualBytes** property.</span></span> <span data-ttu-id="e6d10-119">O código requer as referências a seguir e **\# inclui** instruções para compilar corretamente.</span><span class="sxs-lookup"><span data-stu-id="e6d10-119">The code requires the following references and **\#include** statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="e6d10-120">O procedimento a seguir mostra como acessar dados de um provedor de alto desempenho em C++.</span><span class="sxs-lookup"><span data-stu-id="e6d10-120">The following procedure shows how to access data from a high-performance provider in C++.</span></span>

<span data-ttu-id="e6d10-121">**Para acessar dados de um provedor de alto desempenho em C++**</span><span class="sxs-lookup"><span data-stu-id="e6d10-121">**To access data from a high-performance provider in C++**</span></span>

1.  <span data-ttu-id="e6d10-122">Estabeleça uma conexão com o namespace do WMI e defina a segurança do WMI usando uma chamada para [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) e [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="e6d10-122">Establish a connection to the WMI namespace, and set WMI security by using a call to [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) and [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="e6d10-123">Esta etapa é uma etapa padrão para a criação de qualquer aplicativo cliente WMI.</span><span class="sxs-lookup"><span data-stu-id="e6d10-123">This step is a standard step for creating any WMI client application.</span></span> <span data-ttu-id="e6d10-124">Para obter mais informações, consulte [criando um aplicativo WMI usando C++](creating-a-wmi-application-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="e6d10-124">For more information, see [Creating a WMI Application Using C++](creating-a-wmi-application-using-c-.md).</span></span>

2.  <span data-ttu-id="e6d10-125">Crie um objeto de atualização usando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com CLSID \_ WbemRefresher.</span><span class="sxs-lookup"><span data-stu-id="e6d10-125">Create a refresher object by using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with CLSID\_WbemRefresher.</span></span> <span data-ttu-id="e6d10-126">Solicite uma interface [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher) por meio do método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .</span><span class="sxs-lookup"><span data-stu-id="e6d10-126">Request an [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher) interface through the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method.</span></span> <span data-ttu-id="e6d10-127">Solicite uma interface [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) por meio do método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="e6d10-127">Request an [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) interface through the **QueryInterface** method.</span></span>

    <span data-ttu-id="e6d10-128">A interface [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) é a interface principal para o objeto [**atualizador**](swbemrefreshableitem-refresher.md) WMI.</span><span class="sxs-lookup"><span data-stu-id="e6d10-128">The [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) interface is the main interface for the WMI [**Refresher**](swbemrefreshableitem-refresher.md) object.</span></span>

    <span data-ttu-id="e6d10-129">O exemplo de código C++ a seguir mostra como recuperar [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher).</span><span class="sxs-lookup"><span data-stu-id="e6d10-129">The following C++ code example shows how to retrieve [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher).</span></span>

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

    

3.  <span data-ttu-id="e6d10-130">Adicione um objeto ao atualizador por meio de uma chamada para o método [**IWbemConfigureRefresher:: AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath) .</span><span class="sxs-lookup"><span data-stu-id="e6d10-130">Add an object to the refresher through a call to the [**IWbemConfigureRefresher::AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath) method.</span></span>

    <span data-ttu-id="e6d10-131">Quando você adiciona um objeto ao atualizador, o WMI atualiza o objeto sempre que você chama o método [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) .</span><span class="sxs-lookup"><span data-stu-id="e6d10-131">When you add an object to the refresher, WMI refreshes the object whenever you call the [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method.</span></span> <span data-ttu-id="e6d10-132">O objeto que você adiciona designa o provedor em seus qualificadores de classe.</span><span class="sxs-lookup"><span data-stu-id="e6d10-132">The object you add designates the provider in its class qualifiers.</span></span>

    <span data-ttu-id="e6d10-133">O exemplo de código C++ a seguir mostra como chamar [**AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath).</span><span class="sxs-lookup"><span data-stu-id="e6d10-133">The following C++ code example shows how to call [**AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath).</span></span>

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

    

4.  <span data-ttu-id="e6d10-134">Para configurar o acesso mais rápido ao objeto, conecte-se à interface [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) por meio de [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) na interface [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="e6d10-134">To set up faster access to the object, connect to the [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface through [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) interface.</span></span>

    <span data-ttu-id="e6d10-135">O exemplo de código C++ a seguir mostra como recuperar um ponteiro para o objeto usando [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) em vez de [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject).</span><span class="sxs-lookup"><span data-stu-id="e6d10-135">The following C++ code example shows how to retrieve a pointer to the object using [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) instead of [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject).</span></span>

    ```C++
        // For quick property retrieval, use IWbemObjectAccess.
        IWbemObjectAccess* pAcc = NULL;
        pObj->QueryInterface( IID_IWbemObjectAccess, (void**) &pAcc );
        // This is not required.
        pObj->Release();
    ```

    

    <span data-ttu-id="e6d10-136">A interface [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) aumenta o desempenho porque você pode obter identificadores para propriedades de contador específicas e requer que você bloqueie e desbloqueie o objeto em seu código, que é uma operação que o [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) executa para cada acesso de propriedade.</span><span class="sxs-lookup"><span data-stu-id="e6d10-136">The [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface increases performance because you can get handles to specific counter properties, and it requires that you lock and unlock the object in your code, which is an operation that [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) performs for each property access.</span></span>

5.  <span data-ttu-id="e6d10-137">Obtenha os identificadores das propriedades para examinar usando chamadas para o método [**IWbemObjectAccess:: GetPropertyHandle**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyhandle) .</span><span class="sxs-lookup"><span data-stu-id="e6d10-137">Obtain the handles of the properties to examine by using calls to the [**IWbemObjectAccess::GetPropertyHandle**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyhandle) method.</span></span>

    <span data-ttu-id="e6d10-138">As alças de propriedade são as mesmas para todas as instâncias de uma classe, o que significa que use o identificador de propriedade que você recupera de uma instância específica para todas as instâncias de uma classe específica.</span><span class="sxs-lookup"><span data-stu-id="e6d10-138">Property handles are the same for all instances of a class, which means that use the property handle you retrieve from a specific instance for all instances of a specific class.</span></span> <span data-ttu-id="e6d10-139">Você também pode obter um identificador de um objeto de classe para recuperar valores de propriedade de um objeto de instância.</span><span class="sxs-lookup"><span data-stu-id="e6d10-139">You can also obtain a handle from a class object to retrieve property values from an instance object.</span></span>

    <span data-ttu-id="e6d10-140">O exemplo de código C++ a seguir mostra como recuperar um identificador de propriedade.</span><span class="sxs-lookup"><span data-stu-id="e6d10-140">The following C++ code example shows how to retrieve a property handle.</span></span>

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

    

6.  <span data-ttu-id="e6d10-141">Crie um loop de programação que execute as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="e6d10-141">Create a programming loop that performs the following actions:</span></span>

    -   <span data-ttu-id="e6d10-142">Atualize o objeto com uma chamada para [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) usando o ponteiro criado na chamada anterior para [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="e6d10-142">Refresh the object with a call to [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) by using the pointer created in the previous call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

        <span data-ttu-id="e6d10-143">Nesta chamada, o atualizador WMI atualiza o objeto de cliente usando os dados que o provedor fornece.</span><span class="sxs-lookup"><span data-stu-id="e6d10-143">In this call, the WMI Refresher refreshes the client object by using data that the provider supplies.</span></span>

    -   <span data-ttu-id="e6d10-144">Execute qualquer ação conforme necessário no objeto, como recuperar um nome de propriedade, tipo de dados ou valor.</span><span class="sxs-lookup"><span data-stu-id="e6d10-144">Perform any action as necessary on the object, such as retrieving a property name, data type, or value.</span></span>

        <span data-ttu-id="e6d10-145">Você pode acessar a propriedade por meio do identificador de propriedade obtido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e6d10-145">You can access the property through the property handle obtained earlier.</span></span> <span data-ttu-id="e6d10-146">Devido à chamada de [**atualização**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) , o WMI atualiza a propriedade a cada vez pelo loop.</span><span class="sxs-lookup"><span data-stu-id="e6d10-146">Due to the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) call, WMI refreshes the property each time through the loop.</span></span>

<span data-ttu-id="e6d10-147">O exemplo de C++ a seguir mostra como usar a API de alto desempenho do WMI.</span><span class="sxs-lookup"><span data-stu-id="e6d10-147">The following C++ example shows how to use the WMI high-performance API.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e6d10-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e6d10-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6d10-149">Classes de contador de desempenho</span><span class="sxs-lookup"><span data-stu-id="e6d10-149">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="e6d10-150">Tarefas do WMI: monitoramento de desempenho</span><span class="sxs-lookup"><span data-stu-id="e6d10-150">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
