---
description: Use as classes WMI que obtêm dados de contadores de desempenho para acessar e atualizar dados sobre o desempenho do computador.
ms.assetid: 4c88de96-992e-4d34-ba93-35d2b6e73c1d
ms.tgt_platform: multiple
title: 'Tarefas do WMI: monitoramento de desempenho'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91302b0d6c6e13f86f275d755c5f4b6150de6a59dd400e47ed877d01f3fe876e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312052"
---
# <a name="wmi-tasks-performance-monitoring"></a>Tarefas do WMI: monitoramento de desempenho

Use as classes WMI que obtêm dados de contadores de desempenho para acessar e atualizar dados sobre o desempenho do computador. Para obter outros exemplos, consulte o TechNet ScriptCenter em [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) . Para obter mais informações, consulte [bibliotecas de desempenho e WMI](performance-libraries-and-wmi.md) e [monitorando dados de desempenho](monitoring-performance-data.md).

Os exemplos de script mostrados neste tópico obtêm dados somente do computador local. Para obter mais informações sobre como usar o script para obter dados de computadores remotos, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).


O procedimento a seguir descreve como executar um script.

**Para executar um script**

1.  Copie o código e salve-o em um arquivo com uma extensão. vbs, como *filename.vbs*. Verifique se o editor de texto não adiciona uma extensão de .txt ao arquivo.
2.  Abra uma janela de prompt de comando e navegue até o diretório em que você salvou o arquivo.
3.  Digite **cscript filename.vbs** no prompt de comando.
4.  Se você não puder acessar um log de eventos, verifique se você está executando a partir de um prompt de comandos com privilégios elevados. Alguns logs de eventos, como o log de eventos de segurança, podem ser protegidos por UAC (controles de acesso do usuário).

> [!Note]  
> Por padrão, o cscript exibe a saída de um script na janela de prompt de comando. Como os scripts WMI podem produzir grandes quantidades de saída, convém redirecionar a saída para um arquivo. Digite **cscript filename.vbs > outfile.txt** no prompt de comando para redirecionar a saída do script de *filename.vbs* para *outfile.txt*.

 

A tabela a seguir lista os exemplos de script que podem ser usados para obter vários tipos de dados do computador local.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Como fazer...</th>
<th>Classes ou métodos WMI</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>... obter os dados do contador de desempenho que posso ver no utilitário Perfmon em um script?</td>
<td>Use classes que têm nomes que começam com &quot; <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Win32_PerfFormattedData</a> &quot; , por exemplo <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a>. Propriedades com nomes como <strong>PageFileBytes</strong> correspondem a contadores de desempenho que você vê no perfmon. As &quot; classes de Win32_PerfFormattedData &quot; calculam os valores finais dos contadores para você.<br/></td>
</tr>
<tr class="even">
<td>... obter dados de desempenho em andamento para um único processo, unidade de disco e outros dados?</td>
<td>Use o <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> ou a classe de <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">contador de desempenho</a> formatada apropriada e o método <a href="swbemobjectex-refresh-.md"><strong>SWbemObjectEx.Refresh_</strong></a> . Para obter mais informações, consulte <a href="scripting-with-swbemobject.md">scripts com SWbemObject</a>.<br/> Em C++, use <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>IWbemConfigureRefresher:: AddObjectByPath</strong></a> e <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>IWbemRefresher:: Refresh</strong></a>. Para obter mais informações, consulte <a href="monitoring-performance-data.md">monitorando dados de desempenho</a>.<br/> O script a seguir é executado até que o computador seja reiniciado, o WMI é interrompido ou o script é interrompido. Para interromper o script manualmente, use o Gerenciador de tarefas para interromper o processo. Para interrompê-lo programaticamente, use o método <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> na classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .<br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
set PerfProcess = objWMIService.Get(_
    &quot;Win32_PerfFormattedData_PerfProc_Process.Name=&#39;Idle&#39;&quot;)

While (True)
    PerfProcess.Refresh_     
    Wscript.Echo PerfProcess.PercentProcessorTime
    Wscript.Sleep 1000
Wend</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="odd">
<td>... obter dados de desempenho em andamento para todos os processos sem sondagem repetida?</td>
<td><p>Use classes que têm nomes que começam com &quot; Win32_PerfFormattedData &quot; e um objeto <a href="swbemrefresher.md"><strong>SWbemRefresher</strong></a> . O atualizador mantém os objetos para que você não precise obter a coleção repetidamente. Um mínimo de dois valores são necessários para calcular os dados de desempenho porque a maioria dos contadores são contadores de taxa. Na primeira vez que você exibe os dados do atualizador, eles estão vazios.</p>
<p>O script a seguir é executado indefinidamente até que o computador seja reinicializado, o WMI é interrompido ou o script é interrompido. Para interromper o script manualmente, use o Gerenciador de tarefas para interromper o processo. Para interrompê-lo programaticamente, use o método <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> na classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
set objRefresher = CreateObject(&quot;WbemScripting.Swbemrefresher&quot;)
Set objProcessor = objRefresher.AddEnum _
    (objWMIService, _
    &quot;Win32_PerfFormattedData_PerfOS_Processor&quot;).ObjectSet

While (True)
    objRefresher.Refresh
        For each RefreshItem in objRefresher
            For each objProcess in RefreshItem.ObjectSet
                Wscript.Echo objProcess.GetObjectText_
            Next
        Next
     Wscript.Sleep 5000
Wend</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>... obter e calcular dados de desempenho para processos no Windows 2000?</td>
<td><p>Use as &quot; classes de Win32_PerfRawData &quot; , como <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfRawData_PerfProc_Process</strong></a>. Obtenha os dados de propriedade, como <strong>PercentProcessorTime</strong>, duas vezes para um processo específico. Pesquisar a fórmula especificada no qualificador de <a href="countertype-qualifier.md"><strong>tipo</strong></a> de propriedade e calcular. O tipo de meio no exemplo é <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>. Para obter mais informações, consulte <a href="monitoring-performance-data.md">monitorando dados de desempenho</a>.</p>
<p>O script a seguir é executado indefinidamente até que o computador seja reinicializado, o WMI é interrompido ou o script é interrompido. Para interromper o script manualmente, use o Gerenciador de tarefas para interromper o processo. Para interrompê-lo programaticamente, use o método <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> na classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)

While (True)
    Set object1 = objWMIService.Get( _
    &quot;Win32_PerfRawData_PerfOS_Processor.Name=&#39;_Total&#39;&quot;)
    N1 = object1.PercentProcessorTime
    D1 = object1.TimeStamp_Sys100NS
    Wscript.Sleep(1000)
    set object2 = objWMIService.Get( _
    &quot;Win32_PerfRawData_PerfOS_Processor.Name=&#39;_Total&#39;&quot;)
    N2 = object2.PercentProcessorTime
    D2 = object2.TimeStamp_Sys100NS
    &#39; CounterType - PERF_100NSEC_TIMER_INV
    &#39; Formula - (1- ((N2 - N1) / (D2 - D1))) x 100
    PercentProcessorTime = (1 - ((N2 - N1)/(D2-D1)))*100
    Wscript.Echo &quot;% Processor Time=&quot; , PercentProcessorTime
Wend</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas do WMI para scripts e aplicativos](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Exemplos de aplicativos WMI C++](wmi-c---application-examples.md)
</dt> <dt>

[ScriptCenter do TechNet](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>
