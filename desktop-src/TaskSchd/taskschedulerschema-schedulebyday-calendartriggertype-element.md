---
title: Elemento ScheduleByDay (calendarTriggerType)
description: Especifica um agendamento diário.
ms.assetid: 5a6097ce-a855-4b08-84c5-71f06343805e
keywords:
- gatilho diário Agendador de Tarefas, elemento XML
- Agendador de Tarefas do elemento ScheduleByDay
topic_type:
- apiref
api_name:
- ScheduleByDay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 614777ede63605dc7ed6936bda952c6071bda371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918939"
---
# <a name="schedulebyday-calendartriggertype-element"></a><span data-ttu-id="d1d8d-105">Elemento ScheduleByDay (calendarTriggerType)</span><span class="sxs-lookup"><span data-stu-id="d1d8d-105">ScheduleByDay (calendarTriggerType) Element</span></span>

<span data-ttu-id="d1d8d-106">Especifica um agendamento diário.</span><span class="sxs-lookup"><span data-stu-id="d1d8d-106">Specifies a daily schedule.</span></span> <span data-ttu-id="d1d8d-107">Por exemplo, a tarefa começa às 8:00, todos os dias, a cada dia, a cada terceiro dia e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d1d8d-107">For example, the task starts at 8:00 AM every day, every-other day, every third day, and so on.</span></span>

``` syntax
<xs:element name="ScheduleByDay"
    type="dailyScheduleType"
 />
```

<span data-ttu-id="d1d8d-108">O elemento **ScheduleByDay** é definido pelo tipo complexo [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d1d8d-108">The **ScheduleByDay** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d1d8d-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="d1d8d-109">Parent element</span></span>



| <span data-ttu-id="d1d8d-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="d1d8d-110">Element</span></span>                                                                             | <span data-ttu-id="d1d8d-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="d1d8d-111">Derived from</span></span>                                                                       | <span data-ttu-id="d1d8d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1d8d-112">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1d8d-113">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="d1d8d-113">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="d1d8d-114">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="d1d8d-114">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="d1d8d-115">Especifica um gatilho diário, semanal, mensal ou um dia da semana (DOW) mensal.</span><span class="sxs-lookup"><span data-stu-id="d1d8d-115">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="d1d8d-116">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d1d8d-116">Child elements</span></span>



| <span data-ttu-id="d1d8d-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="d1d8d-117">Element</span></span>                                                                            | <span data-ttu-id="d1d8d-118">Type</span><span class="sxs-lookup"><span data-stu-id="d1d8d-118">Type</span></span>             | <span data-ttu-id="d1d8d-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1d8d-119">Description</span></span>                                                         |
|------------------------------------------------------------------------------------|------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="d1d8d-120">**DaysInterval**</span><span class="sxs-lookup"><span data-stu-id="d1d8d-120">**DaysInterval**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md) | <span data-ttu-id="d1d8d-121">**unsignedByte**</span><span class="sxs-lookup"><span data-stu-id="d1d8d-121">**unsignedByte**</span></span> | <span data-ttu-id="d1d8d-122">Especifica o intervalo entre os dias no agendamento.</span><span class="sxs-lookup"><span data-stu-id="d1d8d-122">Specifies the interval between the days in the schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d1d8d-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1d8d-123">Remarks</span></span>

<span data-ttu-id="d1d8d-124">O elemento filho listado anteriormente é definido pelos tipos de elementos complexos [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d1d8d-124">The child element listed previously is defined by the [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) complex element types.</span></span>

<span data-ttu-id="d1d8d-125">A hora do dia em que a tarefa é iniciada é definida pelo elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d1d8d-125">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="d1d8d-126">Para o desenvolvimento de scripts, um gatilho diário é especificado usando o objeto [**DailyTrigger**](weeklytrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="d1d8d-126">For scripting development, a daily trigger is specified using the [**DailyTrigger**](weeklytrigger.md) object.</span></span>

<span data-ttu-id="d1d8d-127">Para desenvolvimento em C++, um gatilho diário é especificado usando a interface [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger) .</span><span class="sxs-lookup"><span data-stu-id="d1d8d-127">For C++ development, a daily trigger is specified using the [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="d1d8d-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d1d8d-128">Examples</span></span>

<span data-ttu-id="d1d8d-129">O XML a seguir define um gatilho de calendário diário que inicia a tarefa todos os dias.</span><span class="sxs-lookup"><span data-stu-id="d1d8d-129">The following XML defines a daily calendar trigger that starts the task every day.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



<span data-ttu-id="d1d8d-130">Para obter um exemplo completo do XML para uma tarefa que especifica um agendamento diário, consulte [exemplo de gatilho diário (XML)](daily-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="d1d8d-130">For a complete example of the XML for a task that specifies a daily schedule, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1d8d-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1d8d-131">Requirements</span></span>



| <span data-ttu-id="d1d8d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1d8d-132">Requirement</span></span> | <span data-ttu-id="d1d8d-133">Valor</span><span class="sxs-lookup"><span data-stu-id="d1d8d-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d1d8d-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1d8d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d1d8d-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d1d8d-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d1d8d-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1d8d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d1d8d-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d1d8d-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d1d8d-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1d8d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1d8d-139">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="d1d8d-139">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="d1d8d-140">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="d1d8d-140">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





