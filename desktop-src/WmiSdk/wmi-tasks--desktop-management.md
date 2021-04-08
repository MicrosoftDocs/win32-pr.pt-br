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
# <a name="wmi-tasks-desktop-management"></a>Tarefas WMI: gerenciamento de área de trabalho 

As tarefas do WMI para gerenciamento de desktops podem exercer controle e obter dados de uma área de trabalho remota ou de um computador local. Por exemplo, você pode determinar se o protetor de tela em um computador local requer uma senha. O WMI também oferece a capacidade de desligar um computador remoto. Para obter outros exemplos, consulte o TechNet ScriptCenter em [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

Os exemplos de script mostrados neste tópico obtêm dados somente do computador local. Para obter mais informações sobre como usar o script para obter dados de computadores remotos, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).


O procedimento a seguir descreve como executar um script.

**Para executar um script**

1.  Copie o código e salve-o em um arquivo com uma extensão. vbs, como *filename.vbs*. Verifique se o editor de texto não adiciona uma extensão. txt ao arquivo.
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
<td>... determinar se um computador remoto foi inicializado no modo de segurança com o estado de rede?</td>
<td>Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> e verifique o valor da propriedade <strong>PrimaryOwnerName</strong> .<br/> <span data-codelanguage="VisualBasic"></span>
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
<th>PowerShell</th>
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
<td>... determinar se uma proteção de tela do computador requer uma senha?</td>
<td><p>Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-desktop"><strong>Win32_Desktop</strong></a> e verifique o valor da propriedade <strong>ScreenSaverSecure</strong> .</p>
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
<th>PowerShell</th>
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
<td>... verificar se uma tela de computador foi definida para 800 pixels por 600 pixels?</td>
<td><p>Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-desktopmonitor"><strong>Win32_DesktopMonitor</strong></a> e verifique os valores das propriedades <strong>ScreenHeight</strong> e <strong>ScreenWidth</strong>.</p>
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
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><# Get desktop information #>
$computer = &quot;.&quot;
$desktops = Get-WmiObject -Class Win32_DesktopMonitor
$hostname = hostname

< # exibir detalhes da área de trabalho # > &quot; há {0} áreas de trabalho no da {1} seguinte maneira: &quot; -f $desktops. Contagem, $hostname &quot; &quot; $i = 1 # contagem de áreas de trabalho neste sistema

foreach ($desktop em $desktops) { &quot; Desktop {0} : {1} &quot; -f $i + +, $desktop. altura da tela de legenda &quot; : {0} &quot; -f $desktop. &quot;Largura da tela ScreenHeight: {0} &quot; -f $desktop. ScreenWidth &quot; &quot; }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>... determinar quanto tempo um computador está em execução?</td>
<td><p>Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> e a propriedade <strong>LastBootUpTime</strong> . Subtraia esse valor da hora atual para obter o tempo de atividade do sistema.</p>
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
<th>PowerShell</th>
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
<td>... reinicializar ou desligar um computador remoto?</td>
<td><p>Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> e o método <a href="/windows/desktop/CIMWin32Prov/win32shutdown-method-in-class-win32-operatingsystem"><strong>Win32Shutdown</strong></a> . Você deve incluir o privilégio <a href="privilege-constants.md">RemoteShutdown</a> ao se conectar ao WMI. Para obter mais informações, consulte <a href="executing-privileged-operations-using-vbscript.md">executando operações privilegiadas usando o VBScript</a>. Ao contrário do método <a href="/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem"><strong>Shutdown</strong></a> em <strong>Win32_OperatingSystem</strong>, o método <strong>Win32Shutdown</strong> permite definir sinalizadores para controlar o comportamento de desligamento.</p>
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
<th>PowerShell</th>
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
<td>... determinar quais aplicativos são executados automaticamente toda vez que eu iniciar o Windows?</td>
<td><p>Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-startupcommand"><strong>Win32_StartupCommand</strong></a> .</p>
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
<th>PowerShell</th>
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



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas do WMI para scripts e aplicativos](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Exemplos de aplicativos WMI C++](wmi-c---application-examples.md)
</dt> <dt>

[ScriptCenter do TechNet](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

