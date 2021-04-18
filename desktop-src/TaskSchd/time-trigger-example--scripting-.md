---
title: Exemplo de gatilho de tempo (script)
description: Este exemplo de script mostra como criar uma tarefa que executa o bloco de notas em um horário específico.
ms.assetid: 8511ffcd-166f-4c63-9cd2-ead53dde9ed8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77cbf9eab12f5ca027fbb6c48ade37a9f57d9beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761806"
---
# <a name="time-trigger-example-scripting"></a>Exemplo de gatilho de tempo (script)

Este exemplo de script mostra como criar uma tarefa que executa o bloco de notas em um horário específico. A tarefa contém um gatilho baseado em tempo que especifica um limite inicial para ativar a tarefa, uma ação executável que executa o bloco de notas e um limite final que desativa a tarefa.

O procedimento a seguir descreve como agendar uma tarefa para iniciar um executável em um momento específico.

**Para agendar o bloco de notas para iniciar em uma hora específica**

1.  Crie um objeto [**TaskService**](taskservice.md) . Esse objeto permite que você crie a tarefa em uma pasta especificada.
2.  Obter uma pasta de tarefas e criar uma tarefa. Use o método [**TaskService. GetFolder**](taskservice-getfolder.md) para obter a pasta onde a tarefa está armazenada e o método [**TaskService. NewTask**](taskservice-newtask.md) para criar o objeto [**TaskDefinition**](taskdefinition.md) que representa a tarefa.
3.  Defina informações sobre a tarefa usando o objeto [**TaskDefinition**](taskdefinition.md) . Use a propriedade [**TaskDefinition. Settings**](taskdefinition-settings.md) para definir as configurações que determinam como o serviço de Agendador de tarefas executa a tarefa e a propriedade [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) para definir as informações que descrevem a tarefa.
4.  Crie um gatilho baseado em tempo usando a propriedade [**TaskDefinition. Triggers**](taskdefinition-triggers.md) . Esta propriedade fornece acesso ao objeto [**TriggerCollection**](triggercollection.md) . Use o método [**triggers. Create**](triggercollection-create.md) (especificando o tipo de gatilho que você deseja criar) para criar um gatilho baseado em tempo. Ao criar o gatilho, defina o limite inicial e o limite final do gatilho para ativar e desativar o gatilho. O limite inicial especifica quando a ação da tarefa será executada.
5.  Crie uma ação para a tarefa Executar usando a propriedade [**TaskDefinition. Actions**](taskdefinition-actions.md) . Essa propriedade fornece acesso ao objeto [**ActionCollection**](actioncollection.md) . Use o método [**ActionCollection. Create**](actioncollection-create.md) para especificar o tipo de ação que você deseja criar. Este exemplo usa um objeto [**execaction**](execaction.md) , que representa uma ação que executa uma operação de linha de comando.
6.  Registre a tarefa usando o método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) . Para este exemplo, a tarefa iniciará o bloco de notas na hora atual mais 30 segundos.

O exemplo de VBScript a seguir mostra como agendar uma tarefa para executar o bloco de notas 30 segundos depois que a tarefa é registrada.


```VB
'------------------------------------------------------------------
' This sample schedules a task to start notepad.exe 30 seconds
' from the time the task is registered.
'------------------------------------------------------------------

' A constant that specifies a time-based trigger.
const TriggerTypeTime = 1
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
regInfo.Description = "Start notepad at a certain time"
regInfo.Author = "Author Name"

'********************************************************
' Set the principal for the task
Dim principal
Set principal = taskDefinition.Principal

' Set the logon type to interactive logon
principal.LogonType = 3


' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.Enabled = True
settings.StartWhenAvailable = True
settings.Hidden = False

'********************************************************
' Create a time-based trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeTime)

' Trigger variables that define when the trigger is active.
Dim startTime, endTime

Dim time
time = DateAdd("s", 30, Now)  'start time = 30 seconds from now
startTime = XmlTime(time)

time = DateAdd("n", 5, Now) 'end time = 5 minutes from now
endTime = XmlTime(time)

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.ExecutionTimeLimit = "PT5M"    'Five minutes
trigger.Id = "TimeTriggerId"
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
    "Test TimeTrigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."



'------------------------------------------------------------------
' Used to get the time for the trigger 
' startBoundary and endBoundary.
' Return the time in the correct format: 
' YYYY-MM-DDTHH:MM:SS. 
'------------------------------------------------------------------
Function XmlTime(t)
    Dim cSecond, cMinute, CHour, cDay, cMonth, cYear
    Dim tTime, tDate

    cSecond = "0" & Second(t)
    cMinute = "0" & Minute(t)
    cHour = "0" & Hour(t)
    cDay = "0" & Day(t)
    cMonth = "0" & Month(t)
    cYear = Year(t)

    tTime = Right(cHour, 2) & ":" & Right(cMinute, 2) & _
        ":" & Right(cSecond, 2)
    tDate = cYear & "-" & Right(cMonth, 2) & "-" & Right(cDay, 2)
    XmlTime = tDate & "T" & tTime 
End Function

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Agendador de Tarefas](using-the-task-scheduler.md)
</dt> </dl>

 

 




