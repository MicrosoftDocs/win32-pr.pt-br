---
title: Objeto MonthlyTrigger
description: Objeto de script que representa um gatilho que inicia uma tarefa com base em um agendamento mensal.
ms.assetid: d73715cb-a52e-4daf-930f-e94fbe28881e
keywords:
- Agendador de Tarefas do gatilho mensal, objeto
- Agendador de Tarefas de objeto MonthlyTrigger
- Agendador de Tarefas de objeto MonthlyTrigger, descrito
topic_type:
- apiref
api_name:
- MonthlyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce433f626fbe45e209f881c00787495cc6343bc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644745"
---
# <a name="monthlytrigger-object"></a><span data-ttu-id="639ae-106">Objeto MonthlyTrigger</span><span class="sxs-lookup"><span data-stu-id="639ae-106">MonthlyTrigger object</span></span>

<span data-ttu-id="639ae-107">Objeto de script que representa um gatilho que inicia uma tarefa com base em um agendamento mensal.</span><span class="sxs-lookup"><span data-stu-id="639ae-107">Scripting object that represents a trigger that starts a task based on a monthly schedule.</span></span> <span data-ttu-id="639ae-108">Por exemplo, a tarefa é iniciada em dias específicos de meses específicos.</span><span class="sxs-lookup"><span data-stu-id="639ae-108">For example, the task starts on specific days of specific months.</span></span>

## <a name="members"></a><span data-ttu-id="639ae-109">Membros</span><span class="sxs-lookup"><span data-stu-id="639ae-109">Members</span></span>

<span data-ttu-id="639ae-110">O objeto **MonthlyTrigger** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="639ae-110">The **MonthlyTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="639ae-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="639ae-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="639ae-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="639ae-112">Properties</span></span>

<span data-ttu-id="639ae-113">O objeto **MonthlyTrigger** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="639ae-113">The **MonthlyTrigger** object has these properties.</span></span>



