---
title: Objeto MonthlyDOWTrigger
description: Objeto de script que representa um gatilho que inicia uma tarefa em uma agenda mensal de dia da semana.
ms.assetid: 18607189-295f-4f7d-bf72-f0ac8d5067cf
keywords:
- Agendador de Tarefas do gatilho de DOW mensal, objeto
- Agendador de Tarefas de objeto MonthlyDOWTrigger
- Agendador de Tarefas de objeto MonthlyDOWTrigger, descrito
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7e43925c6ebe27933a39fe5e25f37ffe6cf72e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009158"
---
# <a name="monthlydowtrigger-object"></a><span data-ttu-id="055df-106">Objeto MonthlyDOWTrigger</span><span class="sxs-lookup"><span data-stu-id="055df-106">MonthlyDOWTrigger object</span></span>

<span data-ttu-id="055df-107">Objeto de script que representa um gatilho que inicia uma tarefa em uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="055df-107">Scripting object that represents a trigger that starts a task on a monthly day-of-week schedule.</span></span> <span data-ttu-id="055df-108">Por exemplo, a tarefa começa em todas as primeiras quintas-feiras, pode até outubro.</span><span class="sxs-lookup"><span data-stu-id="055df-108">For example, the task starts on every first Thursday, May through October.</span></span>

## <a name="members"></a><span data-ttu-id="055df-109">Membros</span><span class="sxs-lookup"><span data-stu-id="055df-109">Members</span></span>

<span data-ttu-id="055df-110">O objeto **MonthlyDOWTrigger** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="055df-110">The **MonthlyDOWTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="055df-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="055df-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="055df-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="055df-112">Properties</span></span>

<span data-ttu-id="055df-113">O objeto **MonthlyDOWTrigger** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="055df-113">The **MonthlyDOWTrigger** object has these properties.</span></span>



