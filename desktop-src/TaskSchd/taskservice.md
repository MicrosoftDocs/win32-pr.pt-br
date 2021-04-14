---
title: Objeto TaskService
description: Para scripts, o fornece acesso ao serviço de Agendador de Tarefas para gerenciar tarefas registradas.
ms.assetid: 6ddd43dc-d027-4792-a53b-07fe4d4a3576
keywords:
- Agendador de Tarefas de objeto TaskService
- Agendador de Tarefas de objeto TaskService, descrito
topic_type:
- apiref
api_name:
- TaskService
- HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 762cd2445c3c6b720bba0f01ae48b787abc1fb38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455698"
---
# <a name="taskservice-object"></a><span data-ttu-id="e24c6-105">Objeto TaskService</span><span class="sxs-lookup"><span data-stu-id="e24c6-105">TaskService object</span></span>

<span data-ttu-id="e24c6-106">Para scripts, o fornece acesso ao serviço de Agendador de Tarefas para gerenciar tarefas registradas.</span><span class="sxs-lookup"><span data-stu-id="e24c6-106">For scripting, provides access to the Task Scheduler service for managing registered tasks.</span></span>

<span data-ttu-id="e24c6-107">O método [**TaskService. Connect**](taskservice-connect.md) deve ser chamado antes de chamar qualquer um dos outros métodos **TaskService** .</span><span class="sxs-lookup"><span data-stu-id="e24c6-107">The [**TaskService.Connect**](taskservice-connect.md) method should be called before calling any of the other **TaskService** methods.</span></span>

## <a name="members"></a><span data-ttu-id="e24c6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="e24c6-108">Members</span></span>

<span data-ttu-id="e24c6-109">O objeto **TaskService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e24c6-109">The **TaskService** object has these types of members:</span></span>

-   [<span data-ttu-id="e24c6-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e24c6-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="e24c6-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e24c6-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e24c6-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="e24c6-112">Methods</span></span>

<span data-ttu-id="e24c6-113">O objeto **TaskService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e24c6-113">The **TaskService** object has these methods.</span></span>



| <span data-ttu-id="e24c6-114">Método</span><span class="sxs-lookup"><span data-stu-id="e24c6-114">Method</span></span>                                                 | <span data-ttu-id="e24c6-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="e24c6-115">Description</span></span>                                                                                                                                                                                                          |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e24c6-116">**Connect**</span><span class="sxs-lookup"><span data-stu-id="e24c6-116">**Connect**</span></span>](taskservice-connect.md)                 | <span data-ttu-id="e24c6-117">Conecta-se a um computador remoto e associa todas as chamadas subsequentes nesta interface a uma sessão remota.</span><span class="sxs-lookup"><span data-stu-id="e24c6-117">Connects to a remote machine and associates all subsequent calls on this interface with a remote session.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="e24c6-118">**GetFolder**</span><span class="sxs-lookup"><span data-stu-id="e24c6-118">**GetFolder**</span></span>](taskservice-getfolder.md)             | <span data-ttu-id="e24c6-119">Obtém o caminho para uma pasta de tarefas registradas.</span><span class="sxs-lookup"><span data-stu-id="e24c6-119">Gets the path to a folder of registered tasks.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="e24c6-120">**GetRunningTasks**</span><span class="sxs-lookup"><span data-stu-id="e24c6-120">**GetRunningTasks**</span></span>](taskservice-getrunningtasks.md) | <span data-ttu-id="e24c6-121">Obtém uma coleção de tarefas em execução.</span><span class="sxs-lookup"><span data-stu-id="e24c6-121">Gets a collection of running tasks.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="e24c6-122">**NewTask**</span><span class="sxs-lookup"><span data-stu-id="e24c6-122">**NewTask**</span></span>](taskservice-newtask.md)                 | <span data-ttu-id="e24c6-123">Retorna um objeto de definição de tarefa vazio a ser preenchido com configurações e propriedades e, em seguida, registrado usando o método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="e24c6-123">Returns an empty task definition object to be filled in with settings and properties and then registered using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e24c6-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e24c6-124">Properties</span></span>

<span data-ttu-id="e24c6-125">O objeto **TaskService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e24c6-125">The **TaskService** object has these properties.</span></span>



