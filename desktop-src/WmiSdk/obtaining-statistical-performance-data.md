---
description: No WMI, você pode definir dados de desempenho estatísticos com base em dados em classes de desempenho formatadas derivadas do Win32 \_ PerfFormattedData. As estatísticas disponíveis são média, mínimo, máximo, intervalo e variação, conforme definido em tipos de contador estatístico.
ms.assetid: 5552d5fc-df8c-4353-8593-c106ee19dc84
ms.tgt_platform: multiple
title: Obtendo dados de desempenho estatísticos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 65892608e642b675440d81127ef9afa0badd1d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089834"
---
# <a name="obtaining-statistical-performance-data"></a><span data-ttu-id="7b999-104">Obtendo dados de desempenho estatísticos</span><span class="sxs-lookup"><span data-stu-id="7b999-104">Obtaining Statistical Performance Data</span></span>

<span data-ttu-id="7b999-105">No WMI, você pode definir dados de desempenho estatísticos com base em dados em classes de desempenho formatadas derivadas do [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="7b999-105">In WMI, you can define statistical performance data based on data in formatted performance classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span> <span data-ttu-id="7b999-106">As estatísticas disponíveis são média, mínimo, máximo, intervalo e variação, conforme definido em [tipos de contador estatístico](statistical-counter-types.md).</span><span class="sxs-lookup"><span data-stu-id="7b999-106">The available statistics are average, minimum, maximum, range, and variance, as defined in [Statistical Counter Types](statistical-counter-types.md).</span></span>

<span data-ttu-id="7b999-107">A lista a seguir inclui os tipos de contadores estatísticos especiais:</span><span class="sxs-lookup"><span data-stu-id="7b999-107">The following list includes the special statistical counter types:</span></span>

-   [<span data-ttu-id="7b999-108">média de COOKER \_</span><span class="sxs-lookup"><span data-stu-id="7b999-108">COOKER\_AVERAGE</span></span>](cooker-average.md)
-   [<span data-ttu-id="7b999-109">COOKER \_ mín.</span><span class="sxs-lookup"><span data-stu-id="7b999-109">COOKER\_MIN</span></span>](cooker-min.md)
-   [<span data-ttu-id="7b999-110">COOKER \_ Max</span><span class="sxs-lookup"><span data-stu-id="7b999-110">COOKER\_MAX</span></span>](cooker-max.md)
-   [<span data-ttu-id="7b999-111">intervalo de COOKER \_</span><span class="sxs-lookup"><span data-stu-id="7b999-111">COOKER\_RANGE</span></span>](cooker-range.md)
-   [<span data-ttu-id="7b999-112">variância de COOKER \_</span><span class="sxs-lookup"><span data-stu-id="7b999-112">COOKER\_VARIANCE</span></span>](cooker-variance.md)

<span data-ttu-id="7b999-113">Os exemplos a seguir mostram como:</span><span class="sxs-lookup"><span data-stu-id="7b999-113">The following examples show how to:</span></span>

-   <span data-ttu-id="7b999-114">Crie um arquivo MOF que define uma classe de dados calculados.</span><span class="sxs-lookup"><span data-stu-id="7b999-114">Create a MOF file that defines a class of calculated data.</span></span>
-   <span data-ttu-id="7b999-115">Escreva um script que crie uma instância da classe e atualize periodicamente os dados na instância com os valores estatísticos recalculados.</span><span class="sxs-lookup"><span data-stu-id="7b999-115">Write a script that creates an instance of the class, and periodically refreshes the data in the instance with the recalculated statistical values.</span></span>

## <a name="mof-file"></a><span data-ttu-id="7b999-116">Arquivo MOF</span><span class="sxs-lookup"><span data-stu-id="7b999-116">MOF File</span></span>

<span data-ttu-id="7b999-117">O exemplo de código MOF a seguir cria uma nova classe de dados calculada chamada **Win32 \_ PerfFormattedData \_ AvailableMBytes**.</span><span class="sxs-lookup"><span data-stu-id="7b999-117">The following MOF code example creates a new calculated data class named **Win32\_PerfFormattedData\_AvailableMBytes**.</span></span> <span data-ttu-id="7b999-118">Essa classe contém dados da propriedade **AvailableMBytes** da classe RAW [**Win32 \_ PerfRawData \_ PerfOS \_ Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).</span><span class="sxs-lookup"><span data-stu-id="7b999-118">This class contains data from the **AvailableMBytes** property of the raw class [**Win32\_PerfRawData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).</span></span> <span data-ttu-id="7b999-119">A **classe Win32 \_ PerfFormattedData \_ AvailableBytes** define as propriedades **Average**, **min**, **Max**, **Range** e **Variance**.</span><span class="sxs-lookup"><span data-stu-id="7b999-119">The **Win32\_PerfFormattedData\_AvailableBytes** class defines the properties **Average**, **Min**, **Max**, **Range**, and **Variance**.</span></span>

<span data-ttu-id="7b999-120">O arquivo MOF usa os [**qualificadores de propriedade para classes de contador de desempenho formatadas**](property-qualifiers-for-performance-counter-classes.md) para definir a fonte de dados de propriedade e a fórmula de cálculo.</span><span class="sxs-lookup"><span data-stu-id="7b999-120">The MOF file uses the [**Property Qualifiers for Formatted Performance Counter Classes**](property-qualifiers-for-performance-counter-classes.md) to define the property data source and the calculation formula.</span></span>

-   <span data-ttu-id="7b999-121">A propriedade **Average** obtém dados brutos da [**\_ \_ \_ memória PerfOS Win32 PerfRawData**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).**Propriedade AvailableMBytes** .</span><span class="sxs-lookup"><span data-stu-id="7b999-121">The **Average** property obtains raw data from the [**Win32\_PerfRawData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).**AvailableMBytes** property.</span></span>
-   <span data-ttu-id="7b999-122">O **qualificador** do contador para a propriedade **Average** especifica a fonte de dados brutos.</span><span class="sxs-lookup"><span data-stu-id="7b999-122">The Counter **qualifier** for the **Average** property specifies the raw data source.</span></span>
-   <span data-ttu-id="7b999-123">O qualificador de **culináriatype** especifica a fórmula [Cooker \_ min](cooker-min.md) para calcular os dados.</span><span class="sxs-lookup"><span data-stu-id="7b999-123">The **CookingType** qualifier specifies the formula [COOKER\_MIN](cooker-min.md) for calculating the data.</span></span>
-   <span data-ttu-id="7b999-124">O qualificador **SampleWindow** especifica quantas amostras executar antes de executar o cálculo.</span><span class="sxs-lookup"><span data-stu-id="7b999-124">The **SampleWindow** qualifier specifies how many samples to take before performing the calculation.</span></span>


```mof
// Store the new Win32_PerfFormattedData_MemoryStatistics
//     class in the Root\Cimv2 namespace
#pragma autorecover
#pragma namespace("\\\\.\\Root\\CimV2")

qualifier vendor:ToInstance;
qualifier guid:ToInstance;
qualifier displayname:ToInstance;
qualifier perfindex:ToInstance;
qualifier helpindex:ToInstance;
qualifier perfdetail:ToInstance;
qualifier countertype:ToInstance;
qualifier perfdefault:ToInstance;
qualifier defaultscale:ToInstance;

qualifier dynamic:ToInstance;
qualifier hiperf:ToInstance;
qualifier AutoCook:ToInstance;
qualifier AutoCook_RawClass:ToInstance;
qualifier CookingType:ToInstance;
qualifier Counter:ToInstance;


// Define the Win32_PerFormattedData_MemoryStatistics
//     class, derived from Win32_PerfFormattedData
[
  dynamic,
  // Name of formatted data provider: "WMIPerfInst" for Vista 
  //   and later
  provider("HiPerfCooker_v1"), 
  // Text that will identify new counter in Perfmon
  displayname("My Calculated Counter"),                            
  // A high performance class     
  Hiperf,
  // Contains calculated data 
  Cooked, 
  // Value must be 1 
  AutoCook(1), 
  // Raw performance class to get data for calculations
  AutoCook_RawClass("Win32_PerfRawData_PerfOS_Memory"),
  // Value must be 1        
  AutoCook_RawDefault(1),
  // Name of raw class property to use for timestamp in formulas 
  PerfSysTimeStamp("Timestamp_PerfTime"), 
  // Name of raw class property to use for frequency in formulas
  PerfSysTimeFreq("Frequency_PerfTime"), 
  // Name of raw class property to use for timestamp in formulas
  Perf100NSTimeStamp("Timestamp_Sys100NS"),
  // Name of raw class property to use for frequency in formulas
  Perf100NSTimeFreq("Frequency_Sys100NS"),
  // Name of raw class property to use for timestamp in formulas
  PerfObjTimeStamp("Timestamp_Object"),
  // Name of raw class property to use for frequency in formulas 
  PerfObjTimeFreq("Frequency_Object"),
  // Only one instance of class allowed in namespace
  singleton                                                   
]

class Win32_PerfFormattedData_MemoryStatistics
          : Win32_PerfFormattedData
{

// Define the properties for the class. 
// All the properties perform different
//     statistical operations on the same
//     property, AvailableMBytes, in the raw class

// Define the Average property,
//     which uses the "COOKER_AVERAGE" counter type and 
//     gets its data from the AvailableMBytes 
//     property in the raw class

    [
     CookingType("COOKER_AVERAGE"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Average = 0;

// Define the Min property, which uses
//     the "COOKER_MIN" counter type and 
//     gets its data from the AvailableMBytes
//     property in the raw class

    [
     CookingType("COOKER_MIN"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Min = 0;

// Define the Max property, which uses
//     the "COOKER_MAX" counter type and 
//     gets its data from the
//     AvailableMBytes property in the raw class

    [
     CookingType("COOKER_MAX"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Max = 0;

// Define the Range property, which uses
//     the "COOKER_RANGE" counter type and 
//     gets its data from the AvailableMBytes
//     property in the raw class

    [
     CookingType("COOKER_RANGE"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Range = 0;

// Define the Variance property, which uses
//     the "COOKER_VARIANCE" counter type and 
//     gets its data from the AvailableMBytes
//     property in the raw class

    [
     CookingType("COOKER_VARIANCE"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Variance = 0;
};
```



## <a name="script"></a><span data-ttu-id="7b999-125">Script</span><span class="sxs-lookup"><span data-stu-id="7b999-125">Script</span></span>

<span data-ttu-id="7b999-126">O exemplo de código de script a seguir obtém estatísticas sobre a memória disponível, em megabytes, usando o MOF criado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="7b999-126">The following script code example obtains statistics about available memory, in megabytes, using the MOF created previously.</span></span> <span data-ttu-id="7b999-127">O script usa o objeto de script [**SWbemRefresher**](swbemrefresher.md) para criar um atualizador que contém uma instância da classe de estatísticas que o arquivo MOF cria, que é o **Win32 \_ PerfFormattedData \_ MemoryStatistics**.</span><span class="sxs-lookup"><span data-stu-id="7b999-127">The script uses the [**SWbemRefresher**](swbemrefresher.md) scripting object to create a refresher that contains one instance of the statistics class that the MOF file creates, which is **Win32\_PerfFormattedData\_MemoryStatistics**.</span></span> <span data-ttu-id="7b999-128">Para obter mais informações sobre como usar scripts, consulte [atualizando dados do WMI em scripts](refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="7b999-128">For more information about using scripts, see [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span> <span data-ttu-id="7b999-129">Se estiver trabalhando em C++, consulte [acessando dados de desempenho em c++](accessing-performance-data-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="7b999-129">If working in C++, see [Accessing Performance Data in C++](accessing-performance-data-in-c--.md).</span></span>

> [!Note]  
> <span data-ttu-id="7b999-130">[**SWbemRefreshableItem. Object**](swbemrefreshableitem-object.md) deve ser chamado depois de obter o item da chamada para [**SWbemRefresher. Add**](swbemrefresher-add.md) ou o script falhará.</span><span class="sxs-lookup"><span data-stu-id="7b999-130">[**SWbemRefreshableItem.Object**](swbemrefreshableitem-object.md) must be called after obtaining the item from the call to [**SWbemRefresher.Add**](swbemrefresher-add.md) or the script will fail.</span></span> <span data-ttu-id="7b999-131">[**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) deve ser chamado antes de entrar no loop para obter valores de linha de base ou as propriedades estatísticas são zero (0) na primeira passagem.</span><span class="sxs-lookup"><span data-stu-id="7b999-131">[**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) must be called before entering the loop to obtain baseline values, or the statistical properties is zero (0) on the first pass.</span></span>

 


```VB
' Connect to the Root\Cimv2 namespace
strComputer = "."
Set objService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")

' Create a refresher
Set Refresher = CreateObject("WbemScripting.SWbemRefresher")
If Err <> 0 Then
WScript.Echo Err
WScript.Quit
End If

' Add the single instance of the statistics
'    class to the refresher
Set obMemoryStatistics = Refresher.Add(objService, _
    "Win32_PerfFormattedData_MemoryStatistics=@").Object

' Refresh once to obtain base values for cooking calculations
Refresher.Refresh

Const REFRESH_INTERVAL = 10

' Refresh every REFRESH_INTERVAL seconds 
For I=1 to 3
  WScript.Sleep REFRESH_INTERVAL * 1000
  Refresher.Refresh

  WScript.Echo "System memory statistics" _
      & "(Available Megabytes) " _
      & "for the past 100 seconds - pass " & i 
  WScript.Echo "Average = " _
     & obMemoryStatistics.Average & VBNewLine & "Max = " _
     & obMemoryStatistics.Max & VBNewLine & "Min = " _
     & obMemoryStatistics.Min & VBNewLine & "Range = " _ 
     & obMemoryStatistics.Range & VBNewLine & "Variance = " _
     & obMemoryStatistics.Variance 
Next
```



## <a name="running-the-script"></a><span data-ttu-id="7b999-132">Executando o script</span><span class="sxs-lookup"><span data-stu-id="7b999-132">Running the Script</span></span>

<span data-ttu-id="7b999-133">O procedimento a seguir descreve como executar o exemplo.</span><span class="sxs-lookup"><span data-stu-id="7b999-133">The following procedure describes how to run the example.</span></span>

<span data-ttu-id="7b999-134">**Para executar o script de exemplo**</span><span class="sxs-lookup"><span data-stu-id="7b999-134">**To run the example script**</span></span>

1.  <span data-ttu-id="7b999-135">Copie o código MOF e o script para arquivos em seu computador.</span><span class="sxs-lookup"><span data-stu-id="7b999-135">Copy both the MOF code and script to files on your computer.</span></span>
2.  <span data-ttu-id="7b999-136">Forneça ao arquivo MOF uma extensão. mof e o arquivo de script uma descrição de. vbs.</span><span class="sxs-lookup"><span data-stu-id="7b999-136">Give the MOF file a .mof extension and the script file a .vbs description.</span></span>
3.  <span data-ttu-id="7b999-137">Na linha de comando, altere para o diretório em que os arquivos são armazenados e execute [**Mofcomp**](mofcomp.md) no arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="7b999-137">On the command line, change to the directory where the files are stored, and run [**Mofcomp**](mofcomp.md) on the MOF file.</span></span> <span data-ttu-id="7b999-138">Por exemplo, se você nomear o arquivo *CalculatedData. mof*, o comando será **Mofcomp** *CalculatedData. mof*</span><span class="sxs-lookup"><span data-stu-id="7b999-138">For example, if you name the file *CalculatedData.mof*, then the command is **Mofcomp** *CalculatedData.mof*</span></span>
4.  <span data-ttu-id="7b999-139">Execute o script.</span><span class="sxs-lookup"><span data-stu-id="7b999-139">Run the script.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b999-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7b999-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b999-141">Monitorando dados de desempenho</span><span class="sxs-lookup"><span data-stu-id="7b999-141">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="7b999-142">Acessando classes de desempenho de WMI pré-instalado</span><span class="sxs-lookup"><span data-stu-id="7b999-142">Accessing WMI Preinstalled Performance Classes</span></span>](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="7b999-143">**Qualificadores de propriedade para classes de contador de desempenho formatadas**</span><span class="sxs-lookup"><span data-stu-id="7b999-143">**Property Qualifiers for Formatted Performance Counter Classes**</span></span>](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="7b999-144">Tipos de contadores estatísticos</span><span class="sxs-lookup"><span data-stu-id="7b999-144">Statistical Counter Types</span></span>](statistical-counter-types.md)
</dt> </dl>

 

 
