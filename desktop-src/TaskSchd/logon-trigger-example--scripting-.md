---
title: Exemplo de gatilho de logon (script)
description: Este exemplo de script mostra como criar uma tarefa que está agendada para executar o bloco de notas quando um usuário faz logon.
ms.assetid: f25e105f-9439-4646-bdfd-609ee99a5d55
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72a8c4b5d0d67b59160eb3ed0b13885ee7e0eb51
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159589"
---
# <a name="logon-trigger-example-scripting"></a><span data-ttu-id="77aae-103">Exemplo de gatilho de logon (script)</span><span class="sxs-lookup"><span data-stu-id="77aae-103">Logon Trigger Example (Scripting)</span></span>

<span data-ttu-id="77aae-104">Este exemplo de script mostra como criar uma tarefa que está agendada para executar o bloco de notas quando um usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="77aae-104">This scripting example shows how to create a task that is scheduled to execute Notepad when a user logs on.</span></span> <span data-ttu-id="77aae-105">A tarefa contém um gatilho de logon que especifica um limite inicial para a tarefa iniciar e um identificador de usuário que especifica o usuário.</span><span class="sxs-lookup"><span data-stu-id="77aae-105">The task contains a logon trigger that specifies a start boundary for the task to start and a user identifier that specifies the user.</span></span> <span data-ttu-id="77aae-106">A tarefa é registrada usando o grupo Administradores como um contexto de segurança para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="77aae-106">The task is registered using the Administrators group as a security context to run the task.</span></span>

<span data-ttu-id="77aae-107">O procedimento a seguir descreve como agendar um executável, como o bloco de notas, para iniciar quando um usuário especificado fizer logon.</span><span class="sxs-lookup"><span data-stu-id="77aae-107">The following procedure describes how to schedule an executable such as Notepad to start when a specified user logs on.</span></span>

<span data-ttu-id="77aae-108">**Para agendar o bloco de notas para iniciar quando um usuário fizer logon**</span><span class="sxs-lookup"><span data-stu-id="77aae-108">**To schedule Notepad to start when a user logs on**</span></span>

1.  <span data-ttu-id="77aae-109">Crie um objeto [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="77aae-109">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="77aae-110">Esse objeto permite que você crie a tarefa em uma pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="77aae-110">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="77aae-111">Obter uma pasta de tarefas e criar uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="77aae-111">Get a task folder and create a task.</span></span> <span data-ttu-id="77aae-112">Use o método [**TaskService. GetFolder**](taskservice-getfolder.md) para obter a pasta onde a tarefa está armazenada e o método [**TaskService. NewTask**](taskservice-newtask.md) para criar o objeto [**TaskDefinition**](taskdefinition.md) que representa a tarefa.</span><span class="sxs-lookup"><span data-stu-id="77aae-112">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="77aae-113">Defina informações sobre a tarefa usando o objeto [**TaskDefinition**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="77aae-113">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="77aae-114">Use a propriedade [**TaskDefinition. Settings**](taskdefinition-settings.md) para definir as configurações que determinam como o serviço de Agendador de tarefas executa a tarefa e a propriedade [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) para definir as informações que descrevem a tarefa.</span><span class="sxs-lookup"><span data-stu-id="77aae-114">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="77aae-115">Crie um gatilho de logon usando a propriedade [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="77aae-115">Create a logon trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="77aae-116">Esta propriedade fornece acesso ao objeto [**TriggerCollection**](triggercollection.md) .</span><span class="sxs-lookup"><span data-stu-id="77aae-116">This property provides access to the [**TriggerCollection**](triggercollection.md) object.</span></span> <span data-ttu-id="77aae-117">Use o método [**TriggerCollection. Create**](triggercollection-create.md) (especificando o tipo de gatilho que você deseja criar) para criar um gatilho de logon.</span><span class="sxs-lookup"><span data-stu-id="77aae-117">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger that you want to create) to create a logon trigger.</span></span> <span data-ttu-id="77aae-118">Ao criar o gatilho, defina o limite inicial e o limite final do gatilho para ativar e desativar o gatilho.</span><span class="sxs-lookup"><span data-stu-id="77aae-118">As you create the trigger, set the start boundary and end boundary of the trigger to activate and deactivate the trigger.</span></span> <span data-ttu-id="77aae-119">Você deve definir a propriedade [**userid**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) para o gatilho para que as ações da tarefa sejam agendadas para execução quando o usuário especificado fizer logon após o limite inicial.</span><span class="sxs-lookup"><span data-stu-id="77aae-119">You must set the [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) property for the trigger so that the task's actions will be scheduled to execute when the specified user logs on after the start boundary.</span></span>
5.  <span data-ttu-id="77aae-120">Crie uma ação para a tarefa Executar usando a propriedade [**TaskDefinition. Actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="77aae-120">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="77aae-121">Essa propriedade fornece acesso ao objeto [**ActionCollection**](actioncollection.md) .</span><span class="sxs-lookup"><span data-stu-id="77aae-121">This property provides access to the [**ActionCollection**](actioncollection.md) object.</span></span> <span data-ttu-id="77aae-122">Use o método [**ActionCollection. Create**](actioncollection-create.md) para especificar o tipo de ação que você deseja criar.</span><span class="sxs-lookup"><span data-stu-id="77aae-122">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="77aae-123">Este exemplo usa um objeto [**execaction**](execaction.md) , que representa uma ação que inicia um executável.</span><span class="sxs-lookup"><span data-stu-id="77aae-123">This example uses an [**ExecAction**](execaction.md) object, which represents an action that starts an executable.</span></span>
6.  <span data-ttu-id="77aae-124">Registre a tarefa usando o método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="77aae-124">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="77aae-125">Este exemplo registra a tarefa para que ela use o grupo Administradores como um contexto de segurança para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="77aae-125">This example registers the task so that it uses the Administrators group as a security context to run the task.</span></span>

<span data-ttu-id="77aae-126">O exemplo de VBScript a seguir mostra como agendar uma tarefa para executar o bloco de notas quando um usuário fizer logon.</span><span class="sxs-lookup"><span data-stu-id="77aae-126">The following VBScript example shows how to schedule a task to execute Notepad when a user logs on.</span></span>


```VB
'---------------------------------------------------------
' This sample schedules a task to start notepad.exe when a user logs on.
'---------------------------------------------------------

' A constant that specifies a logon trigger.
const TriggerTypeLogon = 9
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
regInfo.Description = "Task will execute Notepad when a " & _
    "specified user logs on."
regInfo.Author = "Author Name"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.StartWhenAvailable = True

'********************************************************
' Create a logon trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeLogon)

' Trigger variables that define when the trigger is active.
Dim startTime, endTime
startTime = "2006-05-02T10:49:02"
endTime = "2006-05-02T10:52:02"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.ExecutionTimeLimit = "PT5M"    ' Five minutes
trigger.Id = "LogonTriggerId"
trigger.UserId = "DOMAIN\UserName"   ' Must be a valid user account   

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
    "Test Logon Trigger", taskDefinition, createOrUpdateTask, _
    "Builtin\Administrators", , 4)

WScript.Echo "Task submitted."
```



## <a name="related-topics"></a><span data-ttu-id="77aae-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="77aae-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77aae-128">Usando o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="77aae-128">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




