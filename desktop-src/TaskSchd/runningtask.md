---
title: Objeto RunningTask
description: Objeto de script que fornece os métodos para obter informações e controlar uma tarefa em execução.
ms.assetid: 335e69d8-affa-4845-a067-641184e0f7df
keywords:
- Agendador de Tarefas de objeto RunningTask
- Agendador de Tarefas de objeto RunningTask, descrito
topic_type:
- apiref
api_name:
- RunningTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 261be07f71d0d35f5d3140de1b39574b635a531e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499518"
---
# <a name="runningtask-object"></a><span data-ttu-id="2f6a6-105">Objeto RunningTask</span><span class="sxs-lookup"><span data-stu-id="2f6a6-105">RunningTask object</span></span>

<span data-ttu-id="2f6a6-106">Objeto de script que fornece os métodos para obter informações e controlar uma tarefa em execução.</span><span class="sxs-lookup"><span data-stu-id="2f6a6-106">Scripting object that provides the methods to get information from and control a running task.</span></span>

## <a name="members"></a><span data-ttu-id="2f6a6-107">Membros</span><span class="sxs-lookup"><span data-stu-id="2f6a6-107">Members</span></span>

<span data-ttu-id="2f6a6-108">O objeto **RunningTask** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2f6a6-108">The **RunningTask** object has these types of members:</span></span>

-   [<span data-ttu-id="2f6a6-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="2f6a6-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="2f6a6-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2f6a6-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2f6a6-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="2f6a6-111">Methods</span></span>

<span data-ttu-id="2f6a6-112">O objeto **RunningTask** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="2f6a6-112">The **RunningTask** object has these methods.</span></span>



| <span data-ttu-id="2f6a6-113">Método</span><span class="sxs-lookup"><span data-stu-id="2f6a6-113">Method</span></span>                                 | <span data-ttu-id="2f6a6-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="2f6a6-114">Description</span></span>                                                           |
|:---------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="2f6a6-115">**Atualizar**</span><span class="sxs-lookup"><span data-stu-id="2f6a6-115">**Refresh**</span></span>](runningtask-refresh.md) | <span data-ttu-id="2f6a6-116">Atualiza todas as variáveis de instância local da tarefa.</span><span class="sxs-lookup"><span data-stu-id="2f6a6-116">Refreshes all of the local instance variables of the task.</span></span><br/> |
| [<span data-ttu-id="2f6a6-117">**Stop**</span><span class="sxs-lookup"><span data-stu-id="2f6a6-117">**Stop**</span></span>](runningtask-stop.md)       | <span data-ttu-id="2f6a6-118">Interrompe esta instância da tarefa.</span><span class="sxs-lookup"><span data-stu-id="2f6a6-118">Stops this instance of the task.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="2f6a6-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2f6a6-119">Properties</span></span>

<span data-ttu-id="2f6a6-120">O objeto **RunningTask** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2f6a6-120">The **RunningTask** object has these properties.</span></span>



