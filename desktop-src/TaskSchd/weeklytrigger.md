---
title: Objeto WeeklyTrigger
description: Objeto de script que representa um gatilho que inicia uma tarefa com base em uma agenda semanal.
ms.assetid: a000d7a8-0239-440f-b49b-7f0c55b01e8e
keywords:
- gatilho semanal Agendador de Tarefas, objeto
- Agendador de Tarefas de objeto WeeklyTrigger
- Agendador de Tarefas de objeto WeeklyTrigger, descrito
topic_type:
- apiref
api_name:
- WeeklyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58dec9172d38b53f779f44a048b39bc709dbd54f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645237"
---
# <a name="weeklytrigger-object"></a><span data-ttu-id="149ad-106">Objeto WeeklyTrigger</span><span class="sxs-lookup"><span data-stu-id="149ad-106">WeeklyTrigger object</span></span>

<span data-ttu-id="149ad-107">Objeto de script que representa um gatilho que inicia uma tarefa com base em uma agenda semanal.</span><span class="sxs-lookup"><span data-stu-id="149ad-107">Scripting object that represents a trigger that starts a task based on a weekly schedule.</span></span> <span data-ttu-id="149ad-108">Por exemplo, a tarefa começa às 8:00.</span><span class="sxs-lookup"><span data-stu-id="149ad-108">For example, the task starts at 8:00 A.M.</span></span> <span data-ttu-id="149ad-109">em um dia específico da semana a cada semana ou a cada semana.</span><span class="sxs-lookup"><span data-stu-id="149ad-109">on a specific day of the week every week or every other week.</span></span>

## <a name="members"></a><span data-ttu-id="149ad-110">Membros</span><span class="sxs-lookup"><span data-stu-id="149ad-110">Members</span></span>

<span data-ttu-id="149ad-111">O objeto **WeeklyTrigger** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="149ad-111">The **WeeklyTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="149ad-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="149ad-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="149ad-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="149ad-113">Properties</span></span>

<span data-ttu-id="149ad-114">O objeto **WeeklyTrigger** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="149ad-114">The **WeeklyTrigger** object has these properties.</span></span>



