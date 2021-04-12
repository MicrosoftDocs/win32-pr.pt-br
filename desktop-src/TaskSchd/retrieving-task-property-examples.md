---
title: Recuperando exemplos de propriedade de tarefa
description: Para recuperar as propriedades de uma tarefa, chame ITaskScheduler Activate para obter a interface do objeto de tarefa e, em seguida, chame o método ITask apropriado para recuperar a propriedade de tarefa em que você está interessado.
ms.assetid: 9ec9d836-c735-4a32-96b1-3dbd0a31b22a
keywords:
- Recuperando propriedades da tarefa Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2b42bc8044171834b6d99e97c41e3f5c7048ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294364"
---
# <a name="retrieving-task-property-examples"></a><span data-ttu-id="86ef7-104">Recuperando exemplos de propriedade de tarefa</span><span class="sxs-lookup"><span data-stu-id="86ef7-104">Retrieving Task Property Examples</span></span>

<span data-ttu-id="86ef7-105">Para recuperar as propriedades de uma tarefa, chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface do objeto de tarefa e, em seguida, chame o método [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) apropriado para recuperar a propriedade de tarefa em que você está interessado.</span><span class="sxs-lookup"><span data-stu-id="86ef7-105">To retrieve the properties of a task, call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get retrieve the interface of the task object, then call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to retrieve the task property that you are interested in.</span></span> <span data-ttu-id="86ef7-106">Os exemplos de código listados na parte inferior da página mostram como recuperar as diferentes propriedades da tarefa.</span><span class="sxs-lookup"><span data-stu-id="86ef7-106">The code examples listed at the bottom of the page show how to retrieve the different task properties.</span></span>

<span data-ttu-id="86ef7-107">Os exemplos de código listados na parte inferior da página mostram como recuperar as propriedades que são exclusivas de objetos de tarefa.</span><span class="sxs-lookup"><span data-stu-id="86ef7-107">The code examples listed at the bottom of the page show how to retrieve the properties that are unique to task objects.</span></span> <span data-ttu-id="86ef7-108">Para outras propriedades de [*item de trabalho*](w.md) que também se aplicam a tarefas, consulte [recuperando exemplos de item de trabalho](retrieving-work-item-property-examples.md).</span><span class="sxs-lookup"><span data-stu-id="86ef7-108">For other [*work item*](w.md) properties that also apply to tasks, see [Retrieving Work Item Examples](retrieving-work-item-property-examples.md).</span></span>

