---
title: Iniciando um exemplo de tarefa
description: Para iniciar uma tarefa, chame o método Run da interface ITask. Run é um método assíncrono que tenta executar a tarefa e retorna assim que a tarefa é iniciada. O serviço de Agendador de Tarefas deve estar em execução para que esse método tenha sucesso.
ms.assetid: 90f197de-7a32-4e4b-b4c0-d3f706e47de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 325d8d990367a810351ec4eea8b03b7dc0240cd5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105779287"
---
# <a name="starting-a-task-example"></a><span data-ttu-id="0e155-105">Iniciando um exemplo de tarefa</span><span class="sxs-lookup"><span data-stu-id="0e155-105">Starting a Task Example</span></span>

<span data-ttu-id="0e155-106">Para iniciar uma tarefa, chame o método [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) da interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="0e155-106">To start a task, call the [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) method of the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span> <span data-ttu-id="0e155-107">**Run** é um método assíncrono que tenta executar a tarefa e retorna assim que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="0e155-107">**Run** is an asynchronous method that attempts to execute the task and returns as soon as the task has started.</span></span> <span data-ttu-id="0e155-108">O serviço de Agendador de Tarefas deve estar em execução para que esse método tenha sucesso.</span><span class="sxs-lookup"><span data-stu-id="0e155-108">The Task Scheduler service must be running for this method to succeed.</span></span>

<span data-ttu-id="0e155-109">O procedimento a seguir descreve como iniciar uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="0e155-109">The following procedure describes how to start a task.</span></span>

<span data-ttu-id="0e155-110">**Para iniciar uma tarefa**</span><span class="sxs-lookup"><span data-stu-id="0e155-110">**To start a task**</span></span>

1.  <span data-ttu-id="0e155-111">Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="0e155-111">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="0e155-112">(Este exemplo pressupõe que o serviço Agendador de Tarefas está em execução.)</span><span class="sxs-lookup"><span data-stu-id="0e155-112">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="0e155-113">Chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto Task.</span><span class="sxs-lookup"><span data-stu-id="0e155-113">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="0e155-114">(Observe que este exemplo obtém a tarefa "Test Task".)</span><span class="sxs-lookup"><span data-stu-id="0e155-114">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="0e155-115">Chame [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) para iniciar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="0e155-115">Call [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) to start the task.</span></span> <span data-ttu-id="0e155-116">Observe que esse método é herdado pela interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="0e155-116">Note that this method is inherited by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span>
4.  <span data-ttu-id="0e155-117">Continue o processamento conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="0e155-117">Continue processing as needed.</span></span>
5.  <span data-ttu-id="0e155-118">Chame **ITask:: Release** para liberar recursos e [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) para não inicializar com.</span><span class="sxs-lookup"><span data-stu-id="0e155-118">Call **ITask::Release** to free resources and [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) to uninitialize COM.</span></span> <span data-ttu-id="0e155-119">Este exemplo chama [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar o ponteiro para a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="0e155-119">This example calls [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to free the pointer to the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span> <span data-ttu-id="0e155-120">(Observe que **Release** é um método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) herdado por **ITask**.)</span><span class="sxs-lookup"><span data-stu-id="0e155-120">(Note that **Release** is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by **ITask**.)</span></span>



| <span data-ttu-id="0e155-121">Para obter um exemplo de código de</span><span class="sxs-lookup"><span data-stu-id="0e155-121">For a code example of</span></span>    | <span data-ttu-id="0e155-122">Consulte</span><span class="sxs-lookup"><span data-stu-id="0e155-122">See</span></span>                                                                         |
|--------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="0e155-123">Executando uma tarefa existente</span><span class="sxs-lookup"><span data-stu-id="0e155-123">Running an existing task</span></span> | [<span data-ttu-id="0e155-124">Exemplo de código C/C++: iniciando uma tarefa</span><span class="sxs-lookup"><span data-stu-id="0e155-124">C/C++ Code Example: Starting a Task</span></span>](c-c-code-example-starting-a-task.md) |



 

## <a name="related-topics"></a><span data-ttu-id="0e155-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e155-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e155-126">Exemplos de Agendador de Tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="0e155-126">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 