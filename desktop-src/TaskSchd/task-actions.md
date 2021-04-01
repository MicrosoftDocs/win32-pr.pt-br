---
title: Ações de tarefas
description: Os itens de trabalho executados por uma tarefa são chamados de ações. Uma tarefa pode ter uma única ação ou um máximo de 32 ações. Lembre-se de que quando várias ações forem especificadas, elas serão executadas em sequência.
ms.assetid: 4cbe739d-4c4e-4469-8289-4be41b93950c
keywords:
- ações Agendador de Tarefas
- ações Agendador de Tarefas, descritas
- ações Agendador de Tarefas, executar ação
- ações Agendador de Tarefas, ação do manipulador COM
- executar Agendador de Tarefas de ação
- Ação do manipulador COM Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71003e2cea5febfab61617451f3b6ebef4a244a3
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "103639757"
---
# <a name="task-actions"></a><span data-ttu-id="1470f-111">Ações de tarefas</span><span class="sxs-lookup"><span data-stu-id="1470f-111">Task Actions</span></span>

<span data-ttu-id="1470f-112">Os itens de trabalho executados por uma tarefa são chamados de ações.</span><span class="sxs-lookup"><span data-stu-id="1470f-112">The work items performed by a task are called actions.</span></span> <span data-ttu-id="1470f-113">Uma tarefa pode ter uma única ação ou um máximo de 32 ações.</span><span class="sxs-lookup"><span data-stu-id="1470f-113">A task can have a single action or a maximum of 32 actions.</span></span> <span data-ttu-id="1470f-114">Lembre-se de que quando várias ações forem especificadas, elas serão executadas em sequência.</span><span class="sxs-lookup"><span data-stu-id="1470f-114">Be aware that when multiple actions are specified, they are executed sequentially.</span></span>

## <a name="types-of-actions"></a><span data-ttu-id="1470f-115">Tipos de ações</span><span class="sxs-lookup"><span data-stu-id="1470f-115">Types of Actions</span></span>

<span data-ttu-id="1470f-116">A tabela de ações a seguir descreve o tipo de trabalho ou ações que podem ser realizadas por uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="1470f-116">The following table of actions describes the type of work or actions that can be accomplished by a task.</span></span>

| <span data-ttu-id="1470f-117">Tipo de ação</span><span class="sxs-lookup"><span data-stu-id="1470f-117">Type of Action</span></span>      | <span data-ttu-id="1470f-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="1470f-118">Description</span></span>                                                             |
|---------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="1470f-119">Ação do commanipulador</span><span class="sxs-lookup"><span data-stu-id="1470f-119">ComHandler Action</span></span>   | <span data-ttu-id="1470f-120">Essa ação dispara um manipulador COM.</span><span class="sxs-lookup"><span data-stu-id="1470f-120">This action fires a COM handler.</span></span>                                        |
| <span data-ttu-id="1470f-121">Ação de exec</span><span class="sxs-lookup"><span data-stu-id="1470f-121">Exec Action</span></span>         | <span data-ttu-id="1470f-122">Essa ação executa uma operação de linha de comando, como iniciar o bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="1470f-122">This action executes a command-line operation such as starting Notepad.</span></span> |
| <span data-ttu-id="1470f-123">Ação de email</span><span class="sxs-lookup"><span data-stu-id="1470f-123">E-mail Action</span></span>       | <span data-ttu-id="1470f-124">Essa ação envia um email quando uma tarefa é disparada.</span><span class="sxs-lookup"><span data-stu-id="1470f-124">This action sends an email when a task is triggered.</span></span>                    |
| <span data-ttu-id="1470f-125">Mostrar ação de mensagem</span><span class="sxs-lookup"><span data-stu-id="1470f-125">Show Message Action</span></span> | <span data-ttu-id="1470f-126">Essa ação mostra uma caixa de mensagem com uma mensagem e um título especificados.</span><span class="sxs-lookup"><span data-stu-id="1470f-126">This action shows a message box with a specified message and title.</span></span>     |



 