| <span data-ttu-id="149ad-115">Propriedade</span><span class="sxs-lookup"><span data-stu-id="149ad-115">Property</span></span>                                                            | <span data-ttu-id="149ad-116">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="149ad-116">Access type</span></span>           | <span data-ttu-id="149ad-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="149ad-117">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="149ad-118">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="149ad-118">**DaysOfWeek**</span></span>](weeklytrigger-daysofweek.md)<br/>           | <span data-ttu-id="149ad-119">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="149ad-119">Read/write</span></span><br/> | <span data-ttu-id="149ad-120">Obtém ou define os dias da semana em que a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="149ad-120">Gets or sets the days of the week on which the task runs.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="149ad-121">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="149ad-121">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="149ad-122">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="149ad-122">Read/write</span></span><br/> | <span data-ttu-id="149ad-123">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="149ad-123">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="149ad-124">Obtém ou define um valor booliano que indica se o gatilho está habilitado.</span><span class="sxs-lookup"><span data-stu-id="149ad-124">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="149ad-125">**Limite de fim**</span><span class="sxs-lookup"><span data-stu-id="149ad-125">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="149ad-126">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="149ad-126">Read/write</span></span><br/> | <span data-ttu-id="149ad-127">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="149ad-127">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="149ad-128">Obtém ou define a data e a hora em que o gatilho é desativado.</span><span class="sxs-lookup"><span data-stu-id="149ad-128">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="149ad-129">O gatilho não pode iniciar a tarefa depois que ela é desativada.</span><span class="sxs-lookup"><span data-stu-id="149ad-129">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="149ad-130">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="149ad-130">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="149ad-131">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="149ad-131">Read/write</span></span><br/> | <span data-ttu-id="149ad-132">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="149ad-132">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="149ad-133">Obtém ou define a quantidade máxima de tempo que a tarefa iniciada pelo gatilho tem permissão para ser executada.</span><span class="sxs-lookup"><span data-stu-id="149ad-133">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="149ad-134">**ID**</span><span class="sxs-lookup"><span data-stu-id="149ad-134">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="149ad-135">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="149ad-135">Read/write</span></span><br/> | <span data-ttu-id="149ad-136">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="149ad-136">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="149ad-137">Obtém ou define o identificador do gatilho.</span><span class="sxs-lookup"><span data-stu-id="149ad-137">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="149ad-138">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="149ad-138">**RandomDelay**</span></span>](weeklytrigger-randomdelay.md)<br/>         | <span data-ttu-id="149ad-139">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="149ad-139">Read/write</span></span><br/> | <span data-ttu-id="149ad-140">Obtém ou define um tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho.</span><span class="sxs-lookup"><span data-stu-id="149ad-140">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="149ad-141">**Repetição**</span><span class="sxs-lookup"><span data-stu-id="149ad-141">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="149ad-142">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="149ad-142">Read/write</span></span><br/> | <span data-ttu-id="149ad-143">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="149ad-143">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="149ad-144">Obtém ou define com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="149ad-144">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="149ad-145">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="149ad-145">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="149ad-146">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="149ad-146">Read/write</span></span><br/> | <span data-ttu-id="149ad-147">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="149ad-147">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="149ad-148">Obtém ou define a data e a hora em que o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="149ad-148">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="149ad-149">**Escreva**</span><span class="sxs-lookup"><span data-stu-id="149ad-149">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="149ad-150">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="149ad-150">Read-only</span></span><br/>  | <span data-ttu-id="149ad-151">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="149ad-151">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="149ad-152">Obtém o tipo do gatilho.</span><span class="sxs-lookup"><span data-stu-id="149ad-152">Gets the type of the trigger.</span></span><br/>                                                                                              |
| [<span data-ttu-id="149ad-153">**WeeksInterval**</span><span class="sxs-lookup"><span data-stu-id="149ad-153">**WeeksInterval**</span></span>](weeklytrigger-weeksinterval.md)<br/>     | <span data-ttu-id="149ad-154">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="149ad-154">Read/write</span></span><br/> | <span data-ttu-id="149ad-155">Obtém ou define o intervalo entre as semanas no agendamento.</span><span class="sxs-lookup"><span data-stu-id="149ad-155">Gets or sets the interval between the weeks in the schedule.</span></span><br/>                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="149ad-156">Comentários</span><span class="sxs-lookup"><span data-stu-id="149ad-156">Remarks</span></span>

<span data-ttu-id="149ad-157">A hora do dia em que a tarefa é iniciada é definida pela propriedade [**StartBoundary**](trigger-startboundary.md) .</span><span class="sxs-lookup"><span data-stu-id="149ad-157">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="149ad-158">Ao ler ou gravar seu próprio XML para uma tarefa, um gatilho semanal é especificado usando o elemento [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="149ad-158">When reading or writing your own XML for a task, a weekly trigger is specified using the [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="149ad-159">Exemplos</span><span class="sxs-lookup"><span data-stu-id="149ad-159">Examples</span></span>

<span data-ttu-id="149ad-160">Para obter mais informações e um exemplo de código para esse objeto de script, consulte [exemplo de gatilho semanal (script)](weekly-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="149ad-160">For more information and a code example for this scripting object, see [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="149ad-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="149ad-161">Requirements</span></span>



| <span data-ttu-id="149ad-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="149ad-162">Requirement</span></span> | <span data-ttu-id="149ad-163">Valor</span><span class="sxs-lookup"><span data-stu-id="149ad-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="149ad-164">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="149ad-164">Minimum supported client</span></span><br/> | <span data-ttu-id="149ad-165">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="149ad-165">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="149ad-166">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="149ad-166">Minimum supported server</span></span><br/> | <span data-ttu-id="149ad-167">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="149ad-167">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="149ad-168">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="149ad-168">Type library</span></span><br/>             | <dl> <span data-ttu-id="149ad-169"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="149ad-169"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="149ad-170">DLL</span><span class="sxs-lookup"><span data-stu-id="149ad-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="149ad-171"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="149ad-171"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="149ad-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="149ad-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="149ad-173">**Of**</span><span class="sxs-lookup"><span data-stu-id="149ad-173">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="149ad-174">**Disparador**</span><span class="sxs-lookup"><span data-stu-id="149ad-174">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="149ad-175">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="149ad-175">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





