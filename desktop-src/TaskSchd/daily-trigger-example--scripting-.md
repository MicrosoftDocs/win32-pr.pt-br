---
title: Exemplo de gatilho diário (script)
description: Este exemplo de script mostra como criar uma tarefa que é Bloco de notas às 8h todos os dias.
ms.assetid: a13bd54d-b45a-46e5-8281-d080f50f6bef
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 530d687264af9d2e7dbd4e9d05cf7dde39a449d3249c3576a35edc8a9e9f088d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139529"
---
# <a name="daily-trigger-example-scripting"></a>Exemplo de gatilho diário (script)

Este exemplo de script mostra como criar uma tarefa que é Bloco de notas às 8h todos os dias. A tarefa contém um gatilho diário que especifica um limite inicial para ativar o gatilho e especificar a hora do dia em que a tarefa é executado, um intervalo de gatilho para especificar que a tarefa é executado todos os dias e um limite final para desativar o gatilho. O exemplo também mostra como definir um padrão de repetição para o gatilho repetir a tarefa. A tarefa também contém uma ação executável que é executada Bloco de notas.

O procedimento a seguir descreve como agendar uma tarefa para iniciar um executável às 8h todos os dias. (Essas etapas correspondem aos comentários de código incluídos no código de exemplo.)

**Para agendar Bloco de notas comece às 8h todos os dias**

1.  Crie um [**objeto TaskService.**](taskservice.md) Esse objeto permite que você crie a tarefa em uma pasta especificada.
2.  Obter uma pasta de tarefas e criar uma tarefa. Use o [**método TaskService.GetFolder**](taskservice-getfolder.md) para obter a pasta em que a tarefa está armazenada e o [**método TaskService.NewTask**](taskservice-newtask.md) para criar o [**objeto TaskDefinition**](taskdefinition.md) que representa a tarefa.
3.  Defina informações sobre a tarefa usando o [**objeto TaskDefinition.**](taskdefinition.md) Use a propriedade [**TaskDefinition.Configurações**](taskdefinition-settings.md) para definir as configurações que determinam como o serviço Agendador de Tarefas executa a tarefa e a propriedade [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) para definir as informações que descrevem a tarefa.
4.  Crie um gatilho diário usando a [**propriedade TaskDefinition.Triggers.**](taskdefinition-triggers.md) Essa propriedade fornece acesso ao [**objeto TriggerCollection**](triggercollection.md) usado para criar o gatilho. Use o [**método TriggerCollection.Create**](triggercollection-create.md) (especificando o tipo de gatilho que você deseja criar) para criar um gatilho diário. Ao criar o gatilho, delimitue o limite inicial para ativar o gatilho e especifique a hora do dia em que a tarefa é executado, o intervalo entre os dias e o limite final para desativar o gatilho. O exemplo a seguir mostra como definir um padrão de repetição para o gatilho repetir a tarefa.
5.  Crie uma ação para a tarefa a ser executada usando a [**propriedade TaskDefinition.Actions.**](taskdefinition-actions.md) Essa propriedade fornece acesso ao [**objeto ActionCollection**](actioncollection.md) usado para criar a ação. Use o [**método ActionCollection.Create**](actioncollection-create.md) para especificar o tipo de ação que você deseja criar. Este exemplo usa um [**objeto ExecAction,**](execaction.md) que representa uma ação que executa uma operação de linha de comando.
6.  Registre a tarefa usando [**o método TaskFolder.RegisterTaskDefinition.**](taskfolder-registertaskdefinition.md) Neste exemplo, a tarefa será Bloco de notas às 8h todos os dias.

O exemplo de VBScript a seguir mostra como agendar uma tarefa para executar Bloco de notas todos os dias às 8h.


```VB
'------------------------------------------------------------------
' This sample schedules a task to start on a daily basis.
'------------------------------------------------------------------

' A constant that specifies a daily trigger.
const TriggerTypeDaily = 2
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
regInfo.Description = "Start notepad at 8:00AM daily"
regInfo.Author = "Administrator"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.Enabled = True
settings.StartWhenAvailable = True
settings.Hidden = False

'********************************************************
' Create a daily trigger. Note that the start boundary 
' specifies the time of day that the task starts and the 
' interval specifies what days the task is run.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeDaily)

' Trigger variables that define when the trigger is active 
' and the time of day that the task is run. The format of 
' this time is YYYY-MM-DDTHH:MM:SS
Dim startTime, endTime

Dim time
startTime = "2006-05-02T08:00:00"  'Task runs at 8:00 AM
endTime = "2015-05-02T08:00:00"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.DaysInterval = 1    'Task runs every day.
trigger.Id = "DailyTriggerId"
trigger.Enabled = True

' Set the task repetition pattern for the task.
' This will repeat the task 5 times.
Dim repetitionPattern
Set repetitionPattern = trigger.Repetition
repetitionPattern.Duration = "PT4M"
repetitionPattern.Interval = "PT1M"

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
    "Test Daily Trigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Agendador de Tarefas](using-the-task-scheduler.md)
</dt> </dl>

 

 




