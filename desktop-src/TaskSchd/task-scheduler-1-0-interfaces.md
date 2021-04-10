---
title: Interfaces Agendador de Tarefas 1,0
description: As interfaces descritas nos tópicos a seguir fornecem acesso programático à funcionalidade que está disponível no Agendador de Tarefas usado nos sistemas operacionais Windows 2000, Windows XP e Windows Server 2003.
ms.assetid: 25f9c1ad-1859-4788-a876-6f4faa6e556e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bab12b59d4b4561ecbe46c09a76c69209574c9d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104162959"
---
# <a name="task-scheduler-10-interfaces"></a><span data-ttu-id="e27d7-103">Interfaces Agendador de Tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="e27d7-103">Task Scheduler 1.0 Interfaces</span></span>

<span data-ttu-id="e27d7-104">\[\[Essa API pode ser alterada ou não estar disponível nas versões subsequentes do sistema operacional ou produto.</span><span class="sxs-lookup"><span data-stu-id="e27d7-104">\[\[This API may be altered or unavailable in subsequent versions of the operating system or product.</span></span> <span data-ttu-id="e27d7-105">Use as [Interfaces Agendador de Tarefas 2,0](task-scheduler-2-0-interfaces.md) ou [Agendador de tarefas tipos enumerados 2,0](task-scheduler-2-0-enumerated-types.md) em vez disso. \]\]</span><span class="sxs-lookup"><span data-stu-id="e27d7-105">Please use the [Task Scheduler 2.0 Interfaces](task-scheduler-2-0-interfaces.md) or [Task Scheduler 2.0 Enumerated Types](task-scheduler-2-0-enumerated-types.md) instead.\] \]</span></span>

<span data-ttu-id="e27d7-106">As interfaces descritas nos tópicos a seguir fornecem acesso programático à funcionalidade que está disponível no Agendador de Tarefas usado nos sistemas operacionais Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e27d7-106">The interfaces that are described in the following topics provide programmatic access to the functionality that is available within the Task Scheduler that is used in the Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="e27d7-107">Esses tópicos contêm uma descrição da interface, uma lista das propriedades e dos métodos definidos pela interface e comentários sobre as circunstâncias especiais que devem ser observadas ao usar a interface.</span><span class="sxs-lookup"><span data-stu-id="e27d7-107">These topics contain a description of the interface, a list of the properties and methods defined by the interface, and remarks about any special circumstances that should be noted when using the interface.</span></span>


<span data-ttu-id="e27d7-108">As interfaces a seguir são introduzidas por Agendador de Tarefas 1,0.</span><span class="sxs-lookup"><span data-stu-id="e27d7-108">The following interfaces are introduced by Task Scheduler 1.0.</span></span>



| <span data-ttu-id="e27d7-109">Interface</span><span class="sxs-lookup"><span data-stu-id="e27d7-109">Interface</span></span>                                        | <span data-ttu-id="e27d7-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e27d7-110">Description</span></span>                                                                                                                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e27d7-111">**IEnumWorkItems**</span><span class="sxs-lookup"><span data-stu-id="e27d7-111">**IEnumWorkItems**</span></span>](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems)         | <span data-ttu-id="e27d7-112">Fornece os métodos para enumerar as tarefas na [*pasta tarefas agendadas*](s.md).</span><span class="sxs-lookup"><span data-stu-id="e27d7-112">Provides the methods for enumerating the tasks in the [*Scheduled Tasks folder*](s.md).</span></span>                                                                                                              |
| [<span data-ttu-id="e27d7-113">**IProvideTaskPage**</span><span class="sxs-lookup"><span data-stu-id="e27d7-113">**IProvideTaskPage**</span></span>](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage)     | <span data-ttu-id="e27d7-114">Fornece os métodos para acessar as configurações de folha de propriedades de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="e27d7-114">Provides the methods to access the property sheet settings of a task.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="e27d7-115">**IScheduledWorkItem**</span><span class="sxs-lookup"><span data-stu-id="e27d7-115">**IScheduledWorkItem**</span></span>](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) | <span data-ttu-id="e27d7-116">Fornece os métodos para gerenciar [*itens de trabalho*](w.md)específicos.</span><span class="sxs-lookup"><span data-stu-id="e27d7-116">Provides the methods for managing specific [*work items*](w.md).</span></span>                                                                                                                                                 |
| [<span data-ttu-id="e27d7-117">**ITask**</span><span class="sxs-lookup"><span data-stu-id="e27d7-117">**ITask**</span></span>](/windows/desktop/api/Mstask/nn-mstask-itask)                           | <span data-ttu-id="e27d7-118">Fornece os métodos para executar tarefas, obter ou definir informações de tarefas e finalizar tarefas.</span><span class="sxs-lookup"><span data-stu-id="e27d7-118">Provides the methods for running tasks, getting or setting task information, and terminating tasks.</span></span> <span data-ttu-id="e27d7-119">Ele é derivado da interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) e herda todos os métodos dessa interface.</span><span class="sxs-lookup"><span data-stu-id="e27d7-119">It is derived from the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface and inherits all the methods of that interface.</span></span> |
| [<span data-ttu-id="e27d7-120">**ITaskScheduler**</span><span class="sxs-lookup"><span data-stu-id="e27d7-120">**ITaskScheduler**</span></span>](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler)         | <span data-ttu-id="e27d7-121">Fornece os métodos para agendar tarefas.</span><span class="sxs-lookup"><span data-stu-id="e27d7-121">Provides the methods for scheduling tasks.</span></span>                                                                                                                                                                                            |
| [<span data-ttu-id="e27d7-122">**ITaskTrigger**</span><span class="sxs-lookup"><span data-stu-id="e27d7-122">**ITaskTrigger**</span></span>](/windows/desktop/api/Mstask/nn-mstask-itasktrigger)             | <span data-ttu-id="e27d7-123">Fornece os métodos para acessar e definir gatilhos para uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="e27d7-123">Provides the methods for accessing and setting triggers for a task.</span></span> <span data-ttu-id="e27d7-124">Os gatilhos especificam os horários de início da tarefa, os critérios de repetição e outros parâmetros que controlam quando uma tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="e27d7-124">Triggers specify task start times, repetition criteria, and other parameters that control when a task is run.</span></span>                                                     |



 

 

 