| <span data-ttu-id="055df-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="055df-114">Property</span></span>                                                                          | <span data-ttu-id="055df-115">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="055df-115">Access type</span></span>           | <span data-ttu-id="055df-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="055df-116">Description</span></span>                                                                                                                                                                                 |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="055df-117">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="055df-117">**DaysOfWeek**</span></span>](monthlydowtrigger-daysofweek.md)<br/>                     | <span data-ttu-id="055df-118">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="055df-118">Read/write</span></span><br/> | <span data-ttu-id="055df-119">Obtém ou define os dias da semana durante os quais a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="055df-119">Gets or sets the days of the week during which the task runs.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="055df-120">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="055df-120">**Enabled**</span></span>](trigger-enabled.md)<br/>                                     | <span data-ttu-id="055df-121">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="055df-121">Read/write</span></span><br/> | <span data-ttu-id="055df-122">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="055df-122">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="055df-123">Obtém ou define um valor booliano que indica se o gatilho está habilitado.</span><span class="sxs-lookup"><span data-stu-id="055df-123">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="055df-124">Limite de fim</span><span class="sxs-lookup"><span data-stu-id="055df-124">EndBoundary</span></span>](trigger-endboundary.md)<br/>                                 | <span data-ttu-id="055df-125">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="055df-125">Read/write</span></span><br/> | <span data-ttu-id="055df-126">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="055df-126">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="055df-127">Obtém ou define a data e a hora em que o gatilho é desativado.</span><span class="sxs-lookup"><span data-stu-id="055df-127">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="055df-128">O gatilho não pode iniciar a tarefa depois que ela é desativada.</span><span class="sxs-lookup"><span data-stu-id="055df-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="055df-129">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="055df-129">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/>               | <span data-ttu-id="055df-130">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="055df-130">Read/write</span></span><br/> | <span data-ttu-id="055df-131">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="055df-131">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="055df-132">Obtém ou define a quantidade máxima de tempo que a tarefa iniciada por esse gatilho tem permissão para ser executada.</span><span class="sxs-lookup"><span data-stu-id="055df-132">Gets or sets the maximum amount of time that the task launched by this trigger is allowed to run.</span></span><br/>                          |
| [<span data-ttu-id="055df-133">**Sessão**</span><span class="sxs-lookup"><span data-stu-id="055df-133">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                              | <span data-ttu-id="055df-134">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="055df-134">Read/write</span></span><br/> | <span data-ttu-id="055df-135">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="055df-135">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="055df-136">Obtém ou define o identificador do gatilho.</span><span class="sxs-lookup"><span data-stu-id="055df-136">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="055df-137">**MonthsOfYear**</span><span class="sxs-lookup"><span data-stu-id="055df-137">**MonthsOfYear**</span></span>](monthlydowtrigger-monthsofyear.md)<br/>                 | <span data-ttu-id="055df-138">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="055df-138">Read/write</span></span><br/> | <span data-ttu-id="055df-139">Obtém ou define os meses do ano durante os quais a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="055df-139">Gets or sets the months of the year during which the task runs.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="055df-140">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="055df-140">**RandomDelay**</span></span>](monthlydowtrigger-randomdelay.md)<br/>                   | <span data-ttu-id="055df-141">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="055df-141">Read/write</span></span><br/> | <span data-ttu-id="055df-142">Obtém ou define um tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho.</span><span class="sxs-lookup"><span data-stu-id="055df-142">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="055df-143">**Repetição**</span><span class="sxs-lookup"><span data-stu-id="055df-143">**Repetition**</span></span>](trigger-repetition.md)<br/>                               | <span data-ttu-id="055df-144">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="055df-144">Read/write</span></span><br/> | <span data-ttu-id="055df-145">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="055df-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="055df-146">Obtém ou define com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="055df-146">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="055df-147">**RunOnLastWeekOfMonth**</span><span class="sxs-lookup"><span data-stu-id="055df-147">**RunOnLastWeekOfMonth**</span></span>](monthlydowtrigger-runonlastweekofmonth.md)<br/> | <span data-ttu-id="055df-148">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="055df-148">Read/write</span></span><br/> | <span data-ttu-id="055df-149">Obtém ou define um valor booliano que indica que a tarefa é executada na última semana do mês.</span><span class="sxs-lookup"><span data-stu-id="055df-149">Gets or sets a Boolean value that indicates that the task runs on the last week of the month.</span></span><br/>                                                                                    |
| [<span data-ttu-id="055df-150">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="055df-150">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>                         | <span data-ttu-id="055df-151">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="055df-151">Read/write</span></span><br/> | <span data-ttu-id="055df-152">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="055df-152">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="055df-153">Obtém ou define a data e a hora em que o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="055df-153">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="055df-154">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="055df-154">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                          | <span data-ttu-id="055df-155">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="055df-155">Read-only</span></span><br/>  | <span data-ttu-id="055df-156">Herdado do objeto de [**gatilho**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="055df-156">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="055df-157">Obtém o tipo do gatilho.</span><span class="sxs-lookup"><span data-stu-id="055df-157">Gets the type of the trigger.</span></span><br/>                                                                                              |
| [<span data-ttu-id="055df-158">**WeeksOfMonth**</span><span class="sxs-lookup"><span data-stu-id="055df-158">**WeeksOfMonth**</span></span>](monthlydowtrigger-weeksofmonth.md)<br/>                 | <span data-ttu-id="055df-159">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="055df-159">Read/write</span></span><br/> | <span data-ttu-id="055df-160">Obtém ou define as semanas do mês em que a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="055df-160">Gets or sets the weeks of the month during which the task runs.</span></span><br/>                                                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="055df-161">Comentários</span><span class="sxs-lookup"><span data-stu-id="055df-161">Remarks</span></span>

<span data-ttu-id="055df-162">A hora do dia em que a tarefa é iniciada é definida pela propriedade [**StartBoundary**](trigger-startboundary.md) .</span><span class="sxs-lookup"><span data-stu-id="055df-162">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="055df-163">Ao ler ou gravar XML para uma tarefa, um gatilho mensal de dia da semana é especificado usando o elemento [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="055df-163">When reading or writing XML for a task, a monthly day-of-week trigger is specified using the [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="055df-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="055df-164">Requirements</span></span>



| <span data-ttu-id="055df-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="055df-165">Requirement</span></span> | <span data-ttu-id="055df-166">Valor</span><span class="sxs-lookup"><span data-stu-id="055df-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="055df-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="055df-167">Minimum supported client</span></span><br/> | <span data-ttu-id="055df-168">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="055df-168">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="055df-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="055df-169">Minimum supported server</span></span><br/> | <span data-ttu-id="055df-170">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="055df-170">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="055df-171">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="055df-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="055df-172"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="055df-172"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="055df-173">DLL</span><span class="sxs-lookup"><span data-stu-id="055df-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="055df-174"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="055df-174"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="055df-175">Confira também</span><span class="sxs-lookup"><span data-stu-id="055df-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="055df-176">**Of**</span><span class="sxs-lookup"><span data-stu-id="055df-176">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="055df-177">Objetos Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="055df-177">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="055df-178">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="055df-178">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="055df-179">**Disparador**</span><span class="sxs-lookup"><span data-stu-id="055df-179">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="055df-180">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="055df-180">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





