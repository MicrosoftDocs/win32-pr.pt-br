---
title: Adicionando itens de trabalho
description: Há duas maneiras de adicionar itens de trabalho ao Tasksfolder agendado. Você pode criar um novo item de trabalho dentro da pasta ou pode adicionar um item de trabalho existente à pasta.
ms.assetid: fad5e813-a2e9-40af-97a9-4f92debf1808
keywords:
- Agendador de Tarefas de itens de trabalho, adicionando
- tarefas Agendador de Tarefas, adicionando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 722f776fd36933995cfd9b5a85612b52dae63f7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105758395"
---
# <a name="adding-work-items"></a><span data-ttu-id="c6125-106">Adicionando itens de trabalho</span><span class="sxs-lookup"><span data-stu-id="c6125-106">Adding Work Items</span></span>

<span data-ttu-id="c6125-107">Há duas maneiras de adicionar [*itens de trabalho*](w.md) ao [*Tasksfolder agendado*](s.md).</span><span class="sxs-lookup"><span data-stu-id="c6125-107">There are two ways to add [*work items*](w.md) to the [*Scheduled Tasksfolder*](s.md).</span></span> <span data-ttu-id="c6125-108">Você pode criar um novo item de trabalho dentro da pasta ou pode adicionar um item de trabalho existente à pasta.</span><span class="sxs-lookup"><span data-stu-id="c6125-108">You can create a new work item within the folder, or you can add an existing work item to the folder.</span></span>

> [!Note]  
> <span data-ttu-id="c6125-109">Atualmente, somente objetos de tarefa podem ser adicionados à pasta tarefas agendadas.</span><span class="sxs-lookup"><span data-stu-id="c6125-109">Currently, only task objects can be added to the Scheduled Tasks folder.</span></span> <span data-ttu-id="c6125-110">Ao adicionar uma tarefa, você deve saber os identificadores para a classe de tarefa e a interface de tarefa [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span><span class="sxs-lookup"><span data-stu-id="c6125-110">When adding a task, you must know the identifiers for the task class and the task interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span></span>

 

<span data-ttu-id="c6125-111">Você cria novos itens de trabalho chamando o método [**ITaskScheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) .</span><span class="sxs-lookup"><span data-stu-id="c6125-111">You create new work items by calling the [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) method.</span></span> <span data-ttu-id="c6125-112">Esse método cria um novo objeto de item de trabalho usando o nome que você fornece e adiciona o item de trabalho à pasta tarefas agendadas.</span><span class="sxs-lookup"><span data-stu-id="c6125-112">This method creates a new work item object using the name that you provide and adds the work item to the Scheduled Tasks folder.</span></span> <span data-ttu-id="c6125-113">Quando você cria um novo item de trabalho, o Agendador de Tarefas aloca a memória necessária para o novo objeto.</span><span class="sxs-lookup"><span data-stu-id="c6125-113">When you create a new work item, the Task Scheduler allocates the memory that is required for the new object.</span></span>

<span data-ttu-id="c6125-114">Para adicionar itens de trabalho existentes à pasta tarefas agendadas, chame o método [**ITaskScheduler:: AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) .</span><span class="sxs-lookup"><span data-stu-id="c6125-114">To add existing work items to the Scheduled Tasks folder, call the [**ITaskScheduler::AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) method.</span></span> <span data-ttu-id="c6125-115">Ao chamar esse método, você deve criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="c6125-115">When you call this method, you must create the object.</span></span>

<span data-ttu-id="c6125-116">Os nomes fornecidos para itens de trabalho devem ser exclusivos na pasta tarefas agendadas.</span><span class="sxs-lookup"><span data-stu-id="c6125-116">The names you supply for work items must be unique within the Scheduled Tasks folder.</span></span> <span data-ttu-id="c6125-117">Se já existir um item de trabalho com o mesmo nome quando você chamar o método [**ITaskScheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) ou o método [**ITaskScheduler:: AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) , o método retornará um erro de **\_ arquivo \_ de erro** .</span><span class="sxs-lookup"><span data-stu-id="c6125-117">If a work item with the same name already exists when you call either the [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) method or the [**ITaskScheduler::AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) method, the method returns an **ERROR\_FILE\_EXISTS** error.</span></span> <span data-ttu-id="c6125-118">Para obter mais informações, consulte [criando uma tarefa usando o exemplo NewWorkItem](creating-a-task-using-newworkitem-example.md).</span><span class="sxs-lookup"><span data-stu-id="c6125-118">For more information, see [Creating a Task Using NewWorkItem Example](creating-a-task-using-newworkitem-example.md).</span></span>

 

 




