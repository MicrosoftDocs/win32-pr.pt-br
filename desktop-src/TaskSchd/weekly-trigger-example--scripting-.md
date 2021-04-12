---
title: Exemplo de gatilho semanal (script)
description: Este exemplo de script mostra como criar uma tarefa que executa o bloco de notas às 8 00 na segunda-feira de cada semana.
ms.assetid: 68ef73b0-3780-480e-90fe-940b6e8a5340
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4d9cf627591250c341008ba3a5129c4cc10cad6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363822"
---
# <a name="weekly-trigger-example-scripting"></a><span data-ttu-id="1801c-103">Exemplo de gatilho semanal (script)</span><span class="sxs-lookup"><span data-stu-id="1801c-103">Weekly Trigger Example (Scripting)</span></span>

<span data-ttu-id="1801c-104">Este exemplo de script mostra como criar uma tarefa que executa o bloco de notas às 8:00 na segunda-feira de cada semana.</span><span class="sxs-lookup"><span data-stu-id="1801c-104">This scripting example shows how to create a task that runs Notepad at 8:00 AM on Monday of every week.</span></span> <span data-ttu-id="1801c-105">A tarefa contém um gatilho diário que especifica quando a tarefa é executada e uma ação executável que executa o bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="1801c-105">The task contains a daily trigger that specifies when the task runs and an executable action that runs Notepad.</span></span>

<span data-ttu-id="1801c-106">O procedimento a seguir descreve como agendar uma tarefa para iniciar um executável às 8:00 na segunda-feira de cada semana.</span><span class="sxs-lookup"><span data-stu-id="1801c-106">The following procedure describes how to schedule a task to start an executable at 8:00 AM on Monday of every week.</span></span>

<span data-ttu-id="1801c-107">**Para agendar o bloco de notas para começar às 8:00 na segunda-feira de cada semana**</span><span class="sxs-lookup"><span data-stu-id="1801c-107">**To schedule Notepad to start at 8:00 AM on Monday of every week**</span></span>

