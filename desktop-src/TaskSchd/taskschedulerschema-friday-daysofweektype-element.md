---
title: Elemento sexta (daysOfWeekType)
description: Especifica que a tarefa é executada na sexta-feira.
ms.assetid: bff85911-d354-4954-8c69-7b6f2ca312d3
keywords:
- Elemento de sexta-feira Agendador de Tarefas
topic_type:
- apiref
api_name:
- Friday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 951142e7e925ea71ef1f833be4421351aaea3b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086070"
---
# <a name="friday-daysofweektype-element"></a><span data-ttu-id="cb402-104">Elemento sexta (daysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="cb402-104">Friday (daysOfWeekType) Element</span></span>

<span data-ttu-id="cb402-105">Especifica que a tarefa é executada na sexta-feira.</span><span class="sxs-lookup"><span data-stu-id="cb402-105">Specifies that the task runs on Friday.</span></span>

``` syntax
<xs:element name="Friday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="cb402-106">O elemento **sexta-feira** é definido pelo tipo complexo [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="cb402-106">The **Friday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="cb402-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="cb402-107">Parent element</span></span>



| <span data-ttu-id="cb402-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="cb402-108">Element</span></span>                                                                                                                  | <span data-ttu-id="cb402-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="cb402-109">Derived from</span></span>                                                             | <span data-ttu-id="cb402-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="cb402-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb402-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="cb402-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="cb402-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="cb402-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="cb402-113">Especifica os dias da semana em que a tarefa é executada por uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="cb402-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="cb402-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="cb402-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="cb402-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="cb402-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="cb402-116">Especifica os dias da semana em que a tarefa é executada para uma agenda semanal.</span><span class="sxs-lookup"><span data-stu-id="cb402-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="cb402-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cb402-117">Examples</span></span>

<span data-ttu-id="cb402-118">O XML a seguir define um calendário de dia da semana que inicia uma tarefa na sexta-feira.</span><span class="sxs-lookup"><span data-stu-id="cb402-118">The following XML defines a day of week calendar that starts a task on Friday.</span></span>


```XML
<DaysOfWeek>
    <Friday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="cb402-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb402-119">Requirements</span></span>



| <span data-ttu-id="cb402-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb402-120">Requirement</span></span> | <span data-ttu-id="cb402-121">Valor</span><span class="sxs-lookup"><span data-stu-id="cb402-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cb402-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb402-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cb402-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb402-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cb402-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb402-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cb402-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cb402-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cb402-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb402-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb402-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="cb402-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="cb402-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="cb402-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





