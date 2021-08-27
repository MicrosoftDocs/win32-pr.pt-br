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
ms.openlocfilehash: 37a1d44a07feea7beb07984c383620fd2f166cdb
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626152"
---
# <a name="wmi-tasks-scheduled-tasks"></a>Tarefas do WMI: tarefas agendadas

As tarefas agendadas do WMI criam e obtêm informações sobre as tarefas agendadas. Para obter outros exemplos, consulte o TechNet ScriptCenter em [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

Os exemplos de script mostrados neste tópico obtêm dados somente do computador local. Para obter mais informações sobre como usar o script para obter dados de computadores remotos, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).


O procedimento a seguir descreve como executar um script.

**Para executar um script**

1.  Copie o código e salve-o em um arquivo com uma extensão. vbs, como *filename.vbs*. Verifique se o editor de texto não adiciona uma extensão de .txt ao arquivo.
2.  Abra uma janela de prompt de comando e navegue até o diretório em que você salvou o arquivo.
3.  Digite **cscript filename.vbs** no prompt de comando.
4.  Se você não puder acessar um log de eventos, verifique se você está executando a partir de um prompt de comandos com privilégios elevados. Alguns logs de eventos, como o log de eventos de segurança, podem ser protegidos por UAC (controles de acesso do usuário).

> [!Note]  
> Por padrão, o cscript exibe a saída de um script na janela de prompt de comando. Como os scripts WMI podem produzir grandes quantidades de saída, convém redirecionar a saída para um arquivo. Digite **cscript filename.vbs > outfile.txt** no prompt de comando para redirecionar a saída do script de *filename.vbs* para *outfile.txt*.

 

A tabela a seguir lista os exemplos de script que podem ser usados para obter vários tipos de dados do computador local.



<table>
<colgroup>
<col  />
<col  />
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
<td>Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> e o método <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> . se você estiver tendo dificuldades para fazer essa tarefa funcionar no Windows 7 ou posterior, consulte a seção <strong>Win32_ScheduledJob</strong> comentários; Provavelmente, suas configurações estão impedindo o uso da classe.<br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
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

<p>Na cadeia de caracteres * * * * * * * &quot; * 143000.000000-420 &quot; (usado no valor do parâmetro <em>StartTime</em> do método <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> ), * * * * * * &quot; * * 143000, 0 &quot; especifica que a tarefa começa às 14,30 (2:30 P.M.) e &quot; -420 &quot; especifica o fuso horário. O número de fuso horário é a diferença atual da tradução de tempo local. A tendência é a diferença entre a hora UTC e a hora local. Para calcular a tendência de seu fuso horário, multiplique o número de horas em que o fuso horário está adiantado ou atrasado no horário de Greenwich (GMT) por 60 (use um número positivo para o número de horas se o fuso horário estiver à frente do GMT e um número negativo se o fuso horário estiver atrás do GMT). Adicione um 60 adicional ao seu cálculo se o seu fuso horário estiver usando o horário de verão. Por exemplo, o fuso horário padrão do Pacífico é de oito horas atrás do GMT, portanto, a tendência é igual a-420 (-8 * 60 + 60) quando o horário de verão está em uso e-480 (-8 * 60) quando o horário de verão não está em uso. Você também pode determinar o valor da tendência consultando a propriedade Bias da classe <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> .</p></td>
</tr>
<tr class="even">
<td>... retornar uma lista de todas as tarefas agendadas em um computador?</td>
<td><p>Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> . Observe que essa classe só pode retornar trabalhos que são criados usando um script ou AT.exe. Ele não pode retornar informações sobre trabalhos que são criados pelo ou modificados pelo assistente de tarefa agendada.</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
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

[Tarefas do WMI para scripts e aplicativos](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Exemplos de aplicativos WMI C++](wmi-c---application-examples.md)
</dt> <dt>

[ScriptCenter do TechNet](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

