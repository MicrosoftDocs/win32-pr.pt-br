---
description: Usando o WMI, você pode acessar os dados do contador do sistema programaticamente de objetos nas bibliotecas de desempenho.
ms.assetid: a0ed14e9-d2ec-43eb-8c8e-eac3c134ea1d
ms.tgt_platform: multiple
title: Monitorando dados de desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95cee18ba88a8aff920c2d14b5709a0fd913e2ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749518"
---
# <a name="monitoring-performance-data"></a><span data-ttu-id="edb9d-103">Monitorando dados de desempenho</span><span class="sxs-lookup"><span data-stu-id="edb9d-103">Monitoring Performance Data</span></span>

<span data-ttu-id="edb9d-104">Usando o WMI, você pode acessar os dados do contador do sistema programaticamente de objetos nas bibliotecas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="edb9d-104">Using WMI, you can access system counter data programmatically from objects in the performance libraries.</span></span> <span data-ttu-id="edb9d-105">Esses são os mesmos dados de desempenho que aparecem no monitor do sistema no utilitário Perfmon.</span><span class="sxs-lookup"><span data-stu-id="edb9d-105">This is the same performance data that appears in the System Monitor in the Perfmon utility.</span></span> <span data-ttu-id="edb9d-106">Use as [classes de contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes) pré-instaladas para obter dados de desempenho em scripts ou aplicativos C++.</span><span class="sxs-lookup"><span data-stu-id="edb9d-106">Use the preinstalled [performance counter classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) to obtain performance data in scripts or C++ applications.</span></span>

