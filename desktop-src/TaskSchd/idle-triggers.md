---
title: Gatilhos ociosos para Agendador de Tarefas 1,0
description: Um gatilho ocioso é um gatilho baseado em evento que é acionado um número específico de vezes após o computador ficar ocioso. Há várias condições que definem quando um computador se torna ocioso, como quando não ocorre nenhuma entrada de teclado ou mouse.
ms.assetid: f2e0b120-dadc-470f-8349-42843149bb60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d6a19f3f6d474a9463667316e353a4803ab8fa9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105800012"
---
# <a name="idle-triggers-for-task-scheduler-10"></a><span data-ttu-id="55afc-104">Gatilhos ociosos para Agendador de Tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="55afc-104">Idle Triggers for Task Scheduler 1.0</span></span>

<span data-ttu-id="55afc-105">Um gatilho ocioso é um gatilho baseado em evento que é acionado um número específico de vezes após o computador ficar ocioso.</span><span class="sxs-lookup"><span data-stu-id="55afc-105">An idle trigger is an event-based trigger that is fired a specific number of times after the computer becomes idle.</span></span> <span data-ttu-id="55afc-106">Há várias condições que definem quando um computador se torna ocioso, como quando não ocorre nenhuma entrada de teclado ou mouse.</span><span class="sxs-lookup"><span data-stu-id="55afc-106">There are multiple conditions that define when a computer becomes idle, such as when no keyboard or mouse input occurs.</span></span>

<span data-ttu-id="55afc-107">Gatilhos ociosos são criados especificando \_ o gatilho de evento de tarefa \_ \_ em \_ ociosidade no membro de [**\_ \_ tipo de gatilho de tarefa**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) da estrutura do [**\_ gatilho de tarefa**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .</span><span class="sxs-lookup"><span data-stu-id="55afc-107">Idle triggers are created by specifying TASK\_EVENT\_TRIGGER\_ON\_IDLE in the [**TASK\_TRIGGER\_TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) member of the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> <span data-ttu-id="55afc-108">O gatilho de ociosidade é acionado quando o sistema fica ocioso pelo período de tempo ocioso especificado pelo tempo de espera de ociosidade do item de trabalho.</span><span class="sxs-lookup"><span data-stu-id="55afc-108">The idle trigger is fired when the system becomes idle for the amount of time that is specified by the idle wait time of the work item.</span></span>

> [!Note]  
> <span data-ttu-id="55afc-109">Quando \_ \_ o gatilho de evento de tarefa \_ \_ está ocioso é especificado, os membros **wStartHour**, **wStartMinute** e **Type** da estrutura de [**\_ gatilho de tarefa**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) são ignorados.</span><span class="sxs-lookup"><span data-stu-id="55afc-109">When TASK\_EVENT\_TRIGGER\_ON\_IDLE is specified, the **wStartHour**, **wStartMinute**, and **Type** members of the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure are ignored.</span></span>

 

<span data-ttu-id="55afc-110">Você pode definir o tempo de espera ocioso de um item de trabalho chamando o método [**IScheduledWorkItem:: SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) .</span><span class="sxs-lookup"><span data-stu-id="55afc-110">You can set the idle wait time of a work item by calling the [**IScheduledWorkItem::SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) method.</span></span> <span data-ttu-id="55afc-111">Esse método define a quantidade de tempo (em minutos) que o sistema deve permanecer ocioso antes que o gatilho seja acionado e o item de trabalho seja executado.</span><span class="sxs-lookup"><span data-stu-id="55afc-111">This method sets the amount of time (in minutes) that the system must remain idle before the trigger is fired and the work item is executed.</span></span>

<span data-ttu-id="55afc-112">Para recuperar o tempo ocioso de uma tarefa, chame o método [**IScheduledWorkItem:: GetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getidlewait) .</span><span class="sxs-lookup"><span data-stu-id="55afc-112">To retrieve the idle time of a task, call the [**IScheduledWorkItem::GetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getidlewait) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55afc-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="55afc-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55afc-114">Gatilhos de tarefa</span><span class="sxs-lookup"><span data-stu-id="55afc-114">Task Triggers</span></span>](task-triggers.md)
</dt> </dl>

 

 




