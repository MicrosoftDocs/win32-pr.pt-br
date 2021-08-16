---
description: As tarefas agendadas do WMI criam e geram informações sobre tarefas agendadas. Para outros exemplos, consulte o TechNet ScriptCenter em https://www.microsoft.com/technet .
ms.assetid: 62151fe8-8880-43f2-b456-628bd9c7cc1c
ms.tgt_platform: multiple
title: 'Tarefas WMI: tarefas agendadas'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee4fcf193296d5c474987a3a99877b3bfb43868f79527200893303df351920cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738835"
---
# <a name="wmi-tasks-scheduled-tasks"></a>Tarefas WMI: tarefas agendadas

As tarefas agendadas do WMI criam e geram informações sobre tarefas agendadas. Para outros exemplos, consulte o TechNet ScriptCenter em [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

Os exemplos de script mostrados neste tópico só obtém dados do computador local. Para obter mais informações sobre como usar o script para obter dados de computadores remotos, consulte Conectando-se [ao WMI em um computador remoto.](connecting-to-wmi-on-a-remote-computer.md)


O procedimento a seguir descreve como executar um script.

**Para executar um script**

1.  Copie o código e salve-o em um arquivo com uma extensão .vbs, *como* filename.vbs. Verifique se o editor de texto não adiciona uma .txt de texto ao arquivo.
2.  Abra uma janela do prompt de comando e navegue até o diretório em que você salvou o arquivo.
3.  Digite **cscript filename.vbs** no prompt de comando.
4.  Se não for possível acessar um log de eventos, verifique se você está executando em um prompt de comando Elevado. Alguns log de eventos, como o Log de Eventos de Segurança, podem ser protegidos por UAC (Controles de Acesso do Usuário).

> [!Note]  
> Por padrão, o cscript exibe a saída de um script na janela do prompt de comando. Como os scripts WMI podem produzir grandes quantidades de saída, talvez você queira redirecionar a saída para um arquivo. Digite **cscript filename.vbs > outfile.txt** no prompt de comando para redirecionar a saída do script *filename.vbs* para *outfile.txt*.

 

A tabela a seguir lista exemplos de script que podem ser usados para obter vários tipos de dados do computador local.



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
<td>... criar tarefas agendadas usando scripts?</td>
<td>Use a <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> e o <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>método</strong></a> Create. Se você estiver tendo dificuldades para fazer essa tarefa funcionar no Windows 7 ou posterior, consulte a <strong>seção Win32_ScheduledJob</strong> comentários; provavelmente suas configurações estão impedindo que você use a classe .<br/> <span data-codelanguage="VisualBasic"></span>
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

<p>Na cadeia de &quot; caracteres ******143000.000000-420 (usado no valor do parâmetro StartTime do método &quot; <em>Create),</em> <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong></strong></a> &quot; *******143000.000000 especifica que a tarefa começa em &quot; 14.30 (2:30 P.M.) e &quot; -420 especifica &quot; o fuso horário. O número do fuso horário é o desvio atual da tradução de horário local. O desvio é a diferença entre a hora UTC e a hora local. Para calcular o desvio para o fuso horário, multiplique o número de horas que seu fuso horário está à frente ou atrás de GMT (Horário de Greenwich) por 60 (use um número positivo para o número de horas se o fuso horário estiver à frente de GMT e um número negativo se o fuso horário estiver atrás de GMT). Adicione mais 60 ao cálculo se o fuso horário estiver usando o horário de verão. Por exemplo, o Fuso Horário Padrão do Pacífico está oito horas atrás do GMT, portanto, o desvio é igual a -420 (-8 * 60 + 60) quando o horário de verão está em uso e -480 (-8 * 60) quando o horário de verão não está em uso. Você também pode determinar o valor do desvio consultando a propriedade bias da <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>classe Win32_TimeZone.</strong></a></p></td>
</tr>
<tr class="even">
<td>... retornar uma lista de todas as tarefas agendadas em um computador?</td>
<td><p>Use a <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>classe Win32_ScheduledJob.</strong></a> Observe que essa classe só pode retornar trabalhos criados usando um script ou AT.exe. Ele não pode retornar informações sobre trabalhos criados pelo ou modificados pelo assistente de Tarefa Agendada.</p>
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



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas WMI para scripts e aplicativos](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Exemplos de aplicativo WMI C++](wmi-c---application-examples.md)
</dt> <dt>

[TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

