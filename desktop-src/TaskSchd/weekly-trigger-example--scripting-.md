---
title: Exemplo de gatilho semanal (script)
description: este exemplo de script mostra como criar uma tarefa que executa Bloco de notas às 8 00 na segunda-feira de cada semana.
ms.assetid: 68ef73b0-3780-480e-90fe-940b6e8a5340
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6500dae3c0444bc41b982acc06b0e331e63aa4fb821385b416dd0d3e079671d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001764"
---
# <a name="weekly-trigger-example-scripting"></a>Exemplo de gatilho semanal (script)

este exemplo de script mostra como criar uma tarefa que executa Bloco de notas às 8:00 na segunda-feira de cada semana. a tarefa contém um gatilho diário que especifica quando a tarefa é executada e uma ação executável que é executada Bloco de notas.

O procedimento a seguir descreve como agendar uma tarefa para iniciar um executável às 8:00 na segunda-feira de cada semana.

**para agendar Bloco de notas iniciar às 8:00 na segunda-feira de cada semana**

1.  Crie um objeto [**TaskService**](taskservice.md) . Esse objeto permite que você crie a tarefa em uma pasta especificada.
2.  Obter uma pasta de tarefas e criar uma tarefa. Use o método [**TaskService. GetFolder**](taskservice-getfolder.md) para obter a pasta onde a tarefa está armazenada e o método [**TaskService. NewTask**](taskservice-newtask.md) para criar o objeto [**TaskDefinition**](taskdefinition.md) que representa a tarefa.
3.  Defina informações sobre a tarefa usando o objeto [**TaskDefinition**](taskdefinition.md) . Use a propriedade [**TaskDefinition. Configurações**](taskdefinition-settings.md) para definir as configurações que determinam como o serviço de Agendador de Tarefas executa a tarefa e a propriedade [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) para definir as informações que descrevem a tarefa.
4.  Crie um gatilho semanal usando a propriedade [**TaskDefinition. Triggers**](taskdefinition-triggers.md) . Essa propriedade fornece acesso ao objeto [**TriggerCollection**](triggercollection.md) que é usado para criar o gatilho.

    Use o método [**TriggerCollection. Create**](triggercollection-create.md) (especificando o tipo de gatilho que você deseja criar) para criar um gatilho semanal.

    Defina a propriedade [**WeeklyTrigger. StartBoundary**](trigger-startboundary.md) para especificar quando o gatilho é ativado e a hora do dia em que a tarefa é executada. Neste exemplo, o gatilho é ativado em 1º de janeiro de 2005 e a tarefa é executada às 8:00.

    Defina a propriedade [**WeeklyTrigger. Endboundal**](trigger-endboundary.md)para especificar quando o gatilho será desativado. Neste exemplo, o gatilho é desativado em 1º de janeiro de 2015.

    Defina a propriedade [**WeeklyTrigger. DaysOfWeek**](weeklytrigger-daysofweek.md) para especificar os dias da semana em que a tarefa é executada. Neste exemplo, a tarefa é executada na segunda-feira.

    Defina a propriedade [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md)para especificar o intervalo entre as semanas na agenda. Neste exemplo, a tarefa é executada todas as semanas.

5.  Crie uma ação para a tarefa Executar usando a propriedade [**TaskDefinition. Actions**](taskdefinition-actions.md) . Essa propriedade fornece acesso ao objeto [**ActionCollection**](actioncollection.md) usado para criar a ação. Use o método [**ActionCollection. Create**](actioncollection-create.md) para especificar o tipo de ação que você deseja criar. Este exemplo usa um objeto [**execaction**](execaction.md) , que representa uma ação que executa uma operação de linha de comando.
6.  Registre a tarefa usando o método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) . para este exemplo, a tarefa será iniciada Bloco de notas às 8:00 na segunda-feira de cada semana.

o exemplo de VBScript a seguir mostra como agendar uma tarefa para execução Bloco de notas todos os dias às 8:00.


```VB
'------------------------------------------------------------------
' This sample schedules a task to start on a weekly basis.
'------------------------------------------------------------------

' A constant that specifies a weekly trigger.
const TriggerTypeWeekly = 3
' A constant that specifies an executable action.
const ActionTypeExec = 0   


'********************************************************
' Create the TaskService object.
Set service = CreateObject("Schedule.Service")
call service.Connect()

'********************************************************
' Get a folder to create a task definition in. 
Dim rootFolder
Set rootFolder = service.GetFolder("\")

' The taskDefinition variable is the TaskDefinition object.
Dim taskDefinition
' The flags parameter is 0 because it is not supported.
Set taskDefinition = service.NewTask(0) 

'********************************************************
' Define information about the task.

' Set the registration info for the task by 
' creating the RegistrationInfo object.
Dim regInfo
Set regInfo = taskDefinition.RegistrationInfo
regInfo.Description = "Start Notepad weekly."
regInfo.Author = "Administrator"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.Enabled = True
settings.StartWhenAvailable = True
settings.Hidden = False

'********************************************************
' Create a weekly trigger. Note that the start boundary 
' specifies the time of day that the task starts, the 
' day-of-week specfies on what day of the week the task 
' runs, and the interval specifies what weeks the task runs.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeWeekly)

' Trigger variables that define when the trigger is active 
' and the time of day that the task is run. The format of 
' this tims is YYYY-MM-DDTHH:MM:SS
Dim startTime, endTime

Dim time
startTime = "2006-05-02T08:00:00"  'Task runs at 8:00 AM
endTime = "2015-05-02T08:00:00"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.DaysOfWeek = 1
trigger.WeeksInterval = 1    'Task runs every week.
trigger.Id = "WeeklyTriggerId"
trigger.Enabled = True

'***********************************************************
' Create the action for the task to execute.

' Add an action to the task to run notepad.exe.
Dim Action
Set Action = taskDefinition.Actions.Create( ActionTypeExec )
Action.Path = "C:\Windows\System32\notepad.exe"

WScript.Echo "Task definition created. About to submit the task..."

'***********************************************************
' Register (create) the task.

call rootFolder.RegisterTaskDefinition( _
    "Test Weekly Trigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Agendador de Tarefas](using-the-task-scheduler.md)
</dt> </dl>

 

 