| <span data-ttu-id="639ae-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="639ae-114">Property</span></span>                                                                     | <span data-ttu-id="639ae-115">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="639ae-115">Access type</span></span>           | <span data-ttu-id="639ae-116">Description</span><span class="sxs-lookup"><span data-stu-id="639ae-116">Description</span></span>                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="639ae-117">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="639ae-117">**DaysOfMonth**</span></span>](monthlytrigger-daysofmonth.md)<br/>                 | <span data-ttu-id="639ae-118">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="639ae-118">Read/write</span></span><br/> | <span data-ttu-id="639ae-119">Obtém ou define os dias do mês durante os quais a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="639ae-119">Gets or sets the days of the month during which the task runs.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="639ae-120">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="639ae-120">**Enabled**</span></span>](trigger-enabled.md)<br/>                                | <span data-ttu-id="639ae-121">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="639ae-121">Read/write</span></span><br/> | <span data-ttu-id="639ae-122">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="639ae-122">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="639ae-123">Obtém ou define um valor booliano que indica se o gatilho está habilitado.</span><span class="sxs-lookup"><span data-stu-id="639ae-123">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="639ae-124">Limite de fim</span><span class="sxs-lookup"><span data-stu-id="639ae-124">EndBoundary</span></span>](trigger-endboundary.md)<br/>                            | <span data-ttu-id="639ae-125">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="639ae-125">Read/write</span></span><br/> | <span data-ttu-id="639ae-126">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="639ae-126">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="639ae-127">Obtém ou define a data e a hora em que o gatilho é desativado.</span><span class="sxs-lookup"><span data-stu-id="639ae-127">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="639ae-128">O gatilho não pode iniciar a tarefa depois que ela é desativada.</span><span class="sxs-lookup"><span data-stu-id="639ae-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="639ae-129">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="639ae-129">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/>          | <span data-ttu-id="639ae-130">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="639ae-130">Read/write</span></span><br/> | <span data-ttu-id="639ae-131">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="639ae-131">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="639ae-132">Obtém ou define a quantidade máxima de tempo que a tarefa iniciada pelo gatilho tem permissão para ser executada.</span><span class="sxs-lookup"><span data-stu-id="639ae-132">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="639ae-133">**Sessão**</span><span class="sxs-lookup"><span data-stu-id="639ae-133">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                         | <span data-ttu-id="639ae-134">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="639ae-134">Read/write</span></span><br/> | <span data-ttu-id="639ae-135">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="639ae-135">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="639ae-136">Obtém ou define o identificador do gatilho.</span><span class="sxs-lookup"><span data-stu-id="639ae-136">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="639ae-137">**MonthsOfYear**</span><span class="sxs-lookup"><span data-stu-id="639ae-137">**MonthsOfYear**</span></span>](monthlytrigger-monthsofyear.md)<br/>               | <span data-ttu-id="639ae-138">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="639ae-138">Read/write</span></span><br/> | <span data-ttu-id="639ae-139">Obtém ou define os meses do ano durante os quais a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="639ae-139">Gets or sets the months of the year during which the task runs.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="639ae-140">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="639ae-140">**RandomDelay**</span></span>](monthlytrigger-randomdelay.md)<br/>                 | <span data-ttu-id="639ae-141">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="639ae-141">Read/write</span></span><br/> | <span data-ttu-id="639ae-142">Obtém ou define um tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho.</span><span class="sxs-lookup"><span data-stu-id="639ae-142">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="639ae-143">**Repetição**</span><span class="sxs-lookup"><span data-stu-id="639ae-143">**Repetition**</span></span>](trigger-repetition.md)<br/>                          | <span data-ttu-id="639ae-144">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="639ae-144">Read/write</span></span><br/> | <span data-ttu-id="639ae-145">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="639ae-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="639ae-146">Obtém ou define com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="639ae-146">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="639ae-147">**RunOnLastDayOfMonth**</span><span class="sxs-lookup"><span data-stu-id="639ae-147">**RunOnLastDayOfMonth**</span></span>](monthlytrigger-runonlastdayofmonth.md)<br/> | <span data-ttu-id="639ae-148">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="639ae-148">Read/write</span></span><br/> | <span data-ttu-id="639ae-149">Obtém ou define um valor booliano que indica que a tarefa é executada no último dia do mês.</span><span class="sxs-lookup"><span data-stu-id="639ae-149">Gets or sets a Boolean value that indicates that the task runs on the last day of the month.</span></span><br/>                                                                                     |
| [<span data-ttu-id="639ae-150">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="639ae-150">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>                    | <span data-ttu-id="639ae-151">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="639ae-151">Read/write</span></span><br/> | <span data-ttu-id="639ae-152">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="639ae-152">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="639ae-153">Obtém ou define a data e a hora em que o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="639ae-153">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="639ae-154">**Escreva**</span><span class="sxs-lookup"><span data-stu-id="639ae-154">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                     | <span data-ttu-id="639ae-155">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="639ae-155">Read-only</span></span><br/>  | <span data-ttu-id="639ae-156">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="639ae-156">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="639ae-157">Obtém o tipo do gatilho.</span><span class="sxs-lookup"><span data-stu-id="639ae-157">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="639ae-158">Comentários</span><span class="sxs-lookup"><span data-stu-id="639ae-158">Remarks</span></span>

<span data-ttu-id="639ae-159">A hora do dia em que a tarefa é iniciada é definida pela propriedade [**StartBoundary**](trigger-startboundary.md) .</span><span class="sxs-lookup"><span data-stu-id="639ae-159">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="639ae-160">Ao ler ou gravar seu próprio XML para uma tarefa, um gatilho mensal é especificado usando o elemento [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="639ae-160">When reading or writing your own XML for a task, a monthly trigger is specified using the [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="639ae-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="639ae-161">Requirements</span></span>



| <span data-ttu-id="639ae-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="639ae-162">Requirement</span></span> | <span data-ttu-id="639ae-163">Valor</span><span class="sxs-lookup"><span data-stu-id="639ae-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="639ae-164">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="639ae-164">Minimum supported client</span></span><br/> | <span data-ttu-id="639ae-165">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="639ae-165">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="639ae-166">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="639ae-166">Minimum supported server</span></span><br/> | <span data-ttu-id="639ae-167">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="639ae-167">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="639ae-168">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="639ae-168">Type library</span></span><br/>             | <dl> <span data-ttu-id="639ae-169"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="639ae-169"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="639ae-170">DLL</span><span class="sxs-lookup"><span data-stu-id="639ae-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="639ae-171"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="639ae-171"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="639ae-172">Consulte também</span><span class="sxs-lookup"><span data-stu-id="639ae-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="639ae-173">**Of**</span><span class="sxs-lookup"><span data-stu-id="639ae-173">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="639ae-174">Objetos Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="639ae-174">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="639ae-175">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="639ae-175">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="639ae-176">**Disparador**</span><span class="sxs-lookup"><span data-stu-id="639ae-176">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="639ae-177">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="639ae-177">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





