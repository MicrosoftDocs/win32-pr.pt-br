---
title: Elemento CalendarTrigger (Trigger)
description: Especifica um gatilho diário, semanal, mensal ou um dia da semana (DOW) mensal.
ms.assetid: 9b9218bf-222c-4ece-8b37-5c5d8b765015
keywords:
- Agendador de Tarefas do gatilho de calendário, elemento XML
- Agendador de Tarefas do elemento CalendarTrigger
topic_type:
- apiref
api_name:
- CalendarTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02c061d8821dffa82eca8756ab26acadc6bb9281
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788040"
---
# <a name="calendartrigger-triggergroup-element"></a><span data-ttu-id="e9f0f-105">Elemento CalendarTrigger (Trigger)</span><span class="sxs-lookup"><span data-stu-id="e9f0f-105">CalendarTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="e9f0f-106">Especifica um gatilho diário, semanal, mensal ou um dia da semana (DOW) mensal.</span><span class="sxs-lookup"><span data-stu-id="e9f0f-106">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span>

``` syntax
<xs:element name="CalendarTrigger"
    type="calendarTriggerType"
 />
```

<span data-ttu-id="e9f0f-107">O elemento **CalendarTrigger** é definido pelo tipo complexo [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e9f0f-107">The **CalendarTrigger** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e9f0f-108">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="e9f0f-108">Parent element</span></span>



| <span data-ttu-id="e9f0f-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="e9f0f-109">Element</span></span>                                                           | <span data-ttu-id="e9f0f-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="e9f0f-110">Derived from</span></span>                                                         | <span data-ttu-id="e9f0f-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="e9f0f-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="e9f0f-112">**Gatilhos**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="e9f0f-113">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="e9f0f-114">Especifica os gatilhos que iniciam a tarefa.</span><span class="sxs-lookup"><span data-stu-id="e9f0f-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="e9f0f-115">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="e9f0f-115">Child elements</span></span>



| <span data-ttu-id="e9f0f-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="e9f0f-116">Element</span></span>                                                                                                                            | <span data-ttu-id="e9f0f-117">Type</span><span class="sxs-lookup"><span data-stu-id="e9f0f-117">Type</span></span>                                                                                                 | <span data-ttu-id="e9f0f-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="e9f0f-118">Description</span></span>                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9f0f-119">**Habilitado (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-119">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                                           | <span data-ttu-id="e9f0f-120">booleano</span><span class="sxs-lookup"><span data-stu-id="e9f0f-120">boolean</span></span>                                                                                              | <span data-ttu-id="e9f0f-121">Especifica que o gatilho está habilitado.</span><span class="sxs-lookup"><span data-stu-id="e9f0f-121">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="e9f0f-122">**TriggerBaseType (limite de entrada)**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-122">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)                                   | <span data-ttu-id="e9f0f-123">dateTime</span><span class="sxs-lookup"><span data-stu-id="e9f0f-123">dateTime</span></span>                                                                                             | <span data-ttu-id="e9f0f-124">Especifica a data e a hora em que o gatilho é desativado.</span><span class="sxs-lookup"><span data-stu-id="e9f0f-124">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="e9f0f-125">O gatilho não pode iniciar a tarefa depois que ela é desativada.</span><span class="sxs-lookup"><span data-stu-id="e9f0f-125">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="e9f0f-126">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-126">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)                     | <span data-ttu-id="e9f0f-127">duration</span><span class="sxs-lookup"><span data-stu-id="e9f0f-127">duration</span></span>                                                                                             | <span data-ttu-id="e9f0f-128">Especifica a quantidade máxima de tempo em que a tarefa pode ser iniciada pelo gatilho.</span><span class="sxs-lookup"><span data-stu-id="e9f0f-128">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="e9f0f-129">**Repetição (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-129">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                                     | [<span data-ttu-id="e9f0f-130">**repetição**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-130">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md)                             | <span data-ttu-id="e9f0f-131">Especifica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="e9f0f-131">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="e9f0f-132">**ScheduleByDay (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-132">**ScheduleByDay (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [<span data-ttu-id="e9f0f-133">**dailyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-133">**dailyScheduleType**</span></span>](taskschedulerschema-dailyscheduletype-complextype.md)                       | <span data-ttu-id="e9f0f-134">Especifica um agendamento diário.</span><span class="sxs-lookup"><span data-stu-id="e9f0f-134">Specifies a daily schedule.</span></span><br/>                                                                                             |
| [<span data-ttu-id="e9f0f-135">**ScheduleByMonth (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-135">**ScheduleByMonth (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [<span data-ttu-id="e9f0f-136">**monthlyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-136">**monthlyScheduleType**</span></span>](taskschedulerschema-monthlyscheduletype-complextype.md)                   | <span data-ttu-id="e9f0f-137">Especifica um agendamento mensal.</span><span class="sxs-lookup"><span data-stu-id="e9f0f-137">Specifies a monthly schedule.</span></span><br/>                                                                                           |
| [<span data-ttu-id="e9f0f-138">**ScheduleByMonthDayOfWeek (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-138">**ScheduleByMonthDayOfWeek (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="e9f0f-139">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-139">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="e9f0f-140">Especifica um gatilho que inicia um trabalho em uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="e9f0f-140">Specifies a trigger that starts a job on a monthly day-of-week schedule.</span></span><br/>                                                |
| [<span data-ttu-id="e9f0f-141">**ScheduleByWeek (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-141">**ScheduleByWeek (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [<span data-ttu-id="e9f0f-142">**weeklyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-142">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md)                     | <span data-ttu-id="e9f0f-143">Especifica uma agenda semanal.</span><span class="sxs-lookup"><span data-stu-id="e9f0f-143">Specifies a weekly schedule.</span></span><br/>                                                                                            |
| [<span data-ttu-id="e9f0f-144">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-144">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)                               | <span data-ttu-id="e9f0f-145">dateTime</span><span class="sxs-lookup"><span data-stu-id="e9f0f-145">dateTime</span></span>                                                                                             | <span data-ttu-id="e9f0f-146">Especifica a data e a hora em que o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="e9f0f-146">Specifies the date and time when the trigger is activated.</span></span> <span data-ttu-id="e9f0f-147">Este elemento é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e9f0f-147">This element is required.</span></span><br/>                                    |



## <a name="attributes"></a><span data-ttu-id="e9f0f-148">Atributos</span><span class="sxs-lookup"><span data-stu-id="e9f0f-148">Attributes</span></span>



| <span data-ttu-id="e9f0f-149">Nome</span><span class="sxs-lookup"><span data-stu-id="e9f0f-149">Name</span></span> | <span data-ttu-id="e9f0f-150">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9f0f-150">Type</span></span> | <span data-ttu-id="e9f0f-151">Descrição</span><span class="sxs-lookup"><span data-stu-id="e9f0f-151">Description</span></span>                               |
|------|------|-------------------------------------------|
| <span data-ttu-id="e9f0f-152">ID</span><span class="sxs-lookup"><span data-stu-id="e9f0f-152">Id</span></span>   | <span data-ttu-id="e9f0f-153">ID</span><span class="sxs-lookup"><span data-stu-id="e9f0f-153">ID</span></span>   | <span data-ttu-id="e9f0f-154">O identificador do gatilho.</span><span class="sxs-lookup"><span data-stu-id="e9f0f-154">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e9f0f-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9f0f-155">Remarks</span></span>

<span data-ttu-id="e9f0f-156">O elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) é um elemento necessário para gatilhos de tempo e calendário ([**timetrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) e **CalendarTrigger**).</span><span class="sxs-lookup"><span data-stu-id="e9f0f-156">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time and calendar triggers ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) and **CalendarTrigger**).</span></span>

<span data-ttu-id="e9f0f-157">Os elementos filho listados acima são definidos pelos tipos de elementos complexos [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) e [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e9f0f-157">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) and [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex element types.</span></span>

<span data-ttu-id="e9f0f-158">Para desenvolvimento de script, os gatilhos de calendário são especificados usando um dos objetos a seguir.</span><span class="sxs-lookup"><span data-stu-id="e9f0f-158">For script development, calendar triggers are specified using one of the following objects.</span></span>

-   [<span data-ttu-id="e9f0f-159">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-159">**DailyTrigger**</span></span>](dailytrigger.md)
-   [<span data-ttu-id="e9f0f-160">**WeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-160">**WeeklyTrigger**</span></span>](weeklytrigger.md)
-   [<span data-ttu-id="e9f0f-161">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-161">**MonthlyTrigger**</span></span>](monthlytrigger.md)
-   [<span data-ttu-id="e9f0f-162">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-162">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)

<span data-ttu-id="e9f0f-163">Para desenvolvimento em C++, os gatilhos de calendário são especificados usando uma das interfaces a seguir.</span><span class="sxs-lookup"><span data-stu-id="e9f0f-163">For C++ development, calendar triggers are specified using one of the following interfaces.</span></span>

-   [<span data-ttu-id="e9f0f-164">**IDailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-164">**IDailyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [<span data-ttu-id="e9f0f-165">**IWeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-165">**IWeeklyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)
-   [<span data-ttu-id="e9f0f-166">**IMonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-166">**IMonthlyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [<span data-ttu-id="e9f0f-167">**IMonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="e9f0f-167">**IMonthlyDOWTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)

## <a name="examples"></a><span data-ttu-id="e9f0f-168">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e9f0f-168">Examples</span></span>

<span data-ttu-id="e9f0f-169">Para obter um exemplo completo do XML para uma tarefa que especifica um gatilho de calendário, consulte [exemplo de gatilho diário (XML)](daily-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="e9f0f-169">For a complete example of the XML for a task that specifies a calendar trigger, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9f0f-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9f0f-170">Requirements</span></span>



| <span data-ttu-id="e9f0f-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9f0f-171">Requirement</span></span> | <span data-ttu-id="e9f0f-172">Valor</span><span class="sxs-lookup"><span data-stu-id="e9f0f-172">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e9f0f-173">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9f0f-173">Minimum supported client</span></span><br/> | <span data-ttu-id="e9f0f-174">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e9f0f-174">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e9f0f-175">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9f0f-175">Minimum supported server</span></span><br/> | <span data-ttu-id="e9f0f-176">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e9f0f-176">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e9f0f-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9f0f-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9f0f-178">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="e9f0f-178">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="e9f0f-179">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="e9f0f-179">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





