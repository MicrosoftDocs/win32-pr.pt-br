---
title: Exemplo de enumeração de tarefas
description: Para enumerar tarefas, você deve chamar ITaskScheduler enum para criar um objeto de enumeração. Em seguida, use a interface IEnumWorkItems do objeto de enumeração para enumerar as tarefas na pasta tarefas agendadas.
ms.assetid: 65a8a8af-f4d8-4948-8dd4-b592f1381bfe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd929ebd7d8e9f1a3c372ce212d63dcb29df82b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105764752"
---
# <a name="enumerating-tasks-example"></a><span data-ttu-id="674c5-104">Exemplo de enumeração de tarefas</span><span class="sxs-lookup"><span data-stu-id="674c5-104">Enumerating Tasks Example</span></span>

<span data-ttu-id="674c5-105">Para enumerar tarefas, você deve chamar [**ITaskScheduler:: enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) para criar um [*objeto de enumeração*](e.md).</span><span class="sxs-lookup"><span data-stu-id="674c5-105">To enumerate tasks, you must call [**ITaskScheduler::Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) to create an [*enumeration object*](e.md).</span></span> <span data-ttu-id="674c5-106">Em seguida, use a interface [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) do objeto de enumeração para enumerar as tarefas na pasta tarefas agendadas.</span><span class="sxs-lookup"><span data-stu-id="674c5-106">Then, use the enumeration object's [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) interface to enumerate the tasks in the Scheduled Tasks folder.</span></span>

<span data-ttu-id="674c5-107">O procedimento a seguir descreve como enumerar as tarefas na pasta tarefas agendadas.</span><span class="sxs-lookup"><span data-stu-id="674c5-107">The following procedure describes how to enumerate the tasks in the Scheduled Tasks folder.</span></span>

<span data-ttu-id="674c5-108">**Para enumerar as tarefas na pasta tarefas agendadas**</span><span class="sxs-lookup"><span data-stu-id="674c5-108">**To enumerate the tasks in the Scheduled Tasks folder**</span></span>

1.  <span data-ttu-id="674c5-109">Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="674c5-109">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="674c5-110">(Este exemplo pressupõe que o serviço Agendador de Tarefas está em execução.)</span><span class="sxs-lookup"><span data-stu-id="674c5-110">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="674c5-111">Chame [**ITaskScheduler:: enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) para obter um objeto de enumeração.</span><span class="sxs-lookup"><span data-stu-id="674c5-111">Call [**ITaskScheduler::Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) to get an enumeration object.</span></span>
3.  <span data-ttu-id="674c5-112">Chame [**IEnumWorkItems:: Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next) para recuperar as tarefas.</span><span class="sxs-lookup"><span data-stu-id="674c5-112">Call [**IEnumWorkItems::Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next) to retrieve the tasks.</span></span> <span data-ttu-id="674c5-113">(Este exemplo tenta recuperar cinco tarefas com cada chamada.)</span><span class="sxs-lookup"><span data-stu-id="674c5-113">(This example tries to retrieve five tasks with each call.)</span></span>
4.  <span data-ttu-id="674c5-114">Processe as tarefas retornadas.</span><span class="sxs-lookup"><span data-stu-id="674c5-114">Process the tasks returned.</span></span> <span data-ttu-id="674c5-115">(Este exemplo simplesmente imprime o nome de cada tarefa na tela.</span><span class="sxs-lookup"><span data-stu-id="674c5-115">(This example simply prints the name of each task to the screen.</span></span>
5.  <span data-ttu-id="674c5-116">Liberar recursos.</span><span class="sxs-lookup"><span data-stu-id="674c5-116">Release resources.</span></span> <span data-ttu-id="674c5-117">Chame [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória usada para nomes.</span><span class="sxs-lookup"><span data-stu-id="674c5-117">Call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory used for names.</span></span>



| <span data-ttu-id="674c5-118">Para obter um exemplo de código de</span><span class="sxs-lookup"><span data-stu-id="674c5-118">For a code example of</span></span>                                                         | <span data-ttu-id="674c5-119">Consulte</span><span class="sxs-lookup"><span data-stu-id="674c5-119">See</span></span>                                                                             |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="674c5-120">Enumerando todas as tarefas na pasta tarefas agendadas do computador local</span><span class="sxs-lookup"><span data-stu-id="674c5-120">Enumerating all the tasks in the Scheduled Tasks folder of the local computer</span></span> | [<span data-ttu-id="674c5-121">Exemplo de código C/C++: enumerando tarefas</span><span class="sxs-lookup"><span data-stu-id="674c5-121">C/C++ Code Example: Enumerating Tasks</span></span>](c-c-code-example-enumerating-tasks.md) |



 

## <a name="related-topics"></a><span data-ttu-id="674c5-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="674c5-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="674c5-123">Exemplos de Agendador de Tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="674c5-123">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 