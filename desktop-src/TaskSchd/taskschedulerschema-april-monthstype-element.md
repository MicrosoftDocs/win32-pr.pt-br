---
title: Elemento April (monthtype)
description: Especifica que a tarefa é executada em abril.
ms.assetid: b642e142-0acc-4b88-a86a-5d539613ead6
keywords:
- Elemento de abril Agendador de Tarefas
topic_type:
- apiref
api_name:
- April
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ecde82e5091adf51c2e42b682e36dba6d45e85c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086291"
---
# <a name="april-monthstype-element"></a><span data-ttu-id="30e6c-104">Elemento April (monthtype)</span><span class="sxs-lookup"><span data-stu-id="30e6c-104">April (monthsType) Element</span></span>

<span data-ttu-id="30e6c-105">Especifica que a tarefa é executada em abril.</span><span class="sxs-lookup"><span data-stu-id="30e6c-105">Specifies that the task runs in April.</span></span>

``` syntax
<xs:element name="April">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="30e6c-106">O elemento **abril** é definido pelo tipo complexo [**monthtype**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="30e6c-106">The **April** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="30e6c-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="30e6c-107">Parent element</span></span>



| <span data-ttu-id="30e6c-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="30e6c-108">Element</span></span>                                                                                                          | <span data-ttu-id="30e6c-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="30e6c-109">Derived from</span></span>                                                     | <span data-ttu-id="30e6c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="30e6c-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="30e6c-111">**Meses (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="30e6c-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="30e6c-112">**monthtype**</span><span class="sxs-lookup"><span data-stu-id="30e6c-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="30e6c-113">Especifica os meses do ano durante os quais a tarefa é executada por um agendamento mensal.</span><span class="sxs-lookup"><span data-stu-id="30e6c-113">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |
| [<span data-ttu-id="30e6c-114">**Meses (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="30e6c-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="30e6c-115">**monthtype**</span><span class="sxs-lookup"><span data-stu-id="30e6c-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="30e6c-116">Especifica os meses do ano durante os quais a tarefa é executada para uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="30e6c-116">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="30e6c-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="30e6c-117">Examples</span></span>

<span data-ttu-id="30e6c-118">O XML a seguir define um calendário de meses que executa a tarefa em abril.</span><span class="sxs-lookup"><span data-stu-id="30e6c-118">The following XML defines a months calendar that runs the task in April.</span></span>


```XML
<Months>
    <April/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="30e6c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30e6c-119">Requirements</span></span>



| <span data-ttu-id="30e6c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="30e6c-120">Requirement</span></span> | <span data-ttu-id="30e6c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="30e6c-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="30e6c-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30e6c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="30e6c-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="30e6c-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="30e6c-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30e6c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="30e6c-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="30e6c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="30e6c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="30e6c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30e6c-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="30e6c-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="30e6c-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="30e6c-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





