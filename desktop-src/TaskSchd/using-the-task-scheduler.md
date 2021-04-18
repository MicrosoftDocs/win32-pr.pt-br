---
title: Usando o Agendador de Tarefas
description: Esta seção contém exemplos de código que ilustram como a API de Agendador de Tarefas é usada e exemplos de XML que mostram como as tarefas são definidas no esquema de Agendador de Tarefas.
ms.assetid: 6346cbd3-b584-47b4-8313-7830f7fd77b3
keywords:
- Agendador de Tarefas de gatilhos, exemplos
- Iniciando uma tarefa Agendador de Tarefas
- Criando tarefas Agendador de Tarefas
- Agendador de Tarefas Agendador de Tarefas, usando
- Exemplos de Agendador de Tarefas Agendador de Tarefas
- Agendador de Tarefas Agendador de Tarefas, exemplos consulte Agendador de Tarefas exemplos Agendador de Tarefas
- exemplos Agendador de Tarefas consulte Agendador de Tarefas exemplos Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f81dda9551917b8f6345248a316bd5941de53f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105758389"
---
# <a name="using-the-task-scheduler"></a><span data-ttu-id="5e08c-110">Usando o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="5e08c-110">Using the Task Scheduler</span></span>

<span data-ttu-id="5e08c-111">Esta seção contém exemplos de código que ilustram como a API de Agendador de Tarefas é usada e exemplos de XML que mostram como as tarefas são definidas no esquema de Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="5e08c-111">This section contains code examples that illustrate how the Task Scheduler API is used and XML examples that show how tasks are defined in the Task Scheduler schema.</span></span> <span data-ttu-id="5e08c-112">A maioria desses exemplos são códigos autônomos que podem ser executados de forma independente ou colados em um aplicativo maior e modificados para os requisitos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5e08c-112">Most of these examples are stand-alone code that can be run independently, or pasted into a larger application and modified to the requirements of the application.</span></span>

<span data-ttu-id="5e08c-113">A tabela a seguir lista os exemplos de Agendador de Tarefas 2,0 incluídos nesta seção.</span><span class="sxs-lookup"><span data-stu-id="5e08c-113">The following table lists Task Scheduler 2.0 examples included in this section.</span></span>



| <span data-ttu-id="5e08c-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5e08c-114">Example</span></span>                                                                                                    | <span data-ttu-id="5e08c-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e08c-115">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e08c-116">Iniciando um executável em um horário específico</span><span class="sxs-lookup"><span data-stu-id="5e08c-116">Starting an Executable at a Specific Time</span></span>](starting-an-executable-at-a-spcific-time.md)                  | <span data-ttu-id="5e08c-117">Define uma tarefa que inicia o bloco de notas em um horário especificado.</span><span class="sxs-lookup"><span data-stu-id="5e08c-117">Defines a task that starts Notepad at a specified time.</span></span>                                |
| [<span data-ttu-id="5e08c-118">Iniciando um executável diariamente</span><span class="sxs-lookup"><span data-stu-id="5e08c-118">Starting an Executable Daily</span></span>](starting-an-executable-daily.md)                                           | <span data-ttu-id="5e08c-119">Define uma tarefa que inicia o bloco de notas diariamente.</span><span class="sxs-lookup"><span data-stu-id="5e08c-119">Defines a task that starts Notepad daily.</span></span>                                              |
| [<span data-ttu-id="5e08c-120">Iniciando um executável na inicialização do sistema</span><span class="sxs-lookup"><span data-stu-id="5e08c-120">Starting an Executable on System Boot</span></span>](starting-an-executable-on-system-boot.md)                         | <span data-ttu-id="5e08c-121">Define uma tarefa que inicia o bloco de notas quando o sistema é inicializado.</span><span class="sxs-lookup"><span data-stu-id="5e08c-121">Defines a task that starts Notepad when the system is booted.</span></span>                          |
| [<span data-ttu-id="5e08c-122">Iniciando um executável semanalmente</span><span class="sxs-lookup"><span data-stu-id="5e08c-122">Starting an Executable Weekly</span></span>](starting-an-executable-weekly.md)                                         | <span data-ttu-id="5e08c-123">Define uma tarefa que inicia o bloco de notas semanalmente.</span><span class="sxs-lookup"><span data-stu-id="5e08c-123">Defines a task that starts Notepad on a weekly basis.</span></span>                                  |
| [<span data-ttu-id="5e08c-124">Iniciando um executável quando uma tarefa é registrada</span><span class="sxs-lookup"><span data-stu-id="5e08c-124">Starting an Executable When a Task is Registered</span></span>](starting-an-executable-when-a-task-is-registered.md)   | <span data-ttu-id="5e08c-125">Define uma tarefa que inicia o bloco de notas quando a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="5e08c-125">Defines a task that starts Notepad when the task is registered.</span></span>                        |
| [<span data-ttu-id="5e08c-126">Iniciando um executável quando um usuário faz logon</span><span class="sxs-lookup"><span data-stu-id="5e08c-126">Starting an Executable When a User Logs On</span></span>](starting-an-executable-when-a-user-logs-on.md)               | <span data-ttu-id="5e08c-127">Define uma tarefa que inicia o bloco de notas quando um usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="5e08c-127">Defines a task that starts Notepad when a user logs on.</span></span>                                |
| [<span data-ttu-id="5e08c-128">Enumerando tarefas e exibindo informações de tarefas</span><span class="sxs-lookup"><span data-stu-id="5e08c-128">Enumerating Tasks and Displaying Task Information</span></span>](enumerating-tasks-and-displaying-task-information.md) | <span data-ttu-id="5e08c-129">Enumera todas as tarefas no computador local e exibe o estado de cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="5e08c-129">Enumerates through all the tasks on the local computer and displays each task's state.</span></span> |



 

