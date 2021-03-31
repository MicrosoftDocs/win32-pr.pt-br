---
title: Exemplo de gatilho diário (XML)
description: O XML neste exemplo define uma tarefa que inicia o bloco de notas às 8 00, todos os dias.
ms.assetid: b7818071-12b6-41df-85b9-282c08cf6e31
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fe673a764e6e7e4e3ae5089022da2232821d9184
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/24/2020
ms.locfileid: "103639066"
---
# <a name="daily-trigger-example-xml"></a><span data-ttu-id="7c251-103">Exemplo de gatilho diário (XML)</span><span class="sxs-lookup"><span data-stu-id="7c251-103">Daily Trigger Example (XML)</span></span>

<span data-ttu-id="7c251-104">O XML neste exemplo define uma tarefa que inicia o bloco de notas às 8:00, todos os dias.</span><span class="sxs-lookup"><span data-stu-id="7c251-104">The XML in this example defines a task that starts Notepad at 8:00 AM every day.</span></span> <span data-ttu-id="7c251-105">O exemplo também mostra como definir um padrão de repetição para o gatilho repetir a tarefa.</span><span class="sxs-lookup"><span data-stu-id="7c251-105">The example also shows how to set a repetition pattern for the trigger to repeat the task.</span></span>

<span data-ttu-id="7c251-106">Para registrar uma tarefa que é definida em XML, você pode usar a função [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) para scripts) ou a ferramenta de linha de comando Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="7c251-106">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="7c251-107">Se você usar a ferramenta de Schtasks.exe (localizada no diretório C: \\ Windows \\ System32), poderá usar o comando a seguir para registrar a tarefa: **SCHTASKS/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="7c251-107">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-every-day-at-800-am"></a><span data-ttu-id="7c251-108">Para definir uma tarefa para iniciar o bloco de notas todos os dias às 8:00</span><span class="sxs-lookup"><span data-stu-id="7c251-108">To define a task to start Notepad every day at 8:00 AM</span></span>

<span data-ttu-id="7c251-109">O exemplo de XML a seguir mostra como definir uma tarefa com uma única ação de execução (iniciando o bloco de notas), um único gatilho de calendário (inicia a tarefa todos os dias às 8:00 AM) e várias outras configurações de tarefa que afetam o modo como a tarefa é manipulada pelo Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="7c251-109">The following XML example shows how to define a task with a single execution action (starting Notepad), a single calendar trigger (starts the task every day at 8:00 AM), and several other task settings that affect how the task is handled by Task Scheduler.</span></span>


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start on a daily basis.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Notepad starts every day.</Description>
    </RegistrationInfo>
    <Triggers>
        <CalendarTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Repetition>
                <Interval>PT1M</Interval>
                <Duration>PT4M</Duration>
            </Repetition>
            <ScheduleByDay>
                <DaysInterval>1</DaysInterval>
            </ScheduleByDay>
        </CalendarTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <UserId>Administrator</UserId>
            <LogonType>InteractiveToken</LogonType>
        </Principal>
    </Principals>
    <Settings>
        <Enabled>true</Enabled>
        <AllowStartOnDemand>true</AllowStartOnDemand>
        <AllowHardTerminate>true</AllowHardTerminate>
    </Settings>
    <Actions>
        <Exec>
            <Command>notepad.exe</Command>
        </Exec>
    </Actions>
</Task>
```



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="7c251-110">Elementos do esquema TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="7c251-110">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="7c251-111">Aqui estão alguns elementos importantes para ter em mente ao usar este exemplo.</span><span class="sxs-lookup"><span data-stu-id="7c251-111">Here are some important elements to keep in mind when using this example.</span></span>

-   [<span data-ttu-id="7c251-112">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="7c251-112">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md)

    <span data-ttu-id="7c251-113">Contém informações de registro sobre a tarefa.</span><span class="sxs-lookup"><span data-stu-id="7c251-113">Contains registration information about the task.</span></span>

-   [<span data-ttu-id="7c251-114">**Gatilhos**</span><span class="sxs-lookup"><span data-stu-id="7c251-114">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)

    <span data-ttu-id="7c251-115">Define o gatilho que inicia a tarefa.</span><span class="sxs-lookup"><span data-stu-id="7c251-115">Defines the trigger that starts the task.</span></span>

-   [<span data-ttu-id="7c251-116">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="7c251-116">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)

    <span data-ttu-id="7c251-117">Define o gatilho de calendário diário.</span><span class="sxs-lookup"><span data-stu-id="7c251-117">Defines the daily calendar trigger.</span></span> <span data-ttu-id="7c251-118">Nesse caso, quatro elementos filho são usados: os limites inicial e final que especificam quando o gatilho é ativado e desativado, o agendamento diário e o padrão de repetição para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="7c251-118">In this case, four child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, the daily schedule, and the repetition pattern for the task.</span></span> <span data-ttu-id="7c251-119">O elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) é um elemento necessário para gatilhos de calendário.</span><span class="sxs-lookup"><span data-stu-id="7c251-119">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for calendar triggers.</span></span>

-   [<span data-ttu-id="7c251-120">**ScheduleByDay**</span><span class="sxs-lookup"><span data-stu-id="7c251-120">**ScheduleByDay**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md)

    <span data-ttu-id="7c251-121">Define o agendamento diário.</span><span class="sxs-lookup"><span data-stu-id="7c251-121">Defines the daily schedule.</span></span> <span data-ttu-id="7c251-122">Nesse caso, o intervalo é definido para executar a tarefa todos os dias.</span><span class="sxs-lookup"><span data-stu-id="7c251-122">In this case, the interval is set to perform the task every day.</span></span>

-   <span data-ttu-id="7c251-123">[**Principal**](taskschedulerschema-principal-principaltype-element.md): define o contexto de segurança em que uma tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="7c251-123">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   [<span data-ttu-id="7c251-124">**Settings**</span><span class="sxs-lookup"><span data-stu-id="7c251-124">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)

    <span data-ttu-id="7c251-125">Define as configurações de tarefa que Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="7c251-125">Defines the task settings that Task Scheduler uses to perform the task.</span></span>

-   [<span data-ttu-id="7c251-126">**Ações**</span><span class="sxs-lookup"><span data-stu-id="7c251-126">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)

    <span data-ttu-id="7c251-127">Define as ações que a tarefa executa (nesse caso, executando o bloco de notas).</span><span class="sxs-lookup"><span data-stu-id="7c251-127">Defines the actions the task performs (in this case, running Notepad).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c251-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7c251-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c251-129">Usando o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="7c251-129">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




