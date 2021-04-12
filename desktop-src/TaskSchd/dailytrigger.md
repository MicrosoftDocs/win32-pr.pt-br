---
title: Objeto DailyTrigger
description: Objeto de script que representa um gatilho que inicia uma tarefa com base em um agendamento diário.
ms.assetid: f03f53a0-0060-4793-96c1-b47a96852579
keywords:
- gatilho diário Agendador de Tarefas, objeto
- Agendador de Tarefas de objeto DailyTrigger
- Agendador de Tarefas de objeto DailyTrigger, descrito
topic_type:
- apiref
api_name:
- DailyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22203ecf7a421f07ccb823745e6619e05f84f550
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454901"
---
# <a name="dailytrigger-object"></a><span data-ttu-id="992cc-106">Objeto DailyTrigger</span><span class="sxs-lookup"><span data-stu-id="992cc-106">DailyTrigger object</span></span>

<span data-ttu-id="992cc-107">Objeto de script que representa um gatilho que inicia uma tarefa com base em um agendamento diário.</span><span class="sxs-lookup"><span data-stu-id="992cc-107">Scripting object that represents a trigger that starts a task based on a daily schedule.</span></span>

## <a name="members"></a><span data-ttu-id="992cc-108">Membros</span><span class="sxs-lookup"><span data-stu-id="992cc-108">Members</span></span>

<span data-ttu-id="992cc-109">O objeto **DailyTrigger** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="992cc-109">The **DailyTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="992cc-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="992cc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="992cc-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="992cc-111">Properties</span></span>

<span data-ttu-id="992cc-112">O objeto **DailyTrigger** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="992cc-112">The **DailyTrigger** object has these properties.</span></span>



| <span data-ttu-id="992cc-113">Propriedade</span><span class="sxs-lookup"><span data-stu-id="992cc-113">Property</span></span>                                                            | <span data-ttu-id="992cc-114">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="992cc-114">Access type</span></span>           | <span data-ttu-id="992cc-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="992cc-115">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="992cc-116">**DaysInterval**</span><span class="sxs-lookup"><span data-stu-id="992cc-116">**DaysInterval**</span></span>](dailytrigger-daysinterval.md)<br/>        | <span data-ttu-id="992cc-117">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="992cc-117">Read/write</span></span><br/> | <span data-ttu-id="992cc-118">Obtém ou define o intervalo entre os dias no agendamento.</span><span class="sxs-lookup"><span data-stu-id="992cc-118">Gets or sets the interval between the days in the schedule.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="992cc-119">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="992cc-119">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="992cc-120">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="992cc-120">Read/write</span></span><br/> | <span data-ttu-id="992cc-121">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="992cc-121">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="992cc-122">Obtém ou define um valor booliano que indica se o gatilho está habilitado.</span><span class="sxs-lookup"><span data-stu-id="992cc-122">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="992cc-123">**Limite de fim**</span><span class="sxs-lookup"><span data-stu-id="992cc-123">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="992cc-124">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="992cc-124">Read/write</span></span><br/> | <span data-ttu-id="992cc-125">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="992cc-125">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="992cc-126">Obtém ou define a data e a hora em que o gatilho é desativado.</span><span class="sxs-lookup"><span data-stu-id="992cc-126">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="992cc-127">O gatilho não pode iniciar a tarefa depois que ela é desativada.</span><span class="sxs-lookup"><span data-stu-id="992cc-127">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="992cc-128">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="992cc-128">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="992cc-129">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="992cc-129">Read/write</span></span><br/> | <span data-ttu-id="992cc-130">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="992cc-130">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="992cc-131">Obtém ou define a quantidade máxima de tempo que a tarefa iniciada pelo gatilho tem permissão para ser executada.</span><span class="sxs-lookup"><span data-stu-id="992cc-131">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="992cc-132">**Sessão**</span><span class="sxs-lookup"><span data-stu-id="992cc-132">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="992cc-133">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="992cc-133">Read/write</span></span><br/> | <span data-ttu-id="992cc-134">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="992cc-134">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="992cc-135">Obtém ou define o identificador do gatilho.</span><span class="sxs-lookup"><span data-stu-id="992cc-135">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="992cc-136">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="992cc-136">**RandomDelay**</span></span>](dailytrigger-randomdelay.md)<br/>          | <span data-ttu-id="992cc-137">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="992cc-137">Read/write</span></span><br/> | <span data-ttu-id="992cc-138">Obtém ou define um tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho.</span><span class="sxs-lookup"><span data-stu-id="992cc-138">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="992cc-139">**Repetição**</span><span class="sxs-lookup"><span data-stu-id="992cc-139">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="992cc-140">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="992cc-140">Read/write</span></span><br/> | <span data-ttu-id="992cc-141">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="992cc-141">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="992cc-142">Obtém ou define com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="992cc-142">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="992cc-143">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="992cc-143">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="992cc-144">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="992cc-144">Read/write</span></span><br/> | <span data-ttu-id="992cc-145">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="992cc-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="992cc-146">Obtém ou define a data e a hora em que o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="992cc-146">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="992cc-147">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="992cc-147">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="992cc-148">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="992cc-148">Read-only</span></span><br/>  | <span data-ttu-id="992cc-149">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="992cc-149">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="992cc-150">Obtém o tipo do gatilho.</span><span class="sxs-lookup"><span data-stu-id="992cc-150">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="992cc-151">Comentários</span><span class="sxs-lookup"><span data-stu-id="992cc-151">Remarks</span></span>

