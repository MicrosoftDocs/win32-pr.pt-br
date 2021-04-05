---
title: Elemento ScheduleByMonth (calendarTriggerType)
description: Especifica um agendamento mensal.
ms.assetid: 3a23f4d0-bdaf-4f2a-81c6-8652a0849fc8
keywords:
- Agendador de Tarefas do elemento ScheduleByMonth
topic_type:
- apiref
api_name:
- ScheduleByMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6fda84a1cd4373f7988fa66a5ad70c97dd371d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086116"
---
# <a name="schedulebymonth-calendartriggertype-element"></a><span data-ttu-id="f9b87-104">Elemento ScheduleByMonth (calendarTriggerType)</span><span class="sxs-lookup"><span data-stu-id="f9b87-104">ScheduleByMonth (calendarTriggerType) Element</span></span>

<span data-ttu-id="f9b87-105">Especifica um agendamento mensal.</span><span class="sxs-lookup"><span data-stu-id="f9b87-105">Specifies a monthly schedule.</span></span> <span data-ttu-id="f9b87-106">Por exemplo, a tarefa começa às 8:00 em dias específicos do mês em meses específicos.</span><span class="sxs-lookup"><span data-stu-id="f9b87-106">For example, the task starts at 8:00 AM on specific days of the month on specific months.</span></span>

``` syntax
<xs:element name="ScheduleByMonth"
    type="monthlyScheduleType"
 />
```

<span data-ttu-id="f9b87-107">O elemento **ScheduleByMonth** é definido pelo tipo complexo [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f9b87-107">The **ScheduleByMonth** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f9b87-108">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="f9b87-108">Parent element</span></span>



| <span data-ttu-id="f9b87-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="f9b87-109">Element</span></span>                                                                             | <span data-ttu-id="f9b87-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="f9b87-110">Derived from</span></span>                                                                       | <span data-ttu-id="f9b87-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9b87-111">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f9b87-112">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="f9b87-112">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="f9b87-113">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="f9b87-113">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="f9b87-114">Especifica um gatilho diário, semanal, mensal ou um dia da semana (DOW) mensal.</span><span class="sxs-lookup"><span data-stu-id="f9b87-114">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="f9b87-115">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f9b87-115">Child elements</span></span>



| <span data-ttu-id="f9b87-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="f9b87-116">Element</span></span>                                                                                                  | <span data-ttu-id="f9b87-117">Type</span><span class="sxs-lookup"><span data-stu-id="f9b87-117">Type</span></span>                                                                       | <span data-ttu-id="f9b87-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9b87-118">Description</span></span>                                                             |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="f9b87-119">**DaysOfMonth (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="f9b87-119">**DaysOfMonth (monthlyScheduleType)**</span></span>](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [<span data-ttu-id="f9b87-120">**daysOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="f9b87-120">**daysOfMonthType**</span></span>](taskschedulerschema-daysofmonthtype-complextype.md) | <span data-ttu-id="f9b87-121">Especifica os dias do mês durante os quais a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="f9b87-121">Specifies the days of the month during which the task runs.</span></span><br/>  |
| [<span data-ttu-id="f9b87-122">**Meses (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="f9b87-122">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)           | [<span data-ttu-id="f9b87-123">**monthtype**</span><span class="sxs-lookup"><span data-stu-id="f9b87-123">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)           | <span data-ttu-id="f9b87-124">Especifica os meses do ano durante os quais a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="f9b87-124">Specifies the months of the year during which the task runs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f9b87-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9b87-125">Remarks</span></span>

<span data-ttu-id="f9b87-126">A hora do dia em que a tarefa é iniciada é definida pelo elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f9b87-126">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="f9b87-127">Para o desenvolvimento de script, um gatilho mensal é especificado usando o objeto [**MonthlyTrigger**](monthlytrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="f9b87-127">For script development, a monthly trigger is specified using the [**MonthlyTrigger**](monthlytrigger.md) object.</span></span>

<span data-ttu-id="f9b87-128">Para desenvolvimento em C++, um gatilho mensal é especificado usando a interface [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger) .</span><span class="sxs-lookup"><span data-stu-id="f9b87-128">For C++ development, a monthly trigger is specified using the [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger) interface.</span></span>

<span data-ttu-id="f9b87-129">Os elementos filho listados abaixo são definidos pelos tipos de elementos complexos [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f9b87-129">The child elements listed below are defined by the [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) complex element types.</span></span>

## <a name="examples"></a><span data-ttu-id="f9b87-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f9b87-130">Examples</span></span>

<span data-ttu-id="f9b87-131">O XML a seguir define um gatilho de calendário mensal que inicia uma tarefa (às 8:00 AM) no 1º e no 15º dia de cada mês do ano.</span><span class="sxs-lookup"><span data-stu-id="f9b87-131">The following XML defines a monthly calendar trigger that starts a task ( at 8:00 AM) on the 1st and 15th day of every month of the year.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>
            <Day>15</Day>
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
        </Months>
    </ScheduleByMonth>
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="f9b87-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9b87-132">Requirements</span></span>



| <span data-ttu-id="f9b87-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9b87-133">Requirement</span></span> | <span data-ttu-id="f9b87-134">Valor</span><span class="sxs-lookup"><span data-stu-id="f9b87-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f9b87-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9b87-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f9b87-136">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f9b87-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f9b87-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9b87-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f9b87-138">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f9b87-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9b87-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9b87-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9b87-140">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f9b87-140">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f9b87-141">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f9b87-141">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





