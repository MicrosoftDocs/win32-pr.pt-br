---
description: As tarefas do WMI para o software de computador obtêm informações, como qual software é instalado pelo Microsoft Windows Installer (MSI) e por versões de software. Para obter outros exemplos, consulte o TechNet ScriptCenter em https://www.microsoft.com/technet .
ms.assetid: 65a61be3-7870-4178-9e96-78b82898271f
ms.tgt_platform: multiple
title: 'Tarefas do WMI: software do computador'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 800a42764cbb1b9552a8ecc87debc04685d28850
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506201"
---
# <a name="wmi-tasks-computer-software"></a><span data-ttu-id="71ad9-104">Tarefas do WMI: software do computador</span><span class="sxs-lookup"><span data-stu-id="71ad9-104">WMI Tasks: Computer Software</span></span>

<span data-ttu-id="71ad9-105">As tarefas do WMI para o software de computador obtêm informações, como qual software é instalado pelo Microsoft Windows Installer (MSI) e por versões de software.</span><span class="sxs-lookup"><span data-stu-id="71ad9-105">WMI tasks for computer software obtain information such as which software is installed by the Microsoft Windows Installer (MSI) and software versions.</span></span> <span data-ttu-id="71ad9-106">Para obter outros exemplos, consulte o TechNet ScriptCenter em [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="71ad9-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="71ad9-107">Os exemplos de script mostrados neste tópico obtêm dados somente do computador local.</span><span class="sxs-lookup"><span data-stu-id="71ad9-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="71ad9-108">Para obter mais informações sobre como usar o script para obter dados de computadores remotos, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="71ad9-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="71ad9-109">O procedimento a seguir descreve como executar um script.</span><span class="sxs-lookup"><span data-stu-id="71ad9-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="71ad9-110">**Para executar um script**</span><span class="sxs-lookup"><span data-stu-id="71ad9-110">**To run a script**</span></span>

1.  <span data-ttu-id="71ad9-111">Copie o código e salve-o em um arquivo com uma extensão. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="71ad9-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="71ad9-112">Verifique se o editor de texto não adiciona uma extensão. txt ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="71ad9-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="71ad9-113">Abra uma janela de prompt de comando e navegue até o diretório em que você salvou o arquivo.</span><span class="sxs-lookup"><span data-stu-id="71ad9-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="71ad9-114">Digite **cscript filename.vbs** no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="71ad9-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="71ad9-115">Se você não puder acessar um log de eventos, verifique se você está executando a partir de um prompt de comandos com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="71ad9-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="71ad9-116">Alguns logs de eventos, como o log de eventos de segurança, podem ser protegidos por UAC (controles de acesso do usuário).</span><span class="sxs-lookup"><span data-stu-id="71ad9-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="71ad9-117">Por padrão, o cscript exibe a saída de um script na janela de prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="71ad9-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="71ad9-118">Como os scripts WMI podem produzir grandes quantidades de saída, convém redirecionar a saída para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="71ad9-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="71ad9-119">Digite **cscript filename.vbs > outfile.txt** no prompt de comando para redirecionar a saída do script de *filename.vbs* para *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="71ad9-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

> [!Note]  
> <span data-ttu-id="71ad9-120">A execução de uma \* consulta "selecionar de um \_ produto Win32" pode resultar em um comportamento inesperado.</span><span class="sxs-lookup"><span data-stu-id="71ad9-120">Running a "Select \* from Win32\_Product" query may result in unexpected behavior.</span></span> <span data-ttu-id="71ad9-121">Isso ocorre porque o provedor que dá suporte ao \_ produto Win32 não é otimizado para consulta.</span><span class="sxs-lookup"><span data-stu-id="71ad9-121">This is because the provider that supports Win32\_Product is not query optimized.</span></span> <span data-ttu-id="71ad9-122">Para obter mais informações, consulte o [artigo 974524 da base](https://support.microsoft.com/kb/974524)de dados de conhecimento.</span><span class="sxs-lookup"><span data-stu-id="71ad9-122">For more information, see [KB Article 974524](https://support.microsoft.com/kb/974524).</span></span>

 

<span data-ttu-id="71ad9-123">A tabela a seguir lista os exemplos de script que podem ser usados para obter vários tipos de dados do computador local.</span><span class="sxs-lookup"><span data-stu-id="71ad9-123">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71ad9-124">Como fazer...</span><span class="sxs-lookup"><span data-stu-id="71ad9-124">How do I...</span></span></th>
<th><span data-ttu-id="71ad9-125">Classes ou métodos WMI</span><span class="sxs-lookup"><span data-stu-id="71ad9-125">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="71ad9-126">... desinstalar o software usando um script?</span><span class="sxs-lookup"><span data-stu-id="71ad9-126">...uninstall software using a script?</span></span></td>
<td><span data-ttu-id="71ad9-127">Se o software tiver sido instalado usando Microsoft Windows Installer (MSI), use a classe WMI <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a> e o método <a href="/previous-versions/windows/desktop/msiprov/uninstall-method-in-class-win32-product"><strong>Uninstall</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="71ad9-127">If the software was installed using Microsoft Windows Installer (MSI), use the WMI class <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a> and the <a href="/previous-versions/windows/desktop/msiprov/uninstall-method-in-class-win32-product"><strong>Uninstall</strong></a> method.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71ad9-128">VB</span><span class="sxs-lookup"><span data-stu-id="71ad9-128">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colSoftware = objWMIService.ExecQuery _
    (&quot;Select * from Win32_Product &quot; _
        & &quot;Where Name = &#39;Personnel database&#39;&quot;)
For Each objSoftware in colSoftware
    objSoftware.Uninstall()
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
<th><span data-ttu-id="71ad9-129">PowerShell</span><span class="sxs-lookup"><span data-stu-id="71ad9-129">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSoftware = Get-WmiObject -Class Win32_Product | Where-Object {$_.name -eq &quot;Personnel database&quot;}

foreach ($colItem in $colSoftware)
{
    $colItem.Uninstall()
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ad9-130">... inventariar todo o software instalado em um computador com um script?</span><span class="sxs-lookup"><span data-stu-id="71ad9-130">...inventory all the software installed on a computer with a script?</span></span></td>
<td><p><span data-ttu-id="71ad9-131">Se o software tiver sido instalado usando Microsoft Windows Installer (MSI), use a classe WMI <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="71ad9-131">If the software was installed using Microsoft Windows Installer (MSI) use the WMI class <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71ad9-132">VB</span><span class="sxs-lookup"><span data-stu-id="71ad9-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colSoftware = objWMIService.ExecQuery _
    (&quot;Select * from Win32_Product&quot;)

For Each objSoftware in colSoftware
    Wscript.Echo &quot;Name: &quot; & objSoftware.Name
    Wscript.Echo &quot;Version: &quot; & objSoftware.Version
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
<th><span data-ttu-id="71ad9-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="71ad9-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSoftware = Get-WmiObject -Class Win32_Product

foreach ($colItem in $colSoftware)
{
    &quot;Name: &quot; + $colItem.Name
    &quot;Version: &quot;+ $colItem.Version
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ad9-134">... determinar qual versão do Microsoft Office está instalada?</span><span class="sxs-lookup"><span data-stu-id="71ad9-134">...determine what version of Microsoft Office is installed?</span></span></td>
<td><p><span data-ttu-id="71ad9-135">Use a classe <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a> e verifique o valor da propriedade <strong>version</strong> .</span><span class="sxs-lookup"><span data-stu-id="71ad9-135">Use the <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a> class and check the value of the <strong>Version</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71ad9-136">VB</span><span class="sxs-lookup"><span data-stu-id="71ad9-136">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colSoftware = objWMIService.ExecQuery(_
    &quot;Select * from Win32_Product &quot; & _
    &quot;Where IdentifyingNumber =&quot; _
        & &quot; &#39;{90280409-6000-11D3-8CFE-0050048383C9}&#39;&quot;)
For Each objItem in colSoftware
    Wscript.Echo &quot;Name: &quot; & objItem.Name
    Wscript.Echo &quot;Version: &quot; & objItem.Version
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
<th><span data-ttu-id="71ad9-137">PowerShell</span><span class="sxs-lookup"><span data-stu-id="71ad9-137">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSoftware = Get-WmiObject -Class Win32_Product | Where-Object {$_.IdentifyingNumber -eq &quot;{90280409-6000-11D3-8CFE-0050048383C9}&quot;}

foreach ($colItem in $colSoftware)
{
    &quot;Name: &quot; + $colItem.Name
    &quot;Version: &quot; + $colItem.Version
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a><span data-ttu-id="71ad9-138">Exemplos</span><span class="sxs-lookup"><span data-stu-id="71ad9-138">Examples</span></span>

<span data-ttu-id="71ad9-139">O exemplo de código PowerShell do [script de informações do PC remoto do PowerShell](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) usa uma série de classes de hardware e software, incluindo Win32Product, para encontrar várias informações sobre um computador remoto usando o WMI e o registro remoto.</span><span class="sxs-lookup"><span data-stu-id="71ad9-139">The [Powershell Remote PC Info Script](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) PowerShell code sample uses a number of hardware and software classes, including Win32Product, to find various information about a remote PC using WMI and the remote registry.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71ad9-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="71ad9-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71ad9-141">Tarefas do WMI para scripts e aplicativos</span><span class="sxs-lookup"><span data-stu-id="71ad9-141">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="71ad9-142">Exemplos de aplicativos WMI C++</span><span class="sxs-lookup"><span data-stu-id="71ad9-142">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="71ad9-143">ScriptCenter do TechNet</span><span class="sxs-lookup"><span data-stu-id="71ad9-143">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

