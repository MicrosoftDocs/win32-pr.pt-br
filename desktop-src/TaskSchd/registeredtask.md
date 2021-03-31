---
title: Objeto RegisteredTask
description: Objeto de script que fornece os métodos que são usados para executar a tarefa imediatamente, obter todas as instâncias em execução da tarefa, obter ou definir as credenciais que são usadas para registrar a tarefa e as propriedades que descrevem a tarefa.
ms.assetid: d280f22b-4dd1-44df-be12-286fb1c029a3
keywords:
- Agendador de Tarefas de objeto RegisteredTask
- Agendador de Tarefas de objeto RegisteredTask, descrito
topic_type:
- apiref
api_name:
- RegisteredTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ce300375e5122a7b63266c0cd21cdddf34606b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644392"
---
# <a name="registeredtask-object"></a><span data-ttu-id="52d31-105">Objeto RegisteredTask</span><span class="sxs-lookup"><span data-stu-id="52d31-105">RegisteredTask object</span></span>

<span data-ttu-id="52d31-106">Objeto de script que fornece os métodos que são usados para executar a tarefa imediatamente, obter todas as instâncias em execução da tarefa, obter ou definir as credenciais que são usadas para registrar a tarefa e as propriedades que descrevem a tarefa.</span><span class="sxs-lookup"><span data-stu-id="52d31-106">Scripting object that provides the methods that are used to run the task immediately, get any running instances of the task, get or set the credentials that are used to register the task, and the properties that describe the task.</span></span>

## <a name="members"></a><span data-ttu-id="52d31-107">Membros</span><span class="sxs-lookup"><span data-stu-id="52d31-107">Members</span></span>

<span data-ttu-id="52d31-108">O objeto **RegisteredTask** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="52d31-108">The **RegisteredTask** object has these types of members:</span></span>

