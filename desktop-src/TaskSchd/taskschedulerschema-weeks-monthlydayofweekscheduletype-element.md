---
title: Elemento Weeks (monthlyDayOfWeekScheduleType)
description: Especifica as semanas do mês em que a tarefa é executada.
ms.assetid: c126d1e2-6e60-4067-9fc2-86c9522cce5d
keywords:
- Elemento Weeks Agendador de Tarefas
topic_type:
- apiref
api_name:
- Weeks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e032b936353d2c89a84b5da684f681ea3c2b6d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645102"
---
# <a name="weeks-monthlydayofweekscheduletype-element"></a><span data-ttu-id="694a1-104">Elemento Weeks (monthlyDayOfWeekScheduleType)</span><span class="sxs-lookup"><span data-stu-id="694a1-104">Weeks (monthlyDayOfWeekScheduleType) Element</span></span>

<span data-ttu-id="694a1-105">Especifica as semanas do mês em que a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="694a1-105">Specifies the weeks of the month in which the task is run.</span></span>

``` syntax
<xs:element name="Weeks"
    type="weeksType"
 />
```

<span data-ttu-id="694a1-106">O elemento **Weeks** é definido pelo tipo complexo [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="694a1-106">The **Weeks** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="694a1-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="694a1-107">Parent element</span></span>



| <span data-ttu-id="694a1-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="694a1-108">Element</span></span>                                                                                                      | <span data-ttu-id="694a1-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="694a1-109">Derived from</span></span>                                                                                         | <span data-ttu-id="694a1-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="694a1-110">Description</span></span>                                                                         |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="694a1-111">**ScheduleByMonthDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="694a1-111">**ScheduleByMonthDayOfWeek**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="694a1-112">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="694a1-112">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="694a1-113">Especifica um gatilho que inicia um trabalho em uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="694a1-113">Specifies a trigger that starts a job on a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="694a1-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="694a1-114">Child elements</span></span>



| <span data-ttu-id="694a1-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="694a1-115">Element</span></span>                                                    | <span data-ttu-id="694a1-116">Type</span><span class="sxs-lookup"><span data-stu-id="694a1-116">Type</span></span>                                                        | <span data-ttu-id="694a1-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="694a1-117">Description</span></span>                                        |
|------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="694a1-118">**Semana**</span><span class="sxs-lookup"><span data-stu-id="694a1-118">**Week**</span></span>](taskschedulerschema-week-weekstype-element.md) | [<span data-ttu-id="694a1-119">**weektype**</span><span class="sxs-lookup"><span data-stu-id="694a1-119">**weekType**</span></span>](taskschedulerschema-weektype-simpletype.md) | <span data-ttu-id="694a1-120">Especifica uma semana específica do mês.</span><span class="sxs-lookup"><span data-stu-id="694a1-120">Specifies a specific week of the month.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="694a1-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="694a1-121">Remarks</span></span>

<span data-ttu-id="694a1-122">Para o desenvolvimento de scripts, as semanas do mês são especificadas usando a propriedade [**MonthlyDOWTrigger. WeeksOfMonth**](monthlydowtrigger-weeksofmonth.md) .</span><span class="sxs-lookup"><span data-stu-id="694a1-122">For scripting development, the weeks of the month are specified using the [**MonthlyDOWTrigger.WeeksOfMonth**](monthlydowtrigger-weeksofmonth.md) property.</span></span>

<span data-ttu-id="694a1-123">Para desenvolvimento em C++, as semanas do mês são especificadas usando a propriedade [**IMonthlyDOWTrigger:: WeeksOfMonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_weeksofmonth) .</span><span class="sxs-lookup"><span data-stu-id="694a1-123">For C++ development, the weeks of the month are specified using the [**IMonthlyDOWTrigger::WeeksOfMonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_weeksofmonth) property.</span></span>

<span data-ttu-id="694a1-124">Ao especificar as semanas do mês, use 1-4 para especificar as primeiras quatro semanas do mês ou use a cadeia de caracteres "Last" para indicar a semana passada, independentemente de qual é a semana.</span><span class="sxs-lookup"><span data-stu-id="694a1-124">When specifying the weeks of the month, use 1-4 to specify the first four weeks of the month or use the string "Last" to indicate the last week regardless of which week it is.</span></span>

## <a name="examples"></a><span data-ttu-id="694a1-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="694a1-125">Examples</span></span>

<span data-ttu-id="694a1-126">O XML a seguir define um calendário mensal de dia da semana que inicia a tarefa na segunda-feira da primeira semana para cada mês do ano.</span><span class="sxs-lookup"><span data-stu-id="694a1-126">The following XML defines a monthly day-of-week calendar that starts the task on Monday of the first week for each month of the year.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="694a1-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="694a1-127">Requirements</span></span>



| <span data-ttu-id="694a1-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="694a1-128">Requirement</span></span> | <span data-ttu-id="694a1-129">Valor</span><span class="sxs-lookup"><span data-stu-id="694a1-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="694a1-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="694a1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="694a1-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="694a1-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="694a1-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="694a1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="694a1-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="694a1-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="694a1-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="694a1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="694a1-135">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="694a1-135">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="694a1-136">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="694a1-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





