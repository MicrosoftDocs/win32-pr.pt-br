---
title: Elemento sábado (daysOfWeekType)
description: Especifica que a tarefa é executada no sábado.
ms.assetid: def26a72-c143-466a-b5b0-6105078afffa
keywords:
- Agendador de Tarefas de elemento sábado
topic_type:
- apiref
api_name:
- Saturday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b5f7cb36002b2add64cdea541caa2fd28df37ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644998"
---
# <a name="saturday-daysofweektype-element"></a><span data-ttu-id="36079-104">Elemento sábado (daysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="36079-104">Saturday (daysOfWeekType) Element</span></span>

<span data-ttu-id="36079-105">Especifica que a tarefa é executada no sábado.</span><span class="sxs-lookup"><span data-stu-id="36079-105">Specifies that the task runs on Saturday.</span></span>

``` syntax
<xs:element name="Saturday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="36079-106">O elemento **sábado** é definido pelo tipo complexo [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="36079-106">The **Saturday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="36079-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="36079-107">Parent element</span></span>



| <span data-ttu-id="36079-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="36079-108">Element</span></span>                                                                                                                  | <span data-ttu-id="36079-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="36079-109">Derived from</span></span>                                                             | <span data-ttu-id="36079-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="36079-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36079-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="36079-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="36079-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="36079-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="36079-113">Especifica os dias da semana em que a tarefa é executada por uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="36079-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="36079-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="36079-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="36079-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="36079-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="36079-116">Especifica os dias da semana em que a tarefa é executada para uma agenda semanal.</span><span class="sxs-lookup"><span data-stu-id="36079-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="36079-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="36079-117">Examples</span></span>

<span data-ttu-id="36079-118">O XML a seguir define um calendário de dia da semana que inicia uma tarefa no sábado.</span><span class="sxs-lookup"><span data-stu-id="36079-118">The following XML defines a day of week calendar that starts a task on Saturday.</span></span>


```XML
<DaysOfWeek>
    <Saturday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="36079-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36079-119">Requirements</span></span>



| <span data-ttu-id="36079-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="36079-120">Requirement</span></span> | <span data-ttu-id="36079-121">Valor</span><span class="sxs-lookup"><span data-stu-id="36079-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="36079-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36079-122">Minimum supported client</span></span><br/> | <span data-ttu-id="36079-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="36079-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="36079-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36079-124">Minimum supported server</span></span><br/> | <span data-ttu-id="36079-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="36079-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="36079-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="36079-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36079-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="36079-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="36079-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="36079-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





