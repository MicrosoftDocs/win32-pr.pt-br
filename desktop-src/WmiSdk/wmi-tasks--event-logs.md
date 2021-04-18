---
description: As tarefas do WMI para logs de eventos obtêm dados de eventos de arquivos de log de eventos e executam operações como backup ou limpeza de arquivos de log. Para obter outros exemplos, consulte o TechNet ScriptCenter em https://www.microsoft.com/technet .
ms.assetid: f6d4e68e-d757-44aa-be74-3b26168626b8
ms.tgt_platform: multiple
title: 'Tarefas WMI: logs de eventos '
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8fdcfe3f547e58fa60e552abad9867f8556fc8b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790390"
---
# <a name="wmi-tasks-event-logs"></a><span data-ttu-id="7cc4b-104">Tarefas WMI: logs de eventos </span><span class="sxs-lookup"><span data-stu-id="7cc4b-104">WMI Tasks: Event Logs</span></span>

<span data-ttu-id="7cc4b-105">As tarefas do WMI para logs de eventos obtêm dados de eventos de arquivos de log de eventos e executam operações como backup ou limpeza de arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="7cc4b-105">WMI tasks for event logs obtain event data from event log files and perform operations like backing up or clearing log files.</span></span> <span data-ttu-id="7cc4b-106">Para obter outros exemplos, consulte o TechNet ScriptCenter em [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7cc4b-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="7cc4b-107">Os exemplos de script mostrados neste tópico obtêm dados somente do computador local.</span><span class="sxs-lookup"><span data-stu-id="7cc4b-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="7cc4b-108">Para obter mais informações sobre como usar o script para obter dados de computadores remotos, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="7cc4b-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="7cc4b-109">O procedimento a seguir descreve como executar um script.</span><span class="sxs-lookup"><span data-stu-id="7cc4b-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="7cc4b-110">**Para executar um script**</span><span class="sxs-lookup"><span data-stu-id="7cc4b-110">**To run a script**</span></span>

1.  <span data-ttu-id="7cc4b-111">Copie o código e salve-o em um arquivo com uma extensão. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="7cc4b-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="7cc4b-112">Verifique se o editor de texto não adiciona uma extensão. txt ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="7cc4b-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="7cc4b-113">Abra uma janela de prompt de comando e navegue até o diretório em que você salvou o arquivo.</span><span class="sxs-lookup"><span data-stu-id="7cc4b-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="7cc4b-114">Digite **cscript filename.vbs** no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="7cc4b-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="7cc4b-115">Se você não puder acessar um log de eventos, verifique se você está executando a partir de um prompt de comandos com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="7cc4b-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="7cc4b-116">Alguns logs de eventos, como o log de eventos de segurança, podem ser protegidos por UAC (controles de acesso do usuário).</span><span class="sxs-lookup"><span data-stu-id="7cc4b-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="7cc4b-117">Por padrão, o cscript exibe a saída de um script na janela de prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="7cc4b-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="7cc4b-118">Como os scripts WMI podem produzir grandes quantidades de saída, convém redirecionar a saída para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="7cc4b-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="7cc4b-119">Digite **cscript filename.vbs > outfile.txt** no prompt de comando para redirecionar a saída do script de *filename.vbs* para *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="7cc4b-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="7cc4b-120">A tabela a seguir lista os exemplos de script que podem ser usados para obter vários tipos de dados do computador local.</span><span class="sxs-lookup"><span data-stu-id="7cc4b-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7cc4b-121">Como fazer...</span><span class="sxs-lookup"><span data-stu-id="7cc4b-121">How do I...</span></span></th>
<th><span data-ttu-id="7cc4b-122">Classes ou métodos WMI</span><span class="sxs-lookup"><span data-stu-id="7cc4b-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7cc4b-123">... recuperar informações sobre o log de eventos de segurança?</span><span class="sxs-lookup"><span data-stu-id="7cc4b-123">...retrieve information about the Security event log?</span></span></td>
<td><span data-ttu-id="7cc4b-124">Inclua o privilégio de <a href="privilege-constants.md">segurança</a> ao se conectar à classe <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7cc4b-124">Include the <a href="privilege-constants.md">Security</a> privilege when connecting to the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> class.</span></span> <span data-ttu-id="7cc4b-125">Para obter mais informações, consulte <a href="executing-privileged-operations-using-vbscript.md">executando operações privilegiadas usando o VBScript</a>.</span><span class="sxs-lookup"><span data-stu-id="7cc4b-125">For more information, see <a href="executing-privileged-operations-using-vbscript.md">Executing Privileged Operations Using VBScript</a>.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7cc4b-126">VB</span><span class="sxs-lookup"><span data-stu-id="7cc4b-126">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate,(Security)}!\\&quot; & _
        strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery _
    (&quot;Select * from Win32_NTEventLogFile &quot; _
        & &quot;Where LogFileName=&#39;Security&#39;&quot;)
For Each objLogFile in colLogFiles
    Wscript.Echo objLogFile.NumberOfRecords
    Wscript.Echo &quot;Maximum Size: &quot; _
    &  objLogfile.MaxFileSize 
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
<th><span data-ttu-id="7cc4b-127">PowerShell</span><span class="sxs-lookup"><span data-stu-id="7cc4b-127">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;security&#39;}
foreach ($objLogFile in $colLogFiles) 
{ 
    &quot;Record Number: &quot; + $objLogFile.NumberOfRecords
    &quot;Maximum Size: &quot; + $objLogFile.MaxFileSize
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cc4b-128">... fazer backup de um log de eventos?</span><span class="sxs-lookup"><span data-stu-id="7cc4b-128">...back up an event log?</span></span></td>
<td><p><span data-ttu-id="7cc4b-129">Use a classe <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> e o método <a href="/previous-versions/windows/desktop/eventlogprov/backupeventlog-method-in-class-win32-nteventlogfile"><strong>BackupEventLog</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7cc4b-129">Use the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> class and the <a href="/previous-versions/windows/desktop/eventlogprov/backupeventlog-method-in-class-win32-nteventlogfile"><strong>BackupEventLog</strong></a> method.</span></span> <span data-ttu-id="7cc4b-130">Talvez seja necessário incluir o privilégio de <a href="privilege-constants.md">backup</a> ao conectar-se ao WMI.</span><span class="sxs-lookup"><span data-stu-id="7cc4b-130">You may need to include the <a href="privilege-constants.md">Backup</a> privilege when connecting to WMI.</span></span> <span data-ttu-id="7cc4b-131">Para obter mais informações, consulte <a href="executing-privileged-operations-using-vbscript.md">executando operações privilegiadas usando o VBScript</a>.</span><span class="sxs-lookup"><span data-stu-id="7cc4b-131">For more information, see <a href="executing-privileged-operations-using-vbscript.md">Executing Privileged Operations Using VBScript</a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7cc4b-132">VB</span><span class="sxs-lookup"><span data-stu-id="7cc4b-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate,(Backup)}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery (&quot;Select * from Win32_NTEventLogFile &quot; & &quot;Where LogFileName=&#39;Application&#39;&quot;)
For Each objLogfile in colLogFiles
    errBackupLog = objLogFile.BackupEventLog(&quot;c:\scripts\application.evt&quot;)
    WScript.Echo &quot;File saved as c:\scripts\applications.evt&quot;
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
<th><span data-ttu-id="7cc4b-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="7cc4b-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;Application&#39;}

foreach ($objLogFile in $colLogFiles) 
{ 
    [void]$objLogFile.BackupEventlog(&quot;c:\scripts\applications.evt&quot;)
    &quot;File saved as c:\scripts\applications.evt&quot;
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cc4b-134">... fazer backup de um log de eventos mais de uma vez?</span><span class="sxs-lookup"><span data-stu-id="7cc4b-134">...back up an event log more than once?</span></span></td>
<td><p><span data-ttu-id="7cc4b-135">Verifique se o arquivo de backup tem um nome exclusivo antes de usar o <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> e o método <a href="/previous-versions/windows/desktop/eventlogprov/backupeventlog-method-in-class-win32-nteventlogfile"><strong>BackupEventLog</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7cc4b-135">Ensure that the backup file has a unique name before using the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> and the <a href="/previous-versions/windows/desktop/eventlogprov/backupeventlog-method-in-class-win32-nteventlogfile"><strong>BackupEventLog</strong></a> method.</span></span> <span data-ttu-id="7cc4b-136">O sistema operacional não permite que você substitua um arquivo de backup existente; Você deve mover o arquivo de backup ou renomeá-lo antes de poder executar o script novamente.</span><span class="sxs-lookup"><span data-stu-id="7cc4b-136">The operating system does not allow you to overwrite an existing backup file; you must either move the backup file or rename it before you can run the script again.</span></span> <span data-ttu-id="7cc4b-137">Talvez seja necessário incluir o privilégio de <a href="privilege-constants.md">backup</a> ao conectar-se ao WMI.</span><span class="sxs-lookup"><span data-stu-id="7cc4b-137">You may need to include the <a href="privilege-constants.md">Backup</a> privilege when connecting to WMI.</span></span> <span data-ttu-id="7cc4b-138">Para obter mais informações, consulte <a href="executing-privileged-operations-using-vbscript.md">executando operações privilegiadas usando o VBScript</a>.</span><span class="sxs-lookup"><span data-stu-id="7cc4b-138">For more information, see <a href="executing-privileged-operations-using-vbscript.md">Executing Privileged Operations Using VBScript</a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7cc4b-139">VB</span><span class="sxs-lookup"><span data-stu-id="7cc4b-139">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>dtmThisDay = Day(Date)
dtmThisMonth = Month(Date)
dtmThisYear = Year(Date)
strBackupName = dtmThisYear & &quot;_&quot; & dtmThisMonth & &quot;_&quot; & dtmThisDay
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate,(Backup)}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery (&quot;Select * from Win32_NTEventLogFile &quot; & &quot;Where LogFileName=&#39;Application&#39;&quot;)
For Each objLogfile in colLogFiles
    objLogFile.BackupEventLog(&quot;c:\scripts\&quot; & strBackupName & &quot;_application.evt&quot;)
    objLogFile.ClearEventLog()
    WScript.Echo &quot;File saved: &quot; & strBackupName & &quot;_application.evt&quot;
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
<th><span data-ttu-id="7cc4b-140">PowerShell</span><span class="sxs-lookup"><span data-stu-id="7cc4b-140">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$CurDate = Get-Date
$strBackupName = $curDate.Year.ToString() + &quot;_&quot; + $curDate.Month.ToString() + &quot;_&quot; + $CurDate.Day.ToString()

$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;Application&#39;}
foreach ($objLogFile in $colLogFiles) 
{ 
    $BackupFile = $objLogFile.BackupEventlog(&quot;c:\scripts\&quot; + $strBackupName + &quot;_application.evt&quot;)
    &quot;File saved: c:\scripts\&quot; + $strBackupName + &quot;_application.evt&quot;
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cc4b-141">... determinar o número de registros em um log de eventos?</span><span class="sxs-lookup"><span data-stu-id="7cc4b-141">...determine the number of records in an event log?</span></span></td>
<td><p><span data-ttu-id="7cc4b-142">Use a classe <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> e verifique o valor da propriedade <strong>NumberOfRecords</strong> .</span><span class="sxs-lookup"><span data-stu-id="7cc4b-142">Use the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> class and check the value of the <strong>NumberOfRecords</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7cc4b-143">VB</span><span class="sxs-lookup"><span data-stu-id="7cc4b-143">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery (&quot;Select * from Win32_NTEventLogFile &quot; & &quot;Where LogFileName=&#39;System&#39;&quot;)
For Each objLogFile in colLogFiles
    Wscript.Echo objLogFile.NumberOfRecords
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
<th><span data-ttu-id="7cc4b-144">PowerShell</span><span class="sxs-lookup"><span data-stu-id="7cc4b-144">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;System&#39;}

foreach ($objLogFile in $colLogFiles) 
{ 
    $objLogFile.NumberOfRecords
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cc4b-145">... limpar meus logs de eventos?</span><span class="sxs-lookup"><span data-stu-id="7cc4b-145">...clear my event logs?</span></span></td>
<td><p><span data-ttu-id="7cc4b-146">Use a classe <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> e o método <a href="/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile"><strong>ClearEventLog</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7cc4b-146">Use the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> class and the <a href="/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile"><strong>ClearEventLog</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7cc4b-147">VB</span><span class="sxs-lookup"><span data-stu-id="7cc4b-147">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate,(Backup, Security)}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery (&quot;Select * from Win32_NTEventLogFile &quot; & &quot;Where LogFileName=&#39;Application&#39;&quot;)
For Each objLogfile in colLogFiles
    objLogFile.ClearEventLog()
    WScript.Echo &quot;Cleared application event log file&quot;
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
<th><span data-ttu-id="7cc4b-148">PowerShell</span><span class="sxs-lookup"><span data-stu-id="7cc4b-148">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;System&#39;}

foreach ($objLogFile in $colLogFiles) 
{ 
    [void]$objLogFile.ClearEventlog()
    &quot;Cleared application event log file&quot;
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cc4b-149">... ler eventos dos logs de eventos?</span><span class="sxs-lookup"><span data-stu-id="7cc4b-149">...read events from the event logs?</span></span></td>
<td><p><span data-ttu-id="7cc4b-150">Use a classe <a href="/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent"><strong>Win32_NTLogEvent</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7cc4b-150">Use the <a href="/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent"><strong>Win32_NTLogEvent</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7cc4b-151">VB</span><span class="sxs-lookup"><span data-stu-id="7cc4b-151">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colLoggedEvents = objWMIService.ExecQuery _
    (&quot;Select * from Win32_NTLogEvent &quot; _
        & &quot;Where Logfile = &#39;System&#39;&quot;)
For Each objEvent in colLoggedEvents
    Wscript.Echo &quot;Category: &quot; & objEvent.Category & VBNewLine _
    & &quot;Computer Name: &quot; & objEvent.ComputerName & VBNewLine _
    & &quot;Event Code: &quot; & objEvent.EventCode & VBNewLine _
    & &quot;Message: &quot; & objEvent.Message & VBNewLine _
    & &quot;Record Number: &quot; & objEvent.RecordNumber & VBNewLine _
    & &quot;Source Name: &quot; & objEvent.SourceName & VBNewLine _
    & &quot;Time Written: &quot; & objEvent.TimeWritten & VBNewLine _
    & &quot;Event Type: &quot; & objEvent.Type & VBNewLine _
    & &quot;User: &quot; & objEvent.User
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
<th><span data-ttu-id="7cc4b-152">PowerShell</span><span class="sxs-lookup"><span data-stu-id="7cc4b-152">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTLogEvent -ComputerName $strComputer | Where-Object {$_.LogFile -eq &#39;System&#39;}

foreach ($objEvent in $colLoggedEvents) 
{ 
    &quot;Category: &quot; + $objEvent.Category
    &quot;Computer Name: &quot; + $objEvent.ComputerName
    &quot;Event Code: &quot; + $objEvent.EventCode
    &quot;Message: &quot; + $objEvent.Message
    &quot;Record Number: &quot; + $objEvent.RecordNumber
    &quot;Source Name: &quot; + $objEvent.SourceName
    &quot;Time Written: &quot; + $objEvent.TimeWritten
    &quot;Event Type: &quot; + $objEvent.Type
    &quot;User: &quot; + $objEvent.Use
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="7cc4b-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7cc4b-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cc4b-154">Tarefas do WMI para scripts e aplicativos</span><span class="sxs-lookup"><span data-stu-id="7cc4b-154">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="7cc4b-155">Exemplos de aplicativos WMI C++</span><span class="sxs-lookup"><span data-stu-id="7cc4b-155">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="7cc4b-156">ScriptCenter do TechNet</span><span class="sxs-lookup"><span data-stu-id="7cc4b-156">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

