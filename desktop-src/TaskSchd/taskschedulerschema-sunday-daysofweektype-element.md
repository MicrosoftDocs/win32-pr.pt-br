---
title: Elemento domingo (daysOfWeekType)
description: Especifica que a tarefa é executada no domingo.
ms.assetid: 856db869-2273-4bb8-88c8-c126bb16c87b
keywords:
- Elemento de domingo Agendador de Tarefas
topic_type:
- apiref
api_name:
- Sunday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40efba31b392da5959853feeb1cae567cee25cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086113"
---
# <a name="sunday-daysofweektype-element"></a><span data-ttu-id="f94aa-104">Elemento domingo (daysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="f94aa-104">Sunday (daysOfWeekType) Element</span></span>

<span data-ttu-id="f94aa-105">Especifica que a tarefa é executada no domingo.</span><span class="sxs-lookup"><span data-stu-id="f94aa-105">Specifies that the task runs on Sunday.</span></span>

``` syntax
<xs:element name="Sunday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="f94aa-106">O elemento **domingo** é definido pelo tipo complexo [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f94aa-106">The **Sunday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f94aa-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="f94aa-107">Parent element</span></span>



| <span data-ttu-id="f94aa-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="f94aa-108">Element</span></span>                                                                                                                  | <span data-ttu-id="f94aa-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="f94aa-109">Derived from</span></span>                                                             | <span data-ttu-id="f94aa-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f94aa-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f94aa-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="f94aa-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="f94aa-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="f94aa-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="f94aa-113">Especifica os dias da semana em que a tarefa é executada por uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="f94aa-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="f94aa-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="f94aa-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="f94aa-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="f94aa-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="f94aa-116">Especifica os dias da semana em que a tarefa é executada para uma agenda semanal.</span><span class="sxs-lookup"><span data-stu-id="f94aa-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="f94aa-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f94aa-117">Examples</span></span>

<span data-ttu-id="f94aa-118">O XML a seguir define um calendário de dia da semana que inicia uma tarefa em domingo.</span><span class="sxs-lookup"><span data-stu-id="f94aa-118">The following XML defines a day of week calendar that starts a task on Sunday.</span></span>


```XML
<DaysOfWeek>
    <Sunday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="f94aa-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f94aa-119">Requirements</span></span>



| <span data-ttu-id="f94aa-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f94aa-120">Requirement</span></span> | <span data-ttu-id="f94aa-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f94aa-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f94aa-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f94aa-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f94aa-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f94aa-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f94aa-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f94aa-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f94aa-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f94aa-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f94aa-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f94aa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f94aa-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f94aa-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f94aa-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f94aa-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





