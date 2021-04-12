---
title: Exemplo de gatilho semanal (XML)
description: O XML neste exemplo define uma tarefa que inicia o bloco de notas em uma base quinzenal.
ms.assetid: 1911e8b1-2583-440c-a6ed-d71080b60987
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf8c2683311aecc427e9570a0452c746375eca01
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/24/2020
ms.locfileid: "104365424"
---
# <a name="weekly-trigger-example-xml"></a><span data-ttu-id="63379-103">Exemplo de gatilho semanal (XML)</span><span class="sxs-lookup"><span data-stu-id="63379-103">Weekly Trigger Example (XML)</span></span>

<span data-ttu-id="63379-104">O XML neste exemplo define uma tarefa que inicia o bloco de notas em uma base quinzenal.</span><span class="sxs-lookup"><span data-stu-id="63379-104">The XML in this example defines a task that starts Notepad on a bi-weekly basis.</span></span>

<span data-ttu-id="63379-105">Para registrar uma tarefa que é definida em XML, você pode usar a função [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) para scripts) ou a ferramenta de linha de comando Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="63379-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="63379-106">Se você usar a ferramenta de Schtasks.exe (localizada no diretório C: \\ Windows \\ System32), poderá usar o comando a seguir para registrar a tarefa: **SCHTASKS/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="63379-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-every-other-week-on-monday-at-800-am"></a><span data-ttu-id="63379-107">Para definir uma tarefa para iniciar o bloco de notas a cada outra semana na segunda-feira às 8:00</span><span class="sxs-lookup"><span data-stu-id="63379-107">To define a task to start Notepad every other week on Monday at 8:00 AM</span></span>

<span data-ttu-id="63379-108">O exemplo de XML a seguir mostra como definir uma tarefa com uma única ação de execução (iniciando o bloco de notas), um único gatilho de calendário (inicia a tarefa a cada outra semana na segunda-feira às 8:00 AM) e várias outras configurações de tarefa que afetam o modo como a tarefa é manipulada pelo Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="63379-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single calendar trigger (starts the task every other week on Monday at 8:00 AM), and several other task settings that affect how the task is handled by Task Scheduler.</span></span>


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start on a bi-weekly basis.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-05-01T09:00:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Notepad starts every other week on Monday at 8:00am.</Description>
    </RegistrationInfo>
    <Triggers>
        <CalendarTrigger>
            <StartBoundary>2005-05-02T08:00:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00</EndBoundary>
            <ScheduleByWeek>
                <WeeksInterval>2</WeeksInterval>
                <DaysOfWeek>
                    <Monday/>
                </DaysOfWeek>
            </ScheduleByWeek>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="63379-109">Elementos do esquema TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="63379-109">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="63379-110">Aqui estão alguns elementos importantes para ter em mente ao usar este exemplo.</span><span class="sxs-lookup"><span data-stu-id="63379-110">Here are some important elements to keep in mind when using this example.</span></span>

-   [<span data-ttu-id="63379-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="63379-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md)

    <span data-ttu-id="63379-112">Contém informações de registro sobre a tarefa.</span><span class="sxs-lookup"><span data-stu-id="63379-112">Contains registration information about the task.</span></span>

-   [<span data-ttu-id="63379-113">**Gatilhos**</span><span class="sxs-lookup"><span data-stu-id="63379-113">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)

    <span data-ttu-id="63379-114">Define o gatilho que inicia a tarefa.</span><span class="sxs-lookup"><span data-stu-id="63379-114">Defines the trigger that starts the task.</span></span>

-   [<span data-ttu-id="63379-115">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="63379-115">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)

    <span data-ttu-id="63379-116">Define o gatilho de calendário semanal.</span><span class="sxs-lookup"><span data-stu-id="63379-116">Defines the weekly calendar trigger.</span></span> <span data-ttu-id="63379-117">Nesse caso, somente quatro elementos filho são usados: os limites inicial e final que especificam quando o gatilho é ativado e desativado, o agendamento semanal e os dias da semana em que a tarefa será executada.</span><span class="sxs-lookup"><span data-stu-id="63379-117">In this case, only four child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, the weekly schedule, and the days of the week that the task will run on.</span></span> <span data-ttu-id="63379-118">O elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) é um elemento necessário para gatilhos de calendário.</span><span class="sxs-lookup"><span data-stu-id="63379-118">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for calendar triggers.</span></span>

-   [<span data-ttu-id="63379-119">**ScheduleByWeek**</span><span class="sxs-lookup"><span data-stu-id="63379-119">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)

    <span data-ttu-id="63379-120">Define o agendamento semanal.</span><span class="sxs-lookup"><span data-stu-id="63379-120">Defines the weekly schedule.</span></span> <span data-ttu-id="63379-121">Nesse caso, o intervalo é definido para executar a tarefa a cada segunda semana em uma segunda-feira.</span><span class="sxs-lookup"><span data-stu-id="63379-121">In this case, the interval is set to perform the task every other week on a Monday.</span></span>

-   [<span data-ttu-id="63379-122">**Beneficiário**</span><span class="sxs-lookup"><span data-stu-id="63379-122">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md)

    <span data-ttu-id="63379-123">Define o contexto de segurança em que uma tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="63379-123">Defines the security context that a task runs under.</span></span>

-   [<span data-ttu-id="63379-124">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="63379-124">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)

    <span data-ttu-id="63379-125">Define as configurações de tarefa que Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="63379-125">Defines the task settings that Task Scheduler uses to perform the task.</span></span>

-   [<span data-ttu-id="63379-126">**Ações**</span><span class="sxs-lookup"><span data-stu-id="63379-126">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)

    <span data-ttu-id="63379-127">Define as ações que a tarefa executa (nesse caso, executando o bloco de notas).</span><span class="sxs-lookup"><span data-stu-id="63379-127">Defines the actions the task performs (in this case, running Notepad).</span></span>

## <a name="related-topics"></a><span data-ttu-id="63379-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="63379-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63379-129">Usando o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="63379-129">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