| <span data-ttu-id="e24c6-126">Propriedade</span><span class="sxs-lookup"><span data-stu-id="e24c6-126">Property</span></span>                                                          | <span data-ttu-id="e24c6-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="e24c6-127">Description</span></span>                                                                                                                 |
|:------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e24c6-128">**Conectado**</span><span class="sxs-lookup"><span data-stu-id="e24c6-128">**Connected**</span></span>](taskservice-connected.md)<br/>             | <span data-ttu-id="e24c6-129">Obtém um valor booliano que indica se você está conectado ao serviço de Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="e24c6-129">Gets a Boolean value that indicates if you are connected to the Task Scheduler service.</span></span><br/>                          |
| [<span data-ttu-id="e24c6-130">**ConnectedDomain**</span><span class="sxs-lookup"><span data-stu-id="e24c6-130">**ConnectedDomain**</span></span>](taskservice-connecteddomain.md)<br/> | <span data-ttu-id="e24c6-131">Obtém o nome do domínio ao qual o computador [**TargetServer**](taskservice-targetserver.md) está conectado.</span><span class="sxs-lookup"><span data-stu-id="e24c6-131">Gets the name of the domain to which the [**TargetServer**](taskservice-targetserver.md) computer is connected.</span></span><br/> |
| [<span data-ttu-id="e24c6-132">**ConnectedUser**</span><span class="sxs-lookup"><span data-stu-id="e24c6-132">**ConnectedUser**</span></span>](taskservice-connecteduser.md)<br/>     | <span data-ttu-id="e24c6-133">Obtém o nome do usuário que está conectado ao serviço de Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="e24c6-133">Gets the name of the user that is connected to the Task Scheduler service.</span></span><br/>                                       |
| <span data-ttu-id="e24c6-134">HighestVersion</span><span class="sxs-lookup"><span data-stu-id="e24c6-134">HighestVersion</span></span><br/>                                         | <span data-ttu-id="e24c6-135">Obtém a versão mais recente do Agendador de Tarefas a que um computador dá suporte.</span><span class="sxs-lookup"><span data-stu-id="e24c6-135">Gets the highest version of Task Scheduler that a computer supports.</span></span><br/>                                             |
| [<span data-ttu-id="e24c6-136">**TargetServer**</span><span class="sxs-lookup"><span data-stu-id="e24c6-136">**TargetServer**</span></span>](taskservice-targetserver.md)<br/>       | <span data-ttu-id="e24c6-137">Obtém o nome do computador que está executando o serviço de Agendador de Tarefas ao qual o usuário está conectado.</span><span class="sxs-lookup"><span data-stu-id="e24c6-137">Gets the name of the computer that is running the Task Scheduler service that the user is connected to.</span></span><br/>          |



 

## <a name="examples"></a><span data-ttu-id="e24c6-138">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e24c6-138">Examples</span></span>

<span data-ttu-id="e24c6-139">Para obter mais informações e código de exemplo para este objeto de script, consulte o [exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md), [exemplo de gatilho de evento (script)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [exemplo de gatilho diário (script)](daily-trigger-example--scripting-.md), [exemplo de gatilho de registro (script)](registration-trigger-example--scripting-.md), [exemplo de gatilho semanal (script)](weekly-trigger-example--scripting-.md), [exemplo de gatilho de logon (Scripting)](logon-trigger-example--scripting-.md), [exemplo de gatilho de inicialização (script)](boot-trigger-example--scripting-.md)ou [exibição de nomes de tarefas e Estados (scripts)](displaying-task-names-and-state--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="e24c6-139">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md), [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md), or [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e24c6-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e24c6-140">Requirements</span></span>



| <span data-ttu-id="e24c6-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="e24c6-141">Requirement</span></span> | <span data-ttu-id="e24c6-142">Valor</span><span class="sxs-lookup"><span data-stu-id="e24c6-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e24c6-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e24c6-143">Minimum supported client</span></span><br/> | <span data-ttu-id="e24c6-144">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e24c6-144">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e24c6-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e24c6-145">Minimum supported server</span></span><br/> | <span data-ttu-id="e24c6-146">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e24c6-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e24c6-147">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e24c6-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="e24c6-148"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e24c6-148"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e24c6-149">DLL</span><span class="sxs-lookup"><span data-stu-id="e24c6-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e24c6-150"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e24c6-150"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e24c6-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="e24c6-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e24c6-152">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="e24c6-152">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





