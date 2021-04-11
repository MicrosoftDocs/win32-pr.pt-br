---
title: Estruturas de Agendador de Tarefas e uniões
description: Lista as estruturas e uniões usadas pelas APIs Agendador de Tarefas 1,0.
ms.assetid: 37dc7818-7719-4975-b7bd-f8c2d5cc008b
keywords:
- Agendador de Tarefas Agendador de Tarefas, referência, estruturas e uniões
- gatilhos Agendador de Tarefas, estruturas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bdb73620ccd92eed3ce8aea9bf5a17c5734d926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159426"
---
# <a name="task-scheduler-structures-and-unions"></a><span data-ttu-id="343eb-105">Estruturas de Agendador de Tarefas e uniões</span><span class="sxs-lookup"><span data-stu-id="343eb-105">Task Scheduler Structures and Unions</span></span>

<span data-ttu-id="343eb-106">Esta seção descreve as estruturas e as uniões usadas pelas APIs de Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="343eb-106">This section describes the structures and unions used by the Task Scheduler APIs.</span></span>

<span data-ttu-id="343eb-107">Todas as estruturas e uniões abaixo são usadas pelo Agendador de Tarefas 1,0.</span><span class="sxs-lookup"><span data-stu-id="343eb-107">All the structures and unions below are used by Task Scheduler 1.0.</span></span>



| <span data-ttu-id="343eb-108">Name</span><span class="sxs-lookup"><span data-stu-id="343eb-108">Name</span></span>                                               | <span data-ttu-id="343eb-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="343eb-109">Description</span></span>                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="343eb-110">**DIÁRIO**</span><span class="sxs-lookup"><span data-stu-id="343eb-110">**DAILY**</span></span>](/windows/desktop/api/Mstask/ns-mstask-daily)                             | <span data-ttu-id="343eb-111">Define o intervalo, em dias, no qual uma tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="343eb-111">Defines the interval, in days, at which a task is run.</span></span>                                                                          |
| [<span data-ttu-id="343eb-112">**MONTHLYDATE**</span><span class="sxs-lookup"><span data-stu-id="343eb-112">**MONTHLYDATE**</span></span>](/windows/desktop/api/Mstask/ns-mstask-monthlydate)                 | <span data-ttu-id="343eb-113">Define o dia do mês em que a tarefa será executada.</span><span class="sxs-lookup"><span data-stu-id="343eb-113">Defines the day of the month the task will run.</span></span>                                                                                 |
| [<span data-ttu-id="343eb-114">**MONTHLYDOW**</span><span class="sxs-lookup"><span data-stu-id="343eb-114">**MONTHLYDOW**</span></span>](/windows/desktop/api/Mstask/ns-mstask-monthlydow)                   | <span data-ttu-id="343eb-115">Define as datas em que a tarefa é executada por mês, semana e dia da semana.</span><span class="sxs-lookup"><span data-stu-id="343eb-115">Defines the date(s) that the task runs by month, week, and day of the week.</span></span>                                                     |
| [<span data-ttu-id="343eb-116">**gatilho de tarefa \_**</span><span class="sxs-lookup"><span data-stu-id="343eb-116">**TASK\_TRIGGER**</span></span>](/windows/desktop/api/Mstask/ns-mstask-task_trigger)              | <span data-ttu-id="343eb-117">Define os horários para executar um [*item de trabalho*](w.md)agendado.</span><span class="sxs-lookup"><span data-stu-id="343eb-117">Defines the times to run a scheduled [*work item*](w.md).</span></span>                                                  |
| [<span data-ttu-id="343eb-118">**tipo de gatilho \_ \_ Union**</span><span class="sxs-lookup"><span data-stu-id="343eb-118">**TRIGGER\_TYPE\_UNION**</span></span>](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) | <span data-ttu-id="343eb-119">Define o agendamento de invocação do gatilho dentro do membro de **tipo** de uma estrutura de [**\_ gatilho de tarefa**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .</span><span class="sxs-lookup"><span data-stu-id="343eb-119">Defines the invocation schedule of the trigger within the **Type** member of a [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> |
| [<span data-ttu-id="343eb-120">**QUINZENAL**</span><span class="sxs-lookup"><span data-stu-id="343eb-120">**WEEKLY**</span></span>](/windows/desktop/api/Mstask/ns-mstask-weekly)                           | <span data-ttu-id="343eb-121">Define o intervalo, em semanas, entre as invocações de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="343eb-121">Defines the interval, in weeks, between invocations of a task.</span></span>                                                                  |



 

 

 




