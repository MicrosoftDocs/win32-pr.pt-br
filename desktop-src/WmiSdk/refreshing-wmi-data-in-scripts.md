---
description: Em scripts de monitoramento, você pode evitar chamadas sucessivas para GetObject usando um objeto SWbemRefresher. O objeto SWbemRefresher é um contêiner que pode conter vários objetos WMI cujos dados podem ser atualizados em uma chamada.
ms.assetid: b34567f5-9349-4580-97d5-723759805d88
ms.tgt_platform: multiple
title: Atualizando dados do WMI em scripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0f17ce718fcf5b57e4f3204337634af4129d24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170382"
---
# <a name="refreshing-wmi-data-in-scripts"></a><span data-ttu-id="ab915-104">Atualizando dados do WMI em scripts</span><span class="sxs-lookup"><span data-stu-id="ab915-104">Refreshing WMI Data in Scripts</span></span>

<span data-ttu-id="ab915-105">Em scripts de monitoramento, você pode evitar chamadas sucessivas para **GetObject** usando um objeto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="ab915-105">In monitoring scripts, you can avoid successive calls to **GetObject** by using an [**SWbemRefresher**](swbemrefresher.md) object.</span></span> <span data-ttu-id="ab915-106">O objeto **SWbemRefresher** é um contêiner que pode conter vários objetos WMI cujos dados podem ser atualizados em uma chamada.</span><span class="sxs-lookup"><span data-stu-id="ab915-106">The **SWbemRefresher** object is a container that can hold several WMI objects whose data can be refreshed in one call.</span></span>

<span data-ttu-id="ab915-107">O uso de um objeto [**SWbemRefresher**](swbemrefresher.md) é necessário para obter dados precisos de classes de desempenho do WMI, como [**Win32 \_ PerfFormattedData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) ou outras classes pré-instalados derivadas do [**Win32 \_ perf**](/windows/desktop/CIMWin32Prov/win32-perf).</span><span class="sxs-lookup"><span data-stu-id="ab915-107">Using an [**SWbemRefresher**](swbemrefresher.md) object is required to get accurate data from WMI performance classes, such as [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) or other preinstalled classes derived from [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf).</span></span>

<span data-ttu-id="ab915-108">O procedimento a seguir descreve como atualizar dados em scripts.</span><span class="sxs-lookup"><span data-stu-id="ab915-108">The following procedure describes how to refresh data in scripts.</span></span>

<span data-ttu-id="ab915-109">**Para atualizar dados em scripts**</span><span class="sxs-lookup"><span data-stu-id="ab915-109">**To refresh data in scripts**</span></span>

