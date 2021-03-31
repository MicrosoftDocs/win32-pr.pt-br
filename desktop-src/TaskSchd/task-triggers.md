---
title: Gatilhos de tarefa
description: Um gatilho é um conjunto de critérios que, quando atendidos, inicia a execução de uma tarefa.
ms.assetid: 8b4dff8b-9dc3-4856-aed6-648588a089be
keywords:
- Criando gatilhos Agendador de Tarefas
- Agendador de Tarefas de gatilhos
- disparadores Agendador de Tarefas, descritos
- gatilhos Agendador de Tarefas, com base no tempo
- disparadores Agendador de Tarefas, baseado em evento
- gatilhos baseados em evento Agendador de Tarefas
- gatilhos baseados em tempo Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d465dfa015be19ff220a77d3c85f0cbb223c4899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159457"
---
# <a name="task-triggers"></a><span data-ttu-id="e4f83-110">Gatilhos de tarefa</span><span class="sxs-lookup"><span data-stu-id="e4f83-110">Task Triggers</span></span>

<span data-ttu-id="e4f83-111">Um gatilho é um conjunto de critérios que, quando atendidos, inicia a execução de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="e4f83-111">A trigger is a set of criteria that, when met, starts the execution of a task.</span></span> <span data-ttu-id="e4f83-112">O Agendador de Tarefas fornece gatilhos baseados em tempo e em eventos que podem iniciar uma tarefa de várias maneiras diferentes.</span><span class="sxs-lookup"><span data-stu-id="e4f83-112">Task Scheduler provides both time-based and event-based triggers that can start a task in several different ways.</span></span> <span data-ttu-id="e4f83-113">Uma determinada tarefa pode ser iniciada por um ou mais gatilhos.</span><span class="sxs-lookup"><span data-stu-id="e4f83-113">A given task can be started by one or more triggers.</span></span> <span data-ttu-id="e4f83-114">Uma tarefa pode ter um máximo de 48 gatilhos.</span><span class="sxs-lookup"><span data-stu-id="e4f83-114">A task can have a maximum of 48 triggers.</span></span>

## <a name="time-based-triggers"></a><span data-ttu-id="e4f83-115">Gatilhos baseados em tempo</span><span class="sxs-lookup"><span data-stu-id="e4f83-115">Time-based Triggers</span></span>

<span data-ttu-id="e4f83-116">Os gatilhos baseados em tempo iniciam as tarefas em horários especificados.</span><span class="sxs-lookup"><span data-stu-id="e4f83-116">Time-based triggers start tasks at specified times.</span></span> <span data-ttu-id="e4f83-117">Isso inclui iniciar a tarefa uma vez em um momento específico ou iniciar a tarefa várias vezes em uma agenda diária, semanal, mensal ou mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="e4f83-117">This includes starting the task once at a specific time or starting the task multiple times on a daily, weekly, monthly, or monthly day-of-week schedule.</span></span>

## <a name="event-based-triggers"></a><span data-ttu-id="e4f83-118">Gatilhos baseados em evento</span><span class="sxs-lookup"><span data-stu-id="e4f83-118">Event-based Triggers</span></span>

<span data-ttu-id="e4f83-119">Os gatilhos baseados em evento iniciam uma tarefa em resposta a determinados eventos do sistema.</span><span class="sxs-lookup"><span data-stu-id="e4f83-119">Event-based triggers start a task in response to certain system events.</span></span> <span data-ttu-id="e4f83-120">Por exemplo, os gatilhos baseados em evento podem ser definidos para iniciar uma tarefa quando o sistema é iniciado, quando um usuário faz logon no computador local ou quando o sistema se torna ocioso.</span><span class="sxs-lookup"><span data-stu-id="e4f83-120">For example, event-based triggers can be set to start a task when the system starts up, when a user logs on to the local computer, or when the system becomes idle.</span></span>

## <a name="multiple-triggers"></a><span data-ttu-id="e4f83-121">Vários gatilhos</span><span class="sxs-lookup"><span data-stu-id="e4f83-121">Multiple Triggers</span></span>

<span data-ttu-id="e4f83-122">Cada tarefa pode ser iniciada por um ou mais gatilhos, permitindo que a tarefa seja iniciada de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="e4f83-122">Each task can be started by one or more triggers, allowing the task to be started in any number of ways.</span></span> <span data-ttu-id="e4f83-123">No entanto, vários gatilhos são implementados de forma diferente em Agendador de Tarefas 1,0 e Agendador de Tarefas 2,0.</span><span class="sxs-lookup"><span data-stu-id="e4f83-123">However, multiple triggers are implemented differently in Task Scheduler 1.0 and Task Scheduler 2.0.</span></span>

<span data-ttu-id="e4f83-124">No Agendador de Tarefas 2,0, cada gatilho é definido por uma API de gatilho separada que está associada à tarefa por meio da coleção de gatilhos.</span><span class="sxs-lookup"><span data-stu-id="e4f83-124">In Task Scheduler 2.0, each trigger is defined by a separate trigger API that is associated with the task through the trigger collection.</span></span>

<span data-ttu-id="e4f83-125">No Agendador de Tarefas 1,0, vários gatilhos podem ser considerados como um agendamento, um conjunto de vezes em que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="e4f83-125">In Task Scheduler 1.0, multiple triggers can be thought of as a schedule, a set of times at which the task starts.</span></span> <span data-ttu-id="e4f83-126">Nesse caso, o agendamento é o conjunto de vezes (especificado pela União de todos os gatilhos associados ao item de trabalho) no qual um item de trabalho será executado.</span><span class="sxs-lookup"><span data-stu-id="e4f83-126">In this case, the schedule is the set of times (specified by the union of all of the triggers associated with the work item) at which a work item will execute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4f83-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e4f83-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4f83-128">Repetindo uma tarefa</span><span class="sxs-lookup"><span data-stu-id="e4f83-128">Repeating A Task</span></span>](repeating-a-task.md)
</dt> <dt>

[<span data-ttu-id="e4f83-129">Tipos de gatilho</span><span class="sxs-lookup"><span data-stu-id="e4f83-129">Trigger Types</span></span>](trigger-types.md)
</dt> <dt>

[<span data-ttu-id="e4f83-130">Interfaces de gatilho</span><span class="sxs-lookup"><span data-stu-id="e4f83-130">Trigger Interfaces</span></span>](trigger-interfaces.md)
</dt> <dt>

[<span data-ttu-id="e4f83-131">Sobre o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="e4f83-131">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 




