---
title: Finalizando um exemplo de tarefa
description: Você pode encerrar uma tarefa enquanto ela está em execução chamando IScheduledWorkItem Terminate.
ms.assetid: f8401650-e196-4959-8f23-3d649a55f73d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e632b00a9e957849a5735d31018e3444113190
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162354"
---
# <a name="terminating-a-task-example"></a><span data-ttu-id="33506-103">Finalizando um exemplo de tarefa</span><span class="sxs-lookup"><span data-stu-id="33506-103">Terminating a Task Example</span></span>

<span data-ttu-id="33506-104">Você pode encerrar uma tarefa enquanto ela está em execução chamando [**IScheduledWorkItem:: Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate).</span><span class="sxs-lookup"><span data-stu-id="33506-104">You can terminate a task while it is running by calling [**IScheduledWorkItem::Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate).</span></span>

<span data-ttu-id="33506-105">O procedimento a seguir descreve como encerrar uma tarefa se ela estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="33506-105">The following procedure describes how to terminate a task if it is running.</span></span>

<span data-ttu-id="33506-106">**Para encerrar uma tarefa se ela estiver em execução**</span><span class="sxs-lookup"><span data-stu-id="33506-106">**To terminate a task if it is running**</span></span>

1.  <span data-ttu-id="33506-107">Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="33506-107">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="33506-108">(Este exemplo pressupõe que o serviço Agendador de Tarefas está em execução.)</span><span class="sxs-lookup"><span data-stu-id="33506-108">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="33506-109">Chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto Task.</span><span class="sxs-lookup"><span data-stu-id="33506-109">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="33506-110">(Observe que este exemplo obtém a tarefa "Test Task".)</span><span class="sxs-lookup"><span data-stu-id="33506-110">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="33506-111">Chame **ITask:: GetStatus** para descobrir se a tarefa está em execução.</span><span class="sxs-lookup"><span data-stu-id="33506-111">Call **ITask::GetStatus** to find out if the task is running.</span></span> <span data-ttu-id="33506-112">(Observe que [**GetStatus**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getstatus) é um método [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) herdado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span><span class="sxs-lookup"><span data-stu-id="33506-112">(Note that [**GetStatus**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getstatus) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>
4.  <span data-ttu-id="33506-113">Verifique o status da tarefa e, em seguida, chame **ITask:: Terminate** se a tarefa estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="33506-113">Check the status of the task and then call **ITask::Terminate** if the task is running.</span></span> <span data-ttu-id="33506-114">(Observe que [**Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate) é um método [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) herdado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span><span class="sxs-lookup"><span data-stu-id="33506-114">(Note that [**Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="33506-115">Para obter um exemplo de código de</span><span class="sxs-lookup"><span data-stu-id="33506-115">For a code example of</span></span>                | <span data-ttu-id="33506-116">Consulte</span><span class="sxs-lookup"><span data-stu-id="33506-116">See</span></span>                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="33506-117">Verificando o status de uma tarefa conhecida</span><span class="sxs-lookup"><span data-stu-id="33506-117">Verifying the status of a known task</span></span> | [<span data-ttu-id="33506-118">Exemplo de código do C/C++: finalizando uma tarefa</span><span class="sxs-lookup"><span data-stu-id="33506-118">C/C++ Code Example: Terminating a Task</span></span>](c-c-code-example-terminating-a-task.md) |



 

## <a name="related-topics"></a><span data-ttu-id="33506-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="33506-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33506-120">Exemplos de Agendador de Tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="33506-120">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 