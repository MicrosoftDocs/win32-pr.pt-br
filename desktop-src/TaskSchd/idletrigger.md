---
title: Objeto IdleTrigger
description: Objeto de script que representa um gatilho que inicia uma tarefa quando ocorre uma condição ociosa.
ms.assetid: 627d83cf-27bd-47ce-a647-fa1e9af5263e
keywords:
- Agendador de Tarefas do gatilho de ociosidade, objeto
- Agendador de Tarefas de objeto IdleTrigger
- Agendador de Tarefas de objeto IdleTrigger, descrito
topic_type:
- apiref
api_name:
- IdleTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e72288827fec34257bf4f54a152031ef37068790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761341"
---
# <a name="idletrigger-object"></a><span data-ttu-id="da254-106">Objeto IdleTrigger</span><span class="sxs-lookup"><span data-stu-id="da254-106">IdleTrigger object</span></span>

<span data-ttu-id="da254-107">Objeto de script que representa um gatilho que inicia uma tarefa quando ocorre uma condição ociosa.</span><span class="sxs-lookup"><span data-stu-id="da254-107">Scripting object that represents a trigger that starts a task when an idle condition occurs.</span></span> <span data-ttu-id="da254-108">Para obter informações sobre condições ociosas, consulte [condições de ociosidade da tarefa](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="da254-108">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

## <a name="members"></a><span data-ttu-id="da254-109">Membros</span><span class="sxs-lookup"><span data-stu-id="da254-109">Members</span></span>

<span data-ttu-id="da254-110">O objeto **IdleTrigger** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="da254-110">The **IdleTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="da254-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="da254-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="da254-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="da254-112">Properties</span></span>

<span data-ttu-id="da254-113">O objeto **IdleTrigger** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="da254-113">The **IdleTrigger** object has these properties.</span></span>



| <span data-ttu-id="da254-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="da254-114">Property</span></span>                                                            | <span data-ttu-id="da254-115">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="da254-115">Access type</span></span>           | <span data-ttu-id="da254-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="da254-116">Description</span></span>                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da254-117">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="da254-117">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="da254-118">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="da254-118">Read/write</span></span><br/> | <span data-ttu-id="da254-119">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="da254-119">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="da254-120">Obtém ou define um valor booliano que indica se o gatilho está habilitado.</span><span class="sxs-lookup"><span data-stu-id="da254-120">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="da254-121">Limite de fim</span><span class="sxs-lookup"><span data-stu-id="da254-121">EndBoundary</span></span>](trigger-endboundary.md)<br/>                   | <span data-ttu-id="da254-122">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="da254-122">Read/write</span></span><br/> | <span data-ttu-id="da254-123">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="da254-123">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="da254-124">Obtém ou define a data e a hora em que o gatilho é desativado.</span><span class="sxs-lookup"><span data-stu-id="da254-124">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="da254-125">O gatilho não pode iniciar a tarefa depois que ela é desativada.</span><span class="sxs-lookup"><span data-stu-id="da254-125">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="da254-126">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="da254-126">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="da254-127">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="da254-127">Read/write</span></span><br/> | <span data-ttu-id="da254-128">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="da254-128">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="da254-129">Obtém ou define a quantidade máxima de tempo em que a tarefa pode ser iniciada pelo gatilho.</span><span class="sxs-lookup"><span data-stu-id="da254-129">Gets or sets the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                                 |
| [<span data-ttu-id="da254-130">**Sessão**</span><span class="sxs-lookup"><span data-stu-id="da254-130">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="da254-131">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="da254-131">Read/write</span></span><br/> | <span data-ttu-id="da254-132">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="da254-132">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="da254-133">Obtém ou define o identificador do gatilho.</span><span class="sxs-lookup"><span data-stu-id="da254-133">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="da254-134">**Repetição**</span><span class="sxs-lookup"><span data-stu-id="da254-134">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="da254-135">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="da254-135">Read/write</span></span><br/> | <span data-ttu-id="da254-136">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="da254-136">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="da254-137">Obtém ou define um valor que indica a frequência em que a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="da254-137">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="da254-138">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="da254-138">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="da254-139">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="da254-139">Read/write</span></span><br/> | <span data-ttu-id="da254-140">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="da254-140">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="da254-141">Obtém ou define a data e a hora em que o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="da254-141">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                            |
| [<span data-ttu-id="da254-142">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="da254-142">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="da254-143">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da254-143">Read-only</span></span><br/>  | <span data-ttu-id="da254-144">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="da254-144">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="da254-145">Obtém o tipo do gatilho.</span><span class="sxs-lookup"><span data-stu-id="da254-145">Gets the type of the trigger.</span></span><br/>                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="da254-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="da254-146">Remarks</span></span>

<span data-ttu-id="da254-147">Um gatilho ocioso só disparará uma ação de tarefa se o computador entrar em um estado ocioso após o limite de início do gatilho.</span><span class="sxs-lookup"><span data-stu-id="da254-147">An idle trigger will only trigger a task action if the computer goes into an idle state after the start boundary of the trigger.</span></span>

<span data-ttu-id="da254-148">Ao ler ou gravar XML para uma tarefa, um gatilho de ociosidade é especificado usando o elemento [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="da254-148">When reading or writing XML for a task, an idle trigger is specified using the [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="da254-149">Se uma tarefa for disparada por um gatilho ocioso, a propriedade [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) será ignorada.</span><span class="sxs-lookup"><span data-stu-id="da254-149">If a task is triggered by an idle trigger, then the [**IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) property is ignored.</span></span>

<span data-ttu-id="da254-150">Se a instância inicial de uma tarefa com um gatilho de ociosidade ainda estiver em execução, a tarefa será iniciada apenas uma vez sem repetições, mesmo que várias repetições sejam definidas na propriedade de [**repetição**](trigger-repetition.md) .</span><span class="sxs-lookup"><span data-stu-id="da254-150">If the initial instance of a task with an idle trigger is still running, then the task is only launched once with no repetitions, even if multiple repetition is defined in the [**Repetition**](trigger-repetition.md) property.</span></span> <span data-ttu-id="da254-151">Esse comportamento não ocorrerá se a tarefa for interrompida por si só.</span><span class="sxs-lookup"><span data-stu-id="da254-151">This behavior does not occur if the task stops by itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="da254-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da254-152">Requirements</span></span>



| <span data-ttu-id="da254-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="da254-153">Requirement</span></span> | <span data-ttu-id="da254-154">Valor</span><span class="sxs-lookup"><span data-stu-id="da254-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da254-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da254-155">Minimum supported client</span></span><br/> | <span data-ttu-id="da254-156">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="da254-156">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="da254-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da254-157">Minimum supported server</span></span><br/> | <span data-ttu-id="da254-158">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="da254-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="da254-159">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="da254-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="da254-160"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="da254-160"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="da254-161">DLL</span><span class="sxs-lookup"><span data-stu-id="da254-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da254-162"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da254-162"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da254-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="da254-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da254-164">**Of**</span><span class="sxs-lookup"><span data-stu-id="da254-164">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="da254-165">Objetos Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="da254-165">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="da254-166">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="da254-166">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





