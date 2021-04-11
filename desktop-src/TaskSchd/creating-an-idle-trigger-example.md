---
title: Criando um exemplo de gatilho de ociosidade
description: Para criar um gatilho ocioso, você deve especificar um gatilho ocioso ao criar o gatilho e deve definir o tempo ocioso para a tarefa. Para obter informações sobre condições ociosas, consulte condições de ociosidade da tarefa.
ms.assetid: d36a621c-4011-4c3d-b6f4-b56d1f50983c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a7f8333c79d05dfade609f028f93a816e61adf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294323"
---
# <a name="creating-an-idle-trigger-example"></a><span data-ttu-id="bac16-104">Criando um exemplo de gatilho de ociosidade</span><span class="sxs-lookup"><span data-stu-id="bac16-104">Creating an Idle Trigger Example</span></span>

<span data-ttu-id="bac16-105">Para criar um gatilho ocioso, você deve especificar um gatilho ocioso ao criar o gatilho e deve definir o tempo ocioso para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="bac16-105">To create an idle trigger, you must specify an idle trigger when you create the trigger, and you must set the idle time for the task.</span></span> <span data-ttu-id="bac16-106">Para obter informações sobre condições ociosas, consulte [condições de ociosidade da tarefa](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="bac16-106">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

<span data-ttu-id="bac16-107">Depois de criar o gatilho de ociosidade, chame [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para salvar o novo gatilho em disco.</span><span class="sxs-lookup"><span data-stu-id="bac16-107">After creating the idle trigger, call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to save the new trigger to disk.</span></span>

<span data-ttu-id="bac16-108">O procedimento a seguir descreve como criar um gatilho ocioso para uma tarefa conhecida.</span><span class="sxs-lookup"><span data-stu-id="bac16-108">The following procedure describes how to create an idle trigger for a known task.</span></span>

<span data-ttu-id="bac16-109">**Para criar um gatilho ocioso para uma tarefa conhecida**</span><span class="sxs-lookup"><span data-stu-id="bac16-109">**To create an idle trigger for a known task**</span></span>

1.  <span data-ttu-id="bac16-110">Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="bac16-110">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="bac16-111">(Este exemplo pressupõe que o serviço Agendador de Tarefas está em execução.)</span><span class="sxs-lookup"><span data-stu-id="bac16-111">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="bac16-112">Chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto Task.</span><span class="sxs-lookup"><span data-stu-id="bac16-112">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="bac16-113">(Observe que este exemplo obtém a tarefa "Test Task".)</span><span class="sxs-lookup"><span data-stu-id="bac16-113">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="bac16-114">Chame [**SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) para definir por quanto tempo o sistema deve permanecer ocioso antes que o gatilho seja acionado.</span><span class="sxs-lookup"><span data-stu-id="bac16-114">Call [**SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) to set how long the system must remain idle before the trigger will fire.</span></span> <span data-ttu-id="bac16-115">(Observe que **SetIdleWait** é herdado de [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span><span class="sxs-lookup"><span data-stu-id="bac16-115">(Note that **SetIdleWait** is inherited from [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span></span>
4.  <span data-ttu-id="bac16-116">Defina a estrutura do [**\_ gatilho de tarefa**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) e chame [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) para criar o gatilho ocioso.</span><span class="sxs-lookup"><span data-stu-id="bac16-116">Define the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure and call [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) to create the idle trigger.</span></span> <span data-ttu-id="bac16-117">(Observe que **CreateTrigger** é herdado de [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span><span class="sxs-lookup"><span data-stu-id="bac16-117">(Note that **CreateTrigger** is inherited from [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span></span>
5.  <span data-ttu-id="bac16-118">Salve a tarefa com o novo gatilho de ociosidade em disco usando [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="bac16-118">Save the task with the new idle trigger to disk using [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="bac16-119">(A interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) é uma interface com padrão com suporte da interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .)</span><span class="sxs-lookup"><span data-stu-id="bac16-119">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface supported by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.)</span></span>
6.  <span data-ttu-id="bac16-120">Chame **ITask:: Release** para liberar todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="bac16-120">Call **ITask::Release** to release all resources.</span></span> <span data-ttu-id="bac16-121">(Observe que [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) é um método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) herdado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span><span class="sxs-lookup"><span data-stu-id="bac16-121">(Note that [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="bac16-122">Para obter um exemplo de código de</span><span class="sxs-lookup"><span data-stu-id="bac16-122">For a code example of</span></span>                         | <span data-ttu-id="bac16-123">Consulte</span><span class="sxs-lookup"><span data-stu-id="bac16-123">See</span></span>                                                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bac16-124">Criando um gatilho ocioso para uma tarefa existente</span><span class="sxs-lookup"><span data-stu-id="bac16-124">Creating an idle trigger for an existing task</span></span> | [<span data-ttu-id="bac16-125">Exemplo de código C/C++: Criando um gatilho ocioso</span><span class="sxs-lookup"><span data-stu-id="bac16-125">C/C++ Code Example: Creating an Idle Trigger</span></span>](c-c-code-example-creating-an-idle-trigger.md) |



 

## <a name="related-topics"></a><span data-ttu-id="bac16-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bac16-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bac16-127">Exemplos de Agendador de Tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="bac16-127">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 