<span data-ttu-id="edb9d-107">As seções a seguir são discutidas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="edb9d-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="edb9d-108">Classes de desempenho WMI</span><span class="sxs-lookup"><span data-stu-id="edb9d-108">WMI Performance Classes</span></span>](#wmi-performance-classes)
-   [<span data-ttu-id="edb9d-109">Provedores de dados de desempenho</span><span class="sxs-lookup"><span data-stu-id="edb9d-109">Performance Data Providers</span></span>](#performance-data-providers)
-   [<span data-ttu-id="edb9d-110">Usando classes de dados de desempenho formatadas</span><span class="sxs-lookup"><span data-stu-id="edb9d-110">Using Formatted Performance Data Classes</span></span>](#using-formatted-performance-data-classes)
-   [<span data-ttu-id="edb9d-111">Usando classes de dados de desempenho brutos</span><span class="sxs-lookup"><span data-stu-id="edb9d-111">Using Raw Performance Data Classes</span></span>](#using-raw-performance-data-classes)
-   [<span data-ttu-id="edb9d-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="edb9d-112">Related topics</span></span>](#related-topics)

## <a name="wmi-performance-classes"></a><span data-ttu-id="edb9d-113">Classes de desempenho WMI</span><span class="sxs-lookup"><span data-stu-id="edb9d-113">WMI Performance Classes</span></span>

<span data-ttu-id="edb9d-114">Por exemplo, o objeto "NetworkInterface", no monitor do sistema, é representado no WMI pela classe [**Win32 \_ PerfRawData \_ tcpip \_ NetworkInterface**](./retrieving-raw-and-formatted-performance-data.md) para dados brutos e a [**classe \_ \_ tcpip \_ NetworkInterface do Win32 PerfFormattedData**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) para dados precalculados ou formatados.</span><span class="sxs-lookup"><span data-stu-id="edb9d-114">As an example, the "NetworkInterface" object, in System Monitor, is represented in WMI by the [**Win32\_PerfRawData\_Tcpip\_NetworkInterface**](./retrieving-raw-and-formatted-performance-data.md) class for raw data and the [**Win32\_PerfFormattedData\_Tcpip\_NetworkInterface**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class for precalculated, or formatted data.</span></span> <span data-ttu-id="edb9d-115">As classes derivadas do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e do [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) devem ser usadas com um objeto de [*atualização*](gloss-r.md) .</span><span class="sxs-lookup"><span data-stu-id="edb9d-115">Classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) must be used with a [*refresher*](gloss-r.md) object.</span></span> <span data-ttu-id="edb9d-116">Em classes de dados brutos, seu aplicativo ou script C++ deve executar cálculos para obter a mesma saída que Perfmon.exe.</span><span class="sxs-lookup"><span data-stu-id="edb9d-116">On raw data classes, your C++ application or script must perform calculations to obtain the same output as Perfmon.exe.</span></span> <span data-ttu-id="edb9d-117">As classes de dados formatadas fornecem dados pré-calculados.</span><span class="sxs-lookup"><span data-stu-id="edb9d-117">Formatted data classes supply precalculated data.</span></span> <span data-ttu-id="edb9d-118">Para obter mais informações sobre como obter dados em aplicativos C++, consulte [acessando dados de desempenho em C++](accessing-performance-data-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="edb9d-118">For more information about obtaining data in C++ applications, see [Accessing Performance Data in C++](accessing-performance-data-in-c--.md).</span></span> <span data-ttu-id="edb9d-119">Para scripts, consulte [acessando dados de desempenho em script](accessing-performance-data-in-script.md) e [atualizando dados do WMI em scripts](refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="edb9d-119">For scripting, see [Accessing Performance Data in Script](accessing-performance-data-in-script.md) and [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span>

<span data-ttu-id="edb9d-120">O exemplo de código VBScript a seguir usa o [**\_ \_ \_ processo Win32 PerfFormattedData PerfProc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) para obter dados de desempenho para o processo ocioso.</span><span class="sxs-lookup"><span data-stu-id="edb9d-120">The following VBScript code example uses [**Win32\_PerfFormattedData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) to obtain performance data for the Idle process.</span></span> <span data-ttu-id="edb9d-121">O script exibe os mesmos dados que aparecem no perfmon para o contador% tempo do processador do objeto de processo.</span><span class="sxs-lookup"><span data-stu-id="edb9d-121">The script displays the same data that appears in Perfmon for the % Processor Time counter of the Process object.</span></span> <span data-ttu-id="edb9d-122">A chamada para [**SWbemObjectEx. Refresh \_**](swbemobjectex-refresh-.md) executa a operação de atualização.</span><span class="sxs-lookup"><span data-stu-id="edb9d-122">The call to [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md) performs the refresh operation.</span></span> <span data-ttu-id="edb9d-123">Lembre-se de que os dados devem ser atualizados, na concessão uma vez, para obter uma linha de base.</span><span class="sxs-lookup"><span data-stu-id="edb9d-123">Be aware that the data must be refreshed, at lease once, to obtain a baseline.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")
set PerfProcess = objWMIService.Get(_
    "Win32_PerfFormattedData_PerfProc_Process.Name='Idle'")

While (True)
    PerfProcess.Refresh_     
    Wscript.Echo PerfProcess.PercentProcessorTime
    Wscript.Sleep 1000
Wend
```



<span data-ttu-id="edb9d-124">As classes de contador de desempenho também podem fornecer dados estatísticos.</span><span class="sxs-lookup"><span data-stu-id="edb9d-124">Performance counter classes can also provide statistical data.</span></span> <span data-ttu-id="edb9d-125">Para obter mais informações, consulte [obtendo dados de desempenho estatísticos](obtaining-statistical-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="edb9d-125">For more information, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md).</span></span>

## <a name="performance-data-providers"></a><span data-ttu-id="edb9d-126">Provedores de dados de desempenho</span><span class="sxs-lookup"><span data-stu-id="edb9d-126">Performance Data Providers</span></span>

<span data-ttu-id="edb9d-127">O WMI tem provedores pré-instalados que monitoram o desempenho do sistema no sistema local e remotamente.</span><span class="sxs-lookup"><span data-stu-id="edb9d-127">WMI has preinstalled providers that monitor system performance on both the local system and remotely.</span></span> <span data-ttu-id="edb9d-128">O provedor [WmiPerfClass](wmiperfclass-provider.md) cria as classes derivadas do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e do [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="edb9d-128">The [WmiPerfClass](wmiperfclass-provider.md) provider creates the classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span> <span data-ttu-id="edb9d-129">O provedor [WmiPerfInst](wmiperfinst-provider.md) fornece dados dinamicamente para classes não processadas e formatadas.</span><span class="sxs-lookup"><span data-stu-id="edb9d-129">The [WmiPerfInst](wmiperfinst-provider.md) provider supplies data dynamically to both raw and formatted classes.</span></span>

## <a name="using-formatted-performance-data-classes"></a><span data-ttu-id="edb9d-130">Usando classes de dados de desempenho formatadas</span><span class="sxs-lookup"><span data-stu-id="edb9d-130">Using Formatted Performance Data Classes</span></span>

<span data-ttu-id="edb9d-131">O exemplo de código VBScript a seguir obtém dados de desempenho sobre memória, partições de disco e filas de trabalho do servidor.</span><span class="sxs-lookup"><span data-stu-id="edb9d-131">The following VBScript code example obtains performance data about memory, disk partitions, and server work queues.</span></span> <span data-ttu-id="edb9d-132">O script determina se os valores estão dentro de um intervalo aceitável.</span><span class="sxs-lookup"><span data-stu-id="edb9d-132">The script then determines if the values are within an acceptable range.</span></span>

<span data-ttu-id="edb9d-133">O script usa os seguintes objetos de provedor de WMI e objetos de script:</span><span class="sxs-lookup"><span data-stu-id="edb9d-133">The script uses the following WMI provider objects and scripting objects:</span></span>

-   <span data-ttu-id="edb9d-134">Classes de contador de desempenho de WMI pré-instaladas.</span><span class="sxs-lookup"><span data-stu-id="edb9d-134">Preinstalled WMI performance counter classes.</span></span>
-   <span data-ttu-id="edb9d-135">O objeto do atualizador, [**SWbemRefresher**](swbemrefresher.md).</span><span class="sxs-lookup"><span data-stu-id="edb9d-135">The refresher object, [**SWbemRefresher**](swbemrefresher.md).</span></span>
-   <span data-ttu-id="edb9d-136">Itens a serem adicionados ao contêiner do atualizador, [ **SWbemRefreshableItem**](swbemrefreshableitem.md)</span><span class="sxs-lookup"><span data-stu-id="edb9d-136">Items to add to the refresher container, [**SWbemRefreshableItem**](swbemrefreshableitem.md)</span></span>


```VB
Set objCimv2 = GetObject("winmgmts:root\cimv2")
Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")

' Add items to the SWbemRefresher
' Without the SWbemRefreshableItem.ObjectSet call,
' the script will fail
Set objMemory = objRefresher.AddEnum _
    (objCimv2, _ 
    "Win32_PerfFormattedData_PerfOS_Memory").ObjectSet
Set objDiskQueue = objRefresher.AddEnum _
    (objCimv2, _
    "Win32_PerfFormattedData_PerfDisk_LogicalDisk").ObjectSet
Set objQueueLength = objRefresher.AddEnum _
    (objCimv2, _
    "Win32_PerfFormattedData_PerfNet_ServerWorkQueues").ObjectSet

' Initial refresh needed to get baseline values
objRefresher.Refresh
intTotalHealth = 0
' Do three refreshes to get data
For i = 1 to 3
    WScript.Echo "Refresh " & i
    For each intAvailableBytes in objMemory
        WScript.Echo "Available megabytes of memory: " _
            & intAvailableBytes.AvailableMBytes
        If intAvailableBytes.AvailableMBytes < 4 Then
            intTotalHealth = intTotalHealth + 1
        End If
    Next
    For each intDiskQueue in objDiskQueue
        WScript.Echo "Current disk queue length " & "Name: " _
            & intDiskQueue.Name & ":" _
            & intDiskQueue.CurrentDiskQueueLength
        If intDiskQueue.CurrentDiskQueueLength > 2 Then
            intTotalHealth = intTotalHealth + 1
        End If
    Next
    For each intServerQueueLength in objQueueLength
        WScript.Echo "Server work queue length: " _
            & intServerQueueLength.QueueLength
        If intServerQueueLength.QueueLength > 4 Then
            intTotalHealth = intTotalHealth + 1                       
        End If
    Wscript.Echo "  "
    Next
    If intTotalHealth > 0 Then
        Wscript.Echo "Unhealthy."
    Else
        Wscript.Echo "Healthy."
    End If
    intTotalHealth = 0
    Wscript.Sleep 5000
' Refresh data for all objects in the collection
    objRefresher.Refresh
Next
```



## <a name="using-raw-performance-data-classes"></a><span data-ttu-id="edb9d-137">Usando classes de dados de desempenho brutos</span><span class="sxs-lookup"><span data-stu-id="edb9d-137">Using Raw Performance Data Classes</span></span>

<span data-ttu-id="edb9d-138">O exemplo de código VBScript a seguir obtém o tempo de processador percentual atual bruto no computador local e o converte em uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="edb9d-138">The following VBScript code example obtains raw, current percent processor time on the local computer and converts it to a percentage.</span></span> <span data-ttu-id="edb9d-139">O exemplo mostra como obter dados de desempenho brutos da propriedade **PercentProcessorTime** da classe de [**\_ \_ \_ processador Win32 PerfRawData PerfOS**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) .</span><span class="sxs-lookup"><span data-stu-id="edb9d-139">The example shows you how to obtain raw performance data from the **PercentProcessorTime** property of the [**Win32\_PerfRawData\_PerfOS\_Processor**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class.</span></span>

<span data-ttu-id="edb9d-140">Para calcular o valor da porcentagem de tempo do processador, você deve localizar a fórmula.</span><span class="sxs-lookup"><span data-stu-id="edb9d-140">To calculate the percent processor time value, you must locate the formula.</span></span> <span data-ttu-id="edb9d-141">Pesquise o valor no qualificador de **tipo** para a propriedade **PercentProcessorTime** na tabela de [**qualificador de tipo de ComType**](countertype-qualifier.md) para obter o nome da constante.</span><span class="sxs-lookup"><span data-stu-id="edb9d-141">Look up the value in the **CounterType** qualifier for the **PercentProcessorTime** property in the [**CounterType Qualifier**](countertype-qualifier.md) table to get the constant name.</span></span> <span data-ttu-id="edb9d-142">Localize o nome da constante em [tipos de contadores](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) para obter a fórmula.</span><span class="sxs-lookup"><span data-stu-id="edb9d-142">Locate the constant name in [Counter Types](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) to obtain the formula.</span></span>


```VB
Set objService = GetObject( _
    "Winmgmts:{impersonationlevel=impersonate}!\Root\Cimv2")

For i = 1 to 8
    Set objInstance1 = objService.Get( _
        "Win32_PerfRawData_PerfOS_Processor.Name='_Total'")
    N1 = objInstance1.PercentProcessorTime
    D1 = objInstance1.TimeStamp_Sys100NS

'Sleep for two seconds = 2000 ms
    WScript.Sleep(2000)

    Set perf_instance2 = objService.Get( _
        "Win32_PerfRawData_PerfOS_Processor.Name='_Total'")
    N2 = perf_instance2.PercentProcessorTime
    D2 = perf_instance2.TimeStamp_Sys100NS
' Look up the CounterType qualifier for the PercentProcessorTime 
' and obtain the formula to calculate the meaningful data. 
' CounterType - PERF_100NSEC_TIMER_INV
' Formula - (1- ((N2 - N1) / (D2 - D1))) x 100

    PercentProcessorTime = (1 - ((N2 - N1)/(D2-D1)))*100
    WScript.Echo "% Processor Time=" , Round(PercentProcessorTime,2)
Next
```



## <a name="related-topics"></a><span data-ttu-id="edb9d-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="edb9d-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edb9d-144">Usando o WMI</span><span class="sxs-lookup"><span data-stu-id="edb9d-144">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

 
