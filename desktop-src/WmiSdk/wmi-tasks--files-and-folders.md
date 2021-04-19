---
description: As tarefas do WMI para arquivos e pastas alteram as propriedades de arquivo ou pasta por meio do WMI, incluindo a criação de um compartilhamento ou a renomeação de um arquivo.
ms.assetid: 91281fe1-0461-48da-ac5c-cab7e8e1b285
ms.tgt_platform: multiple
title: 'Tarefas do WMI: arquivos e pastas'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b24d5f7708b88507cd08b73c0b08a83c94f6bb28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793961"
---
# <a name="wmi-tasks-files-and-folders"></a><span data-ttu-id="85522-103">Tarefas do WMI: arquivos e pastas</span><span class="sxs-lookup"><span data-stu-id="85522-103">WMI Tasks: Files and Folders</span></span>

<span data-ttu-id="85522-104">As tarefas do WMI para arquivos e pastas alteram as propriedades de arquivo ou pasta por meio do WMI, incluindo a criação de um compartilhamento ou a renomeação de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="85522-104">WMI tasks for files and folders change file or folder properties through WMI, including creating a share or renaming a file.</span></span> <span data-ttu-id="85522-105">Se você quiser copiar um arquivo ou ler e gravar um arquivo, a maneira mais fácil é usar o [sistema](/previous-versions/visualstudio/visual-basic-6/aa242706(v=vs.60)) de script do Windows, em vez do WMI.</span><span class="sxs-lookup"><span data-stu-id="85522-105">If you want to copy a file or read and write a file, the easiest way is to use the Windows Script Host [FileSystemObject](/previous-versions/visualstudio/visual-basic-6/aa242706(v=vs.60)) rather than WMI.</span></span> <span data-ttu-id="85522-106">Para obter outros exemplos, consulte a seção [arquivos e pastas](/previous-versions/tn-archive/ee176985(v=technet.10)) do [TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter).</span><span class="sxs-lookup"><span data-stu-id="85522-106">For other examples, see the [Files and Folders](/previous-versions/tn-archive/ee176985(v=technet.10)) section of the [TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter).</span></span>

<span data-ttu-id="85522-107">[**CIM \_ O DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile) é uma das poucas [classes CIM](cimclas.md) no WMI que é implementada.</span><span class="sxs-lookup"><span data-stu-id="85522-107">[**CIM\_DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile) is one of the few [CIM classes](cimclas.md) in WMI that is implemented.</span></span> <span data-ttu-id="85522-108">Evite enumerar ou consultar todas as instâncias do **\_ arquivo** de dados CIM em um computador porque o volume de dados provavelmente afetará o desempenho ou fará com que o computador pare de responder.</span><span class="sxs-lookup"><span data-stu-id="85522-108">Avoid enumerating or querying for all instances of **CIM\_DataFile** on a computer because the volume of data is likely to either affect performance or cause the computer to stop responding.</span></span>

<span data-ttu-id="85522-109">Os exemplos de script mostrados neste tópico obtêm dados somente do computador local.</span><span class="sxs-lookup"><span data-stu-id="85522-109">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="85522-110">Para obter mais informações sobre como usar o script para obter dados de computadores remotos, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="85522-110">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="85522-111">O procedimento a seguir descreve como executar um script.</span><span class="sxs-lookup"><span data-stu-id="85522-111">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="85522-112">**Para executar um script**</span><span class="sxs-lookup"><span data-stu-id="85522-112">**To run a script**</span></span>

