---
title: Elemento DaysOfWeek (monthlyDayOfWeekScheduleType)
description: Especifica os dias da semana em que a tarefa é executada. | Elemento DaysOfWeek (monthlyDayOfWeekScheduleType)
ms.assetid: d84f0019-1369-465f-9054-0fb5a83cad6d
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
ms.openlocfilehash: 3867e08dd001a035a3ab25da056f75c1e73eeeef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105760140"
---
# <a name="daysofweek-monthlydayofweekscheduletype-element"></a><span data-ttu-id="54865-105">Elemento DaysOfWeek (monthlyDayOfWeekScheduleType)</span><span class="sxs-lookup"><span data-stu-id="54865-105">DaysOfWeek (monthlyDayOfWeekScheduleType) Element</span></span>

<span data-ttu-id="54865-106">Especifica os dias da semana em que a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="54865-106">Specifies the days of the week in which the task runs.</span></span>

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

<span data-ttu-id="54865-107">O elemento **DaysOfWeek** é definido pelo tipo complexo [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="54865-107">The **DaysOfWeek** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="54865-108">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="54865-108">Parent element</span></span>



| <span data-ttu-id="54865-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="54865-109">Element</span></span>                                                                                                      | <span data-ttu-id="54865-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="54865-110">Derived from</span></span>                                                                                         | <span data-ttu-id="54865-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="54865-111">Description</span></span>                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="54865-112">**ScheduleByMonthDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="54865-112">**ScheduleByMonthDayOfWeek**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="54865-113">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="54865-113">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="54865-114">Especifica um gatilho que inicia um trabalho para uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="54865-114">Specifies a trigger that starts a job for a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="54865-115">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="54865-115">Child elements</span></span>



| <span data-ttu-id="54865-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="54865-116">Element</span></span>                                                                   | <span data-ttu-id="54865-117">Type</span><span class="sxs-lookup"><span data-stu-id="54865-117">Type</span></span> | <span data-ttu-id="54865-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="54865-118">Description</span></span>                                           |
|---------------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="54865-119">**Friday**</span><span class="sxs-lookup"><span data-stu-id="54865-119">**Friday**</span></span>](taskschedulerschema-friday-daysofweektype-element.md)       |      | <span data-ttu-id="54865-120">Especifica que a tarefa é executada na sexta-feira.</span><span class="sxs-lookup"><span data-stu-id="54865-120">Specifies that the task runs on Friday.</span></span><br/>    |
| [<span data-ttu-id="54865-121">**Monday**</span><span class="sxs-lookup"><span data-stu-id="54865-121">**Monday**</span></span>](taskschedulerschema-monday-daysofweektype-element.md)       |      | <span data-ttu-id="54865-122">Especifica que a tarefa é executada na segunda-feira.</span><span class="sxs-lookup"><span data-stu-id="54865-122">Specifies that the task runs on Monday.</span></span><br/>    |
| [<span data-ttu-id="54865-123">**Sábado**</span><span class="sxs-lookup"><span data-stu-id="54865-123">**Saturday**</span></span>](taskschedulerschema-saturday-daysofweektype-element.md)   |      | <span data-ttu-id="54865-124">Especifica que a tarefa é executada no sábado.</span><span class="sxs-lookup"><span data-stu-id="54865-124">Specifies that the task runs on Saturday.</span></span><br/>  |
| [<span data-ttu-id="54865-125">**Sunday**</span><span class="sxs-lookup"><span data-stu-id="54865-125">**Sunday**</span></span>](taskschedulerschema-sunday-daysofweektype-element.md)       |      | <span data-ttu-id="54865-126">Especifica que a tarefa é executada no domingo.</span><span class="sxs-lookup"><span data-stu-id="54865-126">Specifies that the task runs on Sunday.</span></span><br/>    |
| [<span data-ttu-id="54865-127">**Quinta-feira**</span><span class="sxs-lookup"><span data-stu-id="54865-127">**Thursday**</span></span>](taskschedulerschema-thursday-daysofweektype-element.md)   |      | <span data-ttu-id="54865-128">Especifica que a tarefa é executada na quinta-feira.</span><span class="sxs-lookup"><span data-stu-id="54865-128">Specifies that the task runs on Thursday.</span></span><br/>  |
| [<span data-ttu-id="54865-129">**Terça-feira**</span><span class="sxs-lookup"><span data-stu-id="54865-129">**Tuesday**</span></span>](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | <span data-ttu-id="54865-130">Especifica que a tarefa é executada na terça-feira.</span><span class="sxs-lookup"><span data-stu-id="54865-130">Specifies that the task runs on Tuesday.</span></span><br/>   |
| [<span data-ttu-id="54865-131">**Quarta-feira**</span><span class="sxs-lookup"><span data-stu-id="54865-131">**Wednesday**</span></span>](taskschedulerschema-wednesday-daysofweektype-element.md) |      | <span data-ttu-id="54865-132">Especifica que a tarefa é executada na quarta-feira.</span><span class="sxs-lookup"><span data-stu-id="54865-132">Specifies that the task runs on Wednesday.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="54865-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="54865-133">Remarks</span></span>

<span data-ttu-id="54865-134">Para o desenvolvimento de scripts, os dias da semana para um calendário mensal de dia da semana são especificados usando a propriedade [**MonthlyDOWTrigger. DaysOfWeek**](monthlydowtrigger-daysofweek.md) .</span><span class="sxs-lookup"><span data-stu-id="54865-134">For scripting development, the days of the week for a monthly day-of-week calendar are specified using the [**MonthlyDOWTrigger.DaysOfWeek**](monthlydowtrigger-daysofweek.md) property.</span></span>

<span data-ttu-id="54865-135">Para o desenvolvimento em C++, os dias da semana para um calendário mensal de dia da semana são especificados usando a propriedade [**IMonthlyDOWTrigger::D aysofweek**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_daysofweek) .</span><span class="sxs-lookup"><span data-stu-id="54865-135">For C++ development, the days of the week for a monthly day-of-week calendar are specified using the [**IMonthlyDOWTrigger::DaysOfWeek**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_daysofweek) property.</span></span>

<span data-ttu-id="54865-136">Os elementos filho acima são definidos pelo tipo complexo [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="54865-136">The child elements above are defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="examples"></a><span data-ttu-id="54865-137">Exemplos</span><span class="sxs-lookup"><span data-stu-id="54865-137">Examples</span></span>

<span data-ttu-id="54865-138">O XML a seguir define um calendário mensal de dia da semana que inicia a tarefa na segunda-feira da primeira semana para cada mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54865-138">The following XML defines a monthly day-of-week calendar that starts the task on Monday of the first week for each month of the year.</span></span>


```XML
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
```



## <a name="requirements"></a><span data-ttu-id="54865-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54865-139">Requirements</span></span>



| <span data-ttu-id="54865-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="54865-140">Requirement</span></span> | <span data-ttu-id="54865-141">Valor</span><span class="sxs-lookup"><span data-stu-id="54865-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="54865-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54865-142">Minimum supported client</span></span><br/> | <span data-ttu-id="54865-143">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="54865-143">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="54865-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54865-144">Minimum supported server</span></span><br/> | <span data-ttu-id="54865-145">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="54865-145">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="54865-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="54865-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54865-147">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="54865-147">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="54865-148">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="54865-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





