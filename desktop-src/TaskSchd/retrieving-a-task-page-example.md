---
title: Recuperando um exemplo de página de tarefa
description: Para recuperar uma página de tarefas, você deve chamar ITask QueryInterface para recuperar a interface IProvideTaskPage e, em seguida, chamar IProvideTaskPage GetPage. O método GetPage retorna um identificador para a página, que pode ser usado para exibir a página solicitada.
ms.assetid: 97525419-c480-465a-97c6-e701043c0af2
keywords:
- Recuperando a página de tarefas Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd570edf3309b9b9ff0eada291d02a10850885ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007715"
---
# <a name="retrieving-a-task-page-example"></a><span data-ttu-id="ae33e-105">Recuperando um exemplo de página de tarefa</span><span class="sxs-lookup"><span data-stu-id="ae33e-105">Retrieving a Task Page Example</span></span>

<span data-ttu-id="ae33e-106">Para recuperar uma página de tarefas, você deve chamar **ITask:: QueryInterface** para recuperar a interface [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) e, em seguida, chamar [**IProvideTaskPage:: GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage).</span><span class="sxs-lookup"><span data-stu-id="ae33e-106">To retrieve a task page you must call **ITask::QueryInterface** to retrieve the [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) interface, then call [**IProvideTaskPage::GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage).</span></span> <span data-ttu-id="ae33e-107">O método **GetPage** retorna um identificador para a página, que pode ser usado para exibir a página solicitada.</span><span class="sxs-lookup"><span data-stu-id="ae33e-107">The **GetPage** method returns a handle to the page, which can then be used to display the page you requested.</span></span>

> [!Note]  
> <span data-ttu-id="ae33e-108">No exemplo de código a seguir, todas as interfaces são lançadas depois que elas não são mais necessárias.</span><span class="sxs-lookup"><span data-stu-id="ae33e-108">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="ae33e-109">O procedimento a seguir descreve como criar um novo gatilho.</span><span class="sxs-lookup"><span data-stu-id="ae33e-109">The following procedure describes how to create a new trigger.</span></span>

<span data-ttu-id="ae33e-110">**Para criar um novo gatilho**</span><span class="sxs-lookup"><span data-stu-id="ae33e-110">**To create a new trigger**</span></span>

1.  <span data-ttu-id="ae33e-111">Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="ae33e-111">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="ae33e-112">(Este exemplo pressupõe que o serviço Agendador de Tarefas está em execução.)</span><span class="sxs-lookup"><span data-stu-id="ae33e-112">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="ae33e-113">Chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto Task.</span><span class="sxs-lookup"><span data-stu-id="ae33e-113">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="ae33e-114">(Observe que este exemplo obtém a tarefa "Test Task".)</span><span class="sxs-lookup"><span data-stu-id="ae33e-114">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="ae33e-115">Chame **ITask:: QueryInterface** para recuperar a interface [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) e [**IProvideTaskPage:: GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) para recuperar a página.</span><span class="sxs-lookup"><span data-stu-id="ae33e-115">Call **ITask::QueryInterface** to retrieve the [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) interface and [**IProvideTaskPage::GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) to retrieve the page.</span></span>
4.  <span data-ttu-id="ae33e-116">Usando o identificador de página retornado, exiba a página.</span><span class="sxs-lookup"><span data-stu-id="ae33e-116">Using the returned page handle, display the page.</span></span>



| <span data-ttu-id="ae33e-117">Para obter um exemplo de código de</span><span class="sxs-lookup"><span data-stu-id="ae33e-117">For a code example of</span></span>                                   | <span data-ttu-id="ae33e-118">Consulte</span><span class="sxs-lookup"><span data-stu-id="ae33e-118">See</span></span>                                                                   |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="ae33e-119">Recuperando e exibindo a página de tarefas de uma tarefa conhecida</span><span class="sxs-lookup"><span data-stu-id="ae33e-119">Retrieving and displaying the Task page of a known task</span></span> | [<span data-ttu-id="ae33e-120">Recuperando uma página de tarefas</span><span class="sxs-lookup"><span data-stu-id="ae33e-120">Retrieving a Task Page</span></span>](c-c-code-example-retrieving-a-task-page.md) |



 

## <a name="related-topics"></a><span data-ttu-id="ae33e-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ae33e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae33e-122">Exemplos de Agendador de Tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="ae33e-122">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 