---
title: Tipo complexo daysOfWeekType
description: Define os elementos filho e as informações de sequenciamento para os elementos DaysOfWeek (weeklyScheduleType) e DaysOfWeek (monthlyDayOfWeekScheduleType).
ms.assetid: b3315582-af7a-4d4c-8f6f-61de12a85f46
keywords:
- Agendador de Tarefas tipo complexo daysOfWeekType
topic_type:
- apiref
api_name:
- daysOfWeekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b4a1b5e6aeaa77c0bdfe12b1d5b68fde018f236
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295915"
---
# <a name="daysofweektype-complex-type"></a><span data-ttu-id="6267a-104">Tipo complexo daysOfWeekType</span><span class="sxs-lookup"><span data-stu-id="6267a-104">daysOfWeekType Complex Type</span></span>

<span data-ttu-id="6267a-105">Define os elementos filho e as informações de sequenciamento para os elementos [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) e [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6267a-105">Defines the child elements and sequencing information for the [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) and [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) elements.</span></span>

``` syntax
<xs:complexType name="daysOfWeekType">
    <xs:all>
        <xs:element name="Monday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Tuesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Wednesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Thursday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Friday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Saturday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Sunday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="6267a-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6267a-106">Child elements</span></span>



| <span data-ttu-id="6267a-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="6267a-107">Element</span></span>                                                                   | <span data-ttu-id="6267a-108">Type</span><span class="sxs-lookup"><span data-stu-id="6267a-108">Type</span></span> | <span data-ttu-id="6267a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="6267a-109">Description</span></span>                         |
|---------------------------------------------------------------------------|------|-------------------------------------|
| [<span data-ttu-id="6267a-110">**Friday**</span><span class="sxs-lookup"><span data-stu-id="6267a-110">**Friday**</span></span>](taskschedulerschema-friday-daysofweektype-element.md)       | <span data-ttu-id="6267a-111">N/D</span><span class="sxs-lookup"><span data-stu-id="6267a-111">N/A</span></span>  | <span data-ttu-id="6267a-112">A tarefa é executada na sexta-feira.</span><span class="sxs-lookup"><span data-stu-id="6267a-112">Task runs on Friday.</span></span> <br/>    |
| [<span data-ttu-id="6267a-113">**Monday**</span><span class="sxs-lookup"><span data-stu-id="6267a-113">**Monday**</span></span>](taskschedulerschema-monday-daysofweektype-element.md)       | <span data-ttu-id="6267a-114">N/D</span><span class="sxs-lookup"><span data-stu-id="6267a-114">N/A</span></span>  | <span data-ttu-id="6267a-115">A tarefa é executada na segunda-feira.</span><span class="sxs-lookup"><span data-stu-id="6267a-115">Task runs on Monday.</span></span><br/>     |
| [<span data-ttu-id="6267a-116">**Sábado**</span><span class="sxs-lookup"><span data-stu-id="6267a-116">**Saturday**</span></span>](taskschedulerschema-saturday-daysofweektype-element.md)   | <span data-ttu-id="6267a-117">N/D</span><span class="sxs-lookup"><span data-stu-id="6267a-117">N/A</span></span>  | <span data-ttu-id="6267a-118">A tarefa é executada no sábado.</span><span class="sxs-lookup"><span data-stu-id="6267a-118">Task runs on Saturday.</span></span> <br/>  |
| [<span data-ttu-id="6267a-119">**Sunday**</span><span class="sxs-lookup"><span data-stu-id="6267a-119">**Sunday**</span></span>](taskschedulerschema-sunday-daysofweektype-element.md)       | <span data-ttu-id="6267a-120">N/D</span><span class="sxs-lookup"><span data-stu-id="6267a-120">N/A</span></span>  | <span data-ttu-id="6267a-121">A tarefa é executada no domingo.</span><span class="sxs-lookup"><span data-stu-id="6267a-121">Task runs on Sunday.</span></span> <br/>    |
| [<span data-ttu-id="6267a-122">**Quinta-feira**</span><span class="sxs-lookup"><span data-stu-id="6267a-122">**Thursday**</span></span>](taskschedulerschema-thursday-daysofweektype-element.md)   | <span data-ttu-id="6267a-123">N/D</span><span class="sxs-lookup"><span data-stu-id="6267a-123">N/A</span></span>  | <span data-ttu-id="6267a-124">A tarefa é executada na quinta-feira</span><span class="sxs-lookup"><span data-stu-id="6267a-124">Task runs on Thursday</span></span> <br/>   |
| [<span data-ttu-id="6267a-125">**Terça-feira**</span><span class="sxs-lookup"><span data-stu-id="6267a-125">**Tuesday**</span></span>](taskschedulerschema-tuesday-daysofweektype-element.md)     | <span data-ttu-id="6267a-126">N/D</span><span class="sxs-lookup"><span data-stu-id="6267a-126">N/A</span></span>  | <span data-ttu-id="6267a-127">A tarefa é executada na terça-feira.</span><span class="sxs-lookup"><span data-stu-id="6267a-127">Task runs on Tuesday.</span></span> <br/>   |
| [<span data-ttu-id="6267a-128">**Quarta-feira**</span><span class="sxs-lookup"><span data-stu-id="6267a-128">**Wednesday**</span></span>](taskschedulerschema-wednesday-daysofweektype-element.md) | <span data-ttu-id="6267a-129">N/D</span><span class="sxs-lookup"><span data-stu-id="6267a-129">N/A</span></span>  | <span data-ttu-id="6267a-130">A tarefa é executada na quarta-feira.</span><span class="sxs-lookup"><span data-stu-id="6267a-130">Task runs on Wednesday.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="6267a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6267a-131">Requirements</span></span>



| <span data-ttu-id="6267a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6267a-132">Requirement</span></span> | <span data-ttu-id="6267a-133">Valor</span><span class="sxs-lookup"><span data-stu-id="6267a-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6267a-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6267a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6267a-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6267a-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6267a-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6267a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6267a-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6267a-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6267a-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="6267a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6267a-139">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="6267a-139">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="6267a-140">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="6267a-140">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