## <a name="specifying-actions"></a><span data-ttu-id="1470f-127">Especificando ações</span><span class="sxs-lookup"><span data-stu-id="1470f-127">Specifying Actions</span></span>

<span data-ttu-id="1470f-128">As ações de uma tarefa são especificadas quando a tarefa é definida e armazenada em uma coleção de ações usadas pelo serviço de Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="1470f-128">The actions of a task are specified when the task is defined and stored in a collection of actions used by the Task Scheduler service.</span></span> <span data-ttu-id="1470f-129">A tabela a seguir lista links para tópicos de referência para as APIs e elementos XML associados a ações.</span><span class="sxs-lookup"><span data-stu-id="1470f-129">The following table lists links to reference topics for the APIs and XML elements that are associated with actions.</span></span>

<span data-ttu-id="1470f-130">Para obter mais informações e exemplos sobre como usar as interfaces de Agendador de Tarefas, os objetos de script e o XML, consulte [usando o Agendador de tarefas](using-the-task-scheduler.md).</span><span class="sxs-lookup"><span data-stu-id="1470f-130">For more information and examples about how to use the Task Scheduler interfaces, scripting objects, and XML, see [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

### <a name="interface-apis-for-c-development"></a><span data-ttu-id="1470f-131">APIs de interface para desenvolvimento em C++</span><span class="sxs-lookup"><span data-stu-id="1470f-131">Interface APIs for C++ Development</span></span>



| <span data-ttu-id="1470f-132">API</span><span class="sxs-lookup"><span data-stu-id="1470f-132">API</span></span>                                                                    | <span data-ttu-id="1470f-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="1470f-133">Description</span></span>                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="1470f-134">**Propriedade Actions de ITaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="1470f-134">**Actions Property of ITaskDefinition**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) | <span data-ttu-id="1470f-135">Obtém ou define as ações executadas pela tarefa.</span><span class="sxs-lookup"><span data-stu-id="1470f-135">Gets or sets the actions performed by the task.</span></span>              |
| [<span data-ttu-id="1470f-136">**IActionCollection**</span><span class="sxs-lookup"><span data-stu-id="1470f-136">**IActionCollection**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection)                         | <span data-ttu-id="1470f-137">Contém as ações executadas pela tarefa.</span><span class="sxs-lookup"><span data-stu-id="1470f-137">Contains the actions performed by the task.</span></span>                  |
| [<span data-ttu-id="1470f-138">**IComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="1470f-138">**IComHandlerAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)                         | <span data-ttu-id="1470f-139">Representa uma ação que dispara um manipulador.</span><span class="sxs-lookup"><span data-stu-id="1470f-139">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="1470f-140">**IExecAction**</span><span class="sxs-lookup"><span data-stu-id="1470f-140">**IExecAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iexecaction)                                     | <span data-ttu-id="1470f-141">Representa uma ação que executa uma operação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="1470f-141">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="1470f-142">**IEmailAction**</span><span class="sxs-lookup"><span data-stu-id="1470f-142">**IEmailAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iemailaction)                                   | <span data-ttu-id="1470f-143">Representa uma ação que envia uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="1470f-143">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="1470f-144">**IShowMessageAction**</span><span class="sxs-lookup"><span data-stu-id="1470f-144">**IShowMessageAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction)                       | <span data-ttu-id="1470f-145">Representa uma ação que mostra uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="1470f-145">Represents an action that shows a message box.</span></span>               |



 

### <a name="scripting-object-apis-for-scripting-development"></a><span data-ttu-id="1470f-146">APIs de objeto de script para desenvolvimento de scripts</span><span class="sxs-lookup"><span data-stu-id="1470f-146">Scripting Object APIs for Scripting Development</span></span>



