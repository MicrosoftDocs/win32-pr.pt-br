---
title: Exemplo de gatilho de registro (script)
description: Este exemplo de script mostra como criar uma tarefa que está agendada para executar o bloco de notas quando uma tarefa é registrada.
ms.assetid: 956b3a21-7d36-4d06-be84-690884ba653a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bce6271927e74e31f25b3ac86783b35899bbd862
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292819"
---
# <a name="registration-trigger-example-scripting"></a><span data-ttu-id="38de0-103">Exemplo de gatilho de registro (script)</span><span class="sxs-lookup"><span data-stu-id="38de0-103">Registration Trigger Example (Scripting)</span></span>

<span data-ttu-id="38de0-104">Este exemplo de script mostra como criar uma tarefa que está agendada para executar o bloco de notas quando uma tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="38de0-104">This scripting example shows how to create a task that is scheduled to execute Notepad when a task is registered.</span></span> <span data-ttu-id="38de0-105">A tarefa contém um gatilho de registro que especifica um limite inicial e um limite final para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="38de0-105">The task contains a registration trigger that specifies a start boundary and an end boundary for the task.</span></span> <span data-ttu-id="38de0-106">O limite inicial especifica quando o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="38de0-106">The start boundary specifies when the trigger is activated.</span></span> <span data-ttu-id="38de0-107">A tarefa também contém uma ação que especifica a tarefa para executar o bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="38de0-107">The task also contains an action that specifies the task to execute Notepad.</span></span>

> [!Note]  
> <span data-ttu-id="38de0-108">Quando uma tarefa com um gatilho de registro é atualizada, a tarefa será executada Depois que a atualização ocorrer.</span><span class="sxs-lookup"><span data-stu-id="38de0-108">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 

<span data-ttu-id="38de0-109">O procedimento a seguir descreve como agendar um executável, como o bloco de notas, para iniciar quando uma tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="38de0-109">The following procedure describes how to schedule an executable such as Notepad to start when a task is registered.</span></span>

<span data-ttu-id="38de0-110">**Para agendar o bloco de notas para iniciar quando uma tarefa for registrada**</span><span class="sxs-lookup"><span data-stu-id="38de0-110">**To schedule Notepad to start when a task is registered**</span></span>

1.  <span data-ttu-id="38de0-111">Crie um objeto [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="38de0-111">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="38de0-112">Esse objeto permite que você crie a tarefa em uma pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="38de0-112">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="38de0-113">Obter uma pasta de tarefas e criar uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="38de0-113">Get a task folder and create a task.</span></span> <span data-ttu-id="38de0-114">Use o método [**TaskService. GetFolder**](taskservice-getfolder.md) para obter a pasta onde a tarefa está armazenada e o método [**TaskService. NewTask**](taskservice-newtask.md) para criar o objeto [**TaskDefinition**](taskdefinition.md) que representa a tarefa.</span><span class="sxs-lookup"><span data-stu-id="38de0-114">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="38de0-115">Defina informações sobre a tarefa usando o objeto [**TaskDefinition**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="38de0-115">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="38de0-116">Use a propriedade [**TaskDefinition. Settings**](taskdefinition-settings.md) para definir as configurações que determinam como o serviço de Agendador de tarefas executa a tarefa e a propriedade [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) para definir as informações que descrevem a tarefa.</span><span class="sxs-lookup"><span data-stu-id="38de0-116">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="38de0-117">Crie um gatilho de registro usando a propriedade [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="38de0-117">Create a registration trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="38de0-118">Esta propriedade fornece acesso ao objeto [**TriggerCollection**](triggercollection.md) .</span><span class="sxs-lookup"><span data-stu-id="38de0-118">This property provides access to the [**TriggerCollection**](triggercollection.md) object.</span></span> <span data-ttu-id="38de0-119">Use o método [**triggers. Create**](triggercollection-create.md) (especificando o tipo de gatilho que você deseja criar) para criar um gatilho de registro.</span><span class="sxs-lookup"><span data-stu-id="38de0-119">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger that you want to create) to create a registration trigger.</span></span>
5.  <span data-ttu-id="38de0-120">Crie uma ação para a tarefa Executar usando a propriedade [**TaskDefinition. Actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="38de0-120">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="38de0-121">Essa propriedade fornece acesso ao objeto [**ActionCollection**](actioncollection.md) .</span><span class="sxs-lookup"><span data-stu-id="38de0-121">This property provides access to the [**ActionCollection**](actioncollection.md) object.</span></span> <span data-ttu-id="38de0-122">Use o método [**ActionCollection. Create**](actioncollection-create.md) para especificar o tipo de ação que você deseja criar.</span><span class="sxs-lookup"><span data-stu-id="38de0-122">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="38de0-123">Este exemplo usa um objeto [**execaction**](execaction.md) , que representa uma ação que inicia um executável.</span><span class="sxs-lookup"><span data-stu-id="38de0-123">This example uses an [**ExecAction**](execaction.md) object, which represents an action that starts an executable.</span></span>
6.  <span data-ttu-id="38de0-124">Registre a tarefa usando o método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="38de0-124">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span>

<span data-ttu-id="38de0-125">O exemplo de VBScript a seguir mostra como criar uma tarefa que agenda o bloco de notas para ser executado quando a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="38de0-125">The following VBScript example shows how to create a task that schedules Notepad to execute when the task is registered.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="38de0-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="38de0-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38de0-127">Usando o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="38de0-127">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




