---
description: As tarefas do WMI para sistemas operacionais obtêm informações sobre o sistema operacional, como a versão, se ela está ativada ou quais hotfixes estão instalados.
ms.assetid: a216ad56-2650-4d93-86e1-449b56019361
ms.tgt_platform: multiple
title: 'Tarefas do WMI: sistemas operacionais'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8d4dff83cebf5fd3336aeec2cc45ac4d8498cdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756074"
---
# <a name="wmi-tasks-operating-systems"></a><span data-ttu-id="fa98f-103">Tarefas do WMI: sistemas operacionais</span><span class="sxs-lookup"><span data-stu-id="fa98f-103">WMI Tasks: Operating Systems</span></span>

<span data-ttu-id="fa98f-104">As tarefas do WMI para sistemas operacionais obtêm informações sobre o sistema operacional, como a versão, se ela está ativada ou quais hotfixes estão instalados.</span><span class="sxs-lookup"><span data-stu-id="fa98f-104">WMI tasks for operating systems obtain information about the operating system, such as version, whether it is activated, or which hotfixes are installed.</span></span>

<span data-ttu-id="fa98f-105">Os exemplos de script mostrados neste tópico obtêm dados somente do computador local.</span><span class="sxs-lookup"><span data-stu-id="fa98f-105">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="fa98f-106">Para obter mais informações sobre como usar o script para obter dados de computadores remotos, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="fa98f-106">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="fa98f-107">O procedimento a seguir descreve como executar um script.</span><span class="sxs-lookup"><span data-stu-id="fa98f-107">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="fa98f-108">**Para executar um script**</span><span class="sxs-lookup"><span data-stu-id="fa98f-108">**To run a script**</span></span>

