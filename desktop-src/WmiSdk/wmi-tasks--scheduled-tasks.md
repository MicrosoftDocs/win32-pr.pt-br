---
description: As tarefas agendadas do WMI criam e obtêm informações sobre as tarefas agendadas. Para obter outros exemplos, consulte o TechNet ScriptCenter em https://www.microsoft.com/technet .
ms.assetid: 62151fe8-8880-43f2-b456-628bd9c7cc1c
ms.tgt_platform: multiple
title: 'Tarefas do WMI: tarefas agendadas'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4051df4348ee47710b5d2d1f5dcc3f59f607d997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752997"
---
# <a name="wmi-tasks-scheduled-tasks"></a><span data-ttu-id="a9166-104">Tarefas do WMI: tarefas agendadas</span><span class="sxs-lookup"><span data-stu-id="a9166-104">WMI Tasks: Scheduled Tasks</span></span>

<span data-ttu-id="a9166-105">As tarefas agendadas do WMI criam e obtêm informações sobre as tarefas agendadas.</span><span class="sxs-lookup"><span data-stu-id="a9166-105">WMI scheduled tasks create and get information about scheduled tasks.</span></span> <span data-ttu-id="a9166-106">Para obter outros exemplos, consulte o TechNet ScriptCenter em [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a9166-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="a9166-107">Os exemplos de script mostrados neste tópico obtêm dados somente do computador local.</span><span class="sxs-lookup"><span data-stu-id="a9166-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="a9166-108">Para obter mais informações sobre como usar o script para obter dados de computadores remotos, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="a9166-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="a9166-109">O procedimento a seguir descreve como executar um script.</span><span class="sxs-lookup"><span data-stu-id="a9166-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="a9166-110">**Para executar um script**</span><span class="sxs-lookup"><span data-stu-id="a9166-110">**To run a script**</span></span>

1.  <span data-ttu-id="a9166-111">Copie o código e salve-o em um arquivo com uma extensão. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="a9166-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="a9166-112">Verifique se o editor de texto não adiciona uma extensão. txt ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="a9166-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="a9166-113">Abra uma janela de prompt de comando e navegue até o diretório em que você salvou o arquivo.</span><span class="sxs-lookup"><span data-stu-id="a9166-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="a9166-114">Digite **cscript filename.vbs** no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="a9166-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="a9166-115">Se você não puder acessar um log de eventos, verifique se você está executando a partir de um prompt de comandos com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="a9166-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="a9166-116">Alguns logs de eventos, como o log de eventos de segurança, podem ser protegidos por UAC (controles de acesso do usuário).</span><span class="sxs-lookup"><span data-stu-id="a9166-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="a9166-117">Por padrão, o cscript exibe a saída de um script na janela de prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="a9166-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="a9166-118">Como os scripts WMI podem produzir grandes quantidades de saída, convém redirecionar a saída para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a9166-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="a9166-119">Digite **cscript filename.vbs > outfile.txt** no prompt de comando para redirecionar a saída do script de *filename.vbs* para *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="a9166-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="a9166-120">A tabela a seguir lista os exemplos de script que podem ser usados para obter vários tipos de dados do computador local.</span><span class="sxs-lookup"><span data-stu-id="a9166-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a9166-121">Como fazer...</span><span class="sxs-lookup"><span data-stu-id="a9166-121">How do I...</span></span></th>
<th><span data-ttu-id="a9166-122">Classes ou métodos WMI</span><span class="sxs-lookup"><span data-stu-id="a9166-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a9166-123">... criar tarefas agendadas usando scripts?</span><span class="sxs-lookup"><span data-stu-id="a9166-123">...create scheduled tasks using scripts?</span></span></td>
<td><span data-ttu-id="a9166-124">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> e o método <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a9166-124">Use the <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> method.</span></span> <span data-ttu-id="a9166-125">Se você estiver tendo dificuldades para fazer essa tarefa funcionar no Windows 7 ou posterior, consulte a seção <strong>Win32_ScheduledJob</strong> comentários; Provavelmente, suas configurações estão impedindo o uso da classe.</span><span class="sxs-lookup"><span data-stu-id="a9166-125">If you are having difficulty making this task work on Windows 7 or later, see the <strong>Win32_ScheduledJob</strong> Remarks section; likely your settings are preventing you from using the class.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a9166-126">VB</span><span class="sxs-lookup"><span data-stu-id="a9166-126">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
JobID = &quot;Test&quot;
Set objNewJob = objWMIService.Get(&quot;Win32_ScheduledJob&quot;)
errJobCreate = objNewJob.Create _
    (&quot;Notepad.exe&quot;, &quot;********143000.000000-420&quot;, True , 1 OR 4 OR 16, ,True, JobId) 
If errJobCreate = 0 Then
    WScript.Echo &quot;Job created successfully: &quot; & VBNewLine _
        & &quot;Notepad.exe scheduled to run repeately at 14.30 (2:30 P.M.) PST&quot; & VBNewLine _
        & &quot;on Mon, Wed, and Fri.&quot;
Else
    WScript.Echo &quot;Job not created. Error code = &quot; & errJobCreate
End If</code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="a9166-127">Na cadeia de caracteres \* \* \* \* \* \* \* &quot; \* 143000.000000-420 &quot; (usado no valor do parâmetro <em>StartTime</em> do método <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> ), \* \* \* \* \* \* &quot; \* \* 143000, 0 &quot; especifica que a tarefa começa às 14,30 (2:30 P.M.) e &quot; -420 &quot; especifica o fuso horário.</span><span class="sxs-lookup"><span data-stu-id="a9166-127">In the string &quot;\*\*\*\*\*\*\*\*143000.000000-420&quot; (used in the <em>StartTime</em> parameter value of the <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> method), &quot;\*\*\*\*\*\*\*\*143000.000000&quot; specifies that the task starts at 14.30 (2:30 P.M.) and &quot;-420&quot; specifies the time zone.</span></span> <span data-ttu-id="a9166-128">O número de fuso horário é a diferença atual da tradução de tempo local.</span><span class="sxs-lookup"><span data-stu-id="a9166-128">The time zone number is the current bias of the local time translation.</span></span> <span data-ttu-id="a9166-129">A tendência é a diferença entre a hora UTC e a hora local.</span><span class="sxs-lookup"><span data-stu-id="a9166-129">The bias is the difference between the UTC time and the local time.</span></span> <span data-ttu-id="a9166-130">Para calcular a tendência de seu fuso horário, multiplique o número de horas em que o fuso horário está adiantado ou atrasado no horário de Greenwich (GMT) por 60 (use um número positivo para o número de horas se o fuso horário estiver à frente do GMT e um número negativo se o fuso horário estiver atrás do GMT).</span><span class="sxs-lookup"><span data-stu-id="a9166-130">To calculate the bias for your time zone, multiply the number of hours that your time zone is ahead or behind Greenwich Mean Time (GMT) by 60 (use a positive number for the number of hours if your time zone is ahead of GMT and a negative number if your time zone is behind GMT).</span></span> <span data-ttu-id="a9166-131">Adicione um 60 adicional ao seu cálculo se o seu fuso horário estiver usando o horário de verão.</span><span class="sxs-lookup"><span data-stu-id="a9166-131">Add an additional 60 to your calculation if your time zone is using daylight savings time.</span></span> <span data-ttu-id="a9166-132">Por exemplo, o fuso horário padrão do Pacífico é de oito horas atrás do GMT, portanto, a tendência é igual a-420 (-8 \* 60 + 60) quando o horário de verão está em uso e-480 (-8 \* 60) quando o horário de verão não está em uso.</span><span class="sxs-lookup"><span data-stu-id="a9166-132">For example, the Pacific Standard Time zone is eight hours behind GMT, therefore the bias is equals to -420 (-8 \* 60 + 60) when daylight savings time is in use and -480 (-8 \* 60) when daylight savings time is not in use.</span></span> <span data-ttu-id="a9166-133">Você também pode determinar o valor da tendência consultando a propriedade Bias da classe <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a9166-133">You can also determine the value of the bias by querying the bias property of the <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> class.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9166-134">... retornar uma lista de todas as tarefas agendadas em um computador?</span><span class="sxs-lookup"><span data-stu-id="a9166-134">...return a list of all the scheduled tasks on a computer?</span></span></td>
<td><p><span data-ttu-id="a9166-135">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a9166-135">Use the <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> class.</span></span> <span data-ttu-id="a9166-136">Observe que essa classe só pode retornar trabalhos que são criados usando um script ou AT.exe.</span><span class="sxs-lookup"><span data-stu-id="a9166-136">Note that this class can only return jobs that are created using either a script or AT.exe.</span></span> <span data-ttu-id="a9166-137">Ele não pode retornar informações sobre trabalhos que são criados pelo ou modificados pelo assistente de tarefa agendada.</span><span class="sxs-lookup"><span data-stu-id="a9166-137">It cannot return information about jobs that are either created by or modified by the Scheduled Task wizard.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a9166-138">VB</span><span class="sxs-lookup"><span data-stu-id="a9166-138">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colScheduledJobs = objWMIService.ExecQuery (&quot;Select * from Win32_ScheduledJob&quot;)
For Each objJob in colScheduledJobs
    Wscript.Echo &quot;Command: &quot; & objJob.Command & VBNewLine _
    & &quot;Days Of Month: &quot; & objJob.DaysOfMonth & VBNewLine _
    & &quot;Days Of Week: &quot; & objJob.DaysOfWeek & VBNewLine _
    & &quot;Description: &quot; & objJob.Description & VBNewLine _
    & &quot;Elapsed Time: &quot; & objJob.ElapsedTime & VBNewLine _
    & &quot;Install Date: &quot; & objJob.InstallDate & VBNewLine _
    & &quot;Interact with Desktop: &quot; & objJob.InteractWithDesktop & VBNewLine _
    & &quot;Job ID: &quot; & objJob.JobId & VBNewLine _
    & &quot;Job Status: &quot; & objJob.JobStatus & VBNewLine _
    & &quot;Name: &quot; & objJob.Name & VBNewLine _
    & &quot;Notify: &quot; & objJob.Notify & VBNewLine _
    & &quot;Owner: &quot; & objJob.Owner & VBNewLine _
    & &quot;Priority: &quot; & objJob.Priority & VBNewLine _
    & &quot;Run Repeatedly: &quot; & objJob.RunRepeatedly & VBNewLine _
    & &quot;Start Time: &quot; & objJob.StartTime & VBNewLine _
    & &quot;Status: &quot; & objJob.Status & VBNewLine _
    & &quot;Time Submitted: &quot; & objJob.TimeSubmitted & VBNewLine _
    & &quot;Until Time: &quot; & objJob.UntilTime
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="a9166-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a9166-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9166-140">Tarefas do WMI para scripts e aplicativos</span><span class="sxs-lookup"><span data-stu-id="a9166-140">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="a9166-141">Exemplos de aplicativos WMI C++</span><span class="sxs-lookup"><span data-stu-id="a9166-141">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="a9166-142">ScriptCenter do TechNet</span><span class="sxs-lookup"><span data-stu-id="a9166-142">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

