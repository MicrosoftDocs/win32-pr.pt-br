---
title: Elemento da quinta (daysOfWeekType)
description: Especifica que a tarefa é executada na quinta-feira.
ms.assetid: 01d0e7e8-7135-4f43-9d8f-b50c002b93bc
keywords:
- Elemento da quinta Agendador de Tarefas
topic_type:
- apiref
api_name:
- Thursday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 12b1fb602411a9e4562a044b044e43de4800f239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754719"
---
# <a name="thursday-daysofweektype-element"></a><span data-ttu-id="c1851-104">Elemento da quinta (daysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="c1851-104">Thursday (daysOfWeekType) Element</span></span>

<span data-ttu-id="c1851-105">Especifica que a tarefa é executada na quinta-feira.</span><span class="sxs-lookup"><span data-stu-id="c1851-105">Specifies that the task runs on Thursday.</span></span>

``` syntax
<xs:element name="Thursday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="c1851-106">O elemento da **quinta-feira** é definido pelo tipo complexo [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c1851-106">The **Thursday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c1851-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="c1851-107">Parent element</span></span>



| <span data-ttu-id="c1851-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c1851-108">Element</span></span>                                                                                                                  | <span data-ttu-id="c1851-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="c1851-109">Derived from</span></span>                                                             | <span data-ttu-id="c1851-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1851-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1851-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="c1851-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="c1851-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="c1851-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="c1851-113">Especifica os dias da semana em que a tarefa é executada por uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="c1851-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="c1851-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="c1851-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="c1851-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="c1851-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="c1851-116">Especifica os dias da semana em que a tarefa é executada para uma agenda semanal.</span><span class="sxs-lookup"><span data-stu-id="c1851-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="c1851-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c1851-117">Examples</span></span>

<span data-ttu-id="c1851-118">O XML a seguir define um calendário de dia da semana que inicia uma tarefa na quinta-feira.</span><span class="sxs-lookup"><span data-stu-id="c1851-118">The following XML defines a day of week calendar that starts a task on Thursday.</span></span>


```XML
<DaysOfWeek>
    <Thursday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="c1851-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1851-119">Requirements</span></span>



| <span data-ttu-id="c1851-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1851-120">Requirement</span></span> | <span data-ttu-id="c1851-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c1851-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c1851-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1851-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c1851-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c1851-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c1851-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1851-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c1851-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c1851-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1851-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1851-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1851-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="c1851-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c1851-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="c1851-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





