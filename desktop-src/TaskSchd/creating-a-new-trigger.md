---
title: Criando um novo gatilho
description: Para criar um gatilho, você deve usar três interfaces.
ms.assetid: c0f121ff-d0a5-4b6c-935c-6f47b4ea26d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f48ecb7b06e5bade6d5ad80e4c9a82794f6a17e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366376"
---
# <a name="creating-a-new-trigger"></a><span data-ttu-id="a3b48-103">Criando um novo gatilho</span><span class="sxs-lookup"><span data-stu-id="a3b48-103">Creating a New Trigger</span></span>

<span data-ttu-id="a3b48-104">Para criar um gatilho, você deve usar três interfaces.</span><span class="sxs-lookup"><span data-stu-id="a3b48-104">To create a trigger you must use three interfaces.</span></span> <span data-ttu-id="a3b48-105">[**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) fornece o método [**IScheduledWorkItem:: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) para criar o objeto Trigger, [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) fornece o método [**ITaskTrigger:: settrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) para definir os critérios para o gatilho, e a interface com [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) fornece um método **Save** para salvar o novo gatilho no disco.</span><span class="sxs-lookup"><span data-stu-id="a3b48-105">[**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) provides the [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) method for creating the trigger object, [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) provides the [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) method for setting the criteria for the trigger, and the COM interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) provides a **Save** method for saving the new trigger to disk.</span></span>

<span data-ttu-id="a3b48-106">O procedimento a seguir descreve como criar um novo gatilho.</span><span class="sxs-lookup"><span data-stu-id="a3b48-106">The following procedure describes how to create a new trigger.</span></span>

<span data-ttu-id="a3b48-107">**Para criar um novo gatilho**</span><span class="sxs-lookup"><span data-stu-id="a3b48-107">**To create a new trigger**</span></span>

1.  <span data-ttu-id="a3b48-108">Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="a3b48-108">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="a3b48-109">(Este exemplo pressupõe que o serviço Agendador de Tarefas está em execução.)</span><span class="sxs-lookup"><span data-stu-id="a3b48-109">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="a3b48-110">Chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto Task.</span><span class="sxs-lookup"><span data-stu-id="a3b48-110">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="a3b48-111">(Observe que este exemplo obtém a tarefa "Test Task".)</span><span class="sxs-lookup"><span data-stu-id="a3b48-111">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="a3b48-112">Chame [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) para criar um objeto de gatilho.</span><span class="sxs-lookup"><span data-stu-id="a3b48-112">Call [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) to create a trigger object.</span></span> <span data-ttu-id="a3b48-113">(Observe que [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) é herdado de [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span><span class="sxs-lookup"><span data-stu-id="a3b48-113">(Note that [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) is inherited from [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span></span>
4.  <span data-ttu-id="a3b48-114">Defina uma estrutura de [**\_ gatilho de tarefa**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .</span><span class="sxs-lookup"><span data-stu-id="a3b48-114">Define a [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> <span data-ttu-id="a3b48-115">Observe que os membros wBeginDay, wBeginMonth e wBeginYear do **\_ gatilho de tarefa** devem ser definidos como um dia, mês e ano válidos, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a3b48-115">Note that wBeginDay, wBeginMonth, and wBeginYear members of **TASK\_TRIGGER** must be set to a valid day, month, and year respectively.</span></span>
5.  <span data-ttu-id="a3b48-116">Chame o [**gatilho ITaskTrigger::**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) setpara definir os critérios do gatilho.</span><span class="sxs-lookup"><span data-stu-id="a3b48-116">Call [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) to set the trigger criteria.</span></span>
6.  <span data-ttu-id="a3b48-117">Salve a tarefa com o novo gatilho em disco usando [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="a3b48-117">Save the task with the new trigger to disk using [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="a3b48-118">(A interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) é uma interface com padrão com suporte da interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .)</span><span class="sxs-lookup"><span data-stu-id="a3b48-118">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface supported by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.)</span></span>
7.  <span data-ttu-id="a3b48-119">Chame o [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="a3b48-119">Call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release all resources.</span></span> <span data-ttu-id="a3b48-120">(Observe que **Release** é um método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) herdado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span><span class="sxs-lookup"><span data-stu-id="a3b48-120">(Note that **Release** is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="a3b48-121">Para obter um exemplo de código de</span><span class="sxs-lookup"><span data-stu-id="a3b48-121">For a code example of</span></span>                       | <span data-ttu-id="a3b48-122">Consulte</span><span class="sxs-lookup"><span data-stu-id="a3b48-122">See</span></span>                                                                                         |
|---------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3b48-123">Criando um novo gatilho para uma tarefa existente</span><span class="sxs-lookup"><span data-stu-id="a3b48-123">Creating a new trigger for an existing task</span></span> | [<span data-ttu-id="a3b48-124">Exemplo de código C/C++: Criando um gatilho de tarefa</span><span class="sxs-lookup"><span data-stu-id="a3b48-124">C/C++ Code Example: Creating a Task Trigger</span></span>](c-c-code-example-creating-a-task-trigger.md) |



 

## <a name="related-topics"></a><span data-ttu-id="a3b48-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a3b48-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3b48-126">Exemplos de Agendador de Tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="a3b48-126">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 