---
title: Elemento DaysOfWeek (weeklyScheduleType)
description: Especifica os dias da semana em que a tarefa é executada. | Elemento DaysOfWeek (weeklyScheduleType)
ms.assetid: 86555681-2324-4095-9eab-fdef40e0acba
keywords:
- Elemento DaysOfWeek Agendador de Tarefas
topic_type:
- apiref
api_name:
- DaysOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a2b310feb49f3141d1f7f08c4552305f9ffc3ea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105767731"
---
# <a name="daysofweek-weeklyscheduletype-element"></a><span data-ttu-id="e0da2-105">Elemento DaysOfWeek (weeklyScheduleType)</span><span class="sxs-lookup"><span data-stu-id="e0da2-105">DaysOfWeek (weeklyScheduleType) Element</span></span>

<span data-ttu-id="e0da2-106">Especifica os dias da semana em que a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="e0da2-106">Specifies the days of the week in which the task runs.</span></span>

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

<span data-ttu-id="e0da2-107">O elemento **DaysOfWeek** é definido pelo tipo complexo [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e0da2-107">The **DaysOfWeek** element is defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e0da2-108">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="e0da2-108">Parent element</span></span>



| <span data-ttu-id="e0da2-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="e0da2-109">Element</span></span>                                                                                  | <span data-ttu-id="e0da2-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="e0da2-110">Derived from</span></span>                                                                     | <span data-ttu-id="e0da2-111">Description</span><span class="sxs-lookup"><span data-stu-id="e0da2-111">Description</span></span>                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="e0da2-112">**ScheduleByWeek**</span><span class="sxs-lookup"><span data-stu-id="e0da2-112">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [<span data-ttu-id="e0da2-113">**weeklyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="e0da2-113">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md) | <span data-ttu-id="e0da2-114">Especifica uma agenda semanal.</span><span class="sxs-lookup"><span data-stu-id="e0da2-114">Specifies a weekly schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="e0da2-115">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="e0da2-115">Child elements</span></span>



| <span data-ttu-id="e0da2-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="e0da2-116">Element</span></span>                                                                   | <span data-ttu-id="e0da2-117">Type</span><span class="sxs-lookup"><span data-stu-id="e0da2-117">Type</span></span> | <span data-ttu-id="e0da2-118">Description</span><span class="sxs-lookup"><span data-stu-id="e0da2-118">Description</span></span>                                           |
|---------------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="e0da2-119">**Friday**</span><span class="sxs-lookup"><span data-stu-id="e0da2-119">**Friday**</span></span>](taskschedulerschema-friday-daysofweektype-element.md)       |      | <span data-ttu-id="e0da2-120">Especifica que a tarefa é executada na sexta-feira.</span><span class="sxs-lookup"><span data-stu-id="e0da2-120">Specifies that the task runs on Friday.</span></span><br/>    |
| [<span data-ttu-id="e0da2-121">**Monday**</span><span class="sxs-lookup"><span data-stu-id="e0da2-121">**Monday**</span></span>](taskschedulerschema-monday-daysofweektype-element.md)       |      | <span data-ttu-id="e0da2-122">Especifica que a tarefa é executada na segunda-feira.</span><span class="sxs-lookup"><span data-stu-id="e0da2-122">Specifies that the task runs on Monday.</span></span><br/>    |
| [<span data-ttu-id="e0da2-123">**Sábado**</span><span class="sxs-lookup"><span data-stu-id="e0da2-123">**Saturday**</span></span>](taskschedulerschema-saturday-daysofweektype-element.md)   |      | <span data-ttu-id="e0da2-124">Especifica que a tarefa é executada no sábado.</span><span class="sxs-lookup"><span data-stu-id="e0da2-124">Specifies that the task runs on Saturday.</span></span><br/>  |
| [<span data-ttu-id="e0da2-125">**Sunday**</span><span class="sxs-lookup"><span data-stu-id="e0da2-125">**Sunday**</span></span>](taskschedulerschema-sunday-daysofweektype-element.md)       |      | <span data-ttu-id="e0da2-126">Especifica que a tarefa é executada no domingo.</span><span class="sxs-lookup"><span data-stu-id="e0da2-126">Specifies that the task runs on Sunday.</span></span><br/>    |
| [<span data-ttu-id="e0da2-127">**Quinta-feira**</span><span class="sxs-lookup"><span data-stu-id="e0da2-127">**Thursday**</span></span>](taskschedulerschema-thursday-daysofweektype-element.md)   |      | <span data-ttu-id="e0da2-128">Especifica que a tarefa é executada na quinta-feira.</span><span class="sxs-lookup"><span data-stu-id="e0da2-128">Specifies that the task runs on Thursday.</span></span><br/>  |
| [<span data-ttu-id="e0da2-129">**Terça-feira**</span><span class="sxs-lookup"><span data-stu-id="e0da2-129">**Tuesday**</span></span>](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | <span data-ttu-id="e0da2-130">Especifica que a tarefa é executada na terça-feira.</span><span class="sxs-lookup"><span data-stu-id="e0da2-130">Specifies that the task runs on Tuesday.</span></span><br/>   |
| [<span data-ttu-id="e0da2-131">**Quarta-feira**</span><span class="sxs-lookup"><span data-stu-id="e0da2-131">**Wednesday**</span></span>](taskschedulerschema-wednesday-daysofweektype-element.md) |      | <span data-ttu-id="e0da2-132">Especifica que a tarefa é executada na quarta-feira.</span><span class="sxs-lookup"><span data-stu-id="e0da2-132">Specifies that the task runs on Wednesday.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e0da2-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0da2-133">Remarks</span></span>

<span data-ttu-id="e0da2-134">Os elementos filho anteriores são definidos pelo tipo complexo [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e0da2-134">The previous child elements are defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

<span data-ttu-id="e0da2-135">Para o desenvolvimento de scripts, o intervalo semanal é especificado usando a propriedade [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md) .</span><span class="sxs-lookup"><span data-stu-id="e0da2-135">For scripting development, the weekly interval is specified using the [**WeeklyTrigger.WeeksInterval**](weeklytrigger-weeksinterval.md) property.</span></span>

<span data-ttu-id="e0da2-136">Para desenvolvimento em C++, o intervalo semanal é especificado usando a propriedade [**IWeeklyTrigger:: WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) .</span><span class="sxs-lookup"><span data-stu-id="e0da2-136">For C++ development, the weekly interval is specified using the [**IWeeklyTrigger::WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="e0da2-137">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e0da2-137">Examples</span></span>

<span data-ttu-id="e0da2-138">O XML a seguir define um gatilho de calendário diário que inicia uma tarefa de segunda-feira a sexta-feira (às 8:00) todas as semanas.</span><span class="sxs-lookup"><span data-stu-id="e0da2-138">The following XML defines a daily calendar trigger that starts a task Monday through Friday ( at 8:00 AM) every week.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByWeek>
        <WeeksInterval>1</WeeksInterval>
        <DaysOfWeek>
            <Monday/>
            <Tuesday/>
            <Wednesday/>
            <Thurday/>
            <Friday/>
        </DaysOfWeek>
    </ScheduleByWeek>
</CalendarTrigger>
```



<span data-ttu-id="e0da2-139">Para obter um exemplo completo do XML para uma tarefa que usa um gatilho semanal, consulte [exemplo de gatilho semanal (XML)](weekly-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="e0da2-139">For a complete example of the XML for a task that uses a weekly trigger, see [Weekly Trigger Example (XML)](weekly-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0da2-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0da2-140">Requirements</span></span>



| <span data-ttu-id="e0da2-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0da2-141">Requirement</span></span> | <span data-ttu-id="e0da2-142">Valor</span><span class="sxs-lookup"><span data-stu-id="e0da2-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e0da2-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0da2-143">Minimum supported client</span></span><br/> | <span data-ttu-id="e0da2-144">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e0da2-144">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e0da2-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0da2-145">Minimum supported server</span></span><br/> | <span data-ttu-id="e0da2-146">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e0da2-146">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e0da2-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0da2-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0da2-148">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="e0da2-148">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="e0da2-149">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="e0da2-149">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





