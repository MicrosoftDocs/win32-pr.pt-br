---
title: Editando um item de trabalho usando páginas de propriedades
description: Você pode editar as propriedades de um item de trabalho usando a interface gráfica do usuário fornecida pelo serviço Agendador de Tarefas.
ms.assetid: 2d7992ce-fa70-41cc-a8e7-74687171537f
keywords:
- editando itens de trabalho Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0958c361f1c076e8ebed6a7e645bf67694a1d01
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641271"
---
# <a name="editing-a-work-item-using-property-pages"></a><span data-ttu-id="446f2-104">Editando um item de trabalho usando páginas de propriedades</span><span class="sxs-lookup"><span data-stu-id="446f2-104">Editing a Work Item using Property Pages</span></span>

<span data-ttu-id="446f2-105">Você pode editar as propriedades de um item de trabalho usando a interface gráfica do usuário fornecida pelo serviço Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="446f2-105">You can edit the properties of a work item by using the graphic user interface provided by the Task Scheduler Service.</span></span> <span data-ttu-id="446f2-106">(Atualmente, os únicos itens de trabalho válidos são tarefas.)</span><span class="sxs-lookup"><span data-stu-id="446f2-106">(Currently, the only valid work items are tasks.)</span></span>

<span data-ttu-id="446f2-107">O procedimento a seguir descreve como editar uma tarefa usando suas páginas de propriedades.</span><span class="sxs-lookup"><span data-stu-id="446f2-107">The following procedure describes how to edit a task using its property pages.</span></span>

<span data-ttu-id="446f2-108">**Para editar uma tarefa usando suas páginas de propriedades**</span><span class="sxs-lookup"><span data-stu-id="446f2-108">**To edit a task using its property pages**</span></span>

1.  <span data-ttu-id="446f2-109">Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="446f2-109">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="446f2-110">(Esses exemplos pressupõem que o serviço Agendador de Tarefas está em execução.)</span><span class="sxs-lookup"><span data-stu-id="446f2-110">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="446f2-111">Chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto Task.</span><span class="sxs-lookup"><span data-stu-id="446f2-111">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="446f2-112">(Observe que as tarefas são atualmente o único tipo válido de item de trabalho.)</span><span class="sxs-lookup"><span data-stu-id="446f2-112">(Note that tasks are currently the only valid type of work item.)</span></span>
3.  <span data-ttu-id="446f2-113">Chame [**IScheduledWorkItem:: EditWorkItem**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-editworkitem) para exibir as páginas de propriedades da tarefa.</span><span class="sxs-lookup"><span data-stu-id="446f2-113">Call [**IScheduledWorkItem::EditWorkItem**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-editworkitem) to display the property pages for the task.</span></span>
4.  <span data-ttu-id="446f2-114">Edite as propriedades da tarefa conforme necessário e clique em OK para aceitar os novos valores e remover as páginas de propriedades exibidas.</span><span class="sxs-lookup"><span data-stu-id="446f2-114">Edit the properties of the task as needed, then click OK to accept the new values and remove the displayed property pages.</span></span>



| <span data-ttu-id="446f2-115">Para obter um exemplo de código de</span><span class="sxs-lookup"><span data-stu-id="446f2-115">For a code example of</span></span>                                                                                      | <span data-ttu-id="446f2-116">Consulte</span><span class="sxs-lookup"><span data-stu-id="446f2-116">See</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="446f2-117">Exibindo as páginas de propriedades de uma tarefa conhecida e permitindo que um usuário edite as propriedades do item de trabalho</span><span class="sxs-lookup"><span data-stu-id="446f2-117">Displaying the property pages for a known task and allowing a user to edit the properties of the work item</span></span> | [<span data-ttu-id="446f2-118">Exemplo de código do C/C++: editando um item de trabalho</span><span class="sxs-lookup"><span data-stu-id="446f2-118">C/C++ Code Example: Editing a Work Item</span></span>](c-c-code-example-editing-a-work-item.md) |



 

## <a name="related-topics"></a><span data-ttu-id="446f2-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="446f2-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="446f2-120">Exemplos de Agendador de Tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="446f2-120">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 