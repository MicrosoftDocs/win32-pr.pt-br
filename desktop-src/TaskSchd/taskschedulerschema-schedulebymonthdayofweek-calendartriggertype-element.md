---
title: Elemento ScheduleByMonthDayOfWeek (calendarTriggerType)
description: Especifica uma agenda mensal de dia da semana.
ms.assetid: 7ff17bea-fa26-40c4-90fa-d94a3690e464
keywords:
- Agendador de Tarefas do elemento ScheduleByMonthDayOfWeek
topic_type:
- apiref
api_name:
- ScheduleByMonthDayOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e92d6ad530466a2238c8239c9e262f85ae361d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644997"
---
# <a name="schedulebymonthdayofweek-calendartriggertype-element"></a><span data-ttu-id="139a9-104">Elemento ScheduleByMonthDayOfWeek (calendarTriggerType)</span><span class="sxs-lookup"><span data-stu-id="139a9-104">ScheduleByMonthDayOfWeek (calendarTriggerType) Element</span></span>

<span data-ttu-id="139a9-105">Especifica uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="139a9-105">Specifies a monthly day-of-week schedule.</span></span> <span data-ttu-id="139a9-106">Por exemplo, a tarefa é iniciada em dias da semana específicos, semanas do mês e meses do ano.</span><span class="sxs-lookup"><span data-stu-id="139a9-106">For example, the task starts on specific days of the week, weeks of the month, and months of the year.</span></span>

``` syntax
<xs:element name="ScheduleByMonthDayOfWeek"
    type="monthlyDayOfWeekScheduleType"
 />
```

<span data-ttu-id="139a9-107">O elemento **ScheduleByMonthDayOfWeek** é definido pelo tipo complexo [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="139a9-107">The **ScheduleByMonthDayOfWeek** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="139a9-108">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="139a9-108">Parent element</span></span>



| <span data-ttu-id="139a9-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="139a9-109">Element</span></span>                                                                             | <span data-ttu-id="139a9-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="139a9-110">Derived from</span></span>                                                                       | <span data-ttu-id="139a9-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="139a9-111">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="139a9-112">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="139a9-112">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="139a9-113">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="139a9-113">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="139a9-114">Especifica um gatilho diário, semanal, mensal ou um dia da semana (DOW) mensal.</span><span class="sxs-lookup"><span data-stu-id="139a9-114">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="139a9-115">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="139a9-115">Child elements</span></span>



| <span data-ttu-id="139a9-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="139a9-116">Element</span></span>                                                                                   | <span data-ttu-id="139a9-117">Type</span><span class="sxs-lookup"><span data-stu-id="139a9-117">Type</span></span>                                                                     | <span data-ttu-id="139a9-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="139a9-118">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="139a9-119">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="139a9-119">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="139a9-120">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="139a9-120">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="139a9-121">Especifica os dias da semana em que a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="139a9-121">Specifies the days of the week in which the task runs.</span></span><br/>       |
| [<span data-ttu-id="139a9-122">**Meses**</span><span class="sxs-lookup"><span data-stu-id="139a9-122">**Months**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [<span data-ttu-id="139a9-123">**monthtype**</span><span class="sxs-lookup"><span data-stu-id="139a9-123">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)         | <span data-ttu-id="139a9-124">Especifica os meses do ano durante os quais a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="139a9-124">Specifies the months of the year during which the task runs.</span></span><br/> |
| [<span data-ttu-id="139a9-125">**Semanas**</span><span class="sxs-lookup"><span data-stu-id="139a9-125">**Weeks**</span></span>](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | <span data-ttu-id="139a9-126">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="139a9-126">unsignedByte</span></span>                                                             | <span data-ttu-id="139a9-127">Especifica o intervalo entre as semanas no agendamento.</span><span class="sxs-lookup"><span data-stu-id="139a9-127">Specifies the interval between the weeks in the schedule.</span></span><br/>    |



## <a name="remarks"></a><span data-ttu-id="139a9-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="139a9-128">Remarks</span></span>

<span data-ttu-id="139a9-129">A hora do dia em que a tarefa é iniciada é definida pelo elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="139a9-129">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="139a9-130">Para o desenvolvimento de scripts, um gatilho mensal de dia da semana é especificado usando o objeto [**MonthlyDOWTrigger**](monthlydowtrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="139a9-130">For scripting development, a monthly day-of-week trigger is specified using the [**MonthlyDOWTrigger**](monthlydowtrigger.md) object.</span></span>

<span data-ttu-id="139a9-131">Para desenvolvimento em C++, um gatilho mensal de dia da semana é especificado usando a interface [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger) .</span><span class="sxs-lookup"><span data-stu-id="139a9-131">For C++ development, a monthly day-of-week trigger is specified using the [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger) interface.</span></span>

<span data-ttu-id="139a9-132">Os elementos filho listados acima são definidos pelos tipos de elementos complexos [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="139a9-132">The child elements listed above are defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex element types.</span></span>

## <a name="examples"></a><span data-ttu-id="139a9-133">Exemplos</span><span class="sxs-lookup"><span data-stu-id="139a9-133">Examples</span></span>

<span data-ttu-id="139a9-134">O XML a seguir define um gatilho de calendário mensal de dia da semana que inicia uma tarefa (às 8:00 A.M.) na segunda-feira da primeira semana para cada mês do ano.</span><span class="sxs-lookup"><span data-stu-id="139a9-134">The following XML defines a monthly day of week calendar trigger that starts a task ( at 8:00 AM) on Monday of the first week for each month of the year.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonthDayOfWeek>
        <Weeks>
            <Week>1</Week>
        </Weeks>
        <DaysOfWeek>
            <Monday/>
        </DaysOfWeek>
        <Months>
            <January/>
            <February/>
            <March/>
            <April/>
            <May/>
            <June/>
            <July/>
            <August/>
            <September/>
            <October/>
            <November/>
            <December/>
        <Months>
    </ScheduleByMonthDayOfWeek>
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="139a9-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="139a9-135">Requirements</span></span>



| <span data-ttu-id="139a9-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="139a9-136">Requirement</span></span> | <span data-ttu-id="139a9-137">Valor</span><span class="sxs-lookup"><span data-stu-id="139a9-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="139a9-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="139a9-138">Minimum supported client</span></span><br/> | <span data-ttu-id="139a9-139">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="139a9-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="139a9-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="139a9-140">Minimum supported server</span></span><br/> | <span data-ttu-id="139a9-141">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="139a9-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="139a9-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="139a9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="139a9-143">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="139a9-143">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="139a9-144">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="139a9-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