| <span data-ttu-id="1470f-147">API</span><span class="sxs-lookup"><span data-stu-id="1470f-147">API</span></span>                                                      | <span data-ttu-id="1470f-148">Descrição</span><span class="sxs-lookup"><span data-stu-id="1470f-148">Description</span></span>                                                  |
|----------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="1470f-149">**TaskDefinition. Actions**</span><span class="sxs-lookup"><span data-stu-id="1470f-149">**TaskDefinition.Actions**</span></span>](taskdefinition-actions.md) | <span data-ttu-id="1470f-150">Obtém ou define as ações executadas pela tarefa.</span><span class="sxs-lookup"><span data-stu-id="1470f-150">Gets or sets the actions performed by the task.</span></span>              |
| [<span data-ttu-id="1470f-151">**Açãocollection**</span><span class="sxs-lookup"><span data-stu-id="1470f-151">**ActionCollection**</span></span>](actioncollection.md)             | <span data-ttu-id="1470f-152">Contém as ações executadas pela tarefa.</span><span class="sxs-lookup"><span data-stu-id="1470f-152">Contains the actions performed by the task.</span></span>                  |
| [<span data-ttu-id="1470f-153">**Comhandleaction**</span><span class="sxs-lookup"><span data-stu-id="1470f-153">**ComHandlerAction**</span></span>](comhandleraction.md)             | <span data-ttu-id="1470f-154">Representa uma ação que dispara um manipulador.</span><span class="sxs-lookup"><span data-stu-id="1470f-154">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="1470f-155">**Execaction**</span><span class="sxs-lookup"><span data-stu-id="1470f-155">**ExecAction**</span></span>](execaction.md)                         | <span data-ttu-id="1470f-156">Representa uma ação que executa uma operação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="1470f-156">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="1470f-157">**Emailaction**</span><span class="sxs-lookup"><span data-stu-id="1470f-157">**EmailAction**</span></span>](emailaction.md)                       | <span data-ttu-id="1470f-158">Representa uma ação que envia uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="1470f-158">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="1470f-159">**Permessageaction**</span><span class="sxs-lookup"><span data-stu-id="1470f-159">**ShowMessageAction**</span></span>](showmessageaction.md)           | <span data-ttu-id="1470f-160">Representa uma ação que mostra uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="1470f-160">Represents an action that shows a message box.</span></span>               |



 

### <a name="xml-elements"></a><span data-ttu-id="1470f-161">Elementos XML</span><span class="sxs-lookup"><span data-stu-id="1470f-161">XML Elements</span></span>



| <span data-ttu-id="1470f-162">Elemento</span><span class="sxs-lookup"><span data-stu-id="1470f-162">Element</span></span>                                                                    | <span data-ttu-id="1470f-163">Descrição</span><span class="sxs-lookup"><span data-stu-id="1470f-163">Description</span></span>                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="1470f-164">**Ações**</span><span class="sxs-lookup"><span data-stu-id="1470f-164">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)            | <span data-ttu-id="1470f-165">Define as ações executadas pela tarefa.</span><span class="sxs-lookup"><span data-stu-id="1470f-165">Defines the actions performed by the task.</span></span>                   |
| [<span data-ttu-id="1470f-166">**Commanipulador**</span><span class="sxs-lookup"><span data-stu-id="1470f-166">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md)   | <span data-ttu-id="1470f-167">Representa uma ação que dispara um manipulador.</span><span class="sxs-lookup"><span data-stu-id="1470f-167">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="1470f-168">**Exec**</span><span class="sxs-lookup"><span data-stu-id="1470f-168">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md)               | <span data-ttu-id="1470f-169">Representa uma ação que executa uma operação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="1470f-169">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="1470f-170">**SendEmail**</span><span class="sxs-lookup"><span data-stu-id="1470f-170">**SendEmail**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md)     | <span data-ttu-id="1470f-171">Representa uma ação que envia uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="1470f-171">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="1470f-172">**ShowMessage**</span><span class="sxs-lookup"><span data-stu-id="1470f-172">**ShowMessage**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | <span data-ttu-id="1470f-173">Representa uma ação que mostra uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="1470f-173">Represents an action that shows a message box.</span></span>               |



 

## <a name="using-variables-in-action-properties"></a><span data-ttu-id="1470f-174">Usando variáveis em Propriedades de ação</span><span class="sxs-lookup"><span data-stu-id="1470f-174">Using Variables in Action Properties</span></span>

