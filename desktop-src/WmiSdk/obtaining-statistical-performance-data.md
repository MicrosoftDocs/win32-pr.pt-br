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
# <a name="obtaining-statistical-performance-data"></a>Obtendo dados de desempenho estatísticos

No WMI, você pode definir dados de desempenho estatísticos com base em dados em classes de desempenho formatadas derivadas do [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata). As estatísticas disponíveis são média, mínimo, máximo, intervalo e variação, conforme definido em [tipos de contador estatístico](statistical-counter-types.md).

A lista a seguir inclui os tipos de contadores estatísticos especiais:

-   [média de COOKER \_](cooker-average.md)
-   [COOKER \_ mín.](cooker-min.md)
-   [COOKER \_ Max](cooker-max.md)
-   [intervalo de COOKER \_](cooker-range.md)
-   [variância de COOKER \_](cooker-variance.md)

Os exemplos a seguir mostram como:

-   Crie um arquivo MOF que define uma classe de dados calculados.
-   Escreva um script que crie uma instância da classe e atualize periodicamente os dados na instância com os valores estatísticos recalculados.

## <a name="mof-file"></a>Arquivo MOF

O exemplo de código MOF a seguir cria uma nova classe de dados calculada chamada **Win32 \_ PerfFormattedData \_ AvailableMBytes**. Essa classe contém dados da propriedade **AvailableMBytes** da classe RAW [**Win32 \_ PerfRawData \_ PerfOS \_ Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data). A **classe Win32 \_ PerfFormattedData \_ AvailableBytes** define as propriedades **Average**, **min**, **Max**, **Range** e **Variance**.

O arquivo MOF usa os [**qualificadores de propriedade para classes de contador de desempenho formatadas**](property-qualifiers-for-performance-counter-classes.md) para definir a fonte de dados de propriedade e a fórmula de cálculo.

-   A propriedade **Average** obtém dados brutos da [**\_ \_ \_ memória PerfOS Win32 PerfRawData**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).**Propriedade AvailableMBytes** .
-   O **qualificador** do contador para a propriedade **Average** especifica a fonte de dados brutos.
-   O qualificador de **culináriatype** especifica a fórmula [Cooker \_ min](cooker-min.md) para calcular os dados.
-   O qualificador **SampleWindow** especifica quantas amostras executar antes de executar o cálculo.


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



## <a name="script"></a>Script

O exemplo de código de script a seguir obtém estatísticas sobre a memória disponível, em megabytes, usando o MOF criado anteriormente. O script usa o objeto de script [**SWbemRefresher**](swbemrefresher.md) para criar um atualizador que contém uma instância da classe de estatísticas que o arquivo MOF cria, que é o **Win32 \_ PerfFormattedData \_ MemoryStatistics**. Para obter mais informações sobre como usar scripts, consulte [atualizando dados do WMI em scripts](refreshing-wmi-data-in-scripts.md). Se estiver trabalhando em C++, consulte [acessando dados de desempenho em c++](accessing-performance-data-in-c--.md).

> [!Note]  
> [**SWbemRefreshableItem. Object**](swbemrefreshableitem-object.md) deve ser chamado depois de obter o item da chamada para [**SWbemRefresher. Add**](swbemrefresher-add.md) ou o script falhará. [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) deve ser chamado antes de entrar no loop para obter valores de linha de base ou as propriedades estatísticas são zero (0) na primeira passagem.

 


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



## <a name="running-the-script"></a>Executando o script

O procedimento a seguir descreve como executar o exemplo.

**Para executar o script de exemplo**

1.  Copie o código MOF e o script para arquivos em seu computador.
2.  Forneça ao arquivo MOF uma extensão. mof e o arquivo de script uma descrição de. vbs.
3.  Na linha de comando, altere para o diretório em que os arquivos são armazenados e execute [**Mofcomp**](mofcomp.md) no arquivo MOF. Por exemplo, se você nomear o arquivo *CalculatedData. mof*, o comando será **Mofcomp** *CalculatedData. mof*
4.  Execute o script.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Monitorando dados de desempenho](monitoring-performance-data.md)
</dt> <dt>

[Acessando classes de desempenho de WMI pré-instalado](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[**Qualificadores de propriedade para classes de contador de desempenho formatadas**](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[Tipos de contadores estatísticos](statistical-counter-types.md)
</dt> </dl>

 

 
