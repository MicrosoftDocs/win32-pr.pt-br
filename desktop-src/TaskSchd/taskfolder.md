---
title: Objeto TaskFolder
description: Objeto de script que fornece os métodos que são usados para registrar (criar) tarefas na pasta, remover tarefas da pasta e criar ou remover subpastas da pasta.
ms.assetid: f6fd09ec-2777-4903-83b5-e3ac1aa472a0
keywords:
- Agendador de Tarefas de objeto TaskFolder
- Agendador de Tarefas de objeto TaskFolder, descrito
topic_type:
- apiref
api_name:
- TaskFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1ccad9331cf3df12ea5752fdd7e5ac94bfbeba6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499648"
---
# <a name="taskfolder-object"></a><span data-ttu-id="5bc0a-105">Objeto TaskFolder</span><span class="sxs-lookup"><span data-stu-id="5bc0a-105">TaskFolder object</span></span>

<span data-ttu-id="5bc0a-106">Objeto de script que fornece os métodos que são usados para registrar (criar) tarefas na pasta, remover tarefas da pasta e criar ou remover subpastas da pasta.</span><span class="sxs-lookup"><span data-stu-id="5bc0a-106">Scripting object that provides the methods that are used to register (create) tasks in the folder, remove tasks from the folder, and create or remove subfolders from the folder.</span></span>

## <a name="members"></a><span data-ttu-id="5bc0a-107">Membros</span><span class="sxs-lookup"><span data-stu-id="5bc0a-107">Members</span></span>

<span data-ttu-id="5bc0a-108">O objeto **TaskFolder** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5bc0a-108">The **TaskFolder** object has these types of members:</span></span>

-   [<span data-ttu-id="5bc0a-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5bc0a-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="5bc0a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5bc0a-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5bc0a-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="5bc0a-111">Methods</span></span>

<span data-ttu-id="5bc0a-112">O objeto **TaskFolder** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5bc0a-112">The **TaskFolder** object has these methods.</span></span>



| <span data-ttu-id="5bc0a-113">Método</span><span class="sxs-lookup"><span data-stu-id="5bc0a-113">Method</span></span>                                                              | <span data-ttu-id="5bc0a-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5bc0a-114">Description</span></span>                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5bc0a-115">**CreateFolder**</span><span class="sxs-lookup"><span data-stu-id="5bc0a-115">**CreateFolder**</span></span>](taskfolder-createfolder.md)                     | <span data-ttu-id="5bc0a-116">Cria uma pasta para tarefas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="5bc0a-116">Creates a folder for related tasks.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="5bc0a-117">**DeleteFolder**</span><span class="sxs-lookup"><span data-stu-id="5bc0a-117">**DeleteFolder**</span></span>](taskfolder-deletefolder.md)                     | <span data-ttu-id="5bc0a-118">Exclui uma subpasta da pasta pai.</span><span class="sxs-lookup"><span data-stu-id="5bc0a-118">Deletes a subfolder from the parent folder.</span></span><br/>                                                                                         |
| [<span data-ttu-id="5bc0a-119">**DeleteTask**</span><span class="sxs-lookup"><span data-stu-id="5bc0a-119">**DeleteTask**</span></span>](taskfolder-deletetask.md)                         | <span data-ttu-id="5bc0a-120">Exclui uma tarefa da pasta.</span><span class="sxs-lookup"><span data-stu-id="5bc0a-120">Deletes a task from the folder.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="5bc0a-121">**GetFolder**</span><span class="sxs-lookup"><span data-stu-id="5bc0a-121">**GetFolder**</span></span>](taskfolder-getfolder.md)                           | <span data-ttu-id="5bc0a-122">Obtém uma pasta que contém tarefas em um local especificado.</span><span class="sxs-lookup"><span data-stu-id="5bc0a-122">Gets a folder that contains tasks at a specified location.</span></span><br/>                                                                          |
| [<span data-ttu-id="5bc0a-123">**GetFolders**</span><span class="sxs-lookup"><span data-stu-id="5bc0a-123">**GetFolders**</span></span>](taskfolder-getfolders.md)                         | <span data-ttu-id="5bc0a-124">Obtém todas as subpastas na pasta.</span><span class="sxs-lookup"><span data-stu-id="5bc0a-124">Gets all the subfolders in the folder.</span></span><br/>                                                                                              |
| [<span data-ttu-id="5bc0a-125">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="5bc0a-125">**GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)   | <span data-ttu-id="5bc0a-126">Obtém o descritor de segurança para a pasta.</span><span class="sxs-lookup"><span data-stu-id="5bc0a-126">Gets the security descriptor for the folder.</span></span><br/>                                                                                        |
| [<span data-ttu-id="5bc0a-127">**GetTask**</span><span class="sxs-lookup"><span data-stu-id="5bc0a-127">**GetTask**</span></span>](taskfolder-gettask.md)                               | <span data-ttu-id="5bc0a-128">Obtém uma tarefa em um local especificado em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="5bc0a-128">Gets a task at a specified location in a folder.</span></span><br/>                                                                                    |
| [<span data-ttu-id="5bc0a-129">**Gettarefas**</span><span class="sxs-lookup"><span data-stu-id="5bc0a-129">**GetTasks**</span></span>](taskfolder-gettasks.md)                             | <span data-ttu-id="5bc0a-130">Obtém todas as tarefas na pasta.</span><span class="sxs-lookup"><span data-stu-id="5bc0a-130">Gets all the tasks in the folder.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="5bc0a-131">**RegisterTask**</span><span class="sxs-lookup"><span data-stu-id="5bc0a-131">**RegisterTask**</span></span>](taskfolder-registertask.md)                     | <span data-ttu-id="5bc0a-132">Registra (cria) uma nova tarefa na pasta usando XML para definir a tarefa.</span><span class="sxs-lookup"><span data-stu-id="5bc0a-132">Registers (creates) a new task in the folder using XML to define the task.</span></span><br/>                                                          |
| [<span data-ttu-id="5bc0a-133">**RegisterTaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="5bc0a-133">**RegisterTaskDefinition**</span></span>](taskfolder-registertaskdefinition.md) | <span data-ttu-id="5bc0a-134">Registra (cria) uma tarefa em um local especificado usando a interface [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) para definir uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="5bc0a-134">Registers (creates) a task in a specified location using the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) interface to define a task.</span></span><br/> |
| [<span data-ttu-id="5bc0a-135">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="5bc0a-135">**SetSecurityDescriptor**</span></span>](taskfolder-setsecuritydescriptor.md)   | <span data-ttu-id="5bc0a-136">Define o descritor de segurança para a pasta.</span><span class="sxs-lookup"><span data-stu-id="5bc0a-136">Sets the security descriptor for the folder.</span></span><br/>                                                                                        |



 

