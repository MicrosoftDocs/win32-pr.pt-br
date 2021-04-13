---
title: Elemento quarta (daysOfWeekType)
description: Especifica que a tarefa é executada na quarta-feira.
ms.assetid: 6d4f52e2-4390-4f9d-bab8-813bd0851582
keywords:
- Agendador de Tarefas de elemento quarta
topic_type:
- apiref
api_name:
- Wednesday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3f9d8c60cb7cea818cc0b096e99e97e8f1490d47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499609"
---
# <a name="wednesday-daysofweektype-element"></a><span data-ttu-id="64869-104">Elemento quarta (daysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="64869-104">Wednesday (daysOfWeekType) Element</span></span>

<span data-ttu-id="64869-105">Especifica que a tarefa é executada na quarta-feira.</span><span class="sxs-lookup"><span data-stu-id="64869-105">Specifies that the task runs on Wednesday.</span></span>

``` syntax
<xs:element name="Wednesday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="64869-106">O elemento **quarta-feira** é definido pelo tipo complexo [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="64869-106">The **Wednesday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="64869-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="64869-107">Parent element</span></span>



| <span data-ttu-id="64869-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="64869-108">Element</span></span>                                                                                                                  | <span data-ttu-id="64869-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="64869-109">Derived from</span></span>                                                             | <span data-ttu-id="64869-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="64869-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64869-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="64869-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="64869-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="64869-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="64869-113">Especifica os dias da semana em que a tarefa é executada por uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="64869-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="64869-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="64869-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="64869-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="64869-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="64869-116">Especifica os dias da semana em que a tarefa é executada para uma agenda semanal.</span><span class="sxs-lookup"><span data-stu-id="64869-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="64869-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="64869-117">Examples</span></span>

<span data-ttu-id="64869-118">O XML a seguir define um calendário de dia da semana que inicia uma tarefa na quarta-feira.</span><span class="sxs-lookup"><span data-stu-id="64869-118">The following XML defines a day of week calendar that starts a task on Wednesday.</span></span>


```XML
<DaysOfWeek>
    <Wednesday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="64869-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64869-119">Requirements</span></span>



| <span data-ttu-id="64869-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="64869-120">Requirement</span></span> | <span data-ttu-id="64869-121">Valor</span><span class="sxs-lookup"><span data-stu-id="64869-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="64869-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64869-122">Minimum supported client</span></span><br/> | <span data-ttu-id="64869-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="64869-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="64869-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64869-124">Minimum supported server</span></span><br/> | <span data-ttu-id="64869-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="64869-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="64869-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="64869-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64869-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="64869-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="64869-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="64869-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





