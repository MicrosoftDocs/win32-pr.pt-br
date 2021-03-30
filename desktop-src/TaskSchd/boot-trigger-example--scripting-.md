---
title: Exemplo de gatilho de inicialização (script)
description: Este exemplo de script mostra como criar uma tarefa que está agendada para executar o bloco de notas quando o sistema é inicializado.
ms.assetid: 73ae9cc4-ef89-4390-ac05-8a773f45fa46
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72b7735c607dfc39b848532a70e4d24b1a14d346
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005531"
---
# <a name="boot-trigger-example-scripting"></a>Exemplo de gatilho de inicialização (script)

Este exemplo de script mostra como criar uma tarefa que está agendada para executar o bloco de notas quando o sistema é inicializado. A tarefa contém um gatilho de inicialização que especifica um limite inicial e um tempo de atraso para a tarefa ser iniciada depois que o sistema é inicializado. A tarefa também contém uma ação que especifica a tarefa para executar o bloco de notas. A tarefa é registrada usando a conta de serviço local como um contexto de segurança para executar a tarefa.

O procedimento a seguir descreve como agendar um executável, como o bloco de notas, para iniciar quando o sistema for inicializado.

**Para agendar o bloco de notas para iniciar quando o sistema for inicializado**

1.  Crie um objeto [**TaskService**](taskservice.md) . Esse objeto permite que você crie a tarefa em uma pasta especificada.
2.  Obter uma pasta de tarefas e criar uma tarefa. Use o método [**TaskService. GetFolder**](taskservice-getfolder.md) para obter a pasta onde a tarefa está armazenada e o método [**TaskService. NewTask**](taskservice-newtask.md) para criar o objeto [**TaskDefinition**](taskdefinition.md) que representa a tarefa.
3.  Defina informações sobre a tarefa usando o objeto [**TaskDefinition**](taskdefinition.md) . Use a propriedade [**TaskDefinition. Settings**](taskdefinition-settings.md) para definir as configurações que determinam como o serviço de Agendador de tarefas executa a tarefa e a propriedade [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) para definir as informações que descrevem a tarefa.
4.  Crie um gatilho de logon usando a propriedade [**TaskDefinition. Triggers**](taskdefinition-triggers.md) . Esta propriedade fornece acesso ao objeto [**TriggerCollection**](triggercollection.md) . Use o método [**TriggerCollection. Create**](triggercollection-create.md) (especificando o tipo de gatilho que você deseja criar) para criar um gatilho de inicialização. Ao criar o gatilho, defina as propriedades [**StartBoundary**](trigger-startboundary.md) e [**endboundal**](trigger-endboundary.md) do gatilho para ativar e desativar o gatilho. Você também pode especificar um valor para a propriedade [**Delay**](boottrigger-delay.md) do gatilho de inicialização.
5.  Crie uma ação para a tarefa Executar usando a propriedade [**TaskDefinition. Actions**](taskdefinition-actions.md) . Essa propriedade fornece acesso ao objeto [**ActionCollection**](actioncollection.md) . Use o método [**ActionCollection. Create**](actioncollection-create.md) para especificar o tipo de ação que você deseja criar. Este exemplo usa um objeto [**execaction**](execaction.md) , que representa uma ação que inicia um executável.
6.  Registre a tarefa usando o método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) . A tarefa é registrada usando a conta de serviço local como um contexto de segurança para executar a tarefa.

O exemplo de VBScript a seguir mostra como agendar uma tarefa para executar o bloco de notas 30 segundos após a inicialização do sistema.


```VB
'---------------------------------------------------------
' This sample schedules a task to start notepad.exe 30 seconds after
' the system is booted.
'---------------------------------------------------------

' A constant that specifies a boot trigger.
const TriggerTypeBoot = 8
' A constant that specifies an executable action.
const ActionTypeExecutable = 0   

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
regInfo.Description = "Task will execute Notepad when " & _
    "the computer is booted."
regInfo.Author = "Author Name"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.StartWhenAvailable = True

'********************************************************
' Create a boot trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeBoot)

' Trigger variables that define when the trigger is active.
Dim startTime, endTime
startTime = "2006-05-02T10:49:02"
endTime = "2006-05-02T10:52:02"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.ExecutionTimeLimit = "PT5M"    ' Five minutes
trigger.Id = "BootTriggerId"
trigger.Delay = "PT30S"                ' 30 Seconds   

'***********************************************************
' Create the action for the task to execute.

' Add an action to the task. The action executes notepad.
Dim Action
Set Action = taskDefinition.Actions.Create( ActionTypeExecutable )
Action.Path = "C:\Windows\System32\notepad.exe"

WScript.Echo "Task definition created. About to submit the task..."

'***********************************************************
' Register (create) the task.
const createOrUpdateTask = 6
call rootFolder.RegisterTaskDefinition( _
    "Test Boot Trigger", taskDefinition, createOrUpdateTask, _
    "Local Service", , 5)

WScript.Echo "Task submitted."
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Agendador de Tarefas](using-the-task-scheduler.md)
</dt> </dl>

 

 