### <a name="properties"></a><span data-ttu-id="5bc0a-137">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5bc0a-137">Properties</span></span>

<span data-ttu-id="5bc0a-138">O objeto **TaskFolder** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5bc0a-138">The **TaskFolder** object has these properties.</span></span>



| <span data-ttu-id="5bc0a-139">Propriedade</span><span class="sxs-lookup"><span data-stu-id="5bc0a-139">Property</span></span>                                   | <span data-ttu-id="5bc0a-140">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="5bc0a-140">Access type</span></span>          | <span data-ttu-id="5bc0a-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="5bc0a-141">Description</span></span>                                                                        |
|:-------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="5bc0a-142">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5bc0a-142">**Name**</span></span>](taskfolder-name.md)<br/> | <span data-ttu-id="5bc0a-143">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5bc0a-143">Read-only</span></span><br/> | <span data-ttu-id="5bc0a-144">Obtém o nome usado para identificar a pasta que contém uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="5bc0a-144">Gets the name that is used to identify the folder that contains a task.</span></span><br/> |
| [<span data-ttu-id="5bc0a-145">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="5bc0a-145">**Path**</span></span>](taskfolder-path.md)<br/> | <span data-ttu-id="5bc0a-146">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5bc0a-146">Read-only</span></span><br/> | <span data-ttu-id="5bc0a-147">Obtém o caminho para onde a pasta é armazenada.</span><span class="sxs-lookup"><span data-stu-id="5bc0a-147">Gets the path to where the folder is stored.</span></span><br/>                            |



 

## <a name="examples"></a><span data-ttu-id="5bc0a-148">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5bc0a-148">Examples</span></span>

<span data-ttu-id="5bc0a-149">Para obter mais informações e código de exemplo para este objeto de script, consulte o [exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md), [exemplo de gatilho de evento (script)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [exemplo de gatilho diário (script)](daily-trigger-example--scripting-.md), [exemplo de gatilho de registro (script)](registration-trigger-example--scripting-.md), [exemplo de gatilho semanal (script)](weekly-trigger-example--scripting-.md), [exemplo de gatilho de logon (Scripting)](logon-trigger-example--scripting-.md), [exemplo de gatilho de inicialização (script)](boot-trigger-example--scripting-.md)ou [exibição de nomes de tarefas e Estados (scripts)](displaying-task-names-and-state--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="5bc0a-149">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md), [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md), or [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5bc0a-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bc0a-150">Requirements</span></span>



| <span data-ttu-id="5bc0a-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bc0a-151">Requirement</span></span> | <span data-ttu-id="5bc0a-152">Valor</span><span class="sxs-lookup"><span data-stu-id="5bc0a-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5bc0a-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bc0a-153">Minimum supported client</span></span><br/> | <span data-ttu-id="5bc0a-154">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5bc0a-154">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5bc0a-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bc0a-155">Minimum supported server</span></span><br/> | <span data-ttu-id="5bc0a-156">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5bc0a-156">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5bc0a-157">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5bc0a-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="5bc0a-158"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5bc0a-158"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5bc0a-159">DLL</span><span class="sxs-lookup"><span data-stu-id="5bc0a-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bc0a-160"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5bc0a-160"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bc0a-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bc0a-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bc0a-162">Objetos Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="5bc0a-162">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="5bc0a-163">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="5bc0a-163">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