<span data-ttu-id="1470f-175">Algumas propriedades de ação do tipo **BSTR** podem conter as variáveis $ (Arg0), $ (arg1),..., $ (Arg32) em seus valores de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1470f-175">Some action properties that are of type **BSTR** can contain $(Arg0), $(Arg1), ..., $(Arg32) variables in their string values.</span></span> <span data-ttu-id="1470f-176">Essas variáveis são substituídas pelos valores especificados no parâmetro *params* dos métodos [**IRegisteredTask:: Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) e [**IRegisteredTask:: RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) ou estão contidas no gatilho de evento para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="1470f-176">These variables are replaced with the values that are specified in the *params* parameter of the [**IRegisteredTask::Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) and [**IRegisteredTask::RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) methods or are contained within the event trigger for the task.</span></span> <span data-ttu-id="1470f-177">A tabela a seguir lista as propriedades de ação que podem usar variáveis em seus valores de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1470f-177">The following table lists the action properties that can use variables in their string values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1470f-178">Ação</span><span class="sxs-lookup"><span data-stu-id="1470f-178">Action</span></span></th>
<th><span data-ttu-id="1470f-179">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1470f-179">Properties</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1470f-180">Ação do manipulador COM</span><span class="sxs-lookup"><span data-stu-id="1470f-180">COM Handler Action</span></span></td>
<td><span data-ttu-id="1470f-181">C++:</span><span class="sxs-lookup"><span data-stu-id="1470f-181">C++:</span></span>
<ul>
<li><span data-ttu-id="1470f-182"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid"><strong>Propriedade ClassID de IComHandlerAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-182"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid"><strong>ClassId Property of IComHandlerAction</strong></a></span></span></li>
<li><span data-ttu-id="1470f-183"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data"><strong>Propriedade data de IComHandlerAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-183"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data"><strong>Data Property of IComHandlerAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="1470f-184">Script:</span><span class="sxs-lookup"><span data-stu-id="1470f-184">Scripting:</span></span>
<ul>
<li><span data-ttu-id="1470f-185"><a href="comhandleraction-classid.md"><strong>Comhandleaction. ClassID</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-185"><a href="comhandleraction-classid.md"><strong>ComHandlerAction.ClassId</strong></a></span></span></li>
<li><span data-ttu-id="1470f-186"><a href="comhandleraction-data.md"><strong>Comhandleaction. Data</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-186"><a href="comhandleraction-data.md"><strong>ComHandlerAction.Data</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1470f-187">Ação de email</span><span class="sxs-lookup"><span data-stu-id="1470f-187">Email Action</span></span></td>
<td><span data-ttu-id="1470f-188">C++:</span><span class="sxs-lookup"><span data-stu-id="1470f-188">C++:</span></span>
<ul>
<li><span data-ttu-id="1470f-189"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body"><strong>Propriedade Body de IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-189"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body"><strong>Body Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="1470f-190"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server"><strong>Propriedade de servidor de IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-190"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server"><strong>Server Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="1470f-191"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject"><strong>Propriedade Subject de IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-191"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject"><strong>Subject Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="1470f-192"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to"><strong>Para a propriedade de IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-192"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to"><strong>To Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="1470f-193"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc"><strong>Propriedade CC de IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-193"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc"><strong>Cc Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="1470f-194"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc"><strong>Propriedade BCC de IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-194"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc"><strong>Bcc Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="1470f-195"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto"><strong>Propriedade ReplyTo de IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-195"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto"><strong>ReplyTo Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="1470f-196"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from"><strong>Da propriedade de IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-196"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from"><strong>From Property of IEmailAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="1470f-197">Script:</span><span class="sxs-lookup"><span data-stu-id="1470f-197">Scripting:</span></span>
<ul>
<li><span data-ttu-id="1470f-198"><a href="emailaction-body.md"><strong>Emailaction. Body</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-198"><a href="emailaction-body.md"><strong>EmailAction.Body</strong></a></span></span></li>
<li><span data-ttu-id="1470f-199"><a href="emailaction-server.md"><strong>Emailaction. Server</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-199"><a href="emailaction-server.md"><strong>EmailAction.Server</strong></a></span></span></li>
<li><span data-ttu-id="1470f-200"><a href="emailaction-subject.md"><strong>Emailaction. Subject</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-200"><a href="emailaction-subject.md"><strong>EmailAction.Subject</strong></a></span></span></li>
<li><span data-ttu-id="1470f-201"><a href="emailaction-to.md"><strong>EmailAction.To</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-201"><a href="emailaction-to.md"><strong>EmailAction.To</strong></a></span></span></li>
<li><span data-ttu-id="1470f-202"><a href="emailaction-cc.md"><strong>EmailAction.Cc</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-202"><a href="emailaction-cc.md"><strong>EmailAction.Cc</strong></a></span></span></li>
<li><span data-ttu-id="1470f-203"><a href="emailaction-bcc.md"><strong>Emailaction. Bcc</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-203"><a href="emailaction-bcc.md"><strong>EmailAction.Bcc</strong></a></span></span></li>
<li><span data-ttu-id="1470f-204"><a href="emailaction-replyto.md"><strong>Emailaction. ReplyTo</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-204"><a href="emailaction-replyto.md"><strong>EmailAction.ReplyTo</strong></a></span></span></li>
<li><span data-ttu-id="1470f-205"><a href="emailaction-from.md"><strong>Emailaction. from</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-205"><a href="emailaction-from.md"><strong>EmailAction.From</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1470f-206">Ação de exec</span><span class="sxs-lookup"><span data-stu-id="1470f-206">Exec Action</span></span></td>
<td><span data-ttu-id="1470f-207">C++:</span><span class="sxs-lookup"><span data-stu-id="1470f-207">C++:</span></span>
<ul>
<li><span data-ttu-id="1470f-208"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments"><strong>Propriedade Arguments de IExecAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-208"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments"><strong>Arguments Property of IExecAction</strong></a></span></span></li>
<li><span data-ttu-id="1470f-209"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory"><strong>Propriedade WorkingDirectory de IExecAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-209"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory"><strong>WorkingDirectory Property of IExecAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="1470f-210">Script:</span><span class="sxs-lookup"><span data-stu-id="1470f-210">Scripting:</span></span>
<ul>
<li><span data-ttu-id="1470f-211"><a href="execaction-arguments.md"><strong>Argumentos execaction.</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-211"><a href="execaction-arguments.md"><strong>ExecAction.Arguments</strong></a></span></span></li>
<li><span data-ttu-id="1470f-212"><a href="execaction-workingdirectory.md"><strong>Execaction. WorkingDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-212"><a href="execaction-workingdirectory.md"><strong>ExecAction.WorkingDirectory</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1470f-213">Mostrar ação de mensagem</span><span class="sxs-lookup"><span data-stu-id="1470f-213">Show Message Action</span></span></td>
<td><span data-ttu-id="1470f-214">C++:</span><span class="sxs-lookup"><span data-stu-id="1470f-214">C++:</span></span>
<ul>
<li><span data-ttu-id="1470f-215"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title"><strong>Propriedade Title de IShowMessageAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-215"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title"><strong>Title Property of IShowMessageAction</strong></a></span></span></li>
<li><span data-ttu-id="1470f-216"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody"><strong>Propriedade MessageBody de IShowMessageAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-216"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody"><strong>MessageBody Property of IShowMessageAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="1470f-217">Script:</span><span class="sxs-lookup"><span data-stu-id="1470f-217">Scripting:</span></span>
<ul>
<li><span data-ttu-id="1470f-218"><a href="showmessageaction-title.md"><strong>Nome da mensagem. title</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-218"><a href="showmessageaction-title.md"><strong>ShowMessageAction.Title</strong></a></span></span></li>
<li><span data-ttu-id="1470f-219"><a href="showmessageaction-messagebody.md"><strong>MessageBody.</strong></a></span><span class="sxs-lookup"><span data-stu-id="1470f-219"><a href="showmessageaction-messagebody.md"><strong>ShowMessageAction.MessageBody</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="1470f-220">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1470f-220">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1470f-221">Sobre o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="1470f-221">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 





