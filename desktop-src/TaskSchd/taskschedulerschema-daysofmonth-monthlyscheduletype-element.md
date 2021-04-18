---
title: Elemento DaysOfMonth (monthlyScheduleType)
description: Especifica os dias do mês durante os quais a tarefa é executada.
ms.assetid: 62f28f44-b3d8-414e-80d4-f4d8bd3c4527
keywords:
- Agendador de Tarefas do elemento DaysOfMonth
topic_type:
- apiref
api_name:
- DaysOfMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38c2106f8d612ee27dc1297023a59b531fa9548d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760141"
---
# <a name="daysofmonth-monthlyscheduletype-element"></a><span data-ttu-id="26498-104">Elemento DaysOfMonth (monthlyScheduleType)</span><span class="sxs-lookup"><span data-stu-id="26498-104">DaysOfMonth (monthlyScheduleType) Element</span></span>

<span data-ttu-id="26498-105">Especifica os dias do mês durante os quais a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="26498-105">Specifies the days of the month during which the task runs.</span></span>

``` syntax
<xs:element name="DaysOfMonth"
    type="daysOfMonthType"
 />
```

<span data-ttu-id="26498-106">O elemento **DaysOfMonth** é definido pelo tipo complexo [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="26498-106">The **DaysOfMonth** element is defined by the [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="26498-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="26498-107">Parent element</span></span>



| <span data-ttu-id="26498-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="26498-108">Element</span></span>                                                                                    | <span data-ttu-id="26498-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="26498-109">Derived from</span></span>                                                                                         | <span data-ttu-id="26498-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="26498-110">Description</span></span>                                                                          |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="26498-111">**ScheduleByMonth**</span><span class="sxs-lookup"><span data-stu-id="26498-111">**ScheduleByMonth**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [<span data-ttu-id="26498-112">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="26498-112">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="26498-113">Especifica um gatilho que inicia um trabalho para uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="26498-113">Specifies a trigger that starts a job for a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="26498-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="26498-114">Child elements</span></span>



| <span data-ttu-id="26498-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="26498-115">Element</span></span>                                                        | <span data-ttu-id="26498-116">Type</span><span class="sxs-lookup"><span data-stu-id="26498-116">Type</span></span>                                                                    | <span data-ttu-id="26498-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="26498-117">Description</span></span>                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="26498-118">**Dia**</span><span class="sxs-lookup"><span data-stu-id="26498-118">**Day**</span></span>](taskschedulerschema-day-daysofmonthtype-element.md) | [<span data-ttu-id="26498-119">**dayOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="26498-119">**dayOfMonthType**</span></span>](taskschedulerschema-dayofmonthtype-simpletype.md) | <span data-ttu-id="26498-120">Especifica um dia do mês durante o qual a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="26498-120">Specifies a day of the month during which the task runs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="26498-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="26498-121">Remarks</span></span>

<span data-ttu-id="26498-122">Para o desenvolvimento de script, os dias do mês para o agendamento são especificados usando a propriedade [**MonthlyTrigger. DaysOfMonth**](monthlytrigger-daysofmonth.md) .</span><span class="sxs-lookup"><span data-stu-id="26498-122">For script development, the days of the month for the schedule are specified using the [**MonthlyTrigger.DaysOfMonth**](monthlytrigger-daysofmonth.md) property.</span></span>

<span data-ttu-id="26498-123">Para o desenvolvimento em C++, os dias do mês para o agendamento são especificados usando a propriedade [**IMonthlyTrigger::D aysofmonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_daysofmonth) .</span><span class="sxs-lookup"><span data-stu-id="26498-123">For C++ development, the days of the month for the schedule are specified using the [**IMonthlyTrigger::DaysOfMonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_daysofmonth) property.</span></span>

<span data-ttu-id="26498-124">O elemento filho deve ser repetido para cada dia do mês em que a tarefa será executada.</span><span class="sxs-lookup"><span data-stu-id="26498-124">The child element must be repeated for each day of the month the task is to run.</span></span>

## <a name="examples"></a><span data-ttu-id="26498-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="26498-125">Examples</span></span>

<span data-ttu-id="26498-126">O XML a seguir define um gatilho de calendário mensal que inicia uma tarefa (às 8:30 AM) no primeiro dia de cada mês.</span><span class="sxs-lookup"><span data-stu-id="26498-126">The following XML defines a monthly calendar trigger that starts a task (at 8:30 AM) on the 1st day of every month.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>  
        </DaysOfMonth>
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
    </ScheduleByMonth>
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="26498-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26498-127">Requirements</span></span>



| <span data-ttu-id="26498-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="26498-128">Requirement</span></span> | <span data-ttu-id="26498-129">Valor</span><span class="sxs-lookup"><span data-stu-id="26498-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="26498-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26498-130">Minimum supported client</span></span><br/> | <span data-ttu-id="26498-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="26498-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="26498-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26498-132">Minimum supported server</span></span><br/> | <span data-ttu-id="26498-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="26498-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="26498-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="26498-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26498-135">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="26498-135">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="26498-136">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="26498-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





