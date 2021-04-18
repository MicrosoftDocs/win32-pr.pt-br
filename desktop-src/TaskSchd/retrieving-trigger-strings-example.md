---
title: Exemplo de recuperação de cadeias de caracteres de gatilho
description: Você pode recuperar as cadeias de caracteres de gatilho de um gatilho conhecido usando a interface IScheduledWorkItem ou ITaskTrigger, dependendo do tipo de objeto com o qual você está trabalhando.
ms.assetid: adfa95b1-54f0-4bcd-a260-ca76fd77d43e
keywords:
- Recuperando cadeias de caracteres de gatilho Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44708fdbb4025f5d99409297dda65504a909aec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105792606"
---
# <a name="retrieving-trigger-strings-example"></a><span data-ttu-id="d304b-104">Exemplo de recuperação de cadeias de caracteres de gatilho</span><span class="sxs-lookup"><span data-stu-id="d304b-104">Retrieving Trigger Strings Example</span></span>

<span data-ttu-id="d304b-105">Você pode recuperar as cadeias de caracteres de gatilho de um gatilho conhecido usando a interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) ou [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) , dependendo do tipo de objeto com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="d304b-105">You can retrieve the trigger strings of a known trigger using the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) or [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface, depending on the type of object you are working with.</span></span>

<span data-ttu-id="d304b-106">Ao trabalhar com um [*objeto de tarefa*](t.md), use os métodos da interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) para recuperar as cadeias de caracteres de gatilho de um item de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d304b-106">When working with a [*task object*](t.md), use the methods of the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface to retrieve the trigger strings of a work item.</span></span>

<span data-ttu-id="d304b-107">Quando você estiver trabalhando com um [*objeto de gatilho de tarefa*](t.md), use os métodos da interface [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) para recuperar a cadeia de caracteres do gatilho.</span><span class="sxs-lookup"><span data-stu-id="d304b-107">When you are working with a [*task trigger object*](t.md), use the methods of the [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface to retrieve the trigger string of the trigger.</span></span>

<span data-ttu-id="d304b-108">O exemplo a seguir mostra como usar [**IScheduledWorkItem:: Gettriggerstring**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) para exibir as cadeias de caracteres de todos os gatilhos associados a uma tarefa conhecida.</span><span class="sxs-lookup"><span data-stu-id="d304b-108">The following example shows how to use [**IScheduledWorkItem::GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) to display the strings of all triggers associated with a known task.</span></span>

<span data-ttu-id="d304b-109">O procedimento a seguir descreve como recuperar as cadeias de caracteres de gatilho de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="d304b-109">The following procedure describes how to retrieve the trigger strings of a task.</span></span>

<span data-ttu-id="d304b-110">**Para recuperar as cadeias de caracteres de gatilho de uma tarefa**</span><span class="sxs-lookup"><span data-stu-id="d304b-110">**To retrieve the trigger strings of a task**</span></span>

1.  <span data-ttu-id="d304b-111">Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="d304b-111">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="d304b-112">(Este exemplo pressupõe que o serviço Agendador de Tarefas está em execução.)</span><span class="sxs-lookup"><span data-stu-id="d304b-112">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="d304b-113">Chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto Task.</span><span class="sxs-lookup"><span data-stu-id="d304b-113">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="d304b-114">(Observe que este exemplo obtém a tarefa "Test Task".)</span><span class="sxs-lookup"><span data-stu-id="d304b-114">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="d304b-115">Chame **ITask:: GetTriggerCount** para descobrir quantos gatilhos estão associados a uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="d304b-115">Call **ITask::GetTriggerCount** to find out how many triggers are associated with a task.</span></span> <span data-ttu-id="d304b-116">(Observe que [**GetTriggerCount**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount) é um método [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) herdado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span><span class="sxs-lookup"><span data-stu-id="d304b-116">(Note that [**GetTriggerCount**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>
4.  <span data-ttu-id="d304b-117">Exiba as cadeias de caracteres do gatilho, chamando **ITask:: Gettriggerstring** para cada gatilho associado à tarefa.</span><span class="sxs-lookup"><span data-stu-id="d304b-117">Display the trigger strings, calling **ITask::GetTriggerString** for each trigger associated with the task.</span></span> <span data-ttu-id="d304b-118">(Observe que [**Gettriggerstring**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) é um método [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) herdado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span><span class="sxs-lookup"><span data-stu-id="d304b-118">(Note that [**GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>
5.  <span data-ttu-id="d304b-119">Libere todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="d304b-119">Release all resources.</span></span> <span data-ttu-id="d304b-120">Chame [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar as cadeias de caracteres de gatilho e **ITask:: Release** para liberar a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="d304b-120">Call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the trigger strings and **ITask::Release** to release the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span> <span data-ttu-id="d304b-121">(Observe que [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) é um método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) herdado por **ITask**.)</span><span class="sxs-lookup"><span data-stu-id="d304b-121">(Note that [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by **ITask**.)</span></span>



| <span data-ttu-id="d304b-122">Para obter um exemplo de código de</span><span class="sxs-lookup"><span data-stu-id="d304b-122">For a code example of</span></span>                                                         | <span data-ttu-id="d304b-123">Consulte</span><span class="sxs-lookup"><span data-stu-id="d304b-123">See</span></span>                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d304b-124">Recuperando uma cadeia de caracteres de gatilho para todos os gatilhos associados a uma tarefa conhecida</span><span class="sxs-lookup"><span data-stu-id="d304b-124">Retrieving a trigger string for all the triggers associated with a known task</span></span> | [<span data-ttu-id="d304b-125">Exemplo de código: Recuperando cadeias de caracteres de gatilho</span><span class="sxs-lookup"><span data-stu-id="d304b-125">Code Example: Retrieving Trigger Strings</span></span>](c-c-code-example-retrieving-trigger-strings.md) |



 

## <a name="related-topics"></a><span data-ttu-id="d304b-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d304b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d304b-127">Exemplos de Agendador de Tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="d304b-127">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 