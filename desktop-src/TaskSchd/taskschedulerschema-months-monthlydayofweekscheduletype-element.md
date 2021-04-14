---
title: Mês (monthlyDayOfWeekScheduleType) elemento
description: Especifica os meses do ano durante os quais a tarefa é executada para uma agenda mensal de dia da semana.
ms.assetid: 420fa7f4-7106-483e-9b3b-d1ba51f25222
keywords:
- Agendador de Tarefas do elemento months
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76f13a5823e0154519dbdb093dd03ea36bbe77b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369398"
---
# <a name="months-monthlydayofweekscheduletype-element"></a><span data-ttu-id="2e66a-104">Mês (monthlyDayOfWeekScheduleType) elemento</span><span class="sxs-lookup"><span data-stu-id="2e66a-104">Months (monthlyDayOfWeekScheduleType) Element</span></span>

<span data-ttu-id="2e66a-105">Especifica os meses do ano durante os quais a tarefa é executada para uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="2e66a-105">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span>

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

<span data-ttu-id="2e66a-106">O elemento **months** é definido pelo tipo complexo [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2e66a-106">The **Months** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="2e66a-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="2e66a-107">Parent element</span></span>



| <span data-ttu-id="2e66a-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="2e66a-108">Element</span></span>                                                                                                                            | <span data-ttu-id="2e66a-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="2e66a-109">Derived from</span></span>                                                                                         | <span data-ttu-id="2e66a-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e66a-110">Description</span></span>                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="2e66a-111">**ScheduleByMonthDayOfWeek (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="2e66a-111">**ScheduleByMonthDayOfWeek (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="2e66a-112">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="2e66a-112">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="2e66a-113">Especifica um gatilho que inicia um trabalho para uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="2e66a-113">Specifies a trigger that starts a job for a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="2e66a-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2e66a-114">Child elements</span></span>



| <span data-ttu-id="2e66a-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="2e66a-115">Element</span></span>                                                               | <span data-ttu-id="2e66a-116">Type</span><span class="sxs-lookup"><span data-stu-id="2e66a-116">Type</span></span> | <span data-ttu-id="2e66a-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e66a-117">Description</span></span>                                           |
|-----------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="2e66a-118">**Amanda**</span><span class="sxs-lookup"><span data-stu-id="2e66a-118">**April**</span></span>](taskschedulerschema-april-monthstype-element.md)         |      | <span data-ttu-id="2e66a-119">Especifica que a tarefa é executada em abril.</span><span class="sxs-lookup"><span data-stu-id="2e66a-119">Specifies that the task runs in April.</span></span><br/>     |
| [<span data-ttu-id="2e66a-120">**Agosto**</span><span class="sxs-lookup"><span data-stu-id="2e66a-120">**August**</span></span>](taskschedulerschema-august-monthstype-element.md)       |      | <span data-ttu-id="2e66a-121">Especifica que a tarefa é executada em agosto.</span><span class="sxs-lookup"><span data-stu-id="2e66a-121">Specifies that the task runs in August.</span></span><br/>    |
| [<span data-ttu-id="2e66a-122">**Dezembro**</span><span class="sxs-lookup"><span data-stu-id="2e66a-122">**December**</span></span>](taskschedulerschema-december-monthstype-element.md)   |      | <span data-ttu-id="2e66a-123">Especifica que a tarefa é executada em dezembro.</span><span class="sxs-lookup"><span data-stu-id="2e66a-123">Specifies that the task runs in December.</span></span><br/>  |
| [<span data-ttu-id="2e66a-124">**Fevereiro**</span><span class="sxs-lookup"><span data-stu-id="2e66a-124">**February**</span></span>](taskschedulerschema-february-monthstype-element.md)   |      | <span data-ttu-id="2e66a-125">Especifica que a tarefa é executada em fevereiro.</span><span class="sxs-lookup"><span data-stu-id="2e66a-125">Specifies that the task runs in February.</span></span><br/>  |
| [<span data-ttu-id="2e66a-126">**Janeiro**</span><span class="sxs-lookup"><span data-stu-id="2e66a-126">**January**</span></span>](taskschedulerschema-january-monthstype-element.md)     |      | <span data-ttu-id="2e66a-127">Especifica que a tarefa é executada em Janeiro.</span><span class="sxs-lookup"><span data-stu-id="2e66a-127">Specifies that the task runs in January.</span></span><br/>   |
| [<span data-ttu-id="2e66a-128">**Julho**</span><span class="sxs-lookup"><span data-stu-id="2e66a-128">**July**</span></span>](taskschedulerschema-july-monthstype-element.md)           |      | <span data-ttu-id="2e66a-129">Especifica que a tarefa é executada em julho.</span><span class="sxs-lookup"><span data-stu-id="2e66a-129">Specifies that the task runs in July.</span></span><br/>      |
| [<span data-ttu-id="2e66a-130">**Junho**</span><span class="sxs-lookup"><span data-stu-id="2e66a-130">**June**</span></span>](taskschedulerschema-june-monthstype-element.md)           |      | <span data-ttu-id="2e66a-131">Especifica que a tarefa é executada em junho.</span><span class="sxs-lookup"><span data-stu-id="2e66a-131">Specifies that the task runs in June.</span></span><br/>      |
| [<span data-ttu-id="2e66a-132">**Março**</span><span class="sxs-lookup"><span data-stu-id="2e66a-132">**March**</span></span>](taskschedulerschema-march-monthstype-element.md)         |      | <span data-ttu-id="2e66a-133">Especifica que a tarefa é executada em março.</span><span class="sxs-lookup"><span data-stu-id="2e66a-133">Specifies that the task runs in March.</span></span><br/>     |
| [<span data-ttu-id="2e66a-134">**Mai**</span><span class="sxs-lookup"><span data-stu-id="2e66a-134">**May**</span></span>](taskschedulerschema-may-monthstype-element.md)             |      | <span data-ttu-id="2e66a-135">Especifica que a tarefa é executada em maio.</span><span class="sxs-lookup"><span data-stu-id="2e66a-135">Specifies that the task runs in May.</span></span><br/>       |
| [<span data-ttu-id="2e66a-136">**Novembro**</span><span class="sxs-lookup"><span data-stu-id="2e66a-136">**November**</span></span>](taskschedulerschema-november-monthstype-element.md)   |      | <span data-ttu-id="2e66a-137">Especifica que a tarefa é executada em novembro.</span><span class="sxs-lookup"><span data-stu-id="2e66a-137">Specifies that the task runs in November.</span></span><br/>  |
| [<span data-ttu-id="2e66a-138">**Outubro**</span><span class="sxs-lookup"><span data-stu-id="2e66a-138">**October**</span></span>](taskschedulerschema-october-monthstype-element.md)     |      | <span data-ttu-id="2e66a-139">Especifica que a tarefa é executada em outubro.</span><span class="sxs-lookup"><span data-stu-id="2e66a-139">Specifies that the task runs in October.</span></span><br/>   |
| [<span data-ttu-id="2e66a-140">**Setembro**</span><span class="sxs-lookup"><span data-stu-id="2e66a-140">**September**</span></span>](taskschedulerschema-september-monthstype-element.md) |      | <span data-ttu-id="2e66a-141">Especifica que a tarefa é executada em setembro.</span><span class="sxs-lookup"><span data-stu-id="2e66a-141">Specifies that the task runs in September.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2e66a-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e66a-142">Remarks</span></span>

<span data-ttu-id="2e66a-143">Para o desenvolvimento de scripts, os meses de um ano para uma agenda mensal de dia da semana são especificados usando a propriedade [**MonthlyDOWTrigger. MonthsOfYear**](monthlydowtrigger-monthsofyear.md) .</span><span class="sxs-lookup"><span data-stu-id="2e66a-143">For scripting development, the months of a year for a monthly day-of-week schedule are specified using the [**MonthlyDOWTrigger.MonthsOfYear**](monthlydowtrigger-monthsofyear.md) property.</span></span>

<span data-ttu-id="2e66a-144">Para o desenvolvimento em C++, os meses de um ano para uma agenda mensal de dia da semana são especificados usando a propriedade [**IMonthlyDOWTrigger:: MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_monthsofyear) .</span><span class="sxs-lookup"><span data-stu-id="2e66a-144">For C++ development, the months of a year for a monthly day-of-week schedule are specified using the [**IMonthlyDOWTrigger::MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_monthsofyear) property.</span></span>

<span data-ttu-id="2e66a-145">Os elementos filho acima são definidos pelo tipo complexo [**monthtype**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2e66a-145">The child elements above are defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="examples"></a><span data-ttu-id="2e66a-146">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2e66a-146">Examples</span></span>

<span data-ttu-id="2e66a-147">O XML a seguir define um calendário mensal de dia da semana que inicia a tarefa na segunda-feira da primeira semana para cada mês do ano.</span><span class="sxs-lookup"><span data-stu-id="2e66a-147">The following XML defines a monthly day-of-week calendar that starts the task on Monday of the first week for each month of the year.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="2e66a-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e66a-148">Requirements</span></span>



| <span data-ttu-id="2e66a-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e66a-149">Requirement</span></span> | <span data-ttu-id="2e66a-150">Valor</span><span class="sxs-lookup"><span data-stu-id="2e66a-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2e66a-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e66a-151">Minimum supported client</span></span><br/> | <span data-ttu-id="2e66a-152">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e66a-152">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2e66a-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e66a-153">Minimum supported server</span></span><br/> | <span data-ttu-id="2e66a-154">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2e66a-154">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2e66a-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e66a-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e66a-156">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="2e66a-156">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="2e66a-157">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="2e66a-157">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





