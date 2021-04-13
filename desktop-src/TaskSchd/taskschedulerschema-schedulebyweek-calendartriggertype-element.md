---
title: Elemento ScheduleByWeek (calendarTriggerType)
description: Especifica uma agenda semanal.
ms.assetid: d2c33e76-0564-4b3c-ab86-e7bca667fa4f
keywords:
- gatilho semanal Agendador de Tarefas, elemento XML
- Agendador de Tarefas do elemento ScheduleByWeek
topic_type:
- apiref
api_name:
- ScheduleByWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d5ab62a0c39c4c1d0102edcdb96d310e9315820
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369878"
---
# <a name="schedulebyweek-calendartriggertype-element"></a><span data-ttu-id="ee5cd-105">Elemento ScheduleByWeek (calendarTriggerType)</span><span class="sxs-lookup"><span data-stu-id="ee5cd-105">ScheduleByWeek (calendarTriggerType) Element</span></span>

<span data-ttu-id="ee5cd-106">Especifica uma agenda semanal.</span><span class="sxs-lookup"><span data-stu-id="ee5cd-106">Specifies a weekly schedule.</span></span> <span data-ttu-id="ee5cd-107">Por exemplo, a tarefa começa às 8:00 em um dia específico da semana a cada semana ou em um dia específico da semana a cada semana.</span><span class="sxs-lookup"><span data-stu-id="ee5cd-107">For example, the task starts at 8:00 AM on a specific day of the week every week or on a specific day of the week every other week.</span></span>

``` syntax
<xs:element name="ScheduleByWeek"
    type="weeklyScheduleType"
 />
```

<span data-ttu-id="ee5cd-108">O elemento **ScheduleByWeek** é definido pelo tipo complexo [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ee5cd-108">The **ScheduleByWeek** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ee5cd-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="ee5cd-109">Parent element</span></span>



| <span data-ttu-id="ee5cd-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="ee5cd-110">Element</span></span>                                                                             | <span data-ttu-id="ee5cd-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="ee5cd-111">Derived from</span></span>                                                                       | <span data-ttu-id="ee5cd-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee5cd-112">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ee5cd-113">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="ee5cd-113">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="ee5cd-114">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="ee5cd-114">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="ee5cd-115">Especifica um gatilho diário, semanal, mensal ou um dia da semana (DOW) mensal.</span><span class="sxs-lookup"><span data-stu-id="ee5cd-115">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="ee5cd-116">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ee5cd-116">Child elements</span></span>



| <span data-ttu-id="ee5cd-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="ee5cd-117">Element</span></span>                                                                               | <span data-ttu-id="ee5cd-118">Type</span><span class="sxs-lookup"><span data-stu-id="ee5cd-118">Type</span></span>                                                                     | <span data-ttu-id="ee5cd-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee5cd-119">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="ee5cd-120">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="ee5cd-120">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [<span data-ttu-id="ee5cd-121">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="ee5cd-121">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="ee5cd-122">Especifica os dias da semana em que a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="ee5cd-122">Specifies the days of the week in which the task runs.</span></span><br/>    |
| [<span data-ttu-id="ee5cd-123">**WeeksInterval**</span><span class="sxs-lookup"><span data-stu-id="ee5cd-123">**WeeksInterval**</span></span>](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) | <span data-ttu-id="ee5cd-124">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="ee5cd-124">unsignedByte</span></span>                                                             | <span data-ttu-id="ee5cd-125">Especifica o intervalo entre as semanas no agendamento.</span><span class="sxs-lookup"><span data-stu-id="ee5cd-125">Specifies the interval between the weeks in the schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ee5cd-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee5cd-126">Remarks</span></span>

<span data-ttu-id="ee5cd-127">Os elementos filho listados acima são definidos pelos tipos de elementos complexos [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ee5cd-127">The child elements listed above are defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex element types.</span></span>

<span data-ttu-id="ee5cd-128">A hora do dia em que a tarefa é iniciada é definida pelo elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ee5cd-128">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="ee5cd-129">Para o desenvolvimento de scripts, um gatilho semanal é especificado usando o objeto [**WeeklyTrigger**](weeklytrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="ee5cd-129">For scripting development, a weekly trigger is specified using the [**WeeklyTrigger**](weeklytrigger.md) object.</span></span>

<span data-ttu-id="ee5cd-130">Para desenvolvimento em C++, um gatilho semanal é especificado usando a interface [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger) .</span><span class="sxs-lookup"><span data-stu-id="ee5cd-130">For C++ development, a weekly trigger is specified using the [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="ee5cd-131">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ee5cd-131">Examples</span></span>

<span data-ttu-id="ee5cd-132">O XML a seguir define um gatilho de calendário semanal que inicia uma tarefa de segunda-feira a sexta-feira (às 8:00) todas as semanas.</span><span class="sxs-lookup"><span data-stu-id="ee5cd-132">The following XML defines a weekly calendar trigger that starts a task Monday through Friday (at 8:00 AM) every week.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ee5cd-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee5cd-133">Requirements</span></span>



| <span data-ttu-id="ee5cd-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee5cd-134">Requirement</span></span> | <span data-ttu-id="ee5cd-135">Valor</span><span class="sxs-lookup"><span data-stu-id="ee5cd-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ee5cd-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee5cd-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ee5cd-137">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ee5cd-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ee5cd-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee5cd-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ee5cd-139">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ee5cd-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee5cd-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee5cd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee5cd-141">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="ee5cd-141">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="ee5cd-142">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="ee5cd-142">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





