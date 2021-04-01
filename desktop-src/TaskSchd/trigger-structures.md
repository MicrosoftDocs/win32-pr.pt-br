---
title: Estruturas de gatilho para Agendador de Tarefas 1,0
description: Agendador de Tarefas 1,0 usa várias estruturas para definir os critérios de um gatilho.
ms.assetid: dd2ae4f6-fb2d-41f8-9400-7426b7ca4546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a03f28f85782d87ee3349582929babe6f907e8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005650"
---
# <a name="trigger-structures-for-task-scheduler-10"></a><span data-ttu-id="6a571-103">Estruturas de gatilho para Agendador de Tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="6a571-103">Trigger Structures for Task Scheduler 1.0</span></span>

<span data-ttu-id="6a571-104">Agendador de Tarefas 1,0 usa várias estruturas para definir os critérios de um gatilho.</span><span class="sxs-lookup"><span data-stu-id="6a571-104">Task Scheduler 1.0 uses several structures to define the criteria of a trigger.</span></span>

> [!Note]  
> <span data-ttu-id="6a571-105">Para obter mais informações sobre Agendador de Tarefas gatilhos 2,0, consulte [interfaces de gatilho](trigger-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="6a571-105">For more information about Task Scheduler 2.0 triggers, see [Trigger Interfaces](trigger-interfaces.md).</span></span>

 

## <a name="task-scheduler-10-structures"></a><span data-ttu-id="6a571-106">Estruturas Agendador de Tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="6a571-106">Task Scheduler 1.0 Structures</span></span>

<span data-ttu-id="6a571-107">A ilustração a seguir mostra a estrutura do [**\_ gatilho de tarefa**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .</span><span class="sxs-lookup"><span data-stu-id="6a571-107">The following illustration shows the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> <span data-ttu-id="6a571-108">Ele tem três membros necessários (**wBeginYear**, **wBeginMonth** e **wBeginDay**) que devem ser definidos ao criar um novo gatilho.</span><span class="sxs-lookup"><span data-stu-id="6a571-108">It has three required members (**wBeginYear**, **wBeginMonth**, and **wBeginDay**) that must be set when creating a new trigger.</span></span> <span data-ttu-id="6a571-109">(Para ir para a página de referência dessa estrutura, clique no nome da estrutura na ilustração.)</span><span class="sxs-lookup"><span data-stu-id="6a571-109">(To jump to the reference page for this structure, click the structure name in the illustration.)</span></span>

![estrutura do gatilho de tarefa](images/tsktri1.png)

<span data-ttu-id="6a571-111">Lembre-se de que o membro **TriggerType** usa a enumeração de [**\_ \_ tipo de gatilho de tarefa**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) e o membro de **tipo** usa uma estrutura de **\_ \_ União de gatilho de tarefa** .</span><span class="sxs-lookup"><span data-stu-id="6a571-111">Be aware that the **TriggerType** member uses the [**TASK\_TRIGGER\_TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) enumeration and the **Type** member uses a **TASK\_TRIGGER\_UNION** structure.</span></span> <span data-ttu-id="6a571-112">A enumeração do **\_ \_ tipo de gatilho de tarefa** é usada para especificar o tipo de gatilho (tipos de gatilho baseados em eventos e em tempo).</span><span class="sxs-lookup"><span data-stu-id="6a571-112">The **TASK\_TRIGGER\_TYPE** enumeration is used to specify the type of trigger (event and time-based trigger types).</span></span> <span data-ttu-id="6a571-113">A estrutura de [**\_ \_ União do tipo de gatilho**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) é usada para combinar as estruturas [**diária**](/windows/desktop/api/Mstask/ns-mstask-daily), [**semanal**](/windows/desktop/api/Mstask/ns-mstask-weekly), [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate) (dia do mês) e [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow) (dia da semana) usadas para especificar quando um gatilho baseado em tempo será acionado.</span><span class="sxs-lookup"><span data-stu-id="6a571-113">The [**TRIGGER\_TYPE\_UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) structure is used to combine the [**DAILY**](/windows/desktop/api/Mstask/ns-mstask-daily), [**WEEKLY**](/windows/desktop/api/Mstask/ns-mstask-weekly), [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate) (day of month), and [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow) (day of week) structures that are used to specify when a time-based trigger will fire.</span></span>

<span data-ttu-id="6a571-114">Se **TriggerType** especificar um gatilho baseado em tempo único ou um gatilho baseado em evento, o membro de **tipo** será ignorado.</span><span class="sxs-lookup"><span data-stu-id="6a571-114">If **TriggerType** specifies a one-time time-based trigger or an event-based trigger, the **Type** member is ignored.</span></span> <span data-ttu-id="6a571-115">A estrutura de [**\_ \_ União do tipo de gatilho**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) será usada somente se o membro **TriggerType** especificar um gatilho diário, semanal, dia-de-mês ou dia da semana mensal.</span><span class="sxs-lookup"><span data-stu-id="6a571-115">The [**TRIGGER\_TYPE\_UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) structure is used only if the **TriggerType** member specifies a daily, weekly, day-of-month, or monthly day-of-week time-based trigger.</span></span>

<span data-ttu-id="6a571-116">Além disso, a configuração do membro de **tipo** indica qual membro da estrutura [**de \_ \_ União de tipo de gatilho**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) é usado.</span><span class="sxs-lookup"><span data-stu-id="6a571-116">In addition, the setting of the **Type** member indicates which member of the [**TRIGGER\_TYPE\_UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) structure is used.</span></span> <span data-ttu-id="6a571-117">A ilustração a seguir mostra a relação entre os valores da enumeração de [**\_ \_ tipo de gatilho de tarefa**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) e os membros da estrutura de **\_ \_ estrutura do tipo de gatilho** .</span><span class="sxs-lookup"><span data-stu-id="6a571-117">The following illustration shows the relationship between the values of the [**TASK\_TRIGGER\_TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) enumeration and the members of the **TRIGGER\_TYPE\_STRUCTURE** structure.</span></span> <span data-ttu-id="6a571-118">(Para saltar para as páginas de referência dessas estruturas, clique no nome da estrutura na ilustração.)</span><span class="sxs-lookup"><span data-stu-id="6a571-118">(To jump to the reference pages for these structures click the structure name in the illustration.)</span></span>

![relação entre os valores de enumeração do tipo de gatilho de tarefa e os membros da estrutura de estrutura do tipo de gatilho](images/tsktri3.png)

## <a name="related-topics"></a><span data-ttu-id="6a571-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6a571-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a571-121">Gatilhos de tarefa</span><span class="sxs-lookup"><span data-stu-id="6a571-121">Task Triggers</span></span>](task-triggers.md)
</dt> <dt>

[<span data-ttu-id="6a571-122">Tipos de gatilho</span><span class="sxs-lookup"><span data-stu-id="6a571-122">Trigger Types</span></span>](trigger-types.md)
</dt> <dt>

[<span data-ttu-id="6a571-123">Interfaces de gatilho</span><span class="sxs-lookup"><span data-stu-id="6a571-123">Trigger Interfaces</span></span>](trigger-interfaces.md)
</dt> </dl>

 

 




