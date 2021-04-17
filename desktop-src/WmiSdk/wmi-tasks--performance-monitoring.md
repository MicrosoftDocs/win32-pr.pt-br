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
ms.openlocfilehash: bbb254e14280bec5a928bdc32aaa9a3e03c7a4f4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105769088"
---
# <a name="wmi-tasks-performance-monitoring"></a><span data-ttu-id="473c1-103">Tarefas do WMI: monitoramento de desempenho</span><span class="sxs-lookup"><span data-stu-id="473c1-103">WMI Tasks: Performance Monitoring</span></span>

<span data-ttu-id="473c1-104">Use as classes WMI que obtêm dados de contadores de desempenho para acessar e atualizar dados sobre o desempenho do computador.</span><span class="sxs-lookup"><span data-stu-id="473c1-104">Use the WMI classes that obtain data from performance counters to access and refresh data about computer performance.</span></span> <span data-ttu-id="473c1-105">Para obter outros exemplos, consulte o TechNet ScriptCenter em [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="473c1-105">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span> <span data-ttu-id="473c1-106">Para obter mais informações, consulte [bibliotecas de desempenho e WMI](performance-libraries-and-wmi.md) e [monitorando dados de desempenho](monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="473c1-106">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md) and [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

<span data-ttu-id="473c1-107">Os exemplos de script mostrados neste tópico obtêm dados somente do computador local.</span><span class="sxs-lookup"><span data-stu-id="473c1-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="473c1-108">Para obter mais informações sobre como usar o script para obter dados de computadores remotos, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="473c1-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="473c1-109">O procedimento a seguir descreve como executar um script.</span><span class="sxs-lookup"><span data-stu-id="473c1-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="473c1-110">**Para executar um script**</span><span class="sxs-lookup"><span data-stu-id="473c1-110">**To run a script**</span></span>

1.  <span data-ttu-id="473c1-111">Copie o código e salve-o em um arquivo com uma extensão. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="473c1-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="473c1-112">Verifique se o editor de texto não adiciona uma extensão. txt ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="473c1-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="473c1-113">Abra uma janela de prompt de comando e navegue até o diretório em que você salvou o arquivo.</span><span class="sxs-lookup"><span data-stu-id="473c1-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="473c1-114">Digite **cscript filename.vbs** no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="473c1-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="473c1-115">Se você não puder acessar um log de eventos, verifique se você está executando a partir de um prompt de comandos com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="473c1-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="473c1-116">Alguns logs de eventos, como o log de eventos de segurança, podem ser protegidos por UAC (controles de acesso do usuário).</span><span class="sxs-lookup"><span data-stu-id="473c1-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="473c1-117">Por padrão, o cscript exibe a saída de um script na janela de prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="473c1-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="473c1-118">Como os scripts WMI podem produzir grandes quantidades de saída, convém redirecionar a saída para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="473c1-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="473c1-119">Digite **cscript filename.vbs > outfile.txt** no prompt de comando para redirecionar a saída do script de *filename.vbs* para *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="473c1-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="473c1-120">A tabela a seguir lista os exemplos de script que podem ser usados para obter vários tipos de dados do computador local.</span><span class="sxs-lookup"><span data-stu-id="473c1-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="473c1-121">Como fazer...</span><span class="sxs-lookup"><span data-stu-id="473c1-121">How do I...</span></span></th>
<th><span data-ttu-id="473c1-122">Classes ou métodos WMI</span><span class="sxs-lookup"><span data-stu-id="473c1-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="473c1-123">... obter os dados do contador de desempenho que posso ver no utilitário Perfmon em um script?</span><span class="sxs-lookup"><span data-stu-id="473c1-123">...obtain the performance counter data that I can see in the Perfmon utility in a script?</span></span></td>
<td><span data-ttu-id="473c1-124">Use classes que têm nomes que começam com &quot; <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Win32_PerfFormattedData</a> &quot; , por exemplo <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="473c1-124">Use classes that have names that begin with &quot;<a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Win32_PerfFormattedData</a>&quot;, for example <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a>.</span></span> <span data-ttu-id="473c1-125">Propriedades com nomes como <strong>PageFileBytes</strong> correspondem a contadores de desempenho que você vê no perfmon.</span><span class="sxs-lookup"><span data-stu-id="473c1-125">Properties with names like <strong>PageFileBytes</strong> correspond to performance counters you see in Perfmon.</span></span> <span data-ttu-id="473c1-126">As &quot; classes de Win32_PerfFormattedData &quot; calculam os valores finais dos contadores para você.</span><span class="sxs-lookup"><span data-stu-id="473c1-126">The &quot;Win32_PerfFormattedData&quot; classes calculate the final values of counters for you.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="473c1-127">... obter dados de desempenho em andamento para um único processo, unidade de disco e outros dados?</span><span class="sxs-lookup"><span data-stu-id="473c1-127">...get on-going performance data for a single process, disk drive, and other data?</span></span></td>
<td><span data-ttu-id="473c1-128">Use o <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> ou a classe de <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">contador de desempenho</a> formatada apropriada e o método <a href="swbemobjectex-refresh-.md"><strong>SWbemObjectEx.Refresh_</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="473c1-128">Use the <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> or the appropriate formatted <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Performance Counter Class</a> and the <a href="swbemobjectex-refresh-.md"><strong>SWbemObjectEx.Refresh_</strong></a> method.</span></span> <span data-ttu-id="473c1-129">Para obter mais informações, consulte <a href="scripting-with-swbemobject.md">scripts com SWbemObject</a>.</span><span class="sxs-lookup"><span data-stu-id="473c1-129">For more information, see <a href="scripting-with-swbemobject.md">Scripting with SWbemObject</a>.</span></span><br/> <span data-ttu-id="473c1-130">Em C++, use <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>IWbemConfigureRefresher:: AddObjectByPath</strong></a> e <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>IWbemRefresher:: Refresh</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="473c1-130">In C++, use <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>IWbemConfigureRefresher::AddObjectByPath</strong></a> and <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>IWbemRefresher::Refresh</strong></a>.</span></span> <span data-ttu-id="473c1-131">Para obter mais informações, consulte <a href="monitoring-performance-data.md">monitorando dados de desempenho</a>.</span><span class="sxs-lookup"><span data-stu-id="473c1-131">For more information, see <a href="monitoring-performance-data.md">Monitoring Performance Data</a>.</span></span><br/> <span data-ttu-id="473c1-132">O script a seguir é executado até que o computador seja reiniciado, o WMI é interrompido ou o script é interrompido.</span><span class="sxs-lookup"><span data-stu-id="473c1-132">The following script runs until the computer is restarted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="473c1-133">Para interromper o script manualmente, use o Gerenciador de tarefas para interromper o processo.</span><span class="sxs-lookup"><span data-stu-id="473c1-133">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="473c1-134">Para interrompê-lo programaticamente, use o método <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> na classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="473c1-134">To stop it programmatically, use the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method in the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="473c1-135">VB</span><span class="sxs-lookup"><span data-stu-id="473c1-135">VB</span></span></th>
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
<td><span data-ttu-id="473c1-136">... obter dados de desempenho em andamento para todos os processos sem sondagem repetida?</span><span class="sxs-lookup"><span data-stu-id="473c1-136">...get on-going performance data for all processes without repeated polling?</span></span></td>
<td><p><span data-ttu-id="473c1-137">Use classes que têm nomes que começam com &quot; Win32_PerfFormattedData &quot; e um objeto <a href="swbemrefresher.md"><strong>SWbemRefresher</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="473c1-137">Use classes that have names that begin with &quot;Win32_PerfFormattedData&quot; and an <a href="swbemrefresher.md"><strong>SWbemRefresher</strong></a> object.</span></span> <span data-ttu-id="473c1-138">O atualizador mantém os objetos para que você não precise obter a coleção repetidamente.</span><span class="sxs-lookup"><span data-stu-id="473c1-138">The refresher holds the objects so you do not need to get the collection repeatedly.</span></span> <span data-ttu-id="473c1-139">Um mínimo de dois valores são necessários para calcular os dados de desempenho porque a maioria dos contadores são contadores de taxa.</span><span class="sxs-lookup"><span data-stu-id="473c1-139">A minimum of two values are needed to calculate performance data because most counters are rate counters.</span></span> <span data-ttu-id="473c1-140">Na primeira vez que você exibe os dados do atualizador, eles estão vazios.</span><span class="sxs-lookup"><span data-stu-id="473c1-140">The first time you display the refresher data it is empty.</span></span></p>
<p><span data-ttu-id="473c1-141">O script a seguir é executado indefinidamente até que o computador seja reinicializado, o WMI é interrompido ou o script é interrompido.</span><span class="sxs-lookup"><span data-stu-id="473c1-141">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="473c1-142">Para interromper o script manualmente, use o Gerenciador de tarefas para interromper o processo.</span><span class="sxs-lookup"><span data-stu-id="473c1-142">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="473c1-143">Para interrompê-lo programaticamente, use o método <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> na classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="473c1-143">To stop it programmatically, use the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method in the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="473c1-144">VB</span><span class="sxs-lookup"><span data-stu-id="473c1-144">VB</span></span></th>
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
<td><span data-ttu-id="473c1-145">... obter e calcular dados de desempenho para processos no Windows 2000?</span><span class="sxs-lookup"><span data-stu-id="473c1-145">...get and calculate performance data for processes on Windows 2000?</span></span></td>
<td><p><span data-ttu-id="473c1-146">Use as &quot; classes de Win32_PerfRawData &quot; , como <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfRawData_PerfProc_Process</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="473c1-146">Use the &quot;Win32_PerfRawData&quot; classes, such as <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfRawData_PerfProc_Process</strong></a>.</span></span> <span data-ttu-id="473c1-147">Obtenha os dados de propriedade, como <strong>PercentProcessorTime</strong>, duas vezes para um processo específico.</span><span class="sxs-lookup"><span data-stu-id="473c1-147">Get the property data, such as <strong>PercentProcessorTime</strong>, twice for a specific process.</span></span> <span data-ttu-id="473c1-148">Pesquisar a fórmula especificada no qualificador de <a href="countertype-qualifier.md"><strong>tipo</strong></a> de propriedade e calcular.</span><span class="sxs-lookup"><span data-stu-id="473c1-148">Look up the formula specified in the <a href="countertype-qualifier.md"><strong>CounterType</strong></a> qualifier for the property and calculate.</span></span> <span data-ttu-id="473c1-149">O tipo de meio no exemplo é <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>.</span><span class="sxs-lookup"><span data-stu-id="473c1-149">The CounterType in the example is <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>.</span></span> <span data-ttu-id="473c1-150">Para obter mais informações, consulte <a href="monitoring-performance-data.md">monitorando dados de desempenho</a>.</span><span class="sxs-lookup"><span data-stu-id="473c1-150">For more information, see <a href="monitoring-performance-data.md">Monitoring Performance Data</a>.</span></span></p>
<p><span data-ttu-id="473c1-151">O script a seguir é executado indefinidamente até que o computador seja reinicializado, o WMI é interrompido ou o script é interrompido.</span><span class="sxs-lookup"><span data-stu-id="473c1-151">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="473c1-152">Para interromper o script manualmente, use o Gerenciador de tarefas para interromper o processo.</span><span class="sxs-lookup"><span data-stu-id="473c1-152">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="473c1-153">Para interrompê-lo programaticamente, use o método <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> na classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="473c1-153">To stop it programmatically, use the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method in the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="473c1-154">VB</span><span class="sxs-lookup"><span data-stu-id="473c1-154">VB</span></span></th>
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



 

## <a name="related-topics"></a><span data-ttu-id="473c1-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="473c1-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="473c1-156">Tarefas do WMI para scripts e aplicativos</span><span class="sxs-lookup"><span data-stu-id="473c1-156">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="473c1-157">Exemplos de aplicativos WMI C++</span><span class="sxs-lookup"><span data-stu-id="473c1-157">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="473c1-158">ScriptCenter do TechNet</span><span class="sxs-lookup"><span data-stu-id="473c1-158">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>