| <span data-ttu-id="2f6a6-121">Propriedade</span><span class="sxs-lookup"><span data-stu-id="2f6a6-121">Property</span></span>                                                      | <span data-ttu-id="2f6a6-122">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="2f6a6-122">Access type</span></span>          | <span data-ttu-id="2f6a6-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="2f6a6-123">Description</span></span>                                                                         |
|:--------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f6a6-124">**CurrentAction**</span><span class="sxs-lookup"><span data-stu-id="2f6a6-124">**CurrentAction**</span></span>](runningtask-currentaction.md)<br/> | <span data-ttu-id="2f6a6-125">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2f6a6-125">Read-only</span></span><br/> | <span data-ttu-id="2f6a6-126">Obtém o nome da ação atual que a tarefa em execução está executando.</span><span class="sxs-lookup"><span data-stu-id="2f6a6-126">Gets the name of the current action that the running task is performing.</span></span><br/> |
| [<span data-ttu-id="2f6a6-127">**EnginePID**</span><span class="sxs-lookup"><span data-stu-id="2f6a6-127">**EnginePID**</span></span>](runningtask-enginepid.md)<br/>         | <span data-ttu-id="2f6a6-128">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2f6a6-128">Read-only</span></span><br/> | <span data-ttu-id="2f6a6-129">Obtém a ID do processo do mecanismo (processo) que está executando a tarefa.</span><span class="sxs-lookup"><span data-stu-id="2f6a6-129">Gets the process ID for the engine (process) which is running the task.</span></span><br/>  |
| [<span data-ttu-id="2f6a6-130">**InstanceGuid**</span><span class="sxs-lookup"><span data-stu-id="2f6a6-130">**InstanceGuid**</span></span>](runningtask-instanceguid.md)<br/>   | <span data-ttu-id="2f6a6-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2f6a6-131">Read-only</span></span><br/> | <span data-ttu-id="2f6a6-132">Obtém o identificador de GUID para esta instância da tarefa.</span><span class="sxs-lookup"><span data-stu-id="2f6a6-132">Gets the GUID identifier for this instance of the task.</span></span><br/>                  |
| [<span data-ttu-id="2f6a6-133">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2f6a6-133">**Name**</span></span>](runningtask-name.md)<br/>                   | <span data-ttu-id="2f6a6-134">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2f6a6-134">Read-only</span></span><br/> | <span data-ttu-id="2f6a6-135">Obtém o nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="2f6a6-135">Gets the name of the task.</span></span><br/>                                               |
| [<span data-ttu-id="2f6a6-136">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="2f6a6-136">**Path**</span></span>](runningtask-path.md)<br/>                   | <span data-ttu-id="2f6a6-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2f6a6-137">Read-only</span></span><br/> | <span data-ttu-id="2f6a6-138">Obtém o caminho para onde a tarefa é armazenada.</span><span class="sxs-lookup"><span data-stu-id="2f6a6-138">Gets the path to where the task is stored.</span></span><br/>                               |
| [<span data-ttu-id="2f6a6-139">**Status**</span><span class="sxs-lookup"><span data-stu-id="2f6a6-139">**State**</span></span>](runningtask-state.md)<br/>                 | <span data-ttu-id="2f6a6-140">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2f6a6-140">Read-only</span></span><br/> | <span data-ttu-id="2f6a6-141">Obtém o estado da tarefa em execução.</span><span class="sxs-lookup"><span data-stu-id="2f6a6-141">Gets the state of the running task.</span></span> <br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="2f6a6-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f6a6-142">Requirements</span></span>



| <span data-ttu-id="2f6a6-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f6a6-143">Requirement</span></span> | <span data-ttu-id="2f6a6-144">Valor</span><span class="sxs-lookup"><span data-stu-id="2f6a6-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f6a6-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f6a6-145">Minimum supported client</span></span><br/> | <span data-ttu-id="2f6a6-146">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2f6a6-146">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2f6a6-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f6a6-147">Minimum supported server</span></span><br/> | <span data-ttu-id="2f6a6-148">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2f6a6-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2f6a6-149">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2f6a6-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="2f6a6-150"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2f6a6-150"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2f6a6-151">DLL</span><span class="sxs-lookup"><span data-stu-id="2f6a6-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f6a6-152"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f6a6-152"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f6a6-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f6a6-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f6a6-154">Objetos Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="2f6a6-154">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="2f6a6-155">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="2f6a6-155">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="2f6a6-156">**RunningTaskCollection**</span><span class="sxs-lookup"><span data-stu-id="2f6a6-156">**RunningTaskCollection**</span></span>](runningtaskcollection.md)
</dt> <dt>

[<span data-ttu-id="2f6a6-157">**RegisteredTask. Run**</span><span class="sxs-lookup"><span data-stu-id="2f6a6-157">**RegisteredTask.Run**</span></span>](registeredtask-run.md)
</dt> <dt>

[<span data-ttu-id="2f6a6-158">**RegisteredTask.RunEx**</span><span class="sxs-lookup"><span data-stu-id="2f6a6-158">**RegisteredTask.RunEx**</span></span>](registeredtask-runex.md)
</dt> </dl>

 

 





