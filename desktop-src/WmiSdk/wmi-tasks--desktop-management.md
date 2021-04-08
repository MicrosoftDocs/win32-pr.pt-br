---
description: As tarefas do WMI para gerenciamento de desktops podem exercer controle e obter dados de uma área de trabalho remota ou de um computador local.
ms.assetid: bb8356bf-de38-4925-a501-6ad47d23ea8f
ms.tgt_platform: multiple
title: 'Tarefas WMI: gerenciamento de área de trabalho '
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 33f027c808a30463f2747d11020f45d1b8d40edf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827834"
---
# <a name="wmi-tasks-desktop-management"></a><span data-ttu-id="7105f-103">Tarefas WMI: gerenciamento de área de trabalho </span><span class="sxs-lookup"><span data-stu-id="7105f-103">WMI Tasks: Desktop Management</span></span>

<span data-ttu-id="7105f-104">As tarefas do WMI para gerenciamento de desktops podem exercer controle e obter dados de uma área de trabalho remota ou de um computador local.</span><span class="sxs-lookup"><span data-stu-id="7105f-104">WMI tasks for desktop management can exert control and obtain data from either a remote desktop or a local computer.</span></span> <span data-ttu-id="7105f-105">Por exemplo, você pode determinar se o protetor de tela em um computador local requer uma senha.</span><span class="sxs-lookup"><span data-stu-id="7105f-105">For example, you can determine whether the screensaver on a local computer requires a password.</span></span> <span data-ttu-id="7105f-106">O WMI também oferece a capacidade de desligar um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="7105f-106">WMI also gives you the ability shut down a remote computer.</span></span> <span data-ttu-id="7105f-107">Para obter outros exemplos, consulte o TechNet ScriptCenter em [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7105f-107">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="7105f-108">Os exemplos de script mostrados neste tópico obtêm dados somente do computador local.</span><span class="sxs-lookup"><span data-stu-id="7105f-108">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="7105f-109">Para obter mais informações sobre como usar o script para obter dados de computadores remotos, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="7105f-109">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="7105f-110">O procedimento a seguir descreve como executar um script.</span><span class="sxs-lookup"><span data-stu-id="7105f-110">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="7105f-111">**Para executar um script**</span><span class="sxs-lookup"><span data-stu-id="7105f-111">**To run a script**</span></span>

1.  <span data-ttu-id="7105f-112">Copie o código e salve-o em um arquivo com uma extensão. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="7105f-112">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="7105f-113">Verifique se o editor de texto não adiciona uma extensão. txt ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="7105f-113">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="7105f-114">Abra uma janela de prompt de comando e navegue até o diretório em que você salvou o arquivo.</span><span class="sxs-lookup"><span data-stu-id="7105f-114">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="7105f-115">Digite **cscript filename.vbs** no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="7105f-115">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="7105f-116">Se você não puder acessar um log de eventos, verifique se você está executando a partir de um prompt de comandos com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="7105f-116">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="7105f-117">Alguns logs de eventos, como o log de eventos de segurança, podem ser protegidos por UAC (controles de acesso do usuário).</span><span class="sxs-lookup"><span data-stu-id="7105f-117">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="7105f-118">Por padrão, o cscript exibe a saída de um script na janela de prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="7105f-118">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="7105f-119">Como os scripts WMI podem produzir grandes quantidades de saída, convém redirecionar a saída para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="7105f-119">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="7105f-120">Digite **cscript filename.vbs > outfile.txt** no prompt de comando para redirecionar a saída do script de *filename.vbs* para *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="7105f-120">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="7105f-121">A tabela a seguir lista os exemplos de script que podem ser usados para obter vários tipos de dados do computador local.</span><span class="sxs-lookup"><span data-stu-id="7105f-121">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7105f-122">Como fazer...</span><span class="sxs-lookup"><span data-stu-id="7105f-122">How do I...</span></span></th>
<th><span data-ttu-id="7105f-123">Classes ou métodos WMI</span><span class="sxs-lookup"><span data-stu-id="7105f-123">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7105f-124">... determinar se um computador remoto foi inicializado no modo de segurança com o estado de rede?</span><span class="sxs-lookup"><span data-stu-id="7105f-124">...determine if a remote computer has booted up in the Safe Mode with Networking state?</span></span></td>
<td><span data-ttu-id="7105f-125">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> e verifique o valor da propriedade <strong>PrimaryOwnerName</strong> .</span><span class="sxs-lookup"><span data-stu-id="7105f-125">Use the <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> class and check the value of the <strong>PrimaryOwnerName</strong> property.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7105f-126">VB</span><span class="sxs-lookup"><span data-stu-id="7105f-126">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colSettings = objWMIService.ExecQuery (&quot;Select * from Win32_ComputerSystem&quot;)
For Each objComputer in colSettings 
    Wscript.Echo &quot;System Name: &quot; & objComputer.Name
    Wscript.Echo &quot;Registered owner: &quot; & objComputer.PrimaryOwnerName
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
<th><span data-ttu-id="7105f-127">PowerShell</span><span class="sxs-lookup"><span data-stu-id="7105f-127">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSettings = Get-WmiObject -Class Win32_ComputerSystem
foreach ($objComputer in $colSettings)
{
    &quot;System Name: &quot; + $objComputer.Name
    &quot;Registered owner: &quot; + $objComputer.PrimaryOwnerName
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="7105f-128">... determinar se uma proteção de tela do computador requer uma senha?</span><span class="sxs-lookup"><span data-stu-id="7105f-128">...determine if a computer screensaver requires a password?</span></span></td>
<td><p><span data-ttu-id="7105f-129">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-desktop"><strong>Win32_Desktop</strong></a> e verifique o valor da propriedade <strong>ScreenSaverSecure</strong> .</span><span class="sxs-lookup"><span data-stu-id="7105f-129">Use the <a href="/windows/desktop/CIMWin32Prov/win32-desktop"><strong>Win32_Desktop</strong></a> class and check the value of the <strong>ScreenSaverSecure</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7105f-130">VB</span><span class="sxs-lookup"><span data-stu-id="7105f-130">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_Desktop&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Screen Saver Secure: &quot; & objItem.ScreenSaverSecure
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
<th><span data-ttu-id="7105f-131">PowerShell</span><span class="sxs-lookup"><span data-stu-id="7105f-131">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = &quot;.&quot;
$Desktops = Get-WMIObject -class Win32_Desktop -ComputerName $computer
&quot;{0} desktops found as follows&quot; -f $desktops.count
foreach ($desktop in $desktops) {
     &quot;Desktop      : {0}&quot;  -f $Desktop.Name
     &quot;Screen Saver : {0}&quot;  -f $desktop.ScreensaverExecutable
     &quot;Secure       : {0} &quot; -f $desktop.ScreenSaverSecure
     &quot;&quot;
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7105f-132">... verificar se uma tela de computador foi definida para 800 pixels por 600 pixels?</span><span class="sxs-lookup"><span data-stu-id="7105f-132">...verify that a computer screen has been set for 800 pixels by 600 pixels?</span></span></td>
<td><p><span data-ttu-id="7105f-133">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-desktopmonitor"><strong>Win32_DesktopMonitor</strong></a> e verifique os valores das propriedades <strong>ScreenHeight</strong> e <strong>ScreenWidth</strong>.</span><span class="sxs-lookup"><span data-stu-id="7105f-133">Use the <a href="/windows/desktop/CIMWin32Prov/win32-desktopmonitor"><strong>Win32_DesktopMonitor</strong></a> class and check the values of the properties <strong>ScreenHeight</strong> and <strong>ScreenWidth</strong>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7105f-134">VB</span><span class="sxs-lookup"><span data-stu-id="7105f-134">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(_
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_DesktopMonitor&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Screen Height: &quot; & objItem.ScreenHeight
    Wscript.Echo &quot;Screen Width: &quot; & objItem.ScreenWidth
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
<th><span data-ttu-id="7105f-135">PowerShell</span><span class="sxs-lookup"><span data-stu-id="7105f-135">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><# Get desktop information #>
$computer = &quot;.&quot;
$desktops = Get-WmiObject -Class Win32_DesktopMonitor
$hostname = hostname

<span data-ttu-id="7105f-136">< # exibir detalhes da área de trabalho # > &quot; há {0} áreas de trabalho no da {1} seguinte maneira: &quot; -f $desktops. Contagem, $hostname &quot; &quot; $i = 1 # contagem de áreas de trabalho neste sistema</span><span class="sxs-lookup"><span data-stu-id="7105f-136"><# Display desktop details #> &quot;There are {0} Desktops on {1} as follows:&quot; -f $desktops.Count, $hostname &quot;&quot; $i=1 # count of desktops on this system</span></span>

<span data-ttu-id="7105f-137">foreach ($desktop em $desktops) { &quot; Desktop {0} : {1} &quot; -f $i + +, $desktop. altura da tela de legenda &quot; : {0} &quot; -f $desktop. &quot;Largura da tela ScreenHeight: {0} &quot; -f $desktop. ScreenWidth &quot; &quot; }</code></span><span class="sxs-lookup"><span data-stu-id="7105f-137">foreach ($desktop in $desktops) { &quot;Desktop {0}: {1}&quot; -f  $i++, $Desktop.Caption &quot;Screen Height : {0}&quot; -f $desktop.ScreenHeight &quot;Screen Width  : {0}&quot; -f $desktop.ScreenWidth &quot;&quot; }</code></span></span></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7105f-138">... determinar quanto tempo um computador está em execução?</span><span class="sxs-lookup"><span data-stu-id="7105f-138">...determine how long a computer has been running?</span></span></td>
<td><p><span data-ttu-id="7105f-139">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> e a propriedade <strong>LastBootUpTime</strong> .</span><span class="sxs-lookup"><span data-stu-id="7105f-139">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class and the <strong>LastBootUpTime</strong> property.</span></span> <span data-ttu-id="7105f-140">Subtraia esse valor da hora atual para obter o tempo de atividade do sistema.</span><span class="sxs-lookup"><span data-stu-id="7105f-140">Subtract that value from the current time to get the system uptime.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7105f-141">VB</span><span class="sxs-lookup"><span data-stu-id="7105f-141">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
 
For Each objOS in colOperatingSystems
    dtmBootup = objOS.LastBootUpTime
    dtmLastBootUpTime = WMIDateStringToDate(dtmBootup)
    dtmSystemUptime = DateDiff(&quot;h&quot;, dtmLastBootUpTime, Now)
    Wscript.Echo dtmSystemUptime 
Next
 
Function WMIDateStringToDate(dtmBootup)
    WMIDateStringToDate =  CDate(Mid(dtmBootup, 5, 2) & &quot;/&quot; & _
        Mid(dtmBootup, 7, 2) & &quot;/&quot; & Left(dtmBootup, 4) & &quot; &quot; & Mid (dtmBootup, 9, 2) & &quot;:&quot; & _
        Mid(dtmBootup, 11, 2) & &quot;:&quot; & Mid(dtmBootup, 13, 2))
End Function</code></pre></td>
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
<th><span data-ttu-id="7105f-142">PowerShell</span><span class="sxs-lookup"><span data-stu-id="7105f-142">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>function WMIDateStringToDate($Bootup) {
[System.Management.ManagementDateTimeconverter]::ToDateTime($Bootup)
}

<# Main script #>
$Computer = &quot;.&quot; # adjust as needed
$computers = Get-WMIObject -class Win32_OperatingSystem -computer $computer

foreach ($system in $computers) {
    $Bootup = $system.LastBootUpTime
    $LastBootUpTime = WMIDateStringToDate($Bootup)
    $now = Get-Date
 $Uptime = $now-$lastBootUpTime
    &quot;System Up for: {0}&quot; -f $UpTime
} </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7105f-143">... reinicializar ou desligar um computador remoto?</span><span class="sxs-lookup"><span data-stu-id="7105f-143">...reboot or shut down a remote computer?</span></span></td>
<td><p><span data-ttu-id="7105f-144">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> e o método <a href="/windows/desktop/CIMWin32Prov/win32shutdown-method-in-class-win32-operatingsystem"><strong>Win32Shutdown</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7105f-144">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/win32shutdown-method-in-class-win32-operatingsystem"><strong>Win32Shutdown</strong></a> method.</span></span> <span data-ttu-id="7105f-145">Você deve incluir o privilégio <a href="privilege-constants.md">RemoteShutdown</a> ao se conectar ao WMI.</span><span class="sxs-lookup"><span data-stu-id="7105f-145">You must include the <a href="privilege-constants.md">RemoteShutdown</a> privilege when connecting to WMI.</span></span> <span data-ttu-id="7105f-146">Para obter mais informações, consulte <a href="executing-privileged-operations-using-vbscript.md">executando operações privilegiadas usando o VBScript</a>.</span><span class="sxs-lookup"><span data-stu-id="7105f-146">For more information, see <a href="executing-privileged-operations-using-vbscript.md">Executing Privileged Operations Using VBScript</a>.</span></span> <span data-ttu-id="7105f-147">Ao contrário do método <a href="/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem"><strong>Shutdown</strong></a> em <strong>Win32_OperatingSystem</strong>, o método <strong>Win32Shutdown</strong> permite definir sinalizadores para controlar o comportamento de desligamento.</span><span class="sxs-lookup"><span data-stu-id="7105f-147">Unlike the <a href="/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem"><strong>Shutdown</strong></a> method on <strong>Win32_OperatingSystem</strong>, the <strong>Win32Shutdown</strong> method allows you to set flags to control the shutdown behavior.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7105f-148">VB</span><span class="sxs-lookup"><span data-stu-id="7105f-148">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate,(Shutdown)}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    ObjOperatingSystem.Shutdown(1)
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
<th><span data-ttu-id="7105f-149">PowerShell</span><span class="sxs-lookup"><span data-stu-id="7105f-149">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
$colOperatingSystem = Get-WmiObject -Class Win32_OperatingSystem -ComputerName $strComputer -Namespace &quot;wmi\cimv2&quot;
foreach ($objOperatingSystem in $colOperatingSystem)
{
    [void]$objOperatingSystem.Shutdown()
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7105f-150">... determinar quais aplicativos são executados automaticamente toda vez que eu iniciar o Windows?</span><span class="sxs-lookup"><span data-stu-id="7105f-150">...determine what applications automatically run each time I start Windows?</span></span></td>
<td><p><span data-ttu-id="7105f-151">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-startupcommand"><strong>Win32_StartupCommand</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7105f-151">Use the <a href="/windows/desktop/CIMWin32Prov/win32-startupcommand"><strong>Win32_StartupCommand</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7105f-152">VB</span><span class="sxs-lookup"><span data-stu-id="7105f-152">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colStartupCommands = objWMIService.ExecQuery _
    (&quot;Select * from Win32_StartupCommand&quot;)
For Each objStartupCommand in colStartupCommands
    Wscript.Echo &quot;Command: &quot; & objStartupCommand.Command & VBNewLine _
    & &quot;Description: &quot; & objStartupCommand.Description & VBNewLine _
    & &quot;Location: &quot; & objStartupCommand.Location & VBNewLine _
    & &quot;Name: &quot; & objStartupCommand.Name & VBNewLine _
    & &quot;SettingID: &quot; & objStartupCommand.SettingID & VBNewLine _
    & &quot;User: &quot; & objStartupCommand.User
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
<th><span data-ttu-id="7105f-153">PowerShell</span><span class="sxs-lookup"><span data-stu-id="7105f-153">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colItems = Get-WmiObject -Class Win32_StartupCommand -ComputerName $strComputer
foreach ($objStartupCommand in $colItems) 
{ 
    &quot;Command: &quot; + $objStartupCommand.Command
    &quot;Description: &quot; + $objStartupCommand.Description 
    &quot;Location: &quot; + $objStartupCommand.Location 
    &quot;Name: &quot; + $objStartupCommand.Name 
    &quot;SettingID: &quot; + $objStartupCommand.SettingID 
    &quot;User: &quot; + $objStartupCommand.User
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="7105f-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7105f-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7105f-155">Tarefas do WMI para scripts e aplicativos</span><span class="sxs-lookup"><span data-stu-id="7105f-155">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="7105f-156">Exemplos de aplicativos WMI C++</span><span class="sxs-lookup"><span data-stu-id="7105f-156">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="7105f-157">ScriptCenter do TechNet</span><span class="sxs-lookup"><span data-stu-id="7105f-157">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