1.  <span data-ttu-id="fa98f-109">Copie o código e salve-o em um arquivo com uma extensão. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="fa98f-109">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="fa98f-110">Verifique se o editor de texto não adiciona uma extensão. txt ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="fa98f-110">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="fa98f-111">Abra uma janela de prompt de comando e navegue até o diretório em que você salvou o arquivo.</span><span class="sxs-lookup"><span data-stu-id="fa98f-111">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="fa98f-112">Digite **CScript filename.vbs** no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="fa98f-112">Type **CScript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="fa98f-113">Se você não puder acessar um log de eventos, verifique se você está executando a partir de um prompt de comandos com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="fa98f-113">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="fa98f-114">Alguns logs de eventos, como o log de eventos de segurança, podem ser protegidos por UAC (controles de acesso do usuário).</span><span class="sxs-lookup"><span data-stu-id="fa98f-114">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="fa98f-115">Por padrão, o CScript exibe a saída de um script na janela de prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="fa98f-115">By default, CScript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="fa98f-116">Como os scripts WMI podem produzir grandes quantidades de saída, convém redirecionar a saída para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="fa98f-116">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="fa98f-117">Digite **cscript filename.vbs > outfile.txt** no prompt de comando para redirecionar a saída do script de *filename.vbs* para *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="fa98f-117">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="fa98f-118">A tabela a seguir lista os exemplos de script que podem ser usados para obter vários tipos de dados do computador local.</span><span class="sxs-lookup"><span data-stu-id="fa98f-118">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fa98f-119">Como fazer...</span><span class="sxs-lookup"><span data-stu-id="fa98f-119">How do I...</span></span></th>
<th><span data-ttu-id="fa98f-120">Classes ou métodos WMI</span><span class="sxs-lookup"><span data-stu-id="fa98f-120">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fa98f-121">... determinar se um service pack foi instalado em um computador?</span><span class="sxs-lookup"><span data-stu-id="fa98f-121">...determine if a service pack has been installed on a computer?</span></span></td>
<td><span data-ttu-id="fa98f-122">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> e verifique o valor das propriedades <strong>ServicePackMajorVersion</strong> e <strong>ServicePackMinorVersion</strong> .</span><span class="sxs-lookup"><span data-stu-id="fa98f-122">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class and check the value of the <strong>ServicePackMajorVersion</strong> and <strong>ServicePackMinorVersion</strong> properties.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fa98f-123">VB</span><span class="sxs-lookup"><span data-stu-id="fa98f-123">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    Wscript.Echo objOperatingSystem.ServicePackMajorVersion & &quot;.&quot; & objOperatingSystem.ServicePackMinorVersion
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
<th><span data-ttu-id="fa98f-124">PowerShell</span><span class="sxs-lookup"><span data-stu-id="fa98f-124">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_OperatingSystem -Namespace &quot;root\cimv2&quot; | `
   format-list ServicePackMajorVersion, ServicePackMinorVersion</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa98f-125">... determinar quando o sistema operacional foi instalado em um computador?</span><span class="sxs-lookup"><span data-stu-id="fa98f-125">...determine when the operating system was installed on a computer?</span></span></td>
<td><p><span data-ttu-id="fa98f-126">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> e a propriedade <strong>InstallDate</strong> .</span><span class="sxs-lookup"><span data-stu-id="fa98f-126">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class and the <strong>InstallDate</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fa98f-127">VB</span><span class="sxs-lookup"><span data-stu-id="fa98f-127">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    Wscript.Echo &quot;Install Date: &quot; & objOperatingSystem.InstallDate 
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
<th><span data-ttu-id="fa98f-128">PowerShell</span><span class="sxs-lookup"><span data-stu-id="fa98f-128">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_OperatingSystem -Namespace &quot;root\cimv2&quot; | format-list InstallDate</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa98f-129">... determinar qual versão do sistema operacional Windows está instalada em um computador?</span><span class="sxs-lookup"><span data-stu-id="fa98f-129">...determine which version of the Windows operating system is installed on a computer?</span></span></td>
<td><p><span data-ttu-id="fa98f-130">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> e recupere as propriedades <strong>Name</strong> e <strong>version</strong> .</span><span class="sxs-lookup"><span data-stu-id="fa98f-130">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class, and retrieve both the <strong>Name</strong> and <strong>Version</strong> properties.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fa98f-131">VB</span><span class="sxs-lookup"><span data-stu-id="fa98f-131">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    Wscript.Echo objOperatingSystem.Caption & &quot;  &quot; & objOperatingSystem.Version
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
<th><span data-ttu-id="fa98f-132">PowerShell</span><span class="sxs-lookup"><span data-stu-id="fa98f-132">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_OperatingSystem -Namespace &quot;root\cimv2&quot; | format-list Caption, Version</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa98f-133">... Determine qual pasta é a pasta do Windows (% windir%) em um computador?</span><span class="sxs-lookup"><span data-stu-id="fa98f-133">...determine which folder is the Windows folder (%Windir%) on a computer?</span></span></td>
<td><p><span data-ttu-id="fa98f-134">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> e verifique o valor da propriedade <strong>WindowsDirectory</strong> .</span><span class="sxs-lookup"><span data-stu-id="fa98f-134">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class, and check the value of the <strong>WindowsDirectory</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fa98f-135">VB</span><span class="sxs-lookup"><span data-stu-id="fa98f-135">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    Wscript.Echo &quot;Windows Folder: &quot; & objOperatingSystem.WindowsDirectory
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
<th><span data-ttu-id="fa98f-136">PowerShell</span><span class="sxs-lookup"><span data-stu-id="fa98f-136">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_OperatingSystem -Namespace &quot;root\cimv2&quot; | format-list WindowsDirectory</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa98f-137">... determinar quais hotfixes foram instalados em um computador?</span><span class="sxs-lookup"><span data-stu-id="fa98f-137">...determine what hotfixes have been installed on a computer?</span></span></td>
<td><p><span data-ttu-id="fa98f-138">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-quickfixengineering"><strong>Win32_QuickFixEngineering</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="fa98f-138">Use the <a href="/windows/desktop/CIMWin32Prov/win32-quickfixengineering"><strong>Win32_QuickFixEngineering</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fa98f-139">VB</span><span class="sxs-lookup"><span data-stu-id="fa98f-139">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colQuickFixes = objWMIService.ExecQuery (&quot;Select * from Win32_QuickFixEngineering&quot;)
For Each objQuickFix in colQuickFixes
    Wscript.Echo &quot;Description: &quot; & objQuickFix.Description
    Wscript.Echo &quot;Hotfix ID: &quot; & objQuickFix.HotFixID
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
<th><span data-ttu-id="fa98f-140">PowerShell</span><span class="sxs-lookup"><span data-stu-id="fa98f-140">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_QuickFixEngineering -Namespace &quot;root\cimv2&quot; | format-list Description, HotFixIDs</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa98f-141">... determinar se preciso ativar o sistema operacional em um computador?</span><span class="sxs-lookup"><span data-stu-id="fa98f-141">...determine if I need to activate the operating system on a computer?</span></span></td>
<td><p><span data-ttu-id="fa98f-142">Use a classe <a href="/previous-versions/windows/desktop/legacy/aa394520(v=vs.85)"><strong>Win32_WindowsProductActivation</strong></a> e verifique o valor da propriedade <strong>ActivationRequired</strong> .</span><span class="sxs-lookup"><span data-stu-id="fa98f-142">Use the <a href="/previous-versions/windows/desktop/legacy/aa394520(v=vs.85)"><strong>Win32_WindowsProductActivation</strong></a> class and check the value of the <strong>ActivationRequired</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fa98f-143">VB</span><span class="sxs-lookup"><span data-stu-id="fa98f-143">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colWPA = objWMIService.ExecQuery (&quot;Select * from Win32_WindowsProductActivation&quot;)
For Each objWPA in colWPA
    Wscript.Echo &quot;Activation Required: &quot; & objWPA.ActivationRequired
    Wscript.Echo &quot;Remaining Evaluation Period: &quot; & objWPA.RemainingEvaluationPeriod
    Wscript.Echo &quot;Remaining Grace Period: &quot; & objWPA.RemainingGracePeriod
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
<th><span data-ttu-id="fa98f-144">PowerShell</span><span class="sxs-lookup"><span data-stu-id="fa98f-144">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_WindowsProductActivation -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | `
     format-list ActivationRequired, RemainingEvaluationPeriod, RemainingGracePeriod</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="fa98f-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa98f-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa98f-146">Tarefas do WMI para scripts e aplicativos</span><span class="sxs-lookup"><span data-stu-id="fa98f-146">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="fa98f-147">Exemplos de aplicativos WMI C++</span><span class="sxs-lookup"><span data-stu-id="fa98f-147">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="fa98f-148">ScriptCenter do TechNet</span><span class="sxs-lookup"><span data-stu-id="fa98f-148">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