1.  <span data-ttu-id="ab915-110">Chame **CreateObject** para criar um objeto de atualizador [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="ab915-110">Call **CreateObject** to create an [**SWbemRefresher**](swbemrefresher.md) refresher object.</span></span>

    ```VB
    Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
    ```

    

2.  <span data-ttu-id="ab915-111">Conecte-se ao namespace do WMI.</span><span class="sxs-lookup"><span data-stu-id="ab915-111">Connect to the WMI namespace.</span></span> <span data-ttu-id="ab915-112">Para usar as classes de [**desempenho \_ do Win32**](/windows/desktop/CIMWin32Prov/win32-perf) pré-instalado, conecte-se à **\\ cimv2 raiz**.</span><span class="sxs-lookup"><span data-stu-id="ab915-112">To use preinstalled [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf) performances classes, connect to **root\\cimv2**.</span></span>

    ```VB
    Set objServicesCimv2 = GetObject("winmgmts:\\" _
        & strComputer & "\root\cimv2")
    ```

    

3.  <span data-ttu-id="ab915-113">Adicione um único objeto (chame [**SWbemRefresher. Add**](swbemrefresher-add.md)) ou uma coleção (chame [**SWbemRefresher. AddEnum**](swbemrefresher-addenum.md)) ao atualizador.</span><span class="sxs-lookup"><span data-stu-id="ab915-113">Add a single object (call [**SWbemRefresher.Add**](swbemrefresher-add.md)) or a collection (call [**SWbemRefresher.AddEnum**](swbemrefresher-addenum.md)) to the refresher.</span></span>

    <span data-ttu-id="ab915-114">Use as classes de dados precalculadas derivadas do [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), por exemplo, o [**PerfFormattedData de \_ \_ perfdisk \_**](./retrieving-raw-and-formatted-performance-data.md) do Win32, em vez do [**Win32 \_ PerfRawData \_ perfdisk \_**](./retrieving-raw-and-formatted-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="ab915-114">Use the precalculated data classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), for example, [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) instead of [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).</span></span> <span data-ttu-id="ab915-115">Caso contrário, você deve calcular os valores para todas as propriedades que não sejam contadores simples.</span><span class="sxs-lookup"><span data-stu-id="ab915-115">Otherwise, you must calculate the values for all of the properties other than simple counters.</span></span>

    ```VB
    Set objRefreshableItem = _
        objRefresher.AddEnum(objServicesCimv2 , _
        "Win32_PerfFormattedData_PerfProc_Process")
    ```

    

4.  <span data-ttu-id="ab915-116">Atualize os dados uma vez para obter os dados de desempenho iniciais.</span><span class="sxs-lookup"><span data-stu-id="ab915-116">Refresh the data one time to get the initial performance data.</span></span>

    <span data-ttu-id="ab915-117">Chame o método [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) ou o método [**SWbemObjectEx. Refresh \_**](swbemobjectex-refresh-.md) genérico.</span><span class="sxs-lookup"><span data-stu-id="ab915-117">Call either the [**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) method or the generic [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md) method.</span></span>

    ```VB
    objRefresher.Refresh
    ```

    

5.  <span data-ttu-id="ab915-118">Se você estiver monitorando o desempenho e tiver uma coleção no objeto do atualizador, faça um loop pelos objetos da coleção.</span><span class="sxs-lookup"><span data-stu-id="ab915-118">If you are monitoring performance and have a collection in the refresher object, loop through the collection objects.</span></span>

    ```VB
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine _
                & Process.PercentProcessorTime & "%"
        End If
    Next
    ```

    

6.  <span data-ttu-id="ab915-119">Limpe os itens do atualizador chamando [**SWbemRefresher. DeleteAll**](swbemrefresher-deleteall.md) ou remova itens específicos chamando [**SWbemRefresher. Remove**](swbemrefresher-remove.md).</span><span class="sxs-lookup"><span data-stu-id="ab915-119">Clear the items from the refresher by calling [**SWbemRefresher.DeleteAll**](swbemrefresher-deleteall.md) or remove specific items by calling [**SwbemRefresher.Remove**](swbemrefresher-remove.md).</span></span>

<span data-ttu-id="ab915-120">O exemplo de código VBScript a seguir mostra como atualizar um único objeto no computador local.</span><span class="sxs-lookup"><span data-stu-id="ab915-120">The following VBScript code example shows how to refresh a single object on the local computer.</span></span> <span data-ttu-id="ab915-121">O script cria um contêiner de atualização e adiciona uma instância de um enumerador para instâncias de [**processo do Win32 \_ PerfFormattedData \_ PerfProc \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) .</span><span class="sxs-lookup"><span data-stu-id="ab915-121">The script creates a refresher container and adds an instance of an enumerator for [**Win32\_PerfFormattedData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) instances.</span></span> <span data-ttu-id="ab915-122">A chamada de [**atualização**](swbemrefresher-refresh.md) é feita três vezes para demonstrar as alterações na propriedade **PercentProcessorTime** para processos usando mais de uma porcentagem do tempo do processador.</span><span class="sxs-lookup"><span data-stu-id="ab915-122">The [**Refresh**](swbemrefresher-refresh.md) call is made three times to demonstrate the changes in the **PercentProcessorTime** property for processes using more than one percent of the processor time.</span></span>


```VB
On Error Resume Next
strComputer = "."
Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
Set objServicesCimv2 = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
If Err = 0 Then 
Set objRefreshableItem = _
    objRefresher.AddEnum(objServicesCimv2 ,"Win32_PerfFormattedData_PerfProc_Process")
objRefresher.Refresh
' Loop through the processes three times to locate  
'    and display all the process currently using 
'    more than 1 % of the process time. Refresh on each pass.
For i = 1 to 3
    Wscript.Echo "Refresh number " & i 
    objRefresher.Refresh 
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine & Process.PercentProcessorTime & "%"
        End If
    Next
Next
Else
    WScript.Echo Err.Description
End If
```



<span data-ttu-id="ab915-123">A propriedade [**index**](swbemrefreshableitem-index.md) do [**SWbemRefreshableItem**](swbemrefreshableitem.md) retornado representa o índice do objeto na coleção de atualizadores.</span><span class="sxs-lookup"><span data-stu-id="ab915-123">The [**Index**](swbemrefreshableitem-index.md) property of the returned [**SWbemRefreshableItem**](swbemrefreshableitem.md) represents the index of the object in the refresher collection.</span></span> <span data-ttu-id="ab915-124">Você pode chamar a propriedade [**SWbemRefreshableItem. IsSet**](swbemrefreshableitem-isset.md) para determinar se um item em um atualizador é um único item ou uma coleção.</span><span class="sxs-lookup"><span data-stu-id="ab915-124">You can call [**SWbemRefreshableItem.IsSet**](swbemrefreshableitem-isset.md) property to determine whether or not an item in a refresher is a single item or a collection.</span></span> <span data-ttu-id="ab915-125">Para acessar um único item, use a propriedade [**SWbemRefreshableItem. Object**](swbemrefreshableitem-object.md) .</span><span class="sxs-lookup"><span data-stu-id="ab915-125">To access a single item, use the [**SWbemRefreshableItem.Object**](swbemrefreshableitem-object.md) property.</span></span> <span data-ttu-id="ab915-126">Se você não fizer a chamada para **SWbemRefreshableItem. Object**, o script falhará quando você tentar acessar o objeto.</span><span class="sxs-lookup"><span data-stu-id="ab915-126">If you do not make the call to **SWbemRefreshableItem.Object**, then the script fails when you try to access the object.</span></span> <span data-ttu-id="ab915-127">Para acessar uma coleção, use a propriedade [**SWbemRefreshableItem. ObjectSet**](swbemrefreshableitem-objectset.md) .</span><span class="sxs-lookup"><span data-stu-id="ab915-127">To access a collection, use the [**SWbemRefreshableItem.ObjectSet**](swbemrefreshableitem-objectset.md) property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab915-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ab915-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab915-129">Classes de contador de desempenho</span><span class="sxs-lookup"><span data-stu-id="ab915-129">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="ab915-130">Acessando dados de desempenho no script</span><span class="sxs-lookup"><span data-stu-id="ab915-130">Accessing Performance Data in Script</span></span>](accessing-performance-data-in-script.md)
</dt> <dt>

[<span data-ttu-id="ab915-131">Tarefas do WMI: monitoramento de desempenho</span><span class="sxs-lookup"><span data-stu-id="ab915-131">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="ab915-132">Monitorando dados de desempenho</span><span class="sxs-lookup"><span data-stu-id="ab915-132">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
