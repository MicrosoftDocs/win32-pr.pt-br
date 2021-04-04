---
title: Elemento DaysInterval (dailyScheduleType)
description: Especifica o intervalo entre os dias no agendamento.
ms.assetid: 495ea1c0-37eb-4b12-8241-bfc6489e33ed
keywords:
- Agendador de Tarefas do elemento DaysInterval
topic_type:
- apiref
api_name:
- DaysInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 97b50581aa4825b31983a234a5eb47ff7b7b7e06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918092"
---
# <a name="daysinterval-dailyscheduletype-element"></a><span data-ttu-id="dac2d-104">Elemento DaysInterval (dailyScheduleType)</span><span class="sxs-lookup"><span data-stu-id="dac2d-104">DaysInterval (dailyScheduleType) Element</span></span>

<span data-ttu-id="dac2d-105">Especifica o intervalo entre os dias no agendamento.</span><span class="sxs-lookup"><span data-stu-id="dac2d-105">Specifies the interval between the days in the schedule.</span></span>

``` syntax
<xs:element name="DaysInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedInt"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="365"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="dac2d-106">O elemento é definido pelo tipo complexo [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="dac2d-106">The element is defined by the [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="dac2d-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="dac2d-107">Parent element</span></span>



| <span data-ttu-id="dac2d-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="dac2d-108">Element</span></span>                                                                                | <span data-ttu-id="dac2d-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="dac2d-109">Derived from</span></span>                                                                   | <span data-ttu-id="dac2d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="dac2d-110">Description</span></span>                            |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="dac2d-111">**ScheduleByDay**</span><span class="sxs-lookup"><span data-stu-id="dac2d-111">**ScheduleByDay**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md) | [<span data-ttu-id="dac2d-112">**dailyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="dac2d-112">**dailyScheduleType**</span></span>](taskschedulerschema-dailyscheduletype-complextype.md) | <span data-ttu-id="dac2d-113">Especifica um agendamento diário.</span><span class="sxs-lookup"><span data-stu-id="dac2d-113">Specifies a daily schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="dac2d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="dac2d-114">Remarks</span></span>

<span data-ttu-id="dac2d-115">Para o desenvolvimento de script, o intervalo de dias para um gatilho diário é especificado pela propriedade [**DailyTrigger. DaysInterval**](dailytrigger-daysinterval.md) .</span><span class="sxs-lookup"><span data-stu-id="dac2d-115">For script development, the days interval for a daily trigger is specified by the [**DailyTrigger.DaysInterval**](dailytrigger-daysinterval.md) property.</span></span>

<span data-ttu-id="dac2d-116">Para desenvolvimento em C++, o intervalo de dias para um gatilho diário é especificado pela propriedade [**IDailyTrigger::D aysinterval**](/windows/desktop/api/taskschd/nf-taskschd-idailytrigger-get_daysinterval) .</span><span class="sxs-lookup"><span data-stu-id="dac2d-116">For C++ development, the days interval for a daily trigger is specified by the [**IDailyTrigger::DaysInterval**](/windows/desktop/api/taskschd/nf-taskschd-idailytrigger-get_daysinterval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="dac2d-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dac2d-117">Examples</span></span>

<span data-ttu-id="dac2d-118">O XML a seguir define um gatilho de calendário diário que inicia a tarefa todos os dias.</span><span class="sxs-lookup"><span data-stu-id="dac2d-118">The following XML defines a daily calendar trigger that starts the task every day.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



<span data-ttu-id="dac2d-119">Para obter um exemplo completo do XML para uma tarefa que especifica um agendamento diário, consulte [exemplo de gatilho diário (XML)](daily-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="dac2d-119">For a complete example of the XML for a task that specifies a daily schedule, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dac2d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dac2d-120">Requirements</span></span>



| <span data-ttu-id="dac2d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="dac2d-121">Requirement</span></span> | <span data-ttu-id="dac2d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="dac2d-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dac2d-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dac2d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="dac2d-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dac2d-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dac2d-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dac2d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="dac2d-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dac2d-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dac2d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="dac2d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dac2d-128">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="dac2d-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="dac2d-129">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="dac2d-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





