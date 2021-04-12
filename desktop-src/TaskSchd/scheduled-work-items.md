---
title: Itens de trabalho agendados
description: O Agendador de Tarefas usa dois termos para descrever o que pode agendar itens de trabalho e tarefas.
ms.assetid: 6ca182c3-eba8-43dd-bf2e-27dd972e3cf8
keywords:
- Agendador de Tarefas de itens de trabalho
- Agendador de Tarefas de itens de trabalho, em comparação com as tarefas
- tarefas Agendador de Tarefas
- tarefas Agendador de Tarefas, em comparação com itens de trabalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586747e4049529dcfe747959aae994360a7b1485
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292021"
---
# <a name="scheduled-work-items"></a><span data-ttu-id="673f5-107">Itens de trabalho agendados</span><span class="sxs-lookup"><span data-stu-id="673f5-107">Scheduled Work Items</span></span>

<span data-ttu-id="673f5-108">O Agendador de Tarefas usa dois termos para descrever o que ele pode agendar: itens de trabalho e tarefas.</span><span class="sxs-lookup"><span data-stu-id="673f5-108">The Task Scheduler uses two terms to describe what it can schedule: work items and tasks.</span></span> <span data-ttu-id="673f5-109">Desses dois termos, o [*item de trabalho*](w.md) é um termo mais geral que descreve qualquer tipo de item que possa ser agendado.</span><span class="sxs-lookup"><span data-stu-id="673f5-109">Of these two terms, [*work item*](w.md) is a more general term that describes any type of item that can be scheduled.</span></span> <span data-ttu-id="673f5-110">Um *item de trabalho* pode ser qualquer item que o serviço de Agendador de tarefas é executado por vez que é especificado pelos gatilhos do item.</span><span class="sxs-lookup"><span data-stu-id="673f5-110">A *work item* can be any item that the Task Scheduler service runs at a time that is specified by the item's trigger(s).</span></span>

<span data-ttu-id="673f5-111">Por outro lado, uma [*tarefa*](t.md) é um tipo específico de item de trabalho.</span><span class="sxs-lookup"><span data-stu-id="673f5-111">In contrast, a [*task*](t.md) is a specific type of work item.</span></span> <span data-ttu-id="673f5-112">Atualmente, o único tipo de item de trabalho agendado com suporte é uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="673f5-112">Currently, the only type of scheduled work item that is supported is a task.</span></span>

<span data-ttu-id="673f5-113">A interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) contém métodos que têm suporte de todos os tipos de itens de trabalho agendados.</span><span class="sxs-lookup"><span data-stu-id="673f5-113">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface contains methods that are supported by all types of scheduled work items.</span></span> <span data-ttu-id="673f5-114">Por exemplo, as informações da conta, os tempos de execução e os comentários definidos pelo aplicativo são propriedades que podem ser aplicadas a todos os tipos de itens de trabalho.</span><span class="sxs-lookup"><span data-stu-id="673f5-114">For example, account information, run times, and application-defined comments are properties that may apply to all types of work items.</span></span> <span data-ttu-id="673f5-115">Essas propriedades podem ser definidas e recuperadas por meio da interface **IScheduledWorkItem** .</span><span class="sxs-lookup"><span data-stu-id="673f5-115">These properties can be set and retrieved through the **IScheduledWorkItem** interface.</span></span>

<span data-ttu-id="673f5-116">A interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) contém métodos que têm suporte apenas por tarefas.</span><span class="sxs-lookup"><span data-stu-id="673f5-116">The [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface contains methods that are supported only by tasks.</span></span>

<span data-ttu-id="673f5-117">Os métodos da interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) são herdados atualmente pela interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) e, no futuro, serão herdados por outras interfaces de item de trabalho.</span><span class="sxs-lookup"><span data-stu-id="673f5-117">The methods of the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface are currently inherited by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface and in the future will be inherited by other work item interfaces.</span></span>

| <span data-ttu-id="673f5-118">Para obter exemplos de</span><span class="sxs-lookup"><span data-stu-id="673f5-118">For examples of</span></span>                                              | <span data-ttu-id="673f5-119">Consulte</span><span class="sxs-lookup"><span data-stu-id="673f5-119">See</span></span>                                                                                        |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="673f5-120">Criando uma nova tarefa.</span><span class="sxs-lookup"><span data-stu-id="673f5-120">Creating a new task.</span></span>                                         | [<span data-ttu-id="673f5-121">Criando uma tarefa usando o exemplo NewWorkItem</span><span class="sxs-lookup"><span data-stu-id="673f5-121">Creating a Task Using NewWorkItem Example</span></span>](creating-a-task-using-newworkitem-example.md) |
| <span data-ttu-id="673f5-122">Executando uma tarefa existente.</span><span class="sxs-lookup"><span data-stu-id="673f5-122">Running an existing task.</span></span>                                    | [<span data-ttu-id="673f5-123">Iniciando um exemplo de tarefa</span><span class="sxs-lookup"><span data-stu-id="673f5-123">Starting a Task Example</span></span>](starting-a-task-example.md)                                     |
| <span data-ttu-id="673f5-124">Recuperando propriedades que se aplicam a todos os tipos de itens de trabalho.</span><span class="sxs-lookup"><span data-stu-id="673f5-124">Retrieving properties that apply to all types of work items.</span></span> | [<span data-ttu-id="673f5-125">Recuperando exemplos de propriedade de item de trabalho</span><span class="sxs-lookup"><span data-stu-id="673f5-125">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md)       |
| <span data-ttu-id="673f5-126">Definindo propriedades que se aplicam a todos os tipos de itens de trabalho.</span><span class="sxs-lookup"><span data-stu-id="673f5-126">Setting properties that apply to all types of work items.</span></span>    | [<span data-ttu-id="673f5-127">Definindo exemplos de propriedade de item de trabalho</span><span class="sxs-lookup"><span data-stu-id="673f5-127">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)             |



 

 

 