1.  <span data-ttu-id="85522-113">Copie o código e salve-o em um arquivo com uma extensão. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="85522-113">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="85522-114">Verifique se o editor de texto não adiciona uma extensão. txt ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="85522-114">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="85522-115">Abra uma janela de prompt de comando e navegue até o diretório em que você salvou o arquivo.</span><span class="sxs-lookup"><span data-stu-id="85522-115">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="85522-116">Digite **cscript filename.vbs** no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="85522-116">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="85522-117">Se você não puder acessar um log de eventos, verifique se você está executando a partir de um prompt de comandos com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="85522-117">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="85522-118">Alguns logs de eventos, como o log de eventos de segurança, podem ser protegidos por UAC (controles de acesso do usuário).</span><span class="sxs-lookup"><span data-stu-id="85522-118">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="85522-119">Por padrão, o cscript exibe a saída de um script na janela de prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="85522-119">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="85522-120">Como os scripts WMI podem produzir grandes quantidades de saída, convém redirecionar a saída para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="85522-120">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="85522-121">Digite **cscript filename.vbs > outfile.txt** no prompt de comando para redirecionar a saída do script de *filename.vbs* para *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="85522-121">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="85522-122">A tabela a seguir lista os exemplos de script que podem ser usados para obter vários tipos de dados do computador local.</span><span class="sxs-lookup"><span data-stu-id="85522-122">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85522-123">Como fazer...</span><span class="sxs-lookup"><span data-stu-id="85522-123">How do I...</span></span></th>
<th><span data-ttu-id="85522-124">Classes ou métodos WMI</span><span class="sxs-lookup"><span data-stu-id="85522-124">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="85522-125">... Renomear um arquivo sem obter uma mensagem de erro?</span><span class="sxs-lookup"><span data-stu-id="85522-125">...rename a file without getting an error message?</span></span></td>
<td><span data-ttu-id="85522-126">Use a classe <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_Datafile</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="85522-126">Use the <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_DataFile</strong></a> class.</span></span> <span data-ttu-id="85522-127">Certifique-se de passar o nome do caminho inteiro ao chamar o método <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-cim-datafile"><strong>Rename</strong></a> , por exemplo, &quot;C:\Scripts\Test.txt&quot; em vez de &quot;Text.txt&quot; .</span><span class="sxs-lookup"><span data-stu-id="85522-127">Ensure that you pass the entire path name when calling the <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-cim-datafile"><strong>Rename</strong></a> method, for example, &quot;C:\Scripts\Test.txt&quot; instead of &quot;Text.txt&quot;.</span></span> <span data-ttu-id="85522-128">Para o PowerShell, o uso de <strong>CIM_Datafile</strong> pode ser ineficiente.</span><span class="sxs-lookup"><span data-stu-id="85522-128">For PowerShell, using <strong>CIM_DataFile</strong> may be inefficient.</span></span> <span data-ttu-id="85522-129">Como tal, você pode simplesmente usar o cmdlet Rename-Item.</span><span class="sxs-lookup"><span data-stu-id="85522-129">As such, you may simply use the Rename-Item cmdlet.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85522-130">VB</span><span class="sxs-lookup"><span data-stu-id="85522-130">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colFiles = objWMIService.ExecQuery (&quot;Select * from CIM_DataFile where Name = &quot; & &quot;&#39;c:\\scripts\\toggle_service.vbs&#39;&quot;)
For Each objFile in colFiles
    errResult = objFile.Rename(&quot;c:\scripts\toggle_service.old&quot;)
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
<th><span data-ttu-id="85522-131">PowerShell</span><span class="sxs-lookup"><span data-stu-id="85522-131">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>rename-item c:\scripts\toggle_service.vbs toggle_service.old</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="85522-132">... Determine se os usuários têm. Arquivos MP3 armazenados em seu computador?</span><span class="sxs-lookup"><span data-stu-id="85522-132">...determine whether users have .MP3 files stored on their computer?</span></span></td>
<td><p><span data-ttu-id="85522-133">Use a classe <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_Datafile</strong></a> e selecione arquivos usando a seguinte cláusula <strong>Where</strong> do <a href="querying-with-wql.md">WQL</a> : em que extensão = &quot; mp3 &quot; .</span><span class="sxs-lookup"><span data-stu-id="85522-133">Use the <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_DataFile</strong></a> class and select files using the following <a href="querying-with-wql.md">WQL</a> <strong>WHERE</strong> clause: Where Extension = &quot;MP3&quot;.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85522-134">VB</span><span class="sxs-lookup"><span data-stu-id="85522-134">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colFiles = objWMIService.ExecQuery(&quot;Select * from CIM_DataFile where Extension = &#39;mp3&#39;&quot;)
For Each objFile in colFiles
    Wscript.Echo &quot;File Name: &quot; & objFile.Name & &quot;.&quot; & objFile.Extension
    Wscript.Echo &quot;Path: &quot; & objFile.Path
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
<th><span data-ttu-id="85522-135">PowerShell</span><span class="sxs-lookup"><span data-stu-id="85522-135">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class CIM_DataFile -namespace &quot;root\cimv2&quot; -Filter &quot;Extension = &#39;mp3&#39;&quot; | `
   format-list Name, Extension, Path</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85522-136">... criar pastas compartilhadas em um computador?</span><span class="sxs-lookup"><span data-stu-id="85522-136">...create shared folders on a computer?</span></span></td>
