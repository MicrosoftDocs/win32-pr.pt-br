---
description: As tarefas administrativas de conta e domínio obtêm informações como o domínio do computador ou o usuário conectado no momento.
ms.assetid: 1a9cc44b-c366-465d-a0d0-536d5dc818b5
ms.tgt_platform: multiple
title: 'Tarefas do WMI: contas e domínios'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3bcda33677ada6c4a08e2d9bdc1676c9662a5cd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171650"
---
# <a name="wmi-tasks-accounts-and-domains"></a><span data-ttu-id="2bd7b-103">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="2bd7b-103">WMI Tasks: Accounts and Domains</span></span>

<span data-ttu-id="2bd7b-104">As tarefas administrativas de conta e domínio obtêm informações como o domínio do computador ou o usuário conectado no momento.</span><span class="sxs-lookup"><span data-stu-id="2bd7b-104">Account and domain administrative tasks obtain information such as the computer domain or the currently logged-on user.</span></span> <span data-ttu-id="2bd7b-105">Muitas dessas tarefas são mais bem executadas com scripts [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) .</span><span class="sxs-lookup"><span data-stu-id="2bd7b-105">Many of these tasks are best performed with [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) scripts.</span></span> <span data-ttu-id="2bd7b-106">Para obter mais informações e outros exemplos, consulte o repositório de scripts do TechNet [ScriptCenter](https://www.microsoft.com/technet/scriptcenter) .</span><span class="sxs-lookup"><span data-stu-id="2bd7b-106">For more information and other examples, see the TechNet [ScriptCenter](https://www.microsoft.com/technet/scriptcenter) Script Repository.</span></span>

<span data-ttu-id="2bd7b-107">Os exemplos de script mostrados neste tópico obtêm dados somente do computador local.</span><span class="sxs-lookup"><span data-stu-id="2bd7b-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="2bd7b-108">Para obter mais informações sobre como usar o script para obter dados de computadores remotos, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="2bd7b-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="2bd7b-109">O procedimento a seguir descreve como executar um script.</span><span class="sxs-lookup"><span data-stu-id="2bd7b-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="2bd7b-110">**Para executar um script**</span><span class="sxs-lookup"><span data-stu-id="2bd7b-110">**To run a script**</span></span>

1.  <span data-ttu-id="2bd7b-111">Copie o código e salve-o em um arquivo com uma extensão. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="2bd7b-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="2bd7b-112">Verifique se o editor de texto não adiciona uma extensão. txt ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="2bd7b-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="2bd7b-113">Abra uma janela de prompt de comando e navegue até o diretório em que você salvou o arquivo.</span><span class="sxs-lookup"><span data-stu-id="2bd7b-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="2bd7b-114">Digite **cscript filename.vbs** no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="2bd7b-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="2bd7b-115">Se você não puder acessar um log de eventos, verifique se você está executando a partir de um prompt de comandos com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="2bd7b-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="2bd7b-116">Alguns logs de eventos, como o log de eventos de segurança, podem ser protegidos por UAC (controles de acesso do usuário).</span><span class="sxs-lookup"><span data-stu-id="2bd7b-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="2bd7b-117">Por padrão, o cscript exibe a saída de um script na janela de prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="2bd7b-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="2bd7b-118">Como os scripts WMI podem produzir grandes quantidades de saída, convém redirecionar a saída para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="2bd7b-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="2bd7b-119">Digite **cscript filename.vbs > outfile.txt** no prompt de comando para redirecionar a saída do script de *filename.vbs* para *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="2bd7b-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="2bd7b-120">A tabela a seguir lista os exemplos de script que podem ser usados para obter vários tipos de dados do computador local.</span><span class="sxs-lookup"><span data-stu-id="2bd7b-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bd7b-121">Como fazer...</span><span class="sxs-lookup"><span data-stu-id="2bd7b-121">How do I...</span></span></th>
<th><span data-ttu-id="2bd7b-122">Classes ou métodos WMI</span><span class="sxs-lookup"><span data-stu-id="2bd7b-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2bd7b-123">... determinar o domínio ao qual um computador pertence?</span><span class="sxs-lookup"><span data-stu-id="2bd7b-123">...determine the domain in which a computer belongs?</span></span></td>
<td><span data-ttu-id="2bd7b-124">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> e verifique o valor da propriedade <strong>Domain</strong> .</span><span class="sxs-lookup"><span data-stu-id="2bd7b-124">Use the <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> class and check the value of the <strong>Domain</strong> property.</span></span> <span data-ttu-id="2bd7b-125">Você também pode usar a propriedade <strong>DNSDomain</strong> em <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2bd7b-125">You can also use the <strong>DNSDomain</strong> property in <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a>.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bd7b-126">VB</span><span class="sxs-lookup"><span data-stu-id="2bd7b-126">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colSettings = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)

