---
title: Elemento de novembro (monthtype)
description: Especifica que a tarefa é executada em novembro.
ms.assetid: 45f8c47b-3884-4f18-8275-f29f82ee32e2
keywords:
- Elemento de novembro Agendador de Tarefas
topic_type:
- apiref
api_name:
- November
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 295b63a4ff4dad1ec07504bb43c4a471d4389159
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105792603"
---
# <a name="november-monthstype-element"></a><span data-ttu-id="840e2-104">Elemento de novembro (monthtype)</span><span class="sxs-lookup"><span data-stu-id="840e2-104">November (monthsType) Element</span></span>

<span data-ttu-id="840e2-105">Especifica que a tarefa é executada em novembro.</span><span class="sxs-lookup"><span data-stu-id="840e2-105">Specifies that the task runs in November.</span></span>

``` syntax
<xs:element name="November">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="840e2-106">O elemento **novembro** é definido pelo tipo complexo [**monthtype**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="840e2-106">The **November** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="840e2-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="840e2-107">Parent element</span></span>



| <span data-ttu-id="840e2-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="840e2-108">Element</span></span>                                                                                                          | <span data-ttu-id="840e2-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="840e2-109">Derived from</span></span>                                                     | <span data-ttu-id="840e2-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="840e2-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="840e2-111">**Meses (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="840e2-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="840e2-112">**monthtype**</span><span class="sxs-lookup"><span data-stu-id="840e2-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="840e2-113">Especifica os meses do ano durante os quais a tarefa é executada para uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="840e2-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="840e2-114">**Meses (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="840e2-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="840e2-115">**monthtype**</span><span class="sxs-lookup"><span data-stu-id="840e2-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="840e2-116">Especifica os meses do ano durante os quais a tarefa é executada por um agendamento mensal.</span><span class="sxs-lookup"><span data-stu-id="840e2-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="840e2-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="840e2-117">Examples</span></span>

<span data-ttu-id="840e2-118">O XML a seguir define um calendário de meses que executa a tarefa em novembro.</span><span class="sxs-lookup"><span data-stu-id="840e2-118">The following XML defines a months calendar that runs the task in November.</span></span>


```XML
<Months>
    <November/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="840e2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="840e2-119">Requirements</span></span>



| <span data-ttu-id="840e2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="840e2-120">Requirement</span></span> | <span data-ttu-id="840e2-121">Valor</span><span class="sxs-lookup"><span data-stu-id="840e2-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="840e2-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="840e2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="840e2-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="840e2-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="840e2-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="840e2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="840e2-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="840e2-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="840e2-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="840e2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="840e2-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="840e2-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="840e2-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="840e2-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





