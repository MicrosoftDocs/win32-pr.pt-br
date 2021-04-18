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
# <a name="monitoring-performance-data"></a>Monitorando dados de desempenho

Usando o WMI, você pode acessar os dados do contador do sistema programaticamente de objetos nas bibliotecas de desempenho. Esses são os mesmos dados de desempenho que aparecem no monitor do sistema no utilitário Perfmon. Use as [classes de contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes) pré-instaladas para obter dados de desempenho em scripts ou aplicativos C++.

As seções a seguir são discutidas neste tópico:

-   [Classes de desempenho WMI](#wmi-performance-classes)
-   [Provedores de dados de desempenho](#performance-data-providers)
-   [Usando classes de dados de desempenho formatadas](#using-formatted-performance-data-classes)
-   [Usando classes de dados de desempenho brutos](#using-raw-performance-data-classes)
-   [Tópicos relacionados](#related-topics)

## <a name="wmi-performance-classes"></a>Classes de desempenho WMI

Por exemplo, o objeto "NetworkInterface", no monitor do sistema, é representado no WMI pela classe [**Win32 \_ PerfRawData \_ tcpip \_ NetworkInterface**](./retrieving-raw-and-formatted-performance-data.md) para dados brutos e a [**classe \_ \_ tcpip \_ NetworkInterface do Win32 PerfFormattedData**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) para dados precalculados ou formatados. As classes derivadas do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e do [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) devem ser usadas com um objeto de [*atualização*](gloss-r.md) . Em classes de dados brutos, seu aplicativo ou script C++ deve executar cálculos para obter a mesma saída que Perfmon.exe. As classes de dados formatadas fornecem dados pré-calculados. Para obter mais informações sobre como obter dados em aplicativos C++, consulte [acessando dados de desempenho em C++](accessing-performance-data-in-c--.md). Para scripts, consulte [acessando dados de desempenho em script](accessing-performance-data-in-script.md) e [atualizando dados do WMI em scripts](refreshing-wmi-data-in-scripts.md).

O exemplo de código VBScript a seguir usa o [**\_ \_ \_ processo Win32 PerfFormattedData PerfProc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) para obter dados de desempenho para o processo ocioso. O script exibe os mesmos dados que aparecem no perfmon para o contador% tempo do processador do objeto de processo. A chamada para [**SWbemObjectEx. Refresh \_**](swbemobjectex-refresh-.md) executa a operação de atualização. Lembre-se de que os dados devem ser atualizados, na concessão uma vez, para obter uma linha de base.


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



As classes de contador de desempenho também podem fornecer dados estatísticos. Para obter mais informações, consulte [obtendo dados de desempenho estatísticos](obtaining-statistical-performance-data.md).

## <a name="performance-data-providers"></a>Provedores de dados de desempenho

O WMI tem provedores pré-instalados que monitoram o desempenho do sistema no sistema local e remotamente. O provedor [WmiPerfClass](wmiperfclass-provider.md) cria as classes derivadas do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e do [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata). O provedor [WmiPerfInst](wmiperfinst-provider.md) fornece dados dinamicamente para classes não processadas e formatadas.

## <a name="using-formatted-performance-data-classes"></a>Usando classes de dados de desempenho formatadas

O exemplo de código VBScript a seguir obtém dados de desempenho sobre memória, partições de disco e filas de trabalho do servidor. O script determina se os valores estão dentro de um intervalo aceitável.

O script usa os seguintes objetos de provedor de WMI e objetos de script:

-   Classes de contador de desempenho de WMI pré-instaladas.
-   O objeto do atualizador, [**SWbemRefresher**](swbemrefresher.md).
-   Itens a serem adicionados ao contêiner do atualizador, [ **SWbemRefreshableItem**](swbemrefreshableitem.md)


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

O exemplo de código VBScript a seguir obtém o tempo de processador percentual atual bruto no computador local e o converte em uma porcentagem. O exemplo mostra como obter dados de desempenho brutos da propriedade **PercentProcessorTime** da classe de [**\_ \_ \_ processador Win32 PerfRawData PerfOS**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) .

Para calcular o valor da porcentagem de tempo do processador, você deve localizar a fórmula. Pesquise o valor no qualificador de **tipo** para a propriedade **PercentProcessorTime** na tabela de [**qualificador de tipo de ComType**](countertype-qualifier.md) para obter o nome da constante. Localize o nome da constante em [tipos de contadores](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) para obter a fórmula.


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

 

 