> [!Note]  
> <span data-ttu-id="86ef7-109">No exemplo de código a seguir, todas as interfaces são lançadas depois que elas não são mais necessárias.</span><span class="sxs-lookup"><span data-stu-id="86ef7-109">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="86ef7-110">Observe que, se você estiver recuperando uma propriedade de cadeia de caracteres (como o nome do aplicativo, os parâmetros ou o diretório de trabalho), deverá chamar [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória alocada para a cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="86ef7-110">Note that if you are retrieving a string property (such as the application name, parameters, or working directory), you must call [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory allocated for the returned string.</span></span>

<span data-ttu-id="86ef7-111">O procedimento a seguir descreve como recuperar uma propriedade de tarefa.</span><span class="sxs-lookup"><span data-stu-id="86ef7-111">The following procedure describes how to retrieve a task property.</span></span>

<span data-ttu-id="86ef7-112">**Para recuperar uma propriedade de tarefa**</span><span class="sxs-lookup"><span data-stu-id="86ef7-112">**To retrieve a task property**</span></span>

1.  <span data-ttu-id="86ef7-113">Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="86ef7-113">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="86ef7-114">(Esses exemplos pressupõem que o serviço Agendador de Tarefas está em execução.)</span><span class="sxs-lookup"><span data-stu-id="86ef7-114">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="86ef7-115">Chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto Task.</span><span class="sxs-lookup"><span data-stu-id="86ef7-115">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="86ef7-116">(Observe que este exemplo obtém a tarefa "Test Task".)</span><span class="sxs-lookup"><span data-stu-id="86ef7-116">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="86ef7-117">Chame o método [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) apropriado para recuperar a propriedade em que você está interessado.</span><span class="sxs-lookup"><span data-stu-id="86ef7-117">Call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to retrieve the property you are interested in.</span></span>
4.  <span data-ttu-id="86ef7-118">Processe a propriedade conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="86ef7-118">Process the property as needed.</span></span> <span data-ttu-id="86ef7-119">(Esses exemplos imprimem a propriedade na tela.)</span><span class="sxs-lookup"><span data-stu-id="86ef7-119">(These examples print the property to the screen.)</span></span>
5.  <span data-ttu-id="86ef7-120">Se a propriedade retornada for uma cadeia de caracteres, chame [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória alocada para a cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="86ef7-120">If the returned property is a string, call [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory allocated for the returned string.</span></span>



| <span data-ttu-id="86ef7-121">Para obter um exemplo de código de</span><span class="sxs-lookup"><span data-stu-id="86ef7-121">For a code example of</span></span>                                                                                                                           | <span data-ttu-id="86ef7-122">Consulte</span><span class="sxs-lookup"><span data-stu-id="86ef7-122">See</span></span>                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86ef7-123">Recuperando o nome do aplicativo associado a uma determinada tarefa</span><span class="sxs-lookup"><span data-stu-id="86ef7-123">Retrieving the name of the application associated with a given task</span></span>                                                                             | [<span data-ttu-id="86ef7-124">Exemplo de código do C/C++: Recuperando o nome do aplicativo da tarefa</span><span class="sxs-lookup"><span data-stu-id="86ef7-124">C/C++ Code Example: Retrieving the Task Application Name</span></span>](c-c-code-example-retrieving-the-task-application-name.md)   |
| <span data-ttu-id="86ef7-125">Recuperando a quantidade máxima de tempo que a tarefa pode executar e exibindo esse número na tela</span><span class="sxs-lookup"><span data-stu-id="86ef7-125">Retrieving the maximum amount of time the task can run and displaying that number on the screen</span></span>                                                 | [<span data-ttu-id="86ef7-126">Exemplo de código C/C++: Recuperando a tarefa MaxRunTime</span><span class="sxs-lookup"><span data-stu-id="86ef7-126">C/C++ Code Example: Retrieving the Task MaxRunTime</span></span>](c-c-code-example-retrieving-the-task-maxruntime.md)               |
| <span data-ttu-id="86ef7-127">Recuperando a cadeia de caracteres do parâmetro que é executada quando a tarefa é executada e exibindo essa cadeia de caracteres na tela</span><span class="sxs-lookup"><span data-stu-id="86ef7-127">Retrieving the parameter string that is executed when the task is run and displaying that string on the screen</span></span>                                  | [<span data-ttu-id="86ef7-128">Exemplo de código do C/C++: Recuperando parâmetros da tarefa</span><span class="sxs-lookup"><span data-stu-id="86ef7-128">C/C++ Code Example: Retrieving Task Parameters</span></span>](c-c-code-example-retrieving-task-parameters.md)                       |
| <span data-ttu-id="86ef7-129">Recuperando o [*nível de prioridade*](p.md) da tarefa</span><span class="sxs-lookup"><span data-stu-id="86ef7-129">Retrieving the [*priority level*](p.md) of the task</span></span>                                                                    | [<span data-ttu-id="86ef7-130">Exemplo de código do C/C++: Recuperando a prioridade da tarefa</span><span class="sxs-lookup"><span data-stu-id="86ef7-130">C/C++ Code Example: Retrieving Task Priority</span></span>](c-c-code-example-retrieving-task-priority.md)                           |
| <span data-ttu-id="86ef7-131">Recuperando o [*diretório de trabalho*](w.md) de uma tarefa e exibindo o caminho para o diretório de trabalho na tela</span><span class="sxs-lookup"><span data-stu-id="86ef7-131">Retrieving the [*working directory*](w.md) of a task and displaying the path to the working directory on the screen</span></span> | [<span data-ttu-id="86ef7-132">Exemplo de código do C/C++: Recuperando o diretório de trabalho da tarefa</span><span class="sxs-lookup"><span data-stu-id="86ef7-132">C/C++ Code Example: Retrieving the Task Working Directory</span></span>](c-c-code-example-retrieving-the-task-working-directory.md) |



 

## <a name="related-topics"></a><span data-ttu-id="86ef7-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="86ef7-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86ef7-134">Exemplos de Agendador de Tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="86ef7-134">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 