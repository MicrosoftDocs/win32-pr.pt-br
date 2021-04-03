---
title: Elemento Janeiro (monthtype)
description: Especifica que a tarefa é executada em Janeiro.
ms.assetid: 3a0dde08-f2de-4ff4-9c5a-4368ff7a0e2c
keywords:
- Elemento de janeiro Agendador de Tarefas
topic_type:
- apiref
api_name:
- January
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e72967f0fb6addb70af1792ffabf0457b1d20c29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644385"
---
# <a name="january-monthstype-element"></a><span data-ttu-id="112c3-104">Elemento Janeiro (monthtype)</span><span class="sxs-lookup"><span data-stu-id="112c3-104">January (monthsType) Element</span></span>

<span data-ttu-id="112c3-105">Especifica que a tarefa é executada em Janeiro.</span><span class="sxs-lookup"><span data-stu-id="112c3-105">Specifies that the task runs in January.</span></span>

``` syntax
<xs:element name="January">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="112c3-106">O elemento **janeiro** é definido pelo tipo complexo [**monthtype**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="112c3-106">The **January** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="112c3-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="112c3-107">Parent element</span></span>



| <span data-ttu-id="112c3-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="112c3-108">Element</span></span>                                                                                                          | <span data-ttu-id="112c3-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="112c3-109">Derived from</span></span>                                                     | <span data-ttu-id="112c3-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="112c3-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="112c3-111">**Meses (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="112c3-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="112c3-112">**monthtype**</span><span class="sxs-lookup"><span data-stu-id="112c3-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="112c3-113">Especifica os meses do ano durante os quais a tarefa é executada para uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="112c3-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="112c3-114">**Meses (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="112c3-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="112c3-115">**monthtype**</span><span class="sxs-lookup"><span data-stu-id="112c3-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="112c3-116">Especifica os meses do ano durante os quais a tarefa é executada por um agendamento mensal.</span><span class="sxs-lookup"><span data-stu-id="112c3-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="112c3-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="112c3-117">Examples</span></span>

<span data-ttu-id="112c3-118">O XML a seguir define um calendário de meses que executa a tarefa em Janeiro.</span><span class="sxs-lookup"><span data-stu-id="112c3-118">The following XML defines a months calendar that runs the task in January.</span></span>


```XML
<Months>
    <January/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="112c3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="112c3-119">Requirements</span></span>



| <span data-ttu-id="112c3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="112c3-120">Requirement</span></span> | <span data-ttu-id="112c3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="112c3-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="112c3-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="112c3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="112c3-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="112c3-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="112c3-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="112c3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="112c3-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="112c3-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="112c3-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="112c3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="112c3-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="112c3-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="112c3-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="112c3-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





