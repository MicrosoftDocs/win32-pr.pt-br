---
title: Definindo exemplos de propriedade de tarefa
description: Para definir as propriedades de uma tarefa, chame ITaskScheduler Activate para recuperar a interface do objeto Task e, em seguida, chame o método ITask apropriado para definir a Propriedade Task na qual você está interessado.
ms.assetid: df438bff-1ce1-4336-93ee-1e6cab1f1ddd
keywords:
- definindo as propriedades da tarefa Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcb05031961e38314cbc7cd12c20c1d863f54af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105792604"
---
# <a name="setting-task-property-examples"></a><span data-ttu-id="8a4bd-104">Definindo exemplos de propriedade de tarefa</span><span class="sxs-lookup"><span data-stu-id="8a4bd-104">Setting Task Property Examples</span></span>

<span data-ttu-id="8a4bd-105">Para definir as propriedades de uma tarefa, chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para recuperar a interface do objeto de tarefa e, em seguida, chame o método [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) apropriado para definir a propriedade de tarefa em que você está interessado.</span><span class="sxs-lookup"><span data-stu-id="8a4bd-105">To set the properties of a task, call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to retrieve the interface of the task object, then call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to set the task property you are interested in.</span></span>

<span data-ttu-id="8a4bd-106">Os exemplos de código listados na parte inferior da página mostram como definir as propriedades que são exclusivas de objetos de tarefa.</span><span class="sxs-lookup"><span data-stu-id="8a4bd-106">The code examples listed at the bottom of the page show how to set the properties that are unique to task objects.</span></span> <span data-ttu-id="8a4bd-107">Para outras propriedades de [*item de trabalho*](w.md) que também se aplicam a tarefas, consulte [definindo exemplos de propriedade de item de trabalho](setting-work-item-property-examples.md).</span><span class="sxs-lookup"><span data-stu-id="8a4bd-107">For other [*work item*](w.md) properties that also apply to tasks, see [Setting Work Item Property Examples](setting-work-item-property-examples.md).</span></span>

> [!Note]  
> <span data-ttu-id="8a4bd-108">No exemplo de código a seguir, todas as interfaces são lançadas depois que elas não são mais necessárias.</span><span class="sxs-lookup"><span data-stu-id="8a4bd-108">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="8a4bd-109">Nos exemplos a seguir, o objeto de tarefa modificado sempre é salvo em disco por uma chamada para [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="8a4bd-109">In the following examples, the modified task object is always saved to disk by a call to [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="8a4bd-110">(A interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) é uma interface com padrão herdada pelo objeto Task.)</span><span class="sxs-lookup"><span data-stu-id="8a4bd-110">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface inherited by the task object.)</span></span>

<span data-ttu-id="8a4bd-111">O procedimento a seguir descreve como definir uma propriedade de tarefa.</span><span class="sxs-lookup"><span data-stu-id="8a4bd-111">The following procedure describes how to set a task property.</span></span>

<span data-ttu-id="8a4bd-112">**Para definir uma propriedade de tarefa**</span><span class="sxs-lookup"><span data-stu-id="8a4bd-112">**To set a task property**</span></span>

