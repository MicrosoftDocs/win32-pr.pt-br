---
title: Definindo exemplos de propriedade de item de trabalho
description: Para definir as propriedades de um item de trabalho, chame ITaskScheduler Activate para recuperar a interface do objeto de item de trabalho e, em seguida, chame o método apropriado para definir a propriedade de tarefa em que você está interessado. Atualmente, os únicos itens de trabalho válidos são tarefas.
ms.assetid: 80a158de-d312-499d-8ff0-b95e794cf169
keywords:
- definindo propriedades do item de trabalho Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e026ea3d2b3f6677a3d229e9289ab9b201e02b94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917519"
---
# <a name="setting-work-item-property-examples"></a><span data-ttu-id="8b967-105">Definindo exemplos de propriedade de item de trabalho</span><span class="sxs-lookup"><span data-stu-id="8b967-105">Setting Work Item Property Examples</span></span>

<span data-ttu-id="8b967-106">Para definir as propriedades de um item de trabalho, chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para recuperar a interface do objeto de item de trabalho e, em seguida, chame o método apropriado para definir a propriedade de tarefa em que você está interessado.</span><span class="sxs-lookup"><span data-stu-id="8b967-106">To set the properties of a work item, call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to retrieve the interface of the work item object, then call the appropriate method to set the task property you are interested in.</span></span> <span data-ttu-id="8b967-107">Atualmente, os únicos itens de trabalho válidos são tarefas.</span><span class="sxs-lookup"><span data-stu-id="8b967-107">Currently, the only valid work items are tasks.</span></span>

<span data-ttu-id="8b967-108">Os exemplos de código listados na parte inferior da página mostram como definir as propriedades que se aplicam a todos os itens de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8b967-108">The code examples listed at the bottom of the page show how to set the properties that apply to all work items.</span></span> <span data-ttu-id="8b967-109">Para outras propriedades que são exclusivas de tarefas, consulte [definindo exemplos de propriedade de tarefa](setting-task-property-examples.md).</span><span class="sxs-lookup"><span data-stu-id="8b967-109">For other properties that are unique to tasks, see [Setting Task Property Examples](setting-task-property-examples.md).</span></span>

> [!Note]  
> <span data-ttu-id="8b967-110">No exemplo de código a seguir, todas as interfaces são lançadas depois que elas não são mais necessárias.</span><span class="sxs-lookup"><span data-stu-id="8b967-110">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="8b967-111">Nos exemplos a seguir, o objeto modificado é sempre salvo em disco por uma chamada para [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="8b967-111">In the following examples, the modified object is always saved to disk by a call to [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="8b967-112">(A interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) é uma interface com padrão herdada pelo objeto Task.)</span><span class="sxs-lookup"><span data-stu-id="8b967-112">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface inherited by the task object.)</span></span>

<span data-ttu-id="8b967-113">O procedimento a seguir descreve como definir uma propriedade de tarefa.</span><span class="sxs-lookup"><span data-stu-id="8b967-113">The following procedure describes how to set a task property.</span></span>

<span data-ttu-id="8b967-114">**Para definir uma propriedade de tarefa**</span><span class="sxs-lookup"><span data-stu-id="8b967-114">**To set a task property**</span></span>

1.  <span data-ttu-id="8b967-115">Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="8b967-115">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="8b967-116">(Esses exemplos pressupõem que o serviço Agendador de Tarefas está em execução.)</span><span class="sxs-lookup"><span data-stu-id="8b967-116">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="8b967-117">Chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto Task.</span><span class="sxs-lookup"><span data-stu-id="8b967-117">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="8b967-118">(Observe que as tarefas são atualmente o único tipo válido de item de trabalho.)</span><span class="sxs-lookup"><span data-stu-id="8b967-118">(Note that tasks are currently the only valid type of work item.)</span></span>
3.  <span data-ttu-id="8b967-119">Chame o método [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) apropriado para definir a propriedade em que você está interessado.</span><span class="sxs-lookup"><span data-stu-id="8b967-119">Call the appropriate [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method to set the property you are interested in.</span></span> <span data-ttu-id="8b967-120">Observe que os métodos **IScheduledWorkItem** são herdados pela interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="8b967-120">Note that **IScheduledWorkItem** methods are inherited by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span>
4.  <span data-ttu-id="8b967-121">Chame [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para armazenar o objeto de tarefa modificado em disco.</span><span class="sxs-lookup"><span data-stu-id="8b967-121">Call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to store the modified task object to disk.</span></span>



| <span data-ttu-id="8b967-122">Para obter um exemplo de código de</span><span class="sxs-lookup"><span data-stu-id="8b967-122">For a code example of</span></span>                            | <span data-ttu-id="8b967-123">Consulte</span><span class="sxs-lookup"><span data-stu-id="8b967-123">See</span></span>                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b967-124">Definindo as informações da conta para uma tarefa conhecida</span><span class="sxs-lookup"><span data-stu-id="8b967-124">Setting the account information for a known task</span></span> | [<span data-ttu-id="8b967-125">Exemplo de código C/C++: definindo informações da conta da tarefa</span><span class="sxs-lookup"><span data-stu-id="8b967-125">C/C++ Code Example: Setting Task Account Information</span></span>](c-c-code-example-setting-task-account-information.md) |
| <span data-ttu-id="8b967-126">Definindo o comentário de uma tarefa conhecida</span><span class="sxs-lookup"><span data-stu-id="8b967-126">Setting the comment of a known task</span></span>              | [<span data-ttu-id="8b967-127">Exemplo de código C/C++: definindo o comentário da tarefa</span><span class="sxs-lookup"><span data-stu-id="8b967-127">C/C++ Code Example: Setting Task Comment</span></span>](c-c-code-example-setting-task-comment.md)                         |



 

## <a name="related-topics"></a><span data-ttu-id="8b967-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8b967-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b967-129">Exemplos de Agendador de Tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="8b967-129">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 