<span data-ttu-id="992cc-152">A hora do dia em que a tarefa é iniciada é definida pela propriedade [**StartBoundary**](trigger-startboundary.md) .</span><span class="sxs-lookup"><span data-stu-id="992cc-152">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="992cc-153">Um intervalo de 1 produz uma agenda diária.</span><span class="sxs-lookup"><span data-stu-id="992cc-153">An interval of 1 produces a daily schedule.</span></span> <span data-ttu-id="992cc-154">Um intervalo de 2 produz uma agenda de cada dia e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="992cc-154">An interval of 2 produces an every other day schedule and so on.</span></span>

<span data-ttu-id="992cc-155">Ao ler ou gravar seu próprio XML para uma tarefa, um gatilho diário é especificado usando o elemento [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="992cc-155">When reading or writing your own XML for a task, a daily trigger is specified using the [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="992cc-156">Exemplos</span><span class="sxs-lookup"><span data-stu-id="992cc-156">Examples</span></span>

<span data-ttu-id="992cc-157">Para obter mais informações e um exemplo de código para esse objeto de script, consulte [exemplo de gatilho diário (script)](daily-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="992cc-157">For more information and a code example for this scripting object, see [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="992cc-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="992cc-158">Requirements</span></span>



| <span data-ttu-id="992cc-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="992cc-159">Requirement</span></span> | <span data-ttu-id="992cc-160">Valor</span><span class="sxs-lookup"><span data-stu-id="992cc-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="992cc-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="992cc-161">Minimum supported client</span></span><br/> | <span data-ttu-id="992cc-162">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="992cc-162">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="992cc-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="992cc-163">Minimum supported server</span></span><br/> | <span data-ttu-id="992cc-164">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="992cc-164">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="992cc-165">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="992cc-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="992cc-166"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="992cc-166"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="992cc-167">DLL</span><span class="sxs-lookup"><span data-stu-id="992cc-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="992cc-168"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="992cc-168"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="992cc-169">Confira também</span><span class="sxs-lookup"><span data-stu-id="992cc-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="992cc-170">**Of**</span><span class="sxs-lookup"><span data-stu-id="992cc-170">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="992cc-171">**Disparador**</span><span class="sxs-lookup"><span data-stu-id="992cc-171">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="992cc-172">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="992cc-172">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





