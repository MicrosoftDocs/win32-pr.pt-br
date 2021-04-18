---
title: Elemento Tuesday (daysOfWeekType)
description: Especifica que a tarefa é executada na terça-feira.
ms.assetid: 588608e9-33f9-405d-8b4b-35f11ab403db
keywords:
- Elemento de terça-feira Agendador de Tarefas
topic_type:
- apiref
api_name:
- Tuesday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ed48803d0cad5dae409202869c600e7e7a60643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789836"
---
# <a name="tuesday-daysofweektype-element"></a><span data-ttu-id="e1106-104">Elemento Tuesday (daysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="e1106-104">Tuesday (daysOfWeekType) Element</span></span>

<span data-ttu-id="e1106-105">Especifica que a tarefa é executada na terça-feira.</span><span class="sxs-lookup"><span data-stu-id="e1106-105">Specifies that the task runs on Tuesday.</span></span>

``` syntax
<xs:element name="Tuesday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="e1106-106">O elemento **Tuesday** é definido pelo tipo complexo [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e1106-106">The **Tuesday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e1106-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="e1106-107">Parent element</span></span>



| <span data-ttu-id="e1106-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="e1106-108">Element</span></span>                                                                                                                  | <span data-ttu-id="e1106-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="e1106-109">Derived from</span></span>                                                             | <span data-ttu-id="e1106-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1106-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1106-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="e1106-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="e1106-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="e1106-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="e1106-113">Especifica os dias da semana em que a tarefa é executada por uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="e1106-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="e1106-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="e1106-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="e1106-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="e1106-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="e1106-116">Especifica os dias da semana em que a tarefa é executada para uma agenda semanal.</span><span class="sxs-lookup"><span data-stu-id="e1106-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="e1106-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e1106-117">Examples</span></span>

<span data-ttu-id="e1106-118">O XML a seguir define um calendário de dia da semana que inicia uma tarefa na terça-feira.</span><span class="sxs-lookup"><span data-stu-id="e1106-118">The following XML defines a day of week calendar that starts a task on Tuesday.</span></span>


```XML
<DaysOfWeek>
    <Tuesday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="e1106-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1106-119">Requirements</span></span>



| <span data-ttu-id="e1106-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1106-120">Requirement</span></span> | <span data-ttu-id="e1106-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e1106-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e1106-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1106-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e1106-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e1106-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e1106-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1106-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e1106-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e1106-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e1106-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1106-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1106-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="e1106-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="e1106-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="e1106-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





