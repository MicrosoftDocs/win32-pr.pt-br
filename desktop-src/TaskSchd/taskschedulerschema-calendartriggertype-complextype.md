---
title: Tipo complexo calendarTriggerType
description: Define os elementos filho e as informações de sequenciamento para elementos de calendário.
ms.assetid: bf0d964e-aff2-4807-b086-c504f8963663
keywords:
- Agendador de Tarefas tipo complexo calendarTriggerType
topic_type:
- apiref
api_name:
- calendarTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6f45434fa68b6300157a29318ba257f43bac5992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766200"
---
# <a name="calendartriggertype-complex-type"></a><span data-ttu-id="039fa-104">Tipo complexo calendarTriggerType</span><span class="sxs-lookup"><span data-stu-id="039fa-104">calendarTriggerType Complex Type</span></span>

<span data-ttu-id="039fa-105">Define os elementos filho e as informações de sequenciamento para elementos de calendário.</span><span class="sxs-lookup"><span data-stu-id="039fa-105">Defines the child elements and sequencing information for calendar elements.</span></span>

``` syntax
<xs:complexType name="calendarTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:choice>
                    <xs:element name="ScheduleByDay"
                        type="dailyScheduleType"
                     />
                    <xs:element name="ScheduleByWeek"
                        type="weeklyScheduleType"
                     />
                    <xs:element name="ScheduleByMonth"
                        type="monthlyScheduleType"
                     />
                    <xs:element name="ScheduleByMonthDayOfWeek"
                        type="monthlyDayOfWeekScheduleType"
                     />
                </xs:choice>
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="039fa-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="039fa-106">Child elements</span></span>



| <span data-ttu-id="039fa-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="039fa-107">Element</span></span>                                                                                                      | <span data-ttu-id="039fa-108">Type</span><span class="sxs-lookup"><span data-stu-id="039fa-108">Type</span></span>                                                                                                 | <span data-ttu-id="039fa-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="039fa-109">Description</span></span>                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="039fa-110">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="039fa-110">**RandomDelay**</span></span>](taskschedulerschema-randomdelay-calendartriggertype-element.md)                           | <span data-ttu-id="039fa-111">duration</span><span class="sxs-lookup"><span data-stu-id="039fa-111">duration</span></span>                                                                                             | <span data-ttu-id="039fa-112">Contém o tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho.</span><span class="sxs-lookup"><span data-stu-id="039fa-112">Contains the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="039fa-113">O formato para essa cadeia de caracteres é P <days> dt <hours> H <minutes> M <seconds> S (por exemplo, P2DT5S é um atraso de 2 dias, 5 segundos).</span><span class="sxs-lookup"><span data-stu-id="039fa-113">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, P2DT5S is a 2 day, 5 second delay).</span></span><br/> |
| [<span data-ttu-id="039fa-114">**ScheduleByDay**</span><span class="sxs-lookup"><span data-stu-id="039fa-114">**ScheduleByDay**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [<span data-ttu-id="039fa-115">**dailyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="039fa-115">**dailyScheduleType**</span></span>](taskschedulerschema-dailyscheduletype-complextype.md)                       | <span data-ttu-id="039fa-116">Especifica um agendamento diário.</span><span class="sxs-lookup"><span data-stu-id="039fa-116">Specifies a daily schedule.</span></span> <span data-ttu-id="039fa-117">Por exemplo, a tarefa é iniciada todos os dias, a cada dia, a cada terceiro dia e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="039fa-117">For example, the task starts every day, every-other day, every third day, and so on.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="039fa-118">**ScheduleByMonth**</span><span class="sxs-lookup"><span data-stu-id="039fa-118">**ScheduleByMonth**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [<span data-ttu-id="039fa-119">**monthlyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="039fa-119">**monthlyScheduleType**</span></span>](taskschedulerschema-monthlyscheduletype-complextype.md)                   | <span data-ttu-id="039fa-120">Especifica um agendamento mensal.</span><span class="sxs-lookup"><span data-stu-id="039fa-120">Specifies a monthly schedule.</span></span> <span data-ttu-id="039fa-121">Por exemplo, a tarefa começa às 8:00 em dias específicos do mês em meses específicos.</span><span class="sxs-lookup"><span data-stu-id="039fa-121">For example, the task starts at 8:00 AM on specific days of the month on specific months.</span></span> <br/>                                                                                                       |
| [<span data-ttu-id="039fa-122">**ScheduleByMonthDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="039fa-122">**ScheduleByMonthDayOfWeek**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="039fa-123">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="039fa-123">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="039fa-124">Especifica um gatilho que inicia um trabalho em uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="039fa-124">Specifies a trigger that starts a job on a monthly day-of-week schedule.</span></span> <span data-ttu-id="039fa-125">Por exemplo, a tarefa é iniciada em dias da semana específicos, semanas do mês e meses do ano.</span><span class="sxs-lookup"><span data-stu-id="039fa-125">For example, the task starts on specific days of the week, weeks of the month, and months of the year.</span></span> <br/>                                               |
| [<span data-ttu-id="039fa-126">**ScheduleByWeek**</span><span class="sxs-lookup"><span data-stu-id="039fa-126">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [<span data-ttu-id="039fa-127">**weeklyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="039fa-127">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md)                     | <span data-ttu-id="039fa-128">Especifica uma agenda semanal.</span><span class="sxs-lookup"><span data-stu-id="039fa-128">Specifies a weekly schedule.</span></span> <span data-ttu-id="039fa-129">Por exemplo, a tarefa começa às 8:00 em um dia específico da semana a cada semana ou em um dia específico da semana a cada semana.</span><span class="sxs-lookup"><span data-stu-id="039fa-129">For example, the task starts at 8:00 AM on a specific day of the week every week or on a specific day of the week every other week.</span></span> <br/>                                                              |



## <a name="remarks"></a><span data-ttu-id="039fa-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="039fa-130">Remarks</span></span>

<span data-ttu-id="039fa-131">Além do elemento filho definido aqui, o elemento [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) também usa os elementos filho definidos pelo tipo complexo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="039fa-131">In addition to the child element defined here, the [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) element also uses the child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="039fa-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="039fa-132">Requirements</span></span>



| <span data-ttu-id="039fa-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="039fa-133">Requirement</span></span> | <span data-ttu-id="039fa-134">Valor</span><span class="sxs-lookup"><span data-stu-id="039fa-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="039fa-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="039fa-135">Minimum supported client</span></span><br/> | <span data-ttu-id="039fa-136">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="039fa-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="039fa-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="039fa-137">Minimum supported server</span></span><br/> | <span data-ttu-id="039fa-138">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="039fa-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="039fa-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="039fa-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="039fa-140">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="039fa-140">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="039fa-141">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="039fa-141">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





