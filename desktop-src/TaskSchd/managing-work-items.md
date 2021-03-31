---
title: Manipulando itens de trabalho
description: A interface IScheduledWorkItem fornece métodos para recuperar e definir propriedades de item de trabalho; Criando, recuperando e excluindo gatilhos para itens de trabalho (a definição do gatilho deve ser feita com o método settrigger ITaskTrigger); e para executar, encerrar e excluir o item de trabalho. Observação para as propriedades de um tipo específico de item de trabalho, consulte a interface para esse tipo de objeto. Por exemplo, você não pode definir o nível de prioridade de um item de trabalho; no entanto, você pode usar os métodos da interface ITask para recuperar e definir a prioridade de uma tarefa.
ms.assetid: 8aedf96d-e43d-4aac-ad8c-860379209f95
keywords:
- Agendador de Tarefas de itens de trabalho, gerenciando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33680d04da9d34f54085d182ed61edda9e8b232f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641411"
---
# <a name="manipulating-work-items"></a><span data-ttu-id="72b36-105">Manipulando itens de trabalho</span><span class="sxs-lookup"><span data-stu-id="72b36-105">Manipulating Work Items</span></span>

<span data-ttu-id="72b36-106">A interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) fornece métodos para recuperar e definir propriedades de item de trabalho; criar, recuperar e excluir gatilhos para itens de trabalho (definir o gatilho deve ser feito com o método [**ITaskTrigger:: settrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) ); e para executar, encerrar e excluir o item de trabalho.</span><span class="sxs-lookup"><span data-stu-id="72b36-106">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface provides methods for retrieving and setting work item properties; creating, retrieving, and deleting triggers for work items (setting the trigger must be done with the [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) method); and for running, terminating, and deleting the work item.</span></span>

> [!Note]  
> <span data-ttu-id="72b36-107">Para as propriedades de um tipo específico de item de trabalho, consulte a interface para esse tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="72b36-107">For the properties of a specific type of work item, refer to the interface for that type of object.</span></span> <span data-ttu-id="72b36-108">Por exemplo, você não pode definir o nível de prioridade de um item de trabalho; no entanto, você pode usar os métodos da interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) para recuperar e definir a prioridade de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="72b36-108">For example, you cannot set the priority level of a work item; however, you can use the methods of the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface to retrieve and set the priority of a task.</span></span>

 

<span data-ttu-id="72b36-109">Sempre que você modificar um item de trabalho, deverá chamar o objeto [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para salvar o item de trabalho modificado em disco.</span><span class="sxs-lookup"><span data-stu-id="72b36-109">Whenever you modify a work item, you must call the [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) object to save the modified work item to disk.</span></span> <span data-ttu-id="72b36-110">A interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) é uma interface com padrão que é suportada pela interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="72b36-110">The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface that is supported by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span>

| <span data-ttu-id="72b36-111">Para obter exemplos de</span><span class="sxs-lookup"><span data-stu-id="72b36-111">For examples of</span></span>                                                            | <span data-ttu-id="72b36-112">Consulte</span><span class="sxs-lookup"><span data-stu-id="72b36-112">See</span></span>                                                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="72b36-113">Recuperando propriedades que se aplicam a todos os tipos de itens de trabalho</span><span class="sxs-lookup"><span data-stu-id="72b36-113">Retrieving properties that apply to all types of work items</span></span>                | [<span data-ttu-id="72b36-114">Recuperando exemplos de propriedade de item de trabalho</span><span class="sxs-lookup"><span data-stu-id="72b36-114">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md) |
| <span data-ttu-id="72b36-115">Definindo propriedades que se aplicam a todos os tipos de itens de trabalho</span><span class="sxs-lookup"><span data-stu-id="72b36-115">Setting properties that apply to all types of work items</span></span>                   | [<span data-ttu-id="72b36-116">Definindo exemplos de propriedade de item de trabalho</span><span class="sxs-lookup"><span data-stu-id="72b36-116">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)       |
| <span data-ttu-id="72b36-117">Executando uma tarefa conhecida</span><span class="sxs-lookup"><span data-stu-id="72b36-117">Running a known task</span></span>                                                       | [<span data-ttu-id="72b36-118">Iniciando um exemplo de tarefa</span><span class="sxs-lookup"><span data-stu-id="72b36-118">Starting a Task Example</span></span>](starting-a-task-example.md)                               |
| <span data-ttu-id="72b36-119">Finalizando uma tarefa em execução</span><span class="sxs-lookup"><span data-stu-id="72b36-119">Terminating a running task</span></span>                                                 | [<span data-ttu-id="72b36-120">Finalizando um exemplo de tarefa</span><span class="sxs-lookup"><span data-stu-id="72b36-120">Terminating a Task Example</span></span>](terminating-a-task-example.md)                         |
| <span data-ttu-id="72b36-121">Criando um novo gatilho para uma tarefa conhecida</span><span class="sxs-lookup"><span data-stu-id="72b36-121">Creating a new trigger for a known task</span></span>                                    | [<span data-ttu-id="72b36-122">Criando um novo gatilho</span><span class="sxs-lookup"><span data-stu-id="72b36-122">Creating a New Trigger</span></span>](creating-a-new-trigger.md)                                 |
| <span data-ttu-id="72b36-123">Criando um gatilho ocioso baseado em evento para uma tarefa conhecida</span><span class="sxs-lookup"><span data-stu-id="72b36-123">Creating an event-based idle trigger for a known task</span></span>                      | [<span data-ttu-id="72b36-124">Criando um exemplo de gatilho de ociosidade</span><span class="sxs-lookup"><span data-stu-id="72b36-124">Creating an Idle Trigger Example</span></span>](creating-an-idle-trigger-example.md)             |
| <span data-ttu-id="72b36-125">Recuperando a cadeia de caracteres de gatilho de todos os gatilhos associados a uma tarefa conhecida</span><span class="sxs-lookup"><span data-stu-id="72b36-125">Retrieving the trigger string of all triggers associated with a known task</span></span> | [<span data-ttu-id="72b36-126">Exemplo de recuperação de cadeias de caracteres de gatilho</span><span class="sxs-lookup"><span data-stu-id="72b36-126">Retrieving Trigger Strings Example</span></span>](retrieving-trigger-strings-example.md)         |



 

 

 