1.  <span data-ttu-id="1801c-108">Crie um objeto [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="1801c-108">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="1801c-109">Esse objeto permite que você crie a tarefa em uma pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="1801c-109">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="1801c-110">Obter uma pasta de tarefas e criar uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="1801c-110">Get a task folder and create a task.</span></span> <span data-ttu-id="1801c-111">Use o método [**TaskService. GetFolder**](taskservice-getfolder.md) para obter a pasta onde a tarefa está armazenada e o método [**TaskService. NewTask**](taskservice-newtask.md) para criar o objeto [**TaskDefinition**](taskdefinition.md) que representa a tarefa.</span><span class="sxs-lookup"><span data-stu-id="1801c-111">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="1801c-112">Defina informações sobre a tarefa usando o objeto [**TaskDefinition**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="1801c-112">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="1801c-113">Use a propriedade [**TaskDefinition. Settings**](taskdefinition-settings.md) para definir as configurações que determinam como o serviço de Agendador de tarefas executa a tarefa e a propriedade [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) para definir as informações que descrevem a tarefa.</span><span class="sxs-lookup"><span data-stu-id="1801c-113">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="1801c-114">Crie um gatilho semanal usando a propriedade [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="1801c-114">Create a weekly trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="1801c-115">Essa propriedade fornece acesso ao objeto [**TriggerCollection**](triggercollection.md) que é usado para criar o gatilho.</span><span class="sxs-lookup"><span data-stu-id="1801c-115">This property provides access to the [**TriggerCollection**](triggercollection.md) object that is used to create the trigger.</span></span>

    <span data-ttu-id="1801c-116">Use o método [**TriggerCollection. Create**](triggercollection-create.md) (especificando o tipo de gatilho que você deseja criar) para criar um gatilho semanal.</span><span class="sxs-lookup"><span data-stu-id="1801c-116">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger you want to create) to create a weekly trigger.</span></span>

    <span data-ttu-id="1801c-117">Defina a propriedade [**WeeklyTrigger. StartBoundary**](trigger-startboundary.md) para especificar quando o gatilho é ativado e a hora do dia em que a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="1801c-117">Set the [**WeeklyTrigger.StartBoundary**](trigger-startboundary.md) property to specify when the trigger is activated and the time of the day when the task is run.</span></span> <span data-ttu-id="1801c-118">Neste exemplo, o gatilho é ativado em 1º de janeiro de 2005 e a tarefa é executada às 8:00.</span><span class="sxs-lookup"><span data-stu-id="1801c-118">In this example the trigger is activated on January 1, 2005 and the task runs at 8:00 AM.</span></span>

    <span data-ttu-id="1801c-119">Defina a propriedade [**WeeklyTrigger. Endboundal**](trigger-endboundary.md)para especificar quando o gatilho será desativado.</span><span class="sxs-lookup"><span data-stu-id="1801c-119">Set the [**WeeklyTrigger.EndBoundary**](trigger-endboundary.md)property to specify when the trigger is deactivated.</span></span> <span data-ttu-id="1801c-120">Neste exemplo, o gatilho é desativado em 1º de janeiro de 2015.</span><span class="sxs-lookup"><span data-stu-id="1801c-120">In this example the trigger is deactivated on January 1, 2015.</span></span>

    <span data-ttu-id="1801c-121">Defina a propriedade [**WeeklyTrigger. DaysOfWeek**](weeklytrigger-daysofweek.md) para especificar os dias da semana em que a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="1801c-121">Set the [**WeeklyTrigger.DaysOfWeek**](weeklytrigger-daysofweek.md) property to specify the days of the week on which the task runs.</span></span> <span data-ttu-id="1801c-122">Neste exemplo, a tarefa é executada na segunda-feira.</span><span class="sxs-lookup"><span data-stu-id="1801c-122">In this example the task is run on Monday.</span></span>

    <span data-ttu-id="1801c-123">Defina a propriedade [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md)para especificar o intervalo entre as semanas na agenda.</span><span class="sxs-lookup"><span data-stu-id="1801c-123">Set the [**WeeklyTrigger.WeeksInterval**](weeklytrigger-weeksinterval.md)property to specify the interval between the weeks in the schedule.</span></span> <span data-ttu-id="1801c-124">Neste exemplo, a tarefa é executada todas as semanas.</span><span class="sxs-lookup"><span data-stu-id="1801c-124">In this example the task runs every week.</span></span>

5.  <span data-ttu-id="1801c-125">Crie uma ação para a tarefa Executar usando a propriedade [**TaskDefinition. Actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="1801c-125">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="1801c-126">Essa propriedade fornece acesso ao objeto [**ActionCollection**](actioncollection.md) usado para criar a ação.</span><span class="sxs-lookup"><span data-stu-id="1801c-126">This property provides access to the [**ActionCollection**](actioncollection.md) object used to create the action.</span></span> <span data-ttu-id="1801c-127">Use o método [**ActionCollection. Create**](actioncollection-create.md) para especificar o tipo de ação que você deseja criar.</span><span class="sxs-lookup"><span data-stu-id="1801c-127">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action you want to create.</span></span> <span data-ttu-id="1801c-128">Este exemplo usa um objeto [**execaction**](execaction.md) , que representa uma ação que executa uma operação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="1801c-128">This example uses an [**ExecAction**](execaction.md) object, which represents an action that executes a command-line operation.</span></span>
6.  <span data-ttu-id="1801c-129">Registre a tarefa usando o método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="1801c-129">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="1801c-130">Para este exemplo, a tarefa iniciará o bloco de notas às 8:00 na segunda-feira de cada semana.</span><span class="sxs-lookup"><span data-stu-id="1801c-130">For this example the task will start Notepad at 8:00 AM on Monday of every week.</span></span>

<span data-ttu-id="1801c-131">O exemplo de VBScript a seguir mostra como agendar uma tarefa para executar o bloco de notas todos os dias às 8:00.</span><span class="sxs-lookup"><span data-stu-id="1801c-131">The following VBScript example shows how to schedule a task to execute Notepad every day at 8:00 AM.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="1801c-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1801c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1801c-133">Usando o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="1801c-133">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




