---
title: Criando uma tarefa usando o exemplo NewWorkItem
description: Ao criar uma tarefa, você usará duas interfaces de Agendador de Tarefas ITaskScheduler e ITask.
ms.assetid: 1cbdba6a-e017-4f00-87cb-970686a69e0a
keywords:
- criando itens de trabalho Agendador de Tarefas
- Agendador de Tarefas de itens de trabalho, criando tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4e0f05e76ea54b57a101e31515fe089c5f445c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294288"
---
# <a name="creating-a-task-using-newworkitem-example"></a><span data-ttu-id="0440f-105">Criando uma tarefa usando o exemplo NewWorkItem</span><span class="sxs-lookup"><span data-stu-id="0440f-105">Creating a Task Using NewWorkItem Example</span></span>

<span data-ttu-id="0440f-106">Ao criar uma tarefa, você usará duas interfaces Agendador de Tarefas: [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) e [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span><span class="sxs-lookup"><span data-stu-id="0440f-106">When creating a task, you will use two Task Scheduler interfaces: [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) and [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span></span> <span data-ttu-id="0440f-107">Você deve fornecer um nome exclusivo para a tarefa, o identificador de classe do objeto de tarefa e o identificador de interface de **ITask**.</span><span class="sxs-lookup"><span data-stu-id="0440f-107">You must provide a unique name for the task, the class identifier of the task object, and the interface identifier of **ITask**.</span></span> <span data-ttu-id="0440f-108">O identificador de classe e o identificador de interface são mostrados no exemplo de código após este tópico.</span><span class="sxs-lookup"><span data-stu-id="0440f-108">The class identifier and interface identifier are shown in the code example following this topic.</span></span>

> [!Note]  
> <span data-ttu-id="0440f-109">Você também pode criar uma tarefa chamando [**ITaskScheduler:: AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem).</span><span class="sxs-lookup"><span data-stu-id="0440f-109">You can also create a task by calling [**ITaskScheduler::AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem).</span></span> <span data-ttu-id="0440f-110">Quando você faz essa rota, é sua responsabilidade criar uma instância do objeto de **tarefa** (que dá suporte à interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) ) e, em seguida, adicionar a tarefa com o nome que você fornecer.</span><span class="sxs-lookup"><span data-stu-id="0440f-110">When you take this route, it is your responsibility to create an instance of the **Task** object (which supports the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface) and then add the task with the name you supply.</span></span>

 

> [!Note]  
> <span data-ttu-id="0440f-111">Por padrão, somente um membro do grupo Administradores, operadores de backup ou operadores de servidor pode criar tarefas no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0440f-111">By default, only a member of the Administrators, Backup Operators, or Server Operators group can create tasks on Windows Server 2003.</span></span> <span data-ttu-id="0440f-112">Um membro do grupo Administradores pode alterar o descritor de segurança da pasta de tarefas do Windows \\ para permitir que outras pessoas criem tarefas.</span><span class="sxs-lookup"><span data-stu-id="0440f-112">A member of the Administrators group may change the security descriptor of the Windows\\Task folder to let others create tasks.</span></span>

 

<span data-ttu-id="0440f-113">O nome que você fornece para a tarefa deve ser exclusivo na pasta tarefas agendadas.</span><span class="sxs-lookup"><span data-stu-id="0440f-113">The name you supply for the task must be unique within the Scheduled Tasks folder.</span></span> <span data-ttu-id="0440f-114">Se já existir uma tarefa com o mesmo nome, [**ITaskScheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) retornará o \_ arquivo de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="0440f-114">If a task with the same name already exists, [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) returns ERROR\_FILE\_EXISTS.</span></span> <span data-ttu-id="0440f-115">Se você receber esse valor de retorno, deverá especificar um nome diferente e tentar criar a tarefa novamente.</span><span class="sxs-lookup"><span data-stu-id="0440f-115">If you get this return value, you should specify a different name and attempt to create the task again.</span></span>

<span data-ttu-id="0440f-116">O procedimento a seguir descreve como criar uma nova tarefa de item de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0440f-116">The following procedure describes how to create a new work item task.</span></span>

<span data-ttu-id="0440f-117">**Para criar uma nova tarefa de item de trabalho**</span><span class="sxs-lookup"><span data-stu-id="0440f-117">**To create a new work item task**</span></span>

1.  <span data-ttu-id="0440f-118">Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="0440f-118">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="0440f-119">(Este exemplo pressupõe que o serviço Agendador de Tarefas está em execução.)</span><span class="sxs-lookup"><span data-stu-id="0440f-119">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="0440f-120">Chame [**ITaskScheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) para criar uma nova tarefa.</span><span class="sxs-lookup"><span data-stu-id="0440f-120">Call [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) to create a new task.</span></span> <span data-ttu-id="0440f-121">(Esse método retorna um ponteiro para uma interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .)</span><span class="sxs-lookup"><span data-stu-id="0440f-121">(This method returns a pointer to an [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.)</span></span>
3.  <span data-ttu-id="0440f-122">Salve a nova tarefa em disco chamando [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="0440f-122">Save the new task to disk by calling [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="0440f-123">(A interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) é uma interface com padrão com suporte da interface **ITask** .)</span><span class="sxs-lookup"><span data-stu-id="0440f-123">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface supported by the **ITask** interface.)</span></span>
4.  <span data-ttu-id="0440f-124">Chame **ITask:: Release** para liberar todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="0440f-124">Call **ITask::Release** to release all resources.</span></span> <span data-ttu-id="0440f-125">(Observe que [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) é um método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) herdado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span><span class="sxs-lookup"><span data-stu-id="0440f-125">(Note that [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="0440f-126">Para obter um exemplo de código de</span><span class="sxs-lookup"><span data-stu-id="0440f-126">For a code example of</span></span>  | <span data-ttu-id="0440f-127">Consulte</span><span class="sxs-lookup"><span data-stu-id="0440f-127">See</span></span>                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0440f-128">Criando uma única tarefa</span><span class="sxs-lookup"><span data-stu-id="0440f-128">Creating a single task</span></span> | [<span data-ttu-id="0440f-129">Exemplo de código C/C++: criando uma tarefa usando NewWorkItem</span><span class="sxs-lookup"><span data-stu-id="0440f-129">C/C++ Code Example: Creating a Task Using NewWorkItem</span></span>](c-c-code-example-creating-a-task-using-newworkitem.md) |



 

## <a name="related-topics"></a><span data-ttu-id="0440f-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0440f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0440f-131">Exemplos de Agendador de Tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="0440f-131">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 