For Each objComputer in colSettings 
    Wscript.Echo &quot;System Name: &quot; & objComputer.Name
    Wscript.Echo &quot;Domain: &quot; & objComputer.Domain
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
<th><span data-ttu-id="2bd7b-127">PowerShell</span><span class="sxs-lookup"><span data-stu-id="2bd7b-127">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$computer = Get-WmiObject -Class Win32_ComputerSystem
&quot;System Name: {0}&quot; -f $computer.name
&quot;Domain : {0}&quot; -f $computer.domain</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bd7b-128">C#</span><span class="sxs-lookup"><span data-stu-id="2bd7b-128">C#</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>using Microsoft.Management.Infrastructure;
...
CimSession session = CimSession.Create(&quot;localHost&quot;);
IEnumerable<CimInstance> queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

foreach (CimInstance cimObj in queryInstance)
{
   Console.WriteLine(cimObj.CimInstanceProperties[&quot;Name&quot;].ToString());
   Console.WriteLine(cimObj.CimInstanceProperties[&quot;Domain&quot;].ToString());
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bd7b-129">... determinar se um computador é um servidor ou uma estação de trabalho?</span><span class="sxs-lookup"><span data-stu-id="2bd7b-129">...determine whether a computer is a server or a workstation?</span></span></td>
<td><p><span data-ttu-id="2bd7b-130">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> e a propriedade <strong>DomainRole</strong> .</span><span class="sxs-lookup"><span data-stu-id="2bd7b-130">Use the <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> class and the <strong>DomainRole</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bd7b-131">VB</span><span class="sxs-lookup"><span data-stu-id="2bd7b-131">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colComputers = objWMIService.ExecQuery(&quot;Select DomainRole from Win32_ComputerSystem&quot;)
For Each objComputer in colComputers
    Select Case objComputer.DomainRole 
        Case 0 
            strComputerRole = &quot;Standalone Workstation&quot;
        Case 1        
            strComputerRole = &quot;Member Workstation&quot;
        Case 2
            strComputerRole = &quot;Standalone Server&quot;
        Case 3
            strComputerRole = &quot;Member Server&quot;
        Case 4
            strComputerRole = &quot;Backup Domain Controller&quot;
        Case 5
            strComputerRole = &quot;Primary Domain Controller&quot;
    End Select
    Wscript.Echo strComputerRole
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
<th><span data-ttu-id="2bd7b-132">PowerShell</span><span class="sxs-lookup"><span data-stu-id="2bd7b-132">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = Get-WmiObject -Class Win32_ComputerSystem 

&quot;Computer `&quot;{0}.{1}`&quot; is a: &quot;-f $Computer.Name,$computer.domain

switch  ($computer.DomainRole) {
    0 {&quot;Standalone Workstation&quot;}
    1 {&quot;Member Workstation&quot;}
    2 {&quot;Standalone Server&quot;}
    3 {&quot;Member Server&quot;}
    4 {&quot;Backup Domain Controller&quot;}
    5 {&quot;Primary Domain Controller&quot;}
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bd7b-133">... determinar o nome do computador?</span><span class="sxs-lookup"><span data-stu-id="2bd7b-133">...determine the computer name?</span></span></td>
<td><p><span data-ttu-id="2bd7b-134">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> e a propriedade <strong>Name</strong> .</span><span class="sxs-lookup"><span data-stu-id="2bd7b-134">Use the <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> class and the <strong>Name</strong> property.</span></span> <span data-ttu-id="2bd7b-135">Você também pode usar a propriedade <strong>dNSHostName</strong> em <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2bd7b-135">You can also use the <strong>DNSHostName</strong> property in <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bd7b-136">VB</span><span class="sxs-lookup"><span data-stu-id="2bd7b-136">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Computer Name: &quot; & objItem.Name
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
<th><span data-ttu-id="2bd7b-137">PowerShell</span><span class="sxs-lookup"><span data-stu-id="2bd7b-137">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = Get-WmiObject -Class Win32_ComputerSystem
&quot;Computer Name is: {0}&quot; -f $Computer.Name</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bd7b-138">C#</span><span class="sxs-lookup"><span data-stu-id="2bd7b-138">C#</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>using Microsoft.Management.Infrastructure;
...
CimSession session = CimSession.Create(&quot;localHost&quot;);
IEnumerable<CimInstance> queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

foreach (CimInstance cimObj in queryInstance)
{
   Console.WriteLine(cimObj.CimInstanceProperties[&quot;Name&quot;].ToString());
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bd7b-139">... localizar o nome da pessoa conectada no momento a um computador?</span><span class="sxs-lookup"><span data-stu-id="2bd7b-139">...find the name of the person currently logged on to a computer?</span></span></td>
<td><p><span data-ttu-id="2bd7b-140">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> e a propriedade <strong>username</strong> .</span><span class="sxs-lookup"><span data-stu-id="2bd7b-140">Use the <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> class and the <strong>UserName</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bd7b-141">VB</span><span class="sxs-lookup"><span data-stu-id="2bd7b-141">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
Set colComputer = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)
 
For Each objComputer in colComputer
    Wscript.Echo &quot;User Name = &quot; & objComputer.UserName & VBNewLine & &quot;Computer Name = &quot; & objComputer.Name
WScript.Echo objComputer.UserName
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
<th><span data-ttu-id="2bd7b-142">PowerShell</span><span class="sxs-lookup"><span data-stu-id="2bd7b-142">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$computers = Get-WmiObject -Class Win32_ComputerSystem 
&quot;Logged on user(s):&quot;
foreach($computer in $computers) {
   &quot;User: {0}&quot; -f $computer.UserName
}</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bd7b-143">C#</span><span class="sxs-lookup"><span data-stu-id="2bd7b-143">C#</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>using Microsoft.Management.Infrastructure;
...
CimSession session = CimSession.Create(&quot;localHost&quot;);
IEnumerable<CimInstance> queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

foreach (CimInstance cimObj in queryInstance)
{
   Console.WriteLine(&quot;User Name: &quot; + cimObj.CimInstanceProperties[&quot;UserName&quot;].ToString());
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bd7b-144">... Renomear um computador?</span><span class="sxs-lookup"><span data-stu-id="2bd7b-144">...rename a computer?</span></span></td>
<td><p><span data-ttu-id="2bd7b-145">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> e o método <strong>Rename</strong> .</span><span class="sxs-lookup"><span data-stu-id="2bd7b-145">Use the <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> class, and the <strong>Rename</strong> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bd7b-146">VB</span><span class="sxs-lookup"><span data-stu-id="2bd7b-146">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colComputers = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)
For Each objComputer in colComputers
    errReturn = ObjComputer.Rename(&quot;NewName&quot;)
    WScript.Echo &quot;Computer name is now &quot; & objComputer.Name
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
<th><span data-ttu-id="2bd7b-147">PowerShell</span><span class="sxs-lookup"><span data-stu-id="2bd7b-147">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>param (
[$String] $NewName = &#39;NewName&#39;,
[$string] $Comp = &quot;.&quot;
}

<# Get computer object #>
$Computer = Get-WmiObject -Class Win32_ComputerSystem -ComputerName $comp

<# Rename the Computer #>
$Return  = $Computer.Rename($NewName)

if ($return.ReturnValue -eq 0) {
   &quot;Computer name is now: $NewName&quot;
   &quot; but you need to reboot first&quot;
} else {
&quot;  RenameFailed, return code: {0}&quot; -f $return.ReturnValue
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bd7b-148">... recuperar somente grupos locais usando o WMI?</span><span class="sxs-lookup"><span data-stu-id="2bd7b-148">...retrieve only local groups using WMI?</span></span></td>
<td><p><span data-ttu-id="2bd7b-149">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-group"><strong>Win32_Group</strong></a> e inclua a seguinte cláusula <strong>Where</strong> em sua consulta <a href="querying-with-wql.md">WQL</a> .</span><span class="sxs-lookup"><span data-stu-id="2bd7b-149">Use the <a href="/windows/desktop/CIMWin32Prov/win32-group"><strong>Win32_Group</strong></a> class and include the following <strong>WHERE</strong> clause in your <a href="querying-with-wql.md">WQL</a> query.</span></span></p>
<p><code>Where LocalAccount = True</code></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bd7b-150">VB</span><span class="sxs-lookup"><span data-stu-id="2bd7b-150">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery _
    (&quot;Select * from Win32_Group  Where LocalAccount = True&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Local Account: &quot; & objItem.LocalAccount & VBNewLine _
        & &quot;Name: &quot; & objItem.Name & VBNewLine _
        & &quot;SID: &quot; & objItem.SID & VBNewLine _
        & &quot;SID Type: &quot; & objItem.SIDType & VBNewLine _
        & &quot;Status: &quot; & objItem.Status & VBNewLine
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
<th><span data-ttu-id="2bd7b-151">PowerShell</span><span class="sxs-lookup"><span data-stu-id="2bd7b-151">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Accts=Get-WMIObjectWin32_Group|where {$_.LocalAccount}
$accts |ftName, Sid, SidType, Status-autosize</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="2bd7b-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2bd7b-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bd7b-153">Tarefas do WMI para scripts e aplicativos</span><span class="sxs-lookup"><span data-stu-id="2bd7b-153">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="2bd7b-154">Exemplos de aplicativos WMI C++</span><span class="sxs-lookup"><span data-stu-id="2bd7b-154">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="2bd7b-155">ScriptCenter do TechNet</span><span class="sxs-lookup"><span data-stu-id="2bd7b-155">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>
