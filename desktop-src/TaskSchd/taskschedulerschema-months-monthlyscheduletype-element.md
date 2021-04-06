---
title: Mês (monthlyScheduleType) elemento
description: Especifica os meses do ano durante os quais a tarefa é executada por um agendamento mensal.
ms.assetid: 71c9f7ac-01fc-4837-bccf-1869df2bc24e
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
ms.openlocfilehash: 0ed40fd2466f8962f839f39e7addd3b7e1bc33eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086119"
---
# <a name="months-monthlyscheduletype-element"></a><span data-ttu-id="03cdd-104">Mês (monthlyScheduleType) elemento</span><span class="sxs-lookup"><span data-stu-id="03cdd-104">Months (monthlyScheduleType) Element</span></span>

<span data-ttu-id="03cdd-105">Especifica os meses do ano durante os quais a tarefa é executada por um agendamento mensal.</span><span class="sxs-lookup"><span data-stu-id="03cdd-105">Specifies the months of the year during which the task runs for a monthly schedule.</span></span>

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

<span data-ttu-id="03cdd-106">O elemento **months** é definido pelo tipo complexo [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="03cdd-106">The **Months** element is defined by the [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="03cdd-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="03cdd-107">Parent element</span></span>



| <span data-ttu-id="03cdd-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="03cdd-108">Element</span></span>                                                                                    | <span data-ttu-id="03cdd-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="03cdd-109">Derived from</span></span>                                                                       | <span data-ttu-id="03cdd-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="03cdd-110">Description</span></span>                               |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="03cdd-111">**ScheduleByMonth**</span><span class="sxs-lookup"><span data-stu-id="03cdd-111">**ScheduleByMonth**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [<span data-ttu-id="03cdd-112">**monthlyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="03cdd-112">**monthlyScheduleType**</span></span>](taskschedulerschema-monthlyscheduletype-complextype.md) | <span data-ttu-id="03cdd-113">Especifica um agendamento mensal.</span><span class="sxs-lookup"><span data-stu-id="03cdd-113">Specifies a monthly schedule.</span></span> <br/> |



## <a name="child-elements"></a><span data-ttu-id="03cdd-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="03cdd-114">Child elements</span></span>



| <span data-ttu-id="03cdd-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="03cdd-115">Element</span></span>                                                                            | <span data-ttu-id="03cdd-116">Type</span><span class="sxs-lookup"><span data-stu-id="03cdd-116">Type</span></span> | <span data-ttu-id="03cdd-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="03cdd-117">Description</span></span>                                           |
|------------------------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="03cdd-118">**Abril (meses)**</span><span class="sxs-lookup"><span data-stu-id="03cdd-118">**April (monthsType)**</span></span>](taskschedulerschema-april-monthstype-element.md)         |      | <span data-ttu-id="03cdd-119">Especifica que a tarefa é executada em abril.</span><span class="sxs-lookup"><span data-stu-id="03cdd-119">Specifies that the task runs in April.</span></span><br/>     |
| [<span data-ttu-id="03cdd-120">**Agosto (meses)**</span><span class="sxs-lookup"><span data-stu-id="03cdd-120">**August (monthsType)**</span></span>](taskschedulerschema-august-monthstype-element.md)       |      | <span data-ttu-id="03cdd-121">Especifica que a tarefa é executada em agosto.</span><span class="sxs-lookup"><span data-stu-id="03cdd-121">Specifies that the task runs in August.</span></span><br/>    |
| [<span data-ttu-id="03cdd-122">**Dezembro (meses)**</span><span class="sxs-lookup"><span data-stu-id="03cdd-122">**December (monthsType)**</span></span>](taskschedulerschema-december-monthstype-element.md)   |      | <span data-ttu-id="03cdd-123">Especifica que a tarefa é executada em dezembro.</span><span class="sxs-lookup"><span data-stu-id="03cdd-123">Specifies that the task runs in December.</span></span><br/>  |
| [<span data-ttu-id="03cdd-124">**Fevereiro (meses)**</span><span class="sxs-lookup"><span data-stu-id="03cdd-124">**February (monthsType)**</span></span>](taskschedulerschema-february-monthstype-element.md)   |      | <span data-ttu-id="03cdd-125">Especifica que a tarefa é executada em fevereiro.</span><span class="sxs-lookup"><span data-stu-id="03cdd-125">Specifies that the task runs in February.</span></span><br/>  |
| [<span data-ttu-id="03cdd-126">**Janeiro (meses)**</span><span class="sxs-lookup"><span data-stu-id="03cdd-126">**January (monthsType)**</span></span>](taskschedulerschema-january-monthstype-element.md)     |      | <span data-ttu-id="03cdd-127">Especifica que a tarefa é executada em Janeiro.</span><span class="sxs-lookup"><span data-stu-id="03cdd-127">Specifies that the task runs in January.</span></span><br/>   |
| [<span data-ttu-id="03cdd-128">**Julho (meses)**</span><span class="sxs-lookup"><span data-stu-id="03cdd-128">**July (monthsType)**</span></span>](taskschedulerschema-july-monthstype-element.md)           |      | <span data-ttu-id="03cdd-129">Especifica que a tarefa é executada em julho.</span><span class="sxs-lookup"><span data-stu-id="03cdd-129">Specifies that the task runs in July.</span></span><br/>      |
| [<span data-ttu-id="03cdd-130">**Junho (monthtype)**</span><span class="sxs-lookup"><span data-stu-id="03cdd-130">**June (monthsType)**</span></span>](taskschedulerschema-june-monthstype-element.md)           |      | <span data-ttu-id="03cdd-131">Especifica que a tarefa é executada em junho.</span><span class="sxs-lookup"><span data-stu-id="03cdd-131">Specifies that the task runs in June.</span></span><br/>      |
| [<span data-ttu-id="03cdd-132">**Março (meses)**</span><span class="sxs-lookup"><span data-stu-id="03cdd-132">**March (monthsType)**</span></span>](taskschedulerschema-march-monthstype-element.md)         |      | <span data-ttu-id="03cdd-133">Especifica que a tarefa é executada em março.</span><span class="sxs-lookup"><span data-stu-id="03cdd-133">Specifies that the task runs in March.</span></span><br/>     |
| [<span data-ttu-id="03cdd-134">**Maio (monthtype)**</span><span class="sxs-lookup"><span data-stu-id="03cdd-134">**May (monthsType)**</span></span>](taskschedulerschema-may-monthstype-element.md)             |      | <span data-ttu-id="03cdd-135">Especifica que a tarefa é executada em maio.</span><span class="sxs-lookup"><span data-stu-id="03cdd-135">Specifies that the task runs in May.</span></span><br/>       |
| [<span data-ttu-id="03cdd-136">**Novembro (meses)**</span><span class="sxs-lookup"><span data-stu-id="03cdd-136">**November (monthsType)**</span></span>](taskschedulerschema-november-monthstype-element.md)   |      | <span data-ttu-id="03cdd-137">Especifica que a tarefa é executada em novembro.</span><span class="sxs-lookup"><span data-stu-id="03cdd-137">Specifies that the task runs in November.</span></span><br/>  |
| [<span data-ttu-id="03cdd-138">**Outubro (meses)**</span><span class="sxs-lookup"><span data-stu-id="03cdd-138">**October (monthsType)**</span></span>](taskschedulerschema-october-monthstype-element.md)     |      | <span data-ttu-id="03cdd-139">Especifica que a tarefa é executada em outubro.</span><span class="sxs-lookup"><span data-stu-id="03cdd-139">Specifies that the task runs in October.</span></span><br/>   |
| [<span data-ttu-id="03cdd-140">**Setembro (meses)**</span><span class="sxs-lookup"><span data-stu-id="03cdd-140">**September (monthsType)**</span></span>](taskschedulerschema-september-monthstype-element.md) |      | <span data-ttu-id="03cdd-141">Especifica que a tarefa é executada em setembro.</span><span class="sxs-lookup"><span data-stu-id="03cdd-141">Specifies that the task runs in September.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="03cdd-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="03cdd-142">Remarks</span></span>

<span data-ttu-id="03cdd-143">Para o desenvolvimento de script, os meses de agendamento são especificados usando a propriedade [**MonthlyTrigger. MonthsOfYear**](monthlytrigger-monthsofyear.md) .</span><span class="sxs-lookup"><span data-stu-id="03cdd-143">For script development, the months of the schedule are specified using the [**MonthlyTrigger.MonthsOfYear**](monthlytrigger-monthsofyear.md) property.</span></span>

<span data-ttu-id="03cdd-144">Para desenvolvimento em C++, os meses de agendamento são especificados usando a propriedade [**IMonthlyTrigger:: MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_monthsofyear) .</span><span class="sxs-lookup"><span data-stu-id="03cdd-144">For C++ development, the months of the schedule are specified using the [**IMonthlyTrigger::MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_monthsofyear) property.</span></span>

## <a name="examples"></a><span data-ttu-id="03cdd-145">Exemplos</span><span class="sxs-lookup"><span data-stu-id="03cdd-145">Examples</span></span>

<span data-ttu-id="03cdd-146">O XML a seguir define um calendário mensal que inicia a tarefa no 1º e no 15º dia de cada mês do ano.</span><span class="sxs-lookup"><span data-stu-id="03cdd-146">The following XML defines a monthly calendar that starts the task on the 1st and 15th day of every month of the year.</span></span>


```XML
</ScheduleByMonth>
    <DaysOfMonth>
        <Day>1</Day>
        <Day>15</Day>
    </DaysOfMonth
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
```



## <a name="requirements"></a><span data-ttu-id="03cdd-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03cdd-147">Requirements</span></span>



| <span data-ttu-id="03cdd-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="03cdd-148">Requirement</span></span> | <span data-ttu-id="03cdd-149">Valor</span><span class="sxs-lookup"><span data-stu-id="03cdd-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="03cdd-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03cdd-150">Minimum supported client</span></span><br/> | <span data-ttu-id="03cdd-151">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="03cdd-151">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="03cdd-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03cdd-152">Minimum supported server</span></span><br/> | <span data-ttu-id="03cdd-153">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="03cdd-153">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="03cdd-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="03cdd-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03cdd-155">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="03cdd-155">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="03cdd-156">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="03cdd-156">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





