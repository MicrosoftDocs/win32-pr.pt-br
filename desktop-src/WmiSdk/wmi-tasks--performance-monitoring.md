---
description: Use as classes WMI que obtém dados de contadores de desempenho para acessar e atualizar dados sobre o desempenho do computador.
ms.assetid: 4c88de96-992e-4d34-ba93-35d2b6e73c1d
ms.tgt_platform: multiple
title: 'Tarefas WMI: Monitoramento de desempenho'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ff50e0a4656caf33289b534307043694dbe2cdce
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623911"
---
# <a name="wmi-tasks-performance-monitoring"></a>Tarefas WMI: Monitoramento de desempenho

Use as classes WMI que obtém dados de contadores de desempenho para acessar e atualizar dados sobre o desempenho do computador. Para outros exemplos, consulte o TechNet ScriptCenter em [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) . Para obter mais informações, consulte [Bibliotecas de desempenho e WMI](performance-libraries-and-wmi.md) e [Dados de desempenho de monitoramento.](monitoring-performance-data.md)

Os exemplos de script mostrados neste tópico só obtém dados do computador local. Para obter mais informações sobre como usar o script para obter dados de computadores remotos, consulte Conectando-se [ao WMI em um computador remoto.](connecting-to-wmi-on-a-remote-computer.md)


O procedimento a seguir descreve como executar um script.

**Para executar um script**

1.  Copie o código e salve-o em um arquivo com uma extensão .vbs, como *filename.vbs*. Verifique se o editor de texto não adiciona uma .txt de texto ao arquivo.
2.  Abra uma janela do prompt de comando e navegue até o diretório em que você salvou o arquivo.
3.  Digite **cscript filename.vbs** no prompt de comando.
4.  Se não for possível acessar um log de eventos, verifique se você está executando em um prompt de comando Elevado. Alguns log de eventos, como o Log de Eventos de Segurança, podem ser protegidos por UAC (Controles de Acesso do Usuário).

> [!Note]  
> Por padrão, o cscript exibe a saída de um script na janela do prompt de comando. Como os scripts WMI podem produzir grandes quantidades de saída, talvez você queira redirecionar a saída para um arquivo. Digite **cscript filename.vbs > outfile.txt** no prompt de comando para redirecionar a saída do script *filename.vbs* para *outfile.txt*.

 

A tabela a seguir lista exemplos de script que podem ser usados para obter vários tipos de dados do computador local.



<table>
<colgroup>
<col  />
<col  />
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
<td>Use classes que têm nomes que começam com &quot; <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Win32_PerfFormattedData</a> &quot; , por <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>exemplo, Win32_PerfFormattedData_PerfProc_Process</strong></a>. Propriedades com nomes como <strong>PageFileBytes</strong> correspondem aos contadores de desempenho que você vê no Perfmon. As &quot; Win32_PerfFormattedData classes base &quot; calculam os valores finais de contadores para você.<br/></td>
</tr>
<tr class="even">
<td>... obter dados de desempenho em execução para um único processo, unidade de disco e outros dados?</td>
<td>Use a <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> ou a Classe de Contador de Desempenho formatada <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">apropriada</a> e o <a href="swbemobjectex-refresh-.md"><strong>SWbemObjectEx.Refresh_</strong></a> método. Para obter mais informações, <a href="scripting-with-swbemobject.md">consulte Scripts com SWbemObject</a>.<br/> No C++, use <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>IWbemConfigureRefresher::AddObjectByPath</strong></a> e <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>IWbemRefresher::Refresh</strong></a>. Para obter mais informações, consulte <a href="monitoring-performance-data.md">Monitorando dados de desempenho.</a><br/> O script a seguir é executado até que o computador seja reiniciado, o WMI seja interrompido ou o script seja interrompido. Para interromper o script manualmente, use Gerenciador de Tarefas para interromper o processo. Para interromper programaticamente, use o <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>método Terminate</strong></a> na <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>classe Win32_Process.</strong></a><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
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
<td><p>Use classes que têm nomes que começam com &quot; Win32_PerfFormattedData e um objeto &quot; <a href="swbemrefresher.md"><strong>SWbemRefresher.</strong></a> O atualizador contém os objetos para que você não precise obter a coleção repetidamente. Um mínimo de dois valores são necessários para calcular dados de desempenho porque a maioria dos contadores são contadores de taxa. Na primeira vez que você exibe os dados do atualizador, eles estão vazios.</p>
<p>O script a seguir é executado indefinidamente até que o computador seja reinicializado, o WMI seja interrompido ou o script seja interrompido. Para interromper o script manualmente, use Gerenciador de Tarefas para interromper o processo. Para interromper programaticamente, use o <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>método Terminate</strong></a> na <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>classe Win32_Process.</strong></a></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
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
<td>... obter e calcular dados de desempenho para processos Windows 2000?</td>
<td><p>Use as &quot; classes &quot; Win32_PerfRawData, como <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong></strong></a>Win32_PerfRawData_PerfProc_Process . Obter os dados da propriedade, como <strong>PercentProcessorTime,</strong>duas vezes para um processo específico. Procure a fórmula especificada no qualificador <a href="countertype-qualifier.md"><strong>CounterType</strong></a> para a propriedade e calcule. O CounterType no exemplo é <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>. Para obter mais informações, consulte <a href="monitoring-performance-data.md">Monitorando dados de desempenho.</a></p>
<p>O script a seguir é executado indefinidamente até que o computador seja reinicializado, o WMI seja interrompido ou o script seja interrompido. Para interromper o script manualmente, use Gerenciador de Tarefas para interromper o processo. Para interromper programaticamente, use o <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>método Terminate</strong></a> na <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>classe Win32_Process.</strong></a></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
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

[Tarefas WMI para scripts e aplicativos](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Exemplos de aplicativo WMI C++](wmi-c---application-examples.md)
</dt> <dt>

[TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>
