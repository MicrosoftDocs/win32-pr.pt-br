---
description: As tarefas do WMI para processos obtêm informações como a conta sob a qual um processo está sendo executado. Você pode executar ações como criar processos. Para obter outros exemplos, consulte o TechNet ScriptCenter em https://www.microsoft.com/technet .
ms.assetid: 2ae7c302-ab8b-4150-8ece-ffb66374b3f7
ms.tgt_platform: multiple
title: 'Tarefas WMI: processos '
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a720046d8f5cd25c55f2d5f367d2c23d5e4fc882
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104461363"
---
# <a name="wmi-tasks-processes"></a><span data-ttu-id="353a0-105">Tarefas WMI: processos </span><span class="sxs-lookup"><span data-stu-id="353a0-105">WMI Tasks: Processes</span></span>

<span data-ttu-id="353a0-106">As tarefas do WMI para processos obtêm informações como a conta sob a qual um processo está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="353a0-106">WMI tasks for processes obtain information such as the account under which a process is running.</span></span> <span data-ttu-id="353a0-107">Você pode executar ações como criar processos.</span><span class="sxs-lookup"><span data-stu-id="353a0-107">You can perform actions like creating processes.</span></span> <span data-ttu-id="353a0-108">Para obter outros exemplos, consulte o TechNet ScriptCenter em [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="353a0-108">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="353a0-109">Os exemplos de script mostrados neste tópico obtêm dados somente do computador local.</span><span class="sxs-lookup"><span data-stu-id="353a0-109">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="353a0-110">Para obter mais informações sobre como usar o script para obter dados de computadores remotos, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="353a0-110">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="353a0-111">O procedimento a seguir descreve como executar um script.</span><span class="sxs-lookup"><span data-stu-id="353a0-111">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="353a0-112">**Para executar um script**</span><span class="sxs-lookup"><span data-stu-id="353a0-112">**To run a script**</span></span>

1.  <span data-ttu-id="353a0-113">Copie o código e salve-o em um arquivo com uma extensão. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="353a0-113">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="353a0-114">Verifique se o editor de texto não adiciona uma extensão. txt ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="353a0-114">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="353a0-115">Abra uma janela de prompt de comando e navegue até o diretório em que você salvou o arquivo.</span><span class="sxs-lookup"><span data-stu-id="353a0-115">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="353a0-116">Digite **cscript filename.vbs** no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="353a0-116">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="353a0-117">Se você não puder acessar um log de eventos, verifique se você está executando a partir de um prompt de comandos com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="353a0-117">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="353a0-118">Alguns logs de eventos, como o log de eventos de segurança, podem ser protegidos por UAC (controles de acesso do usuário).</span><span class="sxs-lookup"><span data-stu-id="353a0-118">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="353a0-119">Por padrão, o cscript exibe a saída de um script na janela de prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="353a0-119">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="353a0-120">Como os scripts WMI podem produzir grandes quantidades de saída, convém redirecionar a saída para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="353a0-120">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="353a0-121">Digite **cscript filename.vbs > outfile.txt** no prompt de comando para redirecionar a saída do script de *filename.vbs* para *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="353a0-121">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="353a0-122">A tabela a seguir lista os exemplos de script que podem ser usados para obter vários tipos de dados do computador local.</span><span class="sxs-lookup"><span data-stu-id="353a0-122">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="353a0-123">Como fazer...</span><span class="sxs-lookup"><span data-stu-id="353a0-123">How do I...</span></span></th>
<th><span data-ttu-id="353a0-124">Classes ou métodos WMI</span><span class="sxs-lookup"><span data-stu-id="353a0-124">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="353a0-125">... executar um aplicativo em uma janela oculta?</span><span class="sxs-lookup"><span data-stu-id="353a0-125">...run an application in a hidden window?</span></span></td>
<td><span data-ttu-id="353a0-126">Chame o aplicativo de um script que usa as classes <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> e <a href="/windows/desktop/CIMWin32Prov/win32-processstartup"><strong>Win32_ProcessStartup</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="353a0-126">Call the application from a script that uses the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> and <a href="/windows/desktop/CIMWin32Prov/win32-processstartup"><strong>Win32_ProcessStartup</strong></a> classes.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="353a0-127">VB</span><span class="sxs-lookup"><span data-stu-id="353a0-127">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const HIDDEN_WINDOW = 0
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set objStartup = objWMIService.Get(&quot;Win32_ProcessStartup&quot;)
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = HIDDEN_WINDOW
Set objProcess = GetObject(&quot;winmgmts:root\cimv2:Win32_Process&quot;)
errReturn = objProcess.Create( &quot;Notepad.exe&quot;, null, objConfig, intProcessID)</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="353a0-128">PowerShell</span><span class="sxs-lookup"><span data-stu-id="353a0-128">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$startup=[wmiclass]&quot;Win32_ProcessStartup&quot;
$startup.Properties[&#39;ShowWindow&#39;].value=$False
([wmiclass]&quot;win32_Process&quot;).create(&#39;notepad.exe&#39;,&#39;C:\&#39;,$Startup)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="353a0-129">... determinar quais scripts estão em execução no computador local?</span><span class="sxs-lookup"><span data-stu-id="353a0-129">...determine which scripts are running on the local computer?</span></span></td>
<td><p><span data-ttu-id="353a0-130">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> e retorne todos os processos com o nome Cscript.exe ou Wscript.exe.</span><span class="sxs-lookup"><span data-stu-id="353a0-130">Use the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class and return all processes with the name Cscript.exe or Wscript.exe.</span></span> <span data-ttu-id="353a0-131">Para determinar os scripts individuais em execução nesses processos, verifique o valor da propriedade <strong>CommandLine</strong> .</span><span class="sxs-lookup"><span data-stu-id="353a0-131">To determine the individual scripts running in these processes, check the value of the <strong>CommandLine</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="353a0-132">VB</span><span class="sxs-lookup"><span data-stu-id="353a0-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot; 
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\CIMV2&quot;) 
Set colItems = objWMIService.ExecQuery(&quot;SELECT * FROM Win32_Process&quot; & _
           &quot; WHERE Name = &#39;cscript.exe&#39;&quot; & &quot; OR Name = &#39;wscript.exe&#39;&quot;,,48) 
For Each objItem in colItems 
    Wscript.Echo &quot;-------------------------------------------&quot;
    Wscript.Echo &quot;CommandLine: &quot; & objItem.CommandLine
    Wscript.Echo &quot;Name: &quot; & objItem.Name
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="353a0-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="353a0-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
Get-WmiObject -Class &quot;Win32_Process&quot; -ComputerName &quot;.&quot; | `
     where {($_.name -eq &#39;cscript.exe&#39;) -or ($_.name -eq &#39;wscript.exe&#39;) } | `
     Format-List -Property CommandLine, Name</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="353a0-134">... descobrir o nome da conta sob a qual um processo está sendo executado?</span><span class="sxs-lookup"><span data-stu-id="353a0-134">...find out the account name under which a process is running?</span></span></td>
<td><p><span data-ttu-id="353a0-135">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> e o método <a href="/windows/desktop/CIMWin32Prov/getowner-method-in-class-win32-process"><strong>GetOwner</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="353a0-135">Use the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/getowner-method-in-class-win32-process"><strong>GetOwner</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="353a0-136">VB</span><span class="sxs-lookup"><span data-stu-id="353a0-136">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcessList
    colProperties = objProcess.GetOwner( strNameOfUser,strUserDomain)
    Wscript.Echo &quot;Process &quot; & objProcess.Name & &quot; is owned by &quot; & strUserDomain & &quot;\&quot; & strNameOfUser & &quot;.&quot;
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="353a0-137">PowerShell</span><span class="sxs-lookup"><span data-stu-id="353a0-137">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -class win32_process -ComputerName &quot;.&quot; | ForEach-Object { $_.GetOwner() | Select -Property domain, user }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="353a0-138">... alterar a prioridade de um processo em execução?</span><span class="sxs-lookup"><span data-stu-id="353a0-138">...change the priority of a running process?</span></span></td>
<td><p><span data-ttu-id="353a0-139">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> e o método <a href="/windows/desktop/CIMWin32Prov/setpriority-method-in-class-win32-process"><strong>setanteriority</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="353a0-139">Use the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/setpriority-method-in-class-win32-process"><strong>SetPriority</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="353a0-140">VB</span><span class="sxs-lookup"><span data-stu-id="353a0-140">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const ABOVE_NORMAL = 32768
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcesses = objWMIService.ExecQuery (&quot;Select * from Win32_Process Where Name = &#39;Notepad.exe&#39;&quot;)
For Each objProcess in colProcesses
    objProcess.SetPriority(ABOVE_NORMAL) 
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="353a0-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="353a0-141">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$ABOVE_NORMAL = 32768
$strComputer = &quot;.&quot;
$colProcesses = Get-WmiObject -Class Win32_Process -ComputerName $strComputer | Where-Object { $_.name -eq &#39;Notepad.exe&#39; }
foreach ($objProcess in $colProcesses) { $objProcess.SetPriority($ABOVE_NORMAL) }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="353a0-142">... encerrar um processo usando um script?</span><span class="sxs-lookup"><span data-stu-id="353a0-142">...terminate a process using a script?</span></span></td>
<td><p><span data-ttu-id="353a0-143">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> e o método <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="353a0-143">Use the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="353a0-144">VB</span><span class="sxs-lookup"><span data-stu-id="353a0-144">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process Where Name = &#39;Notepad.exe&#39;&quot;)
For Each objProcess in colProcessList
    objProcess.Terminate()
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="353a0-145">PowerShell</span><span class="sxs-lookup"><span data-stu-id="353a0-145">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colProcesses = Get-WmiObject -Class Win32_Process -ComputerName $strComputer | Where-Object { $_.name -eq &#39;Notepad.exe&#39; }
foreach ($objProcess in $colProcesses) { $objProcess.Terminate() }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="353a0-146">... determinar quanto tempo de processador e memória cada processo está usando?</span><span class="sxs-lookup"><span data-stu-id="353a0-146">...determine how much processor time and memory each process is using?</span></span></td>
<td><p><span data-ttu-id="353a0-147">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> e as propriedades como <strong>KernelModeTime</strong>, <strong>WorkingSetSize</strong>, <strong>PageFileUsage</strong>e <strong>PageFaults</strong>.</span><span class="sxs-lookup"><span data-stu-id="353a0-147">Use the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class and properties such as <strong>KernelModeTime</strong>, <strong>WorkingSetSize</strong>, <strong>PageFileUsage</strong>, and <strong>PageFaults</strong>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="353a0-148">VB</span><span class="sxs-lookup"><span data-stu-id="353a0-148">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcesses = objWMIService.ExecQuery(&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcesses
    Wscript.Echo &quot;Process: &quot; & objProcess.Name
    sngProcessTime = (CSng(objProcess.KernelModeTime) + CSng(objProcess.UserModeTime)) / 10000000
    Wscript.Echo &quot;Processor Time: &quot; & sngProcessTime
    Wscript.Echo &quot;Process ID: &quot; & objProcess.ProcessID
    Wscript.Echo &quot;Working Set Size: &quot; & objProcess.WorkingSetSize
    Wscript.Echo &quot;Page File Size: &quot; & objProcess.PageFileUsage
    Wscript.Echo &quot;Page Faults: &quot; & objProcess.PageFaults
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="353a0-149">PowerShell</span><span class="sxs-lookup"><span data-stu-id="353a0-149">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
Get-WmiObject -Class &quot;Win32s_Process&quot; -ComputerName $strComputer | `
     Format-List -Property Name, KernelModeTime, UserModeTime, ProcessID, WorkingSetSize, PageFileUsage, PageFaults</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="353a0-150">... informa quais aplicativos estão em execução em um computador remoto?</span><span class="sxs-lookup"><span data-stu-id="353a0-150">...tell what applications are running on a remote computer?</span></span></td>
<td><p><span data-ttu-id="353a0-151">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="353a0-151">Use the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="353a0-152">VB</span><span class="sxs-lookup"><span data-stu-id="353a0-152">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process: &quot; & objProcess.Name 
    Wscript.Echo &quot;Process ID: &quot; & objProcess.ProcessID 
    Wscript.Echo &quot;Thread Count: &quot; & objProcess.ThreadCount 
    Wscript.Echo &quot;Page File Size: &quot; & objProcess.PageFileUsage 
    Wscript.Echo &quot;Page Faults: &quot; & objProcess.PageFaults 
    Wscript.Echo &quot;Working Set Size: &quot; & objProcess.WorkingSetSize 
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="353a0-153">PowerShell</span><span class="sxs-lookup"><span data-stu-id="353a0-153">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
get-wmiObject -class Win32_Process -Namespace &quot;root\cimv2&quot; -ComputerName $strComputer | `
   Format-list Name, ProcessID, ThreadCount, PageFileUsage, PageFaults, WorkingSetSize</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="353a0-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="353a0-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="353a0-155">Tarefas do WMI para scripts e aplicativos</span><span class="sxs-lookup"><span data-stu-id="353a0-155">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="353a0-156">Exemplos de aplicativos WMI C++</span><span class="sxs-lookup"><span data-stu-id="353a0-156">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="353a0-157">ScriptCenter do TechNet</span><span class="sxs-lookup"><span data-stu-id="353a0-157">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