<td><p><span data-ttu-id="85522-137">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-share"><strong>Win32_Share</strong></a> e o método <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-share"><strong>Create</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="85522-137">Use the <a href="/windows/desktop/CIMWin32Prov/win32-share"><strong>Win32_Share</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-share"><strong>Create</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85522-138">VB</span><span class="sxs-lookup"><span data-stu-id="85522-138">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const FILE_SHARE = 0
Const MAXIMUM_CONNECTIONS = 25
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set objNewShare = objWMIService.Get(&quot;Win32_Share&quot;)
errReturn = objNewShare.Create(&quot;C:\Finance&quot;, &quot;FinanceShare&quot;, FILE_SHARE, MAXIMUM_CONNECTIONS, &quot;Public share for the Finance group.&quot;)</code></pre></td>
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
<th><span data-ttu-id="85522-139">PowerShell</span><span class="sxs-lookup"><span data-stu-id="85522-139">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$FILE_SHARE = 0
$MAXIMUM_CONNECTIONS = 25

$NewDir = new-item C:\Finance -type directory 
$Shares= [WMICLASS]&quot;Win32_Share&quot;
[void]$Shares.Create(&quot;C:\Finance&quot;,&quot;FinanceShare&quot;, $FILE_SHARE, $MAXIMUM_CONNECTIONS, &quot;Public share for the Finance group.&quot;) </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85522-140">... copiar uma pasta?</span><span class="sxs-lookup"><span data-stu-id="85522-140">...copy a folder?</span></span></td>
<td><p><span data-ttu-id="85522-141">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> e o método <a href="/windows/desktop/CIMWin32Prov/copy-method-in-class-win32-directory"><strong>Copy</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="85522-141">Use the <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/copy-method-in-class-win32-directory"><strong>Copy</strong></a> method.</span></span> <span data-ttu-id="85522-142">Para o PowerShell, você pode simplesmente usar o cmdlet Copy-Item.</span><span class="sxs-lookup"><span data-stu-id="85522-142">For PowerShell, you can simply use the Copy-Item cmdlet.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85522-143">VB</span><span class="sxs-lookup"><span data-stu-id="85522-143">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot; 
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
 
Set colFolders = objWMIService.ExecQuery(&quot;Select * from Win32_Directory where Name = &#39;c:\\Scripts&#39;&quot;) 
 
For Each objFolder in colFolders 
    errResults  = objFolder.Copy(&quot;D:\Archive&quot;) 
Next </code></pre></td>
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
<th><span data-ttu-id="85522-144">PowerShell</span><span class="sxs-lookup"><span data-stu-id="85522-144">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Copy-Item C:\Scripts -Destination D:\Archive -Recurse</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85522-145">... mover uma pasta?</span><span class="sxs-lookup"><span data-stu-id="85522-145">...move a folder?</span></span></td>
<td><p><span data-ttu-id="85522-146">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> e o método <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-win32-directory"><strong>Rename</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="85522-146">Use the <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-win32-directory"><strong>Rename</strong></a> method.</span></span> <span data-ttu-id="85522-147">Para o PowerShell, você pode simplesmente usar o cmdlet Move-Item.</span><span class="sxs-lookup"><span data-stu-id="85522-147">For PowerShell, you can simply use the Move-Item cmdlet.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85522-148">VB</span><span class="sxs-lookup"><span data-stu-id="85522-148">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot; 
Set objWMIService = GetObject(&quot;winmgmts:&quot; _ 
    & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
 
Set colFolders = objWMIService.ExecQuery _ 
    (&quot;Select * from Win32_Directory where name = &#39;c:\\Scripts&#39;&quot;) 
 
For Each objFolder in colFolders 
    errResults = objFolder.Rename(&quot;C:\Admins\Documents\Archive\VBScript&quot;) 
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
<th><span data-ttu-id="85522-149">PowerShell</span><span class="sxs-lookup"><span data-stu-id="85522-149">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>move-item -path C:\Scripts -destination C:\Admins\Documents\Archive\PowerShell</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="85522-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="85522-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85522-151">Tarefas do WMI para scripts e aplicativos</span><span class="sxs-lookup"><span data-stu-id="85522-151">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="85522-152">Exemplos de aplicativos WMI C++</span><span class="sxs-lookup"><span data-stu-id="85522-152">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="85522-153">ScriptCenter do TechNet</span><span class="sxs-lookup"><span data-stu-id="85522-153">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
