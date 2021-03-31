---
title: Exemplo de gatilho diário (script)
description: Este exemplo de script mostra como criar uma tarefa que executa o bloco de notas às 8 00, todos os dias.
ms.assetid: a13bd54d-b45a-46e5-8281-d080f50f6bef
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3399934786e1cd0f95ca020c92027ccafafa5272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822541"
---
# <a name="daily-trigger-example-scripting"></a><span data-ttu-id="edd5c-103">Exemplo de gatilho diário (script)</span><span class="sxs-lookup"><span data-stu-id="edd5c-103">Daily Trigger Example (Scripting)</span></span>

<span data-ttu-id="edd5c-104">Este exemplo de script mostra como criar uma tarefa que executa o bloco de notas às 8:00, todos os dias.</span><span class="sxs-lookup"><span data-stu-id="edd5c-104">This scripting example shows how to create a task that runs Notepad at 8:00 AM every day.</span></span> <span data-ttu-id="edd5c-105">A tarefa contém um gatilho diário que especifica um limite inicial para ativar o gatilho e especificar a hora do dia em que a tarefa é executada, um intervalo de gatilho para especificar que a tarefa é executada todos os dias e um limite final para desativar o gatilho.</span><span class="sxs-lookup"><span data-stu-id="edd5c-105">The task contains a daily trigger that specifies a start boundary to activate the trigger and to specify the time of day that the task runs, a trigger interval to specify that the task runs every day, and an end boundary to deactivates the trigger.</span></span> <span data-ttu-id="edd5c-106">O exemplo também mostra como definir um padrão de repetição para o gatilho repetir a tarefa.</span><span class="sxs-lookup"><span data-stu-id="edd5c-106">The example also shows how to set a repetition pattern for the trigger to repeat the task.</span></span> <span data-ttu-id="edd5c-107">A tarefa também contém uma ação executável que executa o bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="edd5c-107">The task also contains an executable action that runs Notepad.</span></span>

<span data-ttu-id="edd5c-108">O procedimento a seguir descreve como agendar uma tarefa para iniciar um executável às 8:00, todos os dias.</span><span class="sxs-lookup"><span data-stu-id="edd5c-108">The following procedure describes how to schedule a task to start an executable at 8:00 AM every day.</span></span> <span data-ttu-id="edd5c-109">(Essas etapas correspondem aos comentários de código incluídos no código de exemplo.)</span><span class="sxs-lookup"><span data-stu-id="edd5c-109">(These steps correspond to the code comments included in the example code.)</span></span>

<span data-ttu-id="edd5c-110">**Para agendar o bloco de notas para começar às 8:00, todos os dias**</span><span class="sxs-lookup"><span data-stu-id="edd5c-110">**To schedule Notepad to start at 8:00 AM every day**</span></span>

1.  <span data-ttu-id="edd5c-111">Crie um objeto [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="edd5c-111">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="edd5c-112">Esse objeto permite que você crie a tarefa em uma pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="edd5c-112">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="edd5c-113">Obter uma pasta de tarefas e criar uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="edd5c-113">Get a task folder and create a task.</span></span> <span data-ttu-id="edd5c-114">Use o método [**TaskService. GetFolder**](taskservice-getfolder.md) para obter a pasta onde a tarefa está armazenada e o método [**TaskService. NewTask**](taskservice-newtask.md) para criar o objeto [**TaskDefinition**](taskdefinition.md) que representa a tarefa.</span><span class="sxs-lookup"><span data-stu-id="edd5c-114">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="edd5c-115">Defina informações sobre a tarefa usando o objeto [**TaskDefinition**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="edd5c-115">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="edd5c-116">Use a propriedade [**TaskDefinition. Settings**](taskdefinition-settings.md) para definir as configurações que determinam como o serviço de Agendador de tarefas executa a tarefa e a propriedade [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) para definir as informações que descrevem a tarefa.</span><span class="sxs-lookup"><span data-stu-id="edd5c-116">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="edd5c-117">Crie um gatilho diário usando a propriedade [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="edd5c-117">Create a daily trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="edd5c-118">Essa propriedade fornece acesso ao objeto [**TriggerCollection**](triggercollection.md) que é usado para criar o gatilho.</span><span class="sxs-lookup"><span data-stu-id="edd5c-118">This property provides access to the [**TriggerCollection**](triggercollection.md) object that is used to create the trigger.</span></span> <span data-ttu-id="edd5c-119">Use o método [**TriggerCollection. Create**](triggercollection-create.md) (especificando o tipo de gatilho que você deseja criar) para criar um gatilho diário.</span><span class="sxs-lookup"><span data-stu-id="edd5c-119">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger you want to create) to create a daily trigger.</span></span> <span data-ttu-id="edd5c-120">Ao criar o gatilho, defina o limite inicial para ativar o gatilho e especifique a hora do dia em que a tarefa é executada, o intervalo entre os dias e o limite final para desativar o gatilho.</span><span class="sxs-lookup"><span data-stu-id="edd5c-120">As you create the trigger, set the start boundary to activate the trigger and specify the time of day that the task runs, the interval between the days, and the end boundary to deactivate the trigger.</span></span> <span data-ttu-id="edd5c-121">O exemplo a seguir mostra como definir um padrão de repetição para o gatilho repetir a tarefa.</span><span class="sxs-lookup"><span data-stu-id="edd5c-121">The example below shows how to set a repetition pattern for the trigger to repeat the task.</span></span>
5.  <span data-ttu-id="edd5c-122">Crie uma ação para a tarefa Executar usando a propriedade [**TaskDefinition. Actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="edd5c-122">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="edd5c-123">Essa propriedade fornece acesso ao objeto [**ActionCollection**](actioncollection.md) usado para criar a ação.</span><span class="sxs-lookup"><span data-stu-id="edd5c-123">This property provides access to the [**ActionCollection**](actioncollection.md) object used to create the action.</span></span> <span data-ttu-id="edd5c-124">Use o método [**ActionCollection. Create**](actioncollection-create.md) para especificar o tipo de ação que você deseja criar.</span><span class="sxs-lookup"><span data-stu-id="edd5c-124">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action you want to create.</span></span> <span data-ttu-id="edd5c-125">Este exemplo usa um objeto [**execaction**](execaction.md) , que representa uma ação que executa uma operação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="edd5c-125">This example uses an [**ExecAction**](execaction.md) object, which represents an action that executes a command-line operation.</span></span>
6.  <span data-ttu-id="edd5c-126">Registre a tarefa usando o método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="edd5c-126">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="edd5c-127">Para este exemplo, a tarefa iniciará o bloco de notas às 8:00, todos os dias.</span><span class="sxs-lookup"><span data-stu-id="edd5c-127">For this example the task will start Notepad at 8:00 AM every day.</span></span>

<span data-ttu-id="edd5c-128">O exemplo de VBScript a seguir mostra como agendar uma tarefa para executar o bloco de notas todos os dias às 8:00.</span><span class="sxs-lookup"><span data-stu-id="edd5c-128">The following VBScript example shows how to schedule a task to execute Notepad every day at 8:00 AM.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="edd5c-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="edd5c-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edd5c-130">Usando o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="edd5c-130">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




