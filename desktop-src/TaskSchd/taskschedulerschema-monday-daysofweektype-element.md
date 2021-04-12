---
title: Elemento segunda (daysOfWeekType)
description: Especifica que a tarefa é executada na segunda-feira.
ms.assetid: 2b7ce0c1-c635-47d0-b482-5c93c0028c92
keywords:
- Elemento segunda-feira Agendador de Tarefas
topic_type:
- apiref
api_name:
- Monday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3967db32a6ccd536e2e389e84de4eec05b333634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455629"
---
# <a name="monday-daysofweektype-element"></a><span data-ttu-id="c3785-104">Elemento segunda (daysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="c3785-104">Monday (daysOfWeekType) Element</span></span>

<span data-ttu-id="c3785-105">Especifica que a tarefa é executada na segunda-feira.</span><span class="sxs-lookup"><span data-stu-id="c3785-105">Specifies that the task runs on Monday.</span></span>

``` syntax
<xs:element name="Monday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="c3785-106">O elemento **segunda-feira** é definido pelo tipo complexo [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c3785-106">The **Monday** element is defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c3785-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="c3785-107">Parent element</span></span>



| <span data-ttu-id="c3785-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c3785-108">Element</span></span>                                                                                                                  | <span data-ttu-id="c3785-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="c3785-109">Derived from</span></span>                                                             | <span data-ttu-id="c3785-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3785-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3785-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="c3785-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="c3785-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="c3785-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="c3785-113">Especifica os dias da semana em que a tarefa é executada por uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="c3785-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="c3785-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="c3785-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="c3785-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="c3785-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="c3785-116">Especifica os dias da semana em que a tarefa é executada para uma agenda semanal.</span><span class="sxs-lookup"><span data-stu-id="c3785-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="c3785-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c3785-117">Examples</span></span>

<span data-ttu-id="c3785-118">O XML a seguir define um calendário de dia da semana que inicia uma tarefa na segunda-feira.</span><span class="sxs-lookup"><span data-stu-id="c3785-118">The following XML defines a day of week calendar that starts a task on Monday.</span></span>


```XML
<DaysOfWeek>
    <Monday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="c3785-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3785-119">Requirements</span></span>



| <span data-ttu-id="c3785-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3785-120">Requirement</span></span> | <span data-ttu-id="c3785-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c3785-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c3785-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3785-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c3785-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c3785-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c3785-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3785-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c3785-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c3785-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c3785-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3785-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3785-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="c3785-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c3785-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="c3785-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





