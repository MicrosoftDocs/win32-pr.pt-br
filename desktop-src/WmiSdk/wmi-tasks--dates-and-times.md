---
description: Há várias classes WMI e um objeto de script para analisar ou converter o formato de data e hora CIM. Para obter outros exemplos, consulte o TechNet ScriptCenter em https://www.microsoft.com/technet .
ms.assetid: dd01a732-5c88-4c24-a551-4d5452e712cc
ms.tgt_platform: multiple
title: 'Tarefas do WMI: datas e horas'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8864deb4f76b8ce6b76017c0348cdb86bf38b697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766528"
---
# <a name="wmi-tasks-dates-and-times"></a><span data-ttu-id="3184f-104">Tarefas do WMI: datas e horas</span><span class="sxs-lookup"><span data-stu-id="3184f-104">WMI Tasks: Dates and Times</span></span>

<span data-ttu-id="3184f-105">Há várias classes WMI e um objeto de script para analisar ou converter o formato de [data e hora CIM](date-and-time-format.md) .</span><span class="sxs-lookup"><span data-stu-id="3184f-105">There are several WMI classes and a scripting object to parse or convert the [CIM datetime](date-and-time-format.md) format.</span></span> <span data-ttu-id="3184f-106">Para obter outros exemplos, consulte o TechNet ScriptCenter em [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3184f-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="3184f-107">Os exemplos de script mostrados neste tópico obtêm dados somente do computador local.</span><span class="sxs-lookup"><span data-stu-id="3184f-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="3184f-108">Para obter mais informações sobre como usar o script para obter dados de computadores remotos, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="3184f-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

## <a name="to-run-a-script"></a><span data-ttu-id="3184f-109">Para executar um script</span><span class="sxs-lookup"><span data-stu-id="3184f-109">To run a script</span></span>

<span data-ttu-id="3184f-110">O procedimento a seguir descreve como executar um script.</span><span class="sxs-lookup"><span data-stu-id="3184f-110">The following procedure describes how to run a script.</span></span>

1.  <span data-ttu-id="3184f-111">Copie o código e salve-o em um arquivo com uma extensão. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="3184f-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="3184f-112">Verifique se o editor de texto não adiciona uma extensão. txt ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="3184f-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="3184f-113">Abra uma janela de prompt de comando e navegue até o diretório em que você salvou o arquivo.</span><span class="sxs-lookup"><span data-stu-id="3184f-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="3184f-114">Digite **cscript filename.vbs** no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="3184f-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="3184f-115">Se você não puder acessar um log de eventos, verifique se você está executando a partir de um prompt de comandos com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="3184f-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="3184f-116">Alguns logs de eventos, como o log de eventos de segurança, podem ser protegidos por UAC (controles de acesso do usuário).</span><span class="sxs-lookup"><span data-stu-id="3184f-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="3184f-117">Por padrão, o cscript exibe a saída de um script na janela de prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="3184f-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="3184f-118">Como os scripts WMI podem produzir grandes quantidades de saída, convém redirecionar a saída para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="3184f-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="3184f-119">Digite **cscript filename.vbs > outfile.txt** no prompt de comando para redirecionar a saída do script de *filename.vbs* para *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="3184f-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="3184f-120">A tabela a seguir lista os exemplos de script que podem ser usados para obter vários tipos de dados do computador local.</span><span class="sxs-lookup"><span data-stu-id="3184f-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3184f-121">Como fazer...</span><span class="sxs-lookup"><span data-stu-id="3184f-121">How do I...</span></span></th>
<th><span data-ttu-id="3184f-122">Classes ou métodos WMI</span><span class="sxs-lookup"><span data-stu-id="3184f-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3184f-123">... converter datas do WMI em datas e horários padrão?</span><span class="sxs-lookup"><span data-stu-id="3184f-123">...convert WMI dates to standard dates and times?</span></span><br/></td>
<td><span data-ttu-id="3184f-124">Use o objeto <a href="swbemdatetime.md"><strong>SWbemDateTime</strong></a> para convertê-los em datas e horas regulares.</span><span class="sxs-lookup"><span data-stu-id="3184f-124">Use the <a href="swbemdatetime.md"><strong>SWbemDateTime</strong></a> object to convert these to regular dates and times.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3184f-125">VB</span><span class="sxs-lookup"><span data-stu-id="3184f-125">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Set dtmInstallDate = CreateObject(&quot;WbemScripting.SWbemDateTime&quot;)
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set objOS = objWMIService.ExecQuery(&quot;Select * from Win32_OperatingSystem&quot;)
For Each strOS in objOS
    dtmInstallDate.Value = strOS.InstallDate
    Wscript.Echo dtmInstallDate.GetVarDate
Next</code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="3184f-126">Ou fazer com que seu código faça a tarefa manualmente.</span><span class="sxs-lookup"><span data-stu-id="3184f-126">Or have your code do the task manually.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3184f-127">VB</span><span class="sxs-lookup"><span data-stu-id="3184f-127">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Function WMIDateStringToDate(dtmInstallDate) 
    WMIDateStringToDate = CDate(Mid(dtmInstallDate, 5, 2) & &quot;/&quot; & Mid(dtmInstallDate, 7, 2) _
                        & &quot;/&quot; & Left(dtmInstallDate, 4) & &quot; &quot; & Mid (dtmInstallDate, 9, 2) & &quot;:&quot; _
                        & Mid(dtmInstallDate, 11, 2) & &quot;:&quot; & Mid(dtmInstallDate,13, 2)) 
End Function </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3184f-128">... determinar o tempo configurado atualmente em um computador?</span><span class="sxs-lookup"><span data-stu-id="3184f-128">...determine the time currently configured on a computer?</span></span></p></td>
<td><p><span data-ttu-id="3184f-129">Use a classe <a href="/previous-versions/windows/desktop/wmitimepprov/win32-localtime"><strong>Win32_LocalTime</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3184f-129">Use the <a href="/previous-versions/windows/desktop/wmitimepprov/win32-localtime"><strong>Win32_LocalTime</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3184f-130">VB</span><span class="sxs-lookup"><span data-stu-id="3184f-130">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_LocalTime&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Day:           &quot; & objItem.Day & VBNewLine _
               & &quot;Day Of Week:   &quot; & objItem.DayOfWeek & VBNewLine _
               & &quot;Hour:          &quot; & objItem.Hour & VBNewLine _
               & &quot;Minute:        &quot; & objItem.Minute & VBNewLine _
               & &quot;Month:         &quot; & objItem.Month & VBNewLine _
               & &quot;Quarter:       &quot; & objItem.Quarter & VBNewLine _
               & &quot;Second:        &quot; & objItem.Second & VBNewLine _
               & &quot;Week In Month: &quot; & objItem.WeekInMonth & VBNewLine _
               & &quot;Year:          &quot; & objItem.Year 
Next</code></pre></td>
</tr>
</tbody>
</table>

</div>
<div class="code">
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3184f-131">PowerShell</span><span class="sxs-lookup"><span data-stu-id="3184f-131">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code># Specify computer and get Local Time
$Computer = &quot;.&quot;
$times = Get-WmiObject Win32_LocalTime -computer $computer

<# Now display the result #>

Foreach ($time in $times) {
    &quot;Day : {0}&quot; -f $Time.Day
    &quot;Day Of Week : {0}&quot; -f $Time.DayOfWeek
    &quot;Hour : {0}&quot; -f $Time.Hour
    &quot;Minute : {0}&quot; -f $Time.Minute
    &quot;Month : {0}&quot; -f $Time.Month
    &quot;Quarter : {0}&quot; -f $Time.Quarter
    &quot;Second : {0}&quot; -f $time.Second 
    &quot;Week In Month: {0}&quot; -f $Time.WeekInMonth 
    &quot;Year : {0}&quot; -f $Time.Year 
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3184f-132">... determinar o nome do fuso horário em que um computador está em execução?</span><span class="sxs-lookup"><span data-stu-id="3184f-132">...determine the name of the time zone in which a computer is running?</span></span></p></td>
<td><p><span data-ttu-id="3184f-133">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> e verifique o valor da propriedade <strong>Description</strong> .</span><span class="sxs-lookup"><span data-stu-id="3184f-133">Use the <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> class and check the value of the <strong>Description</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3184f-134">VB</span><span class="sxs-lookup"><span data-stu-id="3184f-134">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_TimeZone&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Description:   &quot; & objItem.Description
    Wscript.Echo &quot;Daylight Name: &quot; & objItem.DaylightName
    Wscript.Echo &quot;Standard Name: &quot; & objItem.StandardName
    Wscript.Echo
Next</code></pre></td>
</tr>
</tbody>
</table>

</div>
<div class="code">
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3184f-135">PowerShell</span><span class="sxs-lookup"><span data-stu-id="3184f-135">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = &quot;.&quot;  
$timezone = Get-WMIObject -class Win32_TimeZone -ComputerName $computer  
  
<# Display details  #>
if ($computer -eq &quot;.&quot;) {$computer = Hostname}  
&quot;Time zone information on computer `&quot;{0}`&quot;&quot; -f $computer  
&quot;Time Zone Description   : {0}&quot; -f $timezone.Description  
&quot;Daylight Name           : {0}&quot; -f $timezone.DaylightName  
&quot;Standard Name           : {0}&quot; -f $timezone.StandardName  </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3184f-136">... Verifique se &quot; 10/02/2000 &quot; está interpretado como Oct. 2, 2000, não &quot; 10 de fevereiro de 2000 &quot; ?</span><span class="sxs-lookup"><span data-stu-id="3184f-136">...ensure that &quot;10/02/2000&quot; is interpreted as Oct. 2, 2000, not &quot;10 Feb, 2000&quot;?</span></span></p></td>
<td><p><span data-ttu-id="3184f-137">Gerencie datas no formato de <a href="datetime.md">data e hora</a> <a href="gloss-c.md"><em>CIM</em></a> e use métodos <a href="swbemdatetime.md"><strong>SWbemDateTime</strong></a> , como <a href="swbemdatetime-getvardate.md"><strong>GetVarDate</strong></a> para converter para e de formatos <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME</strong></a> ou <strong>VT_Date</strong> .</span><span class="sxs-lookup"><span data-stu-id="3184f-137">Manage dates in <a href="gloss-c.md"><em>CIM</em></a> <a href="datetime.md">DATETIME</a> format and use <a href="swbemdatetime.md"><strong>SWbemDateTime</strong></a> methods, such as <a href="swbemdatetime-getvardate.md"><strong>GetVarDate</strong></a> to convert to them to and from either <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME</strong></a> or <strong>VT_Date</strong> formats.</span></span> <span data-ttu-id="3184f-138">Como o formato DATETIME é independente da localidade, você pode gravar um script que é executado em qualquer computador.</span><span class="sxs-lookup"><span data-stu-id="3184f-138">Because DATETIME format is locale-independent, you can write a script that runs on any machine.</span></span> <span data-ttu-id="3184f-139">Use o objeto <strong>SWbemDateTime</strong> para convertê-los em datas e horas regulares.</span><span class="sxs-lookup"><span data-stu-id="3184f-139">Use the <strong>SWbemDateTime</strong> object to convert these to regular dates and times.</span></span> <span data-ttu-id="3184f-140">Consulte <a href="date-and-time-format.md">formato de data e hora</a> para obter mais informações sobre como converter datas e horas.</span><span class="sxs-lookup"><span data-stu-id="3184f-140">See <a href="date-and-time-format.md">Date and Time Format</a> for more information on converting dates and times.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3184f-141">... converter um DateTime WMI em um valor DateTime .NET?</span><span class="sxs-lookup"><span data-stu-id="3184f-141">...convert a WMI datetime to a .NET DateTime value?</span></span></p></td>
<td><p><span data-ttu-id="3184f-142">Analise manualmente a cadeia de caracteres e coloque os valores recuperados em um objeto <a href="/dotnet/api/system.datetime">DateTime</a> .</span><span class="sxs-lookup"><span data-stu-id="3184f-142">Manually parse the string, then put the retrieved values into a <a href="/dotnet/api/system.datetime">DateTime</a> object.</span></span></p>
<div class="code">
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3184f-143">PowerShell</span><span class="sxs-lookup"><span data-stu-id="3184f-143">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>function WMIDateStringToDateTime( [String] $strWmiDate ) 
{ 
    $strWmiDate.Trim() > $null 
    $iYear   = [Int32]::Parse($strWmiDate.SubString( 0, 4)) 
    $iMonth  = [Int32]::Parse($strWmiDate.SubString( 4, 2)) 
    $iDay    = [Int32]::Parse($strWmiDate.SubString( 6, 2)) 
    $iHour   = [Int32]::Parse($strWmiDate.SubString( 8, 2)) 
    $iMinute = [Int32]::Parse($strWmiDate.SubString(10, 2)) 
    $iSecond = [Int32]::Parse($strWmiDate.SubString(12, 2)) 
<# decimal point is at $strWmiDate.Substring(14, 1) #> 
    $iMicroseconds = [Int32]::Parse($strWmiDate.Substring(15, 6)) 
    $iMilliseconds = $iMicroseconds / 1000 
    $iUtcOffsetMinutes = [Int32]::Parse($strWmiDate.Substring(21, 4)) 
    if ( $iUtcOffsetMinutes -ne 0 ) 
    { 
        $dtkind = [DateTimeKind]::Local 
    } 
    else 
    { 
        $dtkind = [DateTimeKind]::Utc 
    } 
    return New-Object -TypeName DateTime ` 
                      -ArgumentList $iYear, $iMonth, $iDay, ` 
                                    $iHour, $iMinute, $iSecond, ` 
                                    $iMilliseconds, $dtkind 
} </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="3184f-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3184f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3184f-145">Tarefas do WMI para scripts e aplicativos</span><span class="sxs-lookup"><span data-stu-id="3184f-145">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="3184f-146">Exemplos de aplicativos WMI C++</span><span class="sxs-lookup"><span data-stu-id="3184f-146">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="3184f-147">Formato de data e hora</span><span class="sxs-lookup"><span data-stu-id="3184f-147">Date and Time Format</span></span>](date-and-time-format.md)
</dt> <dt>

[<span data-ttu-id="3184f-148">ScriptCenter do TechNet</span><span class="sxs-lookup"><span data-stu-id="3184f-148">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