1.  <span data-ttu-id="8a4bd-113">Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="8a4bd-113">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="8a4bd-114">(Esses exemplos pressupõem que o serviço Agendador de Tarefas está em execução.)</span><span class="sxs-lookup"><span data-stu-id="8a4bd-114">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="8a4bd-115">Chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto Task.</span><span class="sxs-lookup"><span data-stu-id="8a4bd-115">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="8a4bd-116">(Observe que este exemplo obtém a tarefa "Test Task".)</span><span class="sxs-lookup"><span data-stu-id="8a4bd-116">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="8a4bd-117">Chame o método [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) apropriado para definir a propriedade em que você está interessado.</span><span class="sxs-lookup"><span data-stu-id="8a4bd-117">Call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to set the property you are interested in.</span></span>
4.  <span data-ttu-id="8a4bd-118">Chame [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para armazenar o objeto de tarefa modificado em disco.</span><span class="sxs-lookup"><span data-stu-id="8a4bd-118">Call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to store the modified task object to disk.</span></span>



| <span data-ttu-id="8a4bd-119">Para obter um exemplo de código de</span><span class="sxs-lookup"><span data-stu-id="8a4bd-119">For a code example of</span></span>                                                                                                                                | <span data-ttu-id="8a4bd-120">Consulte</span><span class="sxs-lookup"><span data-stu-id="8a4bd-120">See</span></span>                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a4bd-121">Definindo o nome do aplicativo associado a uma tarefa conhecida</span><span class="sxs-lookup"><span data-stu-id="8a4bd-121">Setting the name of the application associated with a known task</span></span>                                                                                     | [<span data-ttu-id="8a4bd-122">Exemplo de código C/C++: definindo o nome do aplicativo</span><span class="sxs-lookup"><span data-stu-id="8a4bd-122">C/C++ Code Example: Setting Application Name</span></span>](c-c-code-example-setting-application-name.md)   |
| <span data-ttu-id="8a4bd-123">Definindo o tempo de execução máximo de uma tarefa conhecida</span><span class="sxs-lookup"><span data-stu-id="8a4bd-123">Setting the maximum run time of a known task</span></span>                                                                                                         | [<span data-ttu-id="8a4bd-124">Exemplo de código C/C++: Configurando MaxRunTime</span><span class="sxs-lookup"><span data-stu-id="8a4bd-124">C/C++ Code Example: Setting MaxRunTime</span></span>](c-c-code-example-setting-maxruntime.md)               |
| <span data-ttu-id="8a4bd-125">Limpando todos os parâmetros de linha de comando associados a uma tarefa conhecida</span><span class="sxs-lookup"><span data-stu-id="8a4bd-125">Clearing all command-line parameters associated with a known task</span></span>                                                                                    | [<span data-ttu-id="8a4bd-126">Exemplo de código C/C++: definindo parâmetros de tarefa</span><span class="sxs-lookup"><span data-stu-id="8a4bd-126">C/C++ Code Example: Setting Task Parameters</span></span>](c-c-code-example-setting-task-parameters.md)     |
| <span data-ttu-id="8a4bd-127">Este exemplo define a prioridade de uma tarefa de teste e salva a tarefa.</span><span class="sxs-lookup"><span data-stu-id="8a4bd-127">This example sets the priority of a test task and then saves the task.</span></span> <span data-ttu-id="8a4bd-128">Este exemplo pressupõe que a tarefa de teste já existe no computador local.</span><span class="sxs-lookup"><span data-stu-id="8a4bd-128">This example assumes that the test task already exists on the local computer.</span></span> | [<span data-ttu-id="8a4bd-129">Exemplo de código C/C++: definindo a prioridade da tarefa</span><span class="sxs-lookup"><span data-stu-id="8a4bd-129">C/C++ Code Example: Setting Task Priority</span></span>](c-c-code-example-setting-task-priority.md)         |
| <span data-ttu-id="8a4bd-130">Definindo o [*diretório de trabalho*](w.md) de uma tarefa conhecida</span><span class="sxs-lookup"><span data-stu-id="8a4bd-130">Setting the [*working directory*](w.md) of a known task</span></span>                                                                  | [<span data-ttu-id="8a4bd-131">Exemplo de código C/C++: definindo diretório de trabalho</span><span class="sxs-lookup"><span data-stu-id="8a4bd-131">C/C++ Code Example: Setting Working Directory</span></span>](c-c-code-example-setting-working-directory.md) |



 

## <a name="related-topics"></a><span data-ttu-id="8a4bd-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8a4bd-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a4bd-133">Exemplos de Agendador de Tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="8a4bd-133">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 