<span data-ttu-id="5e08c-130">A tabela a seguir lista os exemplos de Agendador de Tarefas 1,0 incluídos nesta seção.</span><span class="sxs-lookup"><span data-stu-id="5e08c-130">The following table lists Task Scheduler 1.0 examples included in this section.</span></span> 

| <span data-ttu-id="5e08c-131">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5e08c-131">Example</span></span>                                                                                    | <span data-ttu-id="5e08c-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e08c-132">Description</span></span>                                                                                   |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e08c-133">Criando uma tarefa usando o exemplo NewWorkItem</span><span class="sxs-lookup"><span data-stu-id="5e08c-133">Creating a Task Using NewWorkItem Example</span></span>](creating-a-task-using-newworkitem-example.md) | <span data-ttu-id="5e08c-134">Cria uma nova tarefa.</span><span class="sxs-lookup"><span data-stu-id="5e08c-134">Creates a new task.</span></span>                                                                           |
| [<span data-ttu-id="5e08c-135">Exemplo de enumeração de tarefas</span><span class="sxs-lookup"><span data-stu-id="5e08c-135">Enumerating Tasks Example</span></span>](enumerating-tasks-example.md)                                 | <span data-ttu-id="5e08c-136">Enumera todas as tarefas no computador local.</span><span class="sxs-lookup"><span data-stu-id="5e08c-136">Enumerates all the tasks on the local computer.</span></span>                                               |
| [<span data-ttu-id="5e08c-137">Iniciando um exemplo de tarefa</span><span class="sxs-lookup"><span data-stu-id="5e08c-137">Starting a Task Example</span></span>](starting-a-task-example.md)                                     | <span data-ttu-id="5e08c-138">Inicia uma tarefa conhecida.</span><span class="sxs-lookup"><span data-stu-id="5e08c-138">Starts a known task.</span></span>                                                                          |
| [<span data-ttu-id="5e08c-139">Editando um item de trabalho usando páginas de propriedades</span><span class="sxs-lookup"><span data-stu-id="5e08c-139">Editing a Work Item using Property Pages</span></span>](editing-a-work-item-using-property-pages.md)   | <span data-ttu-id="5e08c-140">Exibe as páginas de propriedades de uma tarefa para edição.</span><span class="sxs-lookup"><span data-stu-id="5e08c-140">Displays the property pages of a task for editing.</span></span>                                            |
| [<span data-ttu-id="5e08c-141">Recuperando exemplos de propriedade de item de trabalho</span><span class="sxs-lookup"><span data-stu-id="5e08c-141">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md)       | <span data-ttu-id="5e08c-142">Um conjunto de exemplos que mostram como recuperar propriedades que se aplicam a todos os tipos de itens de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5e08c-142">A set of examples that show how to retrieve properties that apply to all types of work items.</span></span> |
| [<span data-ttu-id="5e08c-143">Definindo exemplos de propriedade de item de trabalho</span><span class="sxs-lookup"><span data-stu-id="5e08c-143">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)             | <span data-ttu-id="5e08c-144">Um conjunto de exemplos que mostram como definir propriedades que se aplicam a todos os tipos de itens de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5e08c-144">A set of examples that show how to set properties that apply to all types of work items.</span></span>      |
| [<span data-ttu-id="5e08c-145">Recuperando exemplos de propriedade de tarefa</span><span class="sxs-lookup"><span data-stu-id="5e08c-145">Retrieving Task Property Examples</span></span>](retrieving-task-property-examples.md)                 | <span data-ttu-id="5e08c-146">Um conjunto de exemplos que mostram como recuperar propriedades exclusivas de tarefas.</span><span class="sxs-lookup"><span data-stu-id="5e08c-146">A set of examples that show how to retrieve properties unique to tasks.</span></span>                       |
| [<span data-ttu-id="5e08c-147">Definindo exemplos de propriedade de tarefa</span><span class="sxs-lookup"><span data-stu-id="5e08c-147">Setting Task Property Examples</span></span>](setting-task-property-examples.md)                       | <span data-ttu-id="5e08c-148">Um conjunto de exemplos que mostram como definir propriedades exclusivas para tarefas.</span><span class="sxs-lookup"><span data-stu-id="5e08c-148">A set of examples that show how to set properties unique to tasks.</span></span>                            |
| [<span data-ttu-id="5e08c-149">Recuperando um exemplo de página de tarefa</span><span class="sxs-lookup"><span data-stu-id="5e08c-149">Retrieving a Task Page Example</span></span>](retrieving-a-task-page-example.md)                       | <span data-ttu-id="5e08c-150">Recupera e exibe a página de tarefas geral de uma tarefa conhecida.</span><span class="sxs-lookup"><span data-stu-id="5e08c-150">Retrieves and displays the general task page of a known task.</span></span>                                 |
| [<span data-ttu-id="5e08c-151">Criando um novo gatilho</span><span class="sxs-lookup"><span data-stu-id="5e08c-151">Creating a New Trigger</span></span>](creating-a-new-trigger.md)                                       | <span data-ttu-id="5e08c-152">Cria um novo gatilho para uma tarefa conhecida.</span><span class="sxs-lookup"><span data-stu-id="5e08c-152">Creates a new trigger for a known task.</span></span>                                                       |
| [<span data-ttu-id="5e08c-153">Criando um exemplo de gatilho de ociosidade</span><span class="sxs-lookup"><span data-stu-id="5e08c-153">Creating an Idle Trigger Example</span></span>](creating-an-idle-trigger-example.md)                   | <span data-ttu-id="5e08c-154">Cria um gatilho ocioso baseado em evento para uma tarefa conhecida.</span><span class="sxs-lookup"><span data-stu-id="5e08c-154">Creates an event-based idle trigger for a known task.</span></span>                                         |
| [<span data-ttu-id="5e08c-155">Finalizando um exemplo de tarefa</span><span class="sxs-lookup"><span data-stu-id="5e08c-155">Terminating a Task Example</span></span>](terminating-a-task-example.md)                               | <span data-ttu-id="5e08c-156">Encerra uma tarefa enquanto ela está em execução.</span><span class="sxs-lookup"><span data-stu-id="5e08c-156">Terminates a task while it is running.</span></span>                                                        |
| [<span data-ttu-id="5e08c-157">Exemplo de recuperação de cadeias de caracteres de gatilho</span><span class="sxs-lookup"><span data-stu-id="5e08c-157">Retrieving Trigger Strings Example</span></span>](retrieving-trigger-strings-example.md)               | <span data-ttu-id="5e08c-158">Recupera a cadeia de caracteres do gatilho de todos os gatilhos associados a uma tarefa conhecida.</span><span class="sxs-lookup"><span data-stu-id="5e08c-158">Retrieves the trigger string of all triggers associated with a known task.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="5e08c-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5e08c-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e08c-160">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="5e08c-160">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="5e08c-161">Sobre o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="5e08c-161">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 




