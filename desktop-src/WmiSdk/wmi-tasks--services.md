---
description: As tarefas do WMI para serviços obtêm informações sobre serviços, incluindo serviços dependentes ou antecedentes. Para obter outros exemplos, consulte o TechNet ScriptCenter em https://www.microsoft.com/technet .
ms.assetid: 1cd92981-c074-4ff7-a32c-ce492e6d6aa5
ms.tgt_platform: multiple
title: 'Tarefas do WMI: serviços'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b786ce0e358a59922728be4e90bc8cdeaa37a298
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762816"
---
# <a name="wmi-tasks-services"></a><span data-ttu-id="bae80-104">Tarefas do WMI: serviços</span><span class="sxs-lookup"><span data-stu-id="bae80-104">WMI Tasks: Services</span></span>

<span data-ttu-id="bae80-105">As tarefas do WMI para serviços obtêm informações sobre serviços, incluindo serviços dependentes ou antecedentes.</span><span class="sxs-lookup"><span data-stu-id="bae80-105">WMI tasks for services obtain information about services, including dependent or antecedent services.</span></span> <span data-ttu-id="bae80-106">Para obter outros exemplos, consulte o TechNet ScriptCenter em [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="bae80-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="bae80-107">Os exemplos de script mostrados neste tópico obtêm dados somente do computador local.</span><span class="sxs-lookup"><span data-stu-id="bae80-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="bae80-108">Para obter mais informações sobre como usar o script para obter dados de computadores remotos, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="bae80-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="bae80-109">O procedimento a seguir descreve como executar um script.</span><span class="sxs-lookup"><span data-stu-id="bae80-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="bae80-110">**Para executar um script**</span><span class="sxs-lookup"><span data-stu-id="bae80-110">**To run a script**</span></span>

1.  <span data-ttu-id="bae80-111">Copie o código e salve-o em um arquivo com uma extensão. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="bae80-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="bae80-112">Verifique se o editor de texto não adiciona uma extensão. txt ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="bae80-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="bae80-113">Abra uma janela de prompt de comando e navegue até o diretório em que você salvou o arquivo.</span><span class="sxs-lookup"><span data-stu-id="bae80-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="bae80-114">Digite **cscript filename.vbs** no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="bae80-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="bae80-115">Se você não puder acessar um log de eventos, verifique se você está executando a partir de um prompt de comandos com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="bae80-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="bae80-116">Alguns logs de eventos, como o log de eventos de segurança, podem ser protegidos por UAC (controles de acesso do usuário).</span><span class="sxs-lookup"><span data-stu-id="bae80-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="bae80-117">Por padrão, o cscript exibe a saída de um script na janela de prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="bae80-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="bae80-118">Como os scripts WMI podem produzir grandes quantidades de saída, convém redirecionar a saída para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="bae80-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="bae80-119">Digite **cscript filename.vbs > outfile.txt** no prompt de comando para redirecionar a saída do script de *filename.vbs* para *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="bae80-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="bae80-120">A tabela a seguir lista os exemplos de script que podem ser usados para obter vários tipos de dados do computador local.</span><span class="sxs-lookup"><span data-stu-id="bae80-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>




<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bae80-121">Como fazer...</span><span class="sxs-lookup"><span data-stu-id="bae80-121">How do I...</span></span></th>
<th><span data-ttu-id="bae80-122">Classes ou métodos WMI</span><span class="sxs-lookup"><span data-stu-id="bae80-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bae80-123">... determinar quais serviços estão em execução e quais não estão?</span><span class="sxs-lookup"><span data-stu-id="bae80-123">...determine which services are running and which ones are not?</span></span></td>
<td><span data-ttu-id="bae80-124">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> para verificar o estado de todos os serviços.</span><span class="sxs-lookup"><span data-stu-id="bae80-124">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class to check the state of all of the services.</span></span> <span data-ttu-id="bae80-125">A propriedade State permite que você saiba se um serviço está parado ou em execução.</span><span class="sxs-lookup"><span data-stu-id="bae80-125">The state property lets you know if a service is stopped or running.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bae80-126">VB</span><span class="sxs-lookup"><span data-stu-id="bae80-126">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot; 
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\CIMV2&quot;) 
Set colItems = objWMIService.ExecQuery(&quot;SELECT * FROM Win32_Service&quot;,,48) 
For Each objItem in colItems 
    Wscript.Echo &quot;Service Name: &quot; & objItem.Name & VBNewLine & &quot;State: &quot; & objItem.State
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
<th><span data-ttu-id="bae80-127">PowerShell</span><span class="sxs-lookup"><span data-stu-id="bae80-127">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class win32_service -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | format-list Name, State</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="bae80-128">... impedir que usuários avançados iniciem determinados serviços?</span><span class="sxs-lookup"><span data-stu-id="bae80-128">...stop Power Users from starting certain services?</span></span></td>
<td><p><span data-ttu-id="bae80-129">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> e o método <a href="/windows/desktop/CIMWin32Prov/changestartmode-method-in-class-win32-service"><strong>ChangeStartMode</strong></a> para definir a propriedade <strong>startMode</strong> como desabilitada.</span><span class="sxs-lookup"><span data-stu-id="bae80-129">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/changestartmode-method-in-class-win32-service"><strong>ChangeStartMode</strong></a> method to set the <strong>StartMode</strong> property to Disabled.</span></span> <span data-ttu-id="bae80-130">Os serviços desabilitados não podem ser iniciados e, por padrão, os usuários avançados não podem alterar o modo de início de um serviço.</span><span class="sxs-lookup"><span data-stu-id="bae80-130">Disabled services cannot be started, and, by default, Power Users cannot change the start mode of a service.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bae80-131">VB</span><span class="sxs-lookup"><span data-stu-id="bae80-131">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colServiceList = objWMIService.ExecQuery (&quot;Select * from Win32_Service where StartMode = &#39;Manual&#39;&quot;)
For Each objService in colServiceList
    errReturnCode = objService.Change( , , , , &quot;Disabled&quot;)
    WScript.Echo &quot;Changed manual service to disabled: &quot; & objService.Name   
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
<th><span data-ttu-id="bae80-132">PowerShell</span><span class="sxs-lookup"><span data-stu-id="bae80-132">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class win32_service -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | where {$_.startMode -eq &quot;Manual&quot;} | `
    foreach-object { [void]$_.changeStartMode(&#39;Disabled&#39;) }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bae80-133">... Iniciar e parar os serviços?</span><span class="sxs-lookup"><span data-stu-id="bae80-133">...start and stop services?</span></span></td>
<td><p><span data-ttu-id="bae80-134">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> e os métodos <a href="/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service"><strong>StopService</strong></a> e <a href="/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service"><strong>StartService</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="bae80-134">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service"><strong>StopService</strong></a> and <a href="/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service"><strong>StartService</strong></a> methods.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bae80-135">VB</span><span class="sxs-lookup"><span data-stu-id="bae80-135">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colListOfServices = objWMIService.ExecQuery (&quot;Select * from Win32_Service Where Name =&#39;Alerter&#39;&quot;)
For Each objService in colListOfServices
    objService.StartService()
    Wscript.Echo &quot;Started Alerter service&quot;
Next
</code></pre></td>
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
<th><span data-ttu-id="bae80-136">PowerShell</span><span class="sxs-lookup"><span data-stu-id="bae80-136">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class win32_service -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | where {$_.Name -eq &quot;Alerter&quot;} | `
    foreach-object { [void]$_.StartService() }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bae80-137">... alterar as senhas de conta de serviço usando um script?</span><span class="sxs-lookup"><span data-stu-id="bae80-137">...change service account passwords using a script?</span></span></td>
<td><p><span data-ttu-id="bae80-138">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> e o método <a href="/windows/desktop/CIMWin32Prov/change-method-in-class-win32-service"><strong>Change</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="bae80-138">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/change-method-in-class-win32-service"><strong>Change</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bae80-139">VB</span><span class="sxs-lookup"><span data-stu-id="bae80-139">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colServiceList = objWMIService.ExecQuery (&quot;Select * from Win32_Service&quot;)
For Each objservice in colServiceList
    If objService.StartName = &quot;.\netsvc&quot; Then
        errReturn = objService.Change( , , , , , , , &quot;password&quot;)  
    End If 
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bae80-140">.. determinar quais serviços eu posso parar?</span><span class="sxs-lookup"><span data-stu-id="bae80-140">..determine which services I can stop?</span></span></td>
<td><p><span data-ttu-id="bae80-141">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> e verifique o valor da propriedade <strong>AcceptStop</strong> .</span><span class="sxs-lookup"><span data-stu-id="bae80-141">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class, and check the value of the <strong>AcceptStop</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bae80-142">VB</span><span class="sxs-lookup"><span data-stu-id="bae80-142">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colServices = objWMIService.ExecQuery (&quot;Select * from Win32_Service Where AcceptStop = True&quot;)
For Each objService in colServices
    Wscript.Echo objService.DisplayName 
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
<th><span data-ttu-id="bae80-143">PowerShell</span><span class="sxs-lookup"><span data-stu-id="bae80-143">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class win32_service -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | where {$_.AcceptStop -eq &quot;True&quot;} | `
     format-list DisplayName</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bae80-144">... localizar os serviços que devem estar em execução antes que eu possa iniciar o serviço DHCP?</span><span class="sxs-lookup"><span data-stu-id="bae80-144">...find the services that must be running before I can start the DHCP service?</span></span></td>
<td><p><span data-ttu-id="bae80-145">Consulte os <a href="associators-of-statement.md">ASSOCIADORES da</a> classe <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> denominada &quot; DHCP &quot; que estão na classe <a href="/windows/desktop/CIMWin32Prov/win32-dependentservice"><strong>Win32_DependentService</strong></a> e que &quot; dependem da &quot; propriedade <strong>role</strong> .</span><span class="sxs-lookup"><span data-stu-id="bae80-145">Query for <a href="associators-of-statement.md">ASSOCIATORS OF</a> the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class named &quot;DHCP&quot; that are in the <a href="/windows/desktop/CIMWin32Prov/win32-dependentservice"><strong>Win32_DependentService</strong></a> class and have &quot;Dependent&quot; in the <strong>Role</strong> property.</span></span> <span data-ttu-id="bae80-146"><strong>Função</strong> significa a função do serviço DHCP: nesse caso, ele depende dos outros serviços que estão sendo iniciados.</span><span class="sxs-lookup"><span data-stu-id="bae80-146"><strong>Role</strong> means the role of the DHCP service: in this case, it is dependent on the other services that are being started.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bae80-147">VB</span><span class="sxs-lookup"><span data-stu-id="bae80-147">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colServiceList = objWMIService.ExecQuery(&quot;Associators Of &quot; _ 
    & &quot;{Win32_Service.Name=&#39;dhcp&#39;} Where &quot; _
    & &quot;AssocClass=Win32_DependentService &quot; _
    & &quot;Role=Dependent&quot;) 
For Each objService in colServiceList
Wscript.Echo objService.DisplayName 
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
<th><span data-ttu-id="bae80-148">PowerShell</span><span class="sxs-lookup"><span data-stu-id="bae80-148">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$query = &quot;Associators Of {Win32_Service.Name=&#39;dhcp&#39;} Where AssocClass=Win32_DependentService Role=Dependent&quot;
Get-WmiObject -Query $query -Namespace &quot;root\cimv2&quot; | format-list DisplayName</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bae80-149">... localizar os serviços que exigem que o serviço de serviço WMI (Winmgmt) esteja em execução antes que eles possam ser iniciados?</span><span class="sxs-lookup"><span data-stu-id="bae80-149">...find the services that require the WMI service (Winmgmt) service to be running before they can start?</span></span></td>
<td><p><span data-ttu-id="bae80-150">Consulte os <a href="associators-of-statement.md">ASSOCIADORES da</a> classe <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> denominada &quot; DHCP &quot; que estão na classe <a href="/windows/desktop/CIMWin32Prov/win32-dependentservice"><strong>Win32_DependentService</strong></a> e têm &quot; Antecendent &quot; na propriedade <strong>role</strong> .</span><span class="sxs-lookup"><span data-stu-id="bae80-150">Query for <a href="associators-of-statement.md">ASSOCIATORS OF</a> the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class named &quot;DHCP&quot; that are in the <a href="/windows/desktop/CIMWin32Prov/win32-dependentservice"><strong>Win32_DependentService</strong></a> class and have &quot;Antecendent&quot; in the <strong>Role</strong> property.</span></span> <span data-ttu-id="bae80-151"><strong>Função</strong> significa a função do serviço RASMAN: nesse caso, o antecessor deve ser iniciado antes dos serviços dependentes.</span><span class="sxs-lookup"><span data-stu-id="bae80-151"><strong>Role</strong> means the role of the rasman service: in this case, it is antecedent to must be started before the dependent services.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bae80-152">VB</span><span class="sxs-lookup"><span data-stu-id="bae80-152">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\ & strComputer & &quot;\root\cimv2&quot;)
Set colServiceList = _
    objWMIService.ExecQuery(&quot;Associators of &quot; _
    & &quot;{Win32_Service.Name=&#39;winmgmt&#39;} Where &quot; _
    & &quot;AssocClass=Win32_DependentService &quot; _
    & &quot;Role=Antecedent&quot; )
For Each objService in colServiceList
Wscript.Echo &quot;Name: &quot; & objService.Name & VBTab & &quot;Display Name: &quot; & objService.DisplayName 
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
<th><span data-ttu-id="bae80-153">PowerShell</span><span class="sxs-lookup"><span data-stu-id="bae80-153">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$query = &quot;Associators of {Win32_Service.Name=&#39;winmgmt&#39;} Where AssocClass=Win32_DependentService Role=Antecedent&quot;
Get-WmiObject -Query $query -Namespace &quot;root\cimv2&quot; | format-list Name, DisplayName</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="bae80-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bae80-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bae80-155">Tarefas do WMI para scripts e aplicativos</span><span class="sxs-lookup"><span data-stu-id="bae80-155">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="bae80-156">Exemplos de aplicativos WMI C++</span><span class="sxs-lookup"><span data-stu-id="bae80-156">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="bae80-157">ScriptCenter do TechNet</span><span class="sxs-lookup"><span data-stu-id="bae80-157">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
