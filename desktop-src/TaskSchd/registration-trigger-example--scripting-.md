---
title: Exemplo de gatilho de registro (script)
description: Este exemplo de script mostra como criar uma tarefa agendada para ser executada Bloco de notas quando uma tarefa é registrada.
ms.assetid: 956b3a21-7d36-4d06-be84-690884ba653a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f036d4772c98392881f254e07e192c970a2cb407727294c7f196c9c15cb9e11f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011316"
---
# <a name="registration-trigger-example-scripting"></a>Exemplo de gatilho de registro (script)

Este exemplo de script mostra como criar uma tarefa agendada para ser executada Bloco de notas quando uma tarefa é registrada. A tarefa contém um gatilho de registro que especifica um limite inicial e um limite final para a tarefa. O limite inicial especifica quando o gatilho é ativado. A tarefa também contém uma ação que especifica a tarefa a ser executada Bloco de notas.

> [!Note]  
> Quando uma tarefa com um gatilho de registro for atualizada, a tarefa será executada depois que a atualização ocorrer.

 

O procedimento a seguir descreve como agendar um executável, como Bloco de notas iniciar quando uma tarefa é registrada.

**Para agendar Bloco de notas iniciar quando uma tarefa é registrada**

1.  Crie um [**objeto TaskService.**](taskservice.md) Esse objeto permite que você crie a tarefa em uma pasta especificada.
2.  Obter uma pasta de tarefas e criar uma tarefa. Use o [**método TaskService.GetFolder**](taskservice-getfolder.md) para obter a pasta em que a tarefa está armazenada e o [**método TaskService.NewTask**](taskservice-newtask.md) para criar o [**objeto TaskDefinition**](taskdefinition.md) que representa a tarefa.
3.  Defina informações sobre a tarefa usando o [**objeto TaskDefinition.**](taskdefinition.md) Use a propriedade [**TaskDefinition.Configurações**](taskdefinition-settings.md) para definir as configurações que determinam como o serviço Agendador de Tarefas executa a tarefa e a propriedade [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) para definir as informações que descrevem a tarefa.
4.  Crie um gatilho de registro usando [**a propriedade TaskDefinition.Triggers.**](taskdefinition-triggers.md) Essa propriedade fornece acesso ao [**objeto TriggerCollection.**](triggercollection.md) Use o [**método TriggerCollection.Create**](triggercollection-create.md) (especificando o tipo de gatilho que você deseja criar) para criar um gatilho de registro.
5.  Crie uma ação para a tarefa a ser executada usando a [**propriedade TaskDefinition.Actions.**](taskdefinition-actions.md) Essa propriedade fornece acesso ao [**objeto ActionCollection.**](actioncollection.md) Use o [**método ActionCollection.Create**](actioncollection-create.md) para especificar o tipo de ação que você deseja criar. Este exemplo usa um [**objeto ExecAction,**](execaction.md) que representa uma ação que inicia um executável.
6.  Registre a tarefa usando [**o método TaskFolder.RegisterTaskDefinition.**](taskfolder-registertaskdefinition.md)

O exemplo de VBScript a seguir mostra como criar uma tarefa que agende Bloco de notas a ser executada quando a tarefa é registrada.


```VB
'---------------------------------------------------------
' This sample schedules a task to start notepad.exe when
' the task is registered.
'---------------------------------------------------------

' A constant that specifies a registration trigger.
const TriggerTypeRegistration = 7
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
regInfo.Description = "Start Notepad when the task is registered."
regInfo.Author = "Author Name"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.StartWhenAvailable = True

'********************************************************
' Create a registration trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeRegistration)

trigger.ExecutionTimeLimit = "PT5M"    'Five minutes
trigger.Id = "RegistrationTriggerId"   

'***********************************************************
' Create the action for the task to execute.

' Add an action to the task. The action executes Notepad.
Dim Action
Set Action = taskDefinition.Actions.Create( ActionTypeExecutable )
Action.Path = "C:\Windows\System32\notepad.exe"

WScript.Echo "Task definition created. About to submit the task..."

'***********************************************************
' Register (create) the task.

call rootFolder.RegisterTaskDefinition( _
    "Test Registration Trigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Agendador de Tarefas](using-the-task-scheduler.md)
</dt> </dl>

 

 




