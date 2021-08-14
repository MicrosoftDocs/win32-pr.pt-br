---
description: Usando o WMI, você pode acessar dados do contador do sistema programaticamente de objetos nas bibliotecas de desempenho.
ms.assetid: a0ed14e9-d2ec-43eb-8c8e-eac3c134ea1d
ms.tgt_platform: multiple
title: Monitorando dados de desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba4f3ddd5024fb27d83f08225fa65faaa2e7d02cdd28189c86fc979175861453
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317100"
---
# <a name="monitoring-performance-data"></a>Monitorando dados de desempenho

Usando o WMI, você pode acessar dados do contador do sistema programaticamente de objetos nas bibliotecas de desempenho. Esses são os mesmos dados de desempenho que aparecem no Monitor do Sistema no utilitário Perfmon. Use as classes de contador de [desempenho pré-instaladas](/windows/desktop/CIMWin32Prov/performance-counter-classes) para obter dados de desempenho em scripts ou aplicativos C++.

As seções a seguir são discutidas neste tópico:

-   [Classes de desempenho WMI](#wmi-performance-classes)
-   [Provedores de dados de desempenho](#performance-data-providers)
-   [Usando classes de dados de desempenho formatadas](#using-formatted-performance-data-classes)
-   [Usando classes de dados de desempenho brutos](#using-raw-performance-data-classes)
-   [Tópicos relacionados](#related-topics)

## <a name="wmi-performance-classes"></a>Classes de desempenho WMI

Por exemplo, o objeto "NetworkInterface", no Monitor do Sistema, é representado no WMI pela classe [**\_ \_ Tcpip \_ NetworkInterface do Win32 PerfRawData**](./retrieving-raw-and-formatted-performance-data.md) para dados brutos e pela classe [**\_ \_ Tcpip \_ NetworkInterface do Win32 PerfFormattedData**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) para dados pré-calculados ou formatados. As classes derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) devem ser usadas com um [*objeto de atualização.*](gloss-r.md) Em classes de dados brutos, seu aplicativo ou script C++ deve executar cálculos para obter a mesma saída que Perfmon.exe. Classes de dados formatadas fornecem dados pré-calculados. Para obter mais informações sobre como obter dados em aplicativos C++, consulte [Acessando dados de desempenho no C++.](accessing-performance-data-in-c--.md) Para scripts, consulte [Acessando dados de desempenho no script e](accessing-performance-data-in-script.md) [Atualando dados WMI em scripts](refreshing-wmi-data-in-scripts.md).

O exemplo de código VBScript a seguir usa [**o Processo \_ \_ \_ PerfProc Do Win32 PerfFormattedData**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) para obter dados de desempenho para o processo Ocioso. O script exibe os mesmos dados que aparecem em Perfmon para o contador % de Tempo do Processador do objeto Process. A chamada para [**SWbemObjectEx.Refresh \_**](swbemobjectex-refresh-.md) executa a operação de atualização. Esteja ciente de que os dados devem ser atualizados, uma vez em concessão, para obter uma linha de base.


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



Classes de contador de desempenho também podem fornecer dados estatísticos. Para obter mais informações, consulte [Obtendo dados estatísticos de desempenho](obtaining-statistical-performance-data.md).

## <a name="performance-data-providers"></a>Provedores de dados de desempenho

O WMI tem provedores pré-instalados que monitoram o desempenho do sistema no sistema local e remotamente. O [provedor WmiPerfClass](wmiperfclass-provider.md) cria as classes derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e [**de Win32 \_ PerfFormattedData.**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) O [provedor WmiPerfInst](wmiperfinst-provider.md) fornece dados dinamicamente para classes brutas e formatadas.

## <a name="using-formatted-performance-data-classes"></a>Usando classes de dados de desempenho formatadas

O exemplo de código VBScript a seguir obtém dados de desempenho sobre memória, partições de disco e filas de trabalho do servidor. Em seguida, o script determina se os valores estão dentro de um intervalo aceitável.

O script usa os seguintes objetos de provedor WMI e objetos de script:

-   Classes de contador de desempenho WMI pré-instaladas.
-   O objeto de atualização, [**SWbemRefresher.**](swbemrefresher.md)
-   Itens a adicionar ao contêiner de atualização, [ **SWbemRefreshableItem**](swbemrefreshableitem.md)


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



## <a name="using-raw-performance-data-classes"></a>Usando classes de dados de desempenho brutos

O exemplo de código VBScript a seguir obtém o tempo de processador de porcentagem atual bruto no computador local e o converte em um percentual. O exemplo mostra como obter dados brutos de desempenho da propriedade **PercentProcessorTime** da classe [**processador PerfOS Win32 \_ PerfRawData. \_ \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)

Para calcular o valor de tempo do processador percentual, você deve localizar a fórmula. Procure o valor no qualificador **CounterType** para a propriedade **PercentProcessorTime** na tabela [**CounterType Qualifier**](countertype-qualifier.md) para obter o nome da constante. Localize o nome constante em [Tipos de Contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) para obter a fórmula.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o WMI](using-wmi.md)
</dt> </dl>

 

 