-   [<span data-ttu-id="52d31-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="52d31-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="52d31-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="52d31-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="52d31-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="52d31-111">Methods</span></span>

<span data-ttu-id="52d31-112">O objeto **RegisteredTask** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="52d31-112">The **RegisteredTask** object has these methods.</span></span>



| <span data-ttu-id="52d31-113">Método</span><span class="sxs-lookup"><span data-stu-id="52d31-113">Method</span></span>                                                                | <span data-ttu-id="52d31-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="52d31-114">Description</span></span>                                                                                     |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="52d31-115">**GetInstances**</span><span class="sxs-lookup"><span data-stu-id="52d31-115">**GetInstances**</span></span>](registeredtask-getinstances.md)                   | <span data-ttu-id="52d31-116">Retorna todas as instâncias da tarefa registrada que estão em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="52d31-116">Returns all instances of the registered task that are currently running.</span></span><br/>             |
| [<span data-ttu-id="52d31-117">**Getruntimes**</span><span class="sxs-lookup"><span data-stu-id="52d31-117">**GetRunTimes**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-getruntimes)                    | <span data-ttu-id="52d31-118">Obtém os horários em que a tarefa registrada está agendada para ser executada durante um período especificado.</span><span class="sxs-lookup"><span data-stu-id="52d31-118">Gets the times that the registered task is scheduled to run during a specified time.</span></span><br/> |
| [<span data-ttu-id="52d31-119">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="52d31-119">**GetSecurityDescriptor**</span></span>](registeredtask-getsecuritydescriptor.md) | <span data-ttu-id="52d31-120">Obtém o descritor de segurança que é usado como credenciais para a tarefa registrada.</span><span class="sxs-lookup"><span data-stu-id="52d31-120">Gets the security descriptor that is used as credentials for the registered task.</span></span><br/>    |
| [<span data-ttu-id="52d31-121">**Funcionam**</span><span class="sxs-lookup"><span data-stu-id="52d31-121">**Run**</span></span>](registeredtask-run.md)                                     | <span data-ttu-id="52d31-122">Executa a tarefa registrada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="52d31-122">Runs the registered task immediately.</span></span><br/>                                                |
| [<span data-ttu-id="52d31-123">**RunEx**</span><span class="sxs-lookup"><span data-stu-id="52d31-123">**RunEx**</span></span>](registeredtask-runex.md)                                 | <span data-ttu-id="52d31-124">Executa a tarefa registrada imediatamente usando sinalizadores especificados e um identificador de sessão.</span><span class="sxs-lookup"><span data-stu-id="52d31-124">Runs the registered task immediately using specified flags and a session identifier.</span></span><br/> |
| [<span data-ttu-id="52d31-125">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="52d31-125">**SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md) | <span data-ttu-id="52d31-126">Define o descritor de segurança que é usado como credenciais para a tarefa registrada.</span><span class="sxs-lookup"><span data-stu-id="52d31-126">Sets the security descriptor that is used as credentials for the registered task.</span></span><br/>    |
| [<span data-ttu-id="52d31-127">**Stop**</span><span class="sxs-lookup"><span data-stu-id="52d31-127">**Stop**</span></span>](registeredtask-stop.md)                                   | <span data-ttu-id="52d31-128">Interrompe a tarefa registrada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="52d31-128">Stops the registered task immediately.</span></span><br/>                                               |



 

### <a name="properties"></a><span data-ttu-id="52d31-129">Propriedades</span><span class="sxs-lookup"><span data-stu-id="52d31-129">Properties</span></span>

<span data-ttu-id="52d31-130">O objeto **RegisteredTask** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="52d31-130">The **RegisteredTask** object has these properties.</span></span>



| <span data-ttu-id="52d31-131">Propriedade</span><span class="sxs-lookup"><span data-stu-id="52d31-131">Property</span></span>                                                                   | <span data-ttu-id="52d31-132">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="52d31-132">Access type</span></span>           | <span data-ttu-id="52d31-133">Description</span><span class="sxs-lookup"><span data-stu-id="52d31-133">Description</span></span>                                                                               |
|:---------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="52d31-134">**Definição**</span><span class="sxs-lookup"><span data-stu-id="52d31-134">**Definition**</span></span>](registeredtask-definition.md)<br/>                 | <span data-ttu-id="52d31-135">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="52d31-135">Read-only</span></span><br/>  | <span data-ttu-id="52d31-136">Obtém a definição da tarefa.</span><span class="sxs-lookup"><span data-stu-id="52d31-136">Gets the definition of the task.</span></span><br/>                                               |
| [<span data-ttu-id="52d31-137">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="52d31-137">**Enabled**</span></span>](registeredtask-enabled.md)<br/>                       | <span data-ttu-id="52d31-138">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="52d31-138">Read/write</span></span><br/> | <span data-ttu-id="52d31-139">Obtém ou define um valor booliano que indica se a tarefa registrada está habilitada.</span><span class="sxs-lookup"><span data-stu-id="52d31-139">Gets or set a Boolean value that indicates if the registered task is enabled.</span></span><br/>  |
| [<span data-ttu-id="52d31-140">**LastRunTime**</span><span class="sxs-lookup"><span data-stu-id="52d31-140">**LastRunTime**</span></span>](registeredtask-lastruntime.md)<br/>               | <span data-ttu-id="52d31-141">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="52d31-141">Read-only</span></span><br/>  | <span data-ttu-id="52d31-142">Obtém a hora da última execução da tarefa registrada.</span><span class="sxs-lookup"><span data-stu-id="52d31-142">Gets the time the registered task was last run.</span></span><br/>                                |
| [<span data-ttu-id="52d31-143">**LastTaskResult**</span><span class="sxs-lookup"><span data-stu-id="52d31-143">**LastTaskResult**</span></span>](registeredtask-lasttaskresult.md)<br/>         | <span data-ttu-id="52d31-144">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="52d31-144">Read-only</span></span><br/>  | <span data-ttu-id="52d31-145">Obtém os resultados que foram retornados na última vez em que a tarefa registrada foi executada.</span><span class="sxs-lookup"><span data-stu-id="52d31-145">Gets the results that were returned the last time the registered task was run.</span></span><br/> |
| [<span data-ttu-id="52d31-146">**Nomes**</span><span class="sxs-lookup"><span data-stu-id="52d31-146">**Name**</span></span>](registeredtask-name.md)<br/>                             | <span data-ttu-id="52d31-147">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="52d31-147">Read-only</span></span><br/>  | <span data-ttu-id="52d31-148">Obtém o nome da tarefa registrada.</span><span class="sxs-lookup"><span data-stu-id="52d31-148">Gets the name of the registered task.</span></span><br/>                                          |
| [<span data-ttu-id="52d31-149">**NextRunTime**</span><span class="sxs-lookup"><span data-stu-id="52d31-149">**NextRunTime**</span></span>](registeredtask-nextruntime.md)<br/>               | <span data-ttu-id="52d31-150">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="52d31-150">Read-only</span></span><br/>  | <span data-ttu-id="52d31-151">Obtém a hora em que a tarefa registrada está próxima agendada para ser executada.</span><span class="sxs-lookup"><span data-stu-id="52d31-151">Gets the time when the registered task is next scheduled to run.</span></span><br/>               |
| [<span data-ttu-id="52d31-152">**NumberOfMissedRuns**</span><span class="sxs-lookup"><span data-stu-id="52d31-152">**NumberOfMissedRuns**</span></span>](registeredtask-numberofmissedruns.md)<br/> | <span data-ttu-id="52d31-153">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="52d31-153">Read-only</span></span><br/>  | <span data-ttu-id="52d31-154">Obtém o número de vezes que a tarefa registrada perdeu uma execução agendada.</span><span class="sxs-lookup"><span data-stu-id="52d31-154">Gets the number of times the registered task has missed a scheduled run.</span></span><br/>       |
| [<span data-ttu-id="52d31-155">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="52d31-155">**Path**</span></span>](registeredtask-path.md)<br/>                             | <span data-ttu-id="52d31-156">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="52d31-156">Read-only</span></span><br/>  | <span data-ttu-id="52d31-157">Obtém o caminho para onde a tarefa registrada é armazenada.</span><span class="sxs-lookup"><span data-stu-id="52d31-157">Gets the path to where the registered task is stored.</span></span><br/>                          |
| [<span data-ttu-id="52d31-158">**Estado**</span><span class="sxs-lookup"><span data-stu-id="52d31-158">**State**</span></span>](registeredtask-state.md)<br/>                           | <span data-ttu-id="52d31-159">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="52d31-159">Read-only</span></span><br/>  | <span data-ttu-id="52d31-160">Obtém o estado operacional da tarefa registrada.</span><span class="sxs-lookup"><span data-stu-id="52d31-160">Gets the operational state of the registered task.</span></span><br/>                             |
| [<span data-ttu-id="52d31-161">**XML**</span><span class="sxs-lookup"><span data-stu-id="52d31-161">**XML**</span></span>](registeredtask-xml.md)<br/>                               | <span data-ttu-id="52d31-162">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="52d31-162">Read-only</span></span><br/>  | <span data-ttu-id="52d31-163">Obtém as informações de registro formatadas em XML para a tarefa registrada.</span><span class="sxs-lookup"><span data-stu-id="52d31-163">Gets the XML-formatted registration information for the registered task.</span></span><br/>       |



 

## <a name="examples"></a><span data-ttu-id="52d31-164">Exemplos</span><span class="sxs-lookup"><span data-stu-id="52d31-164">Examples</span></span>

<span data-ttu-id="52d31-165">Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md) e [exibição de nomes e Estados de tarefas (scripts)](displaying-task-names-and-state--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="52d31-165">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md) and [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="52d31-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52d31-166">Requirements</span></span>



| <span data-ttu-id="52d31-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="52d31-167">Requirement</span></span> | <span data-ttu-id="52d31-168">Valor</span><span class="sxs-lookup"><span data-stu-id="52d31-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52d31-169">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52d31-169">Minimum supported client</span></span><br/> | <span data-ttu-id="52d31-170">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="52d31-170">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="52d31-171">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52d31-171">Minimum supported server</span></span><br/> | <span data-ttu-id="52d31-172">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="52d31-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="52d31-173">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="52d31-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="52d31-174"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="52d31-174"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="52d31-175">DLL</span><span class="sxs-lookup"><span data-stu-id="52d31-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52d31-176"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52d31-176"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





