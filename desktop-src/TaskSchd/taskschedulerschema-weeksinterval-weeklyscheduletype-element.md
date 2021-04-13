---
title: Elemento WeeksInterval (weeklyScheduleType)
description: Especifica o intervalo entre as semanas no agendamento.
ms.assetid: 6cbf1e7e-a695-4012-97fd-fe3360c362c4
keywords:
- Agendador de Tarefas do elemento WeeksInterval
topic_type:
- apiref
api_name:
- WeeksInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 747ca4b73ff18bdb3e29d8b909d72b8d2367d89b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369837"
---
# <a name="weeksinterval-weeklyscheduletype-element"></a><span data-ttu-id="810ca-104">Elemento WeeksInterval (weeklyScheduleType)</span><span class="sxs-lookup"><span data-stu-id="810ca-104">WeeksInterval (weeklyScheduleType) Element</span></span>

<span data-ttu-id="810ca-105">Especifica o intervalo entre as semanas no agendamento.</span><span class="sxs-lookup"><span data-stu-id="810ca-105">Specifies the interval between the weeks in the schedule.</span></span>

``` syntax
<xs:element name="WeeksInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="52"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="810ca-106">O elemento é definido pelo tipo complexo [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="810ca-106">The element is defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="810ca-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="810ca-107">Parent element</span></span>



| <span data-ttu-id="810ca-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="810ca-108">Element</span></span>                                                                                  | <span data-ttu-id="810ca-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="810ca-109">Derived from</span></span>                                                                     | <span data-ttu-id="810ca-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="810ca-110">Description</span></span>                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="810ca-111">**ScheduleByWeek**</span><span class="sxs-lookup"><span data-stu-id="810ca-111">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [<span data-ttu-id="810ca-112">**weeklyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="810ca-112">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md) | <span data-ttu-id="810ca-113">Especifica uma agenda semanal.</span><span class="sxs-lookup"><span data-stu-id="810ca-113">Specifies a weekly schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="810ca-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="810ca-114">Remarks</span></span>

<span data-ttu-id="810ca-115">Para o desenvolvimento de scripts, o intervalo semanal é especificado usando a propriedade [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md) .</span><span class="sxs-lookup"><span data-stu-id="810ca-115">For scripting development, the weekly interval is specified using the [**WeeklyTrigger.WeeksInterval**](weeklytrigger-weeksinterval.md) property.</span></span>

<span data-ttu-id="810ca-116">Para desenvolvimento em C++, o intervalo semanal é especificado usando a propriedade [**IWeeklyTrigger:: WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) .</span><span class="sxs-lookup"><span data-stu-id="810ca-116">For C++ development, the weekly interval is specified using the [**IWeeklyTrigger::WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="810ca-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="810ca-117">Examples</span></span>

<span data-ttu-id="810ca-118">O XML a seguir define um gatilho de calendário semanal que inicia uma tarefa de segunda-feira a sexta-feira (às 8:00) todas as semanas.</span><span class="sxs-lookup"><span data-stu-id="810ca-118">The following XML defines a weekly calendar trigger that starts a task Monday through Friday ( at 8:00 AM) every week.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="810ca-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="810ca-119">Requirements</span></span>



| <span data-ttu-id="810ca-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="810ca-120">Requirement</span></span> | <span data-ttu-id="810ca-121">Valor</span><span class="sxs-lookup"><span data-stu-id="810ca-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="810ca-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="810ca-122">Minimum supported client</span></span><br/> | <span data-ttu-id="810ca-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="810ca-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="810ca-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="810ca-124">Minimum supported server</span></span><br/> | <span data-ttu-id="810ca-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="810ca-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="810ca-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="810ca-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="810ca-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="810ca-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="810ca-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="810ca-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





