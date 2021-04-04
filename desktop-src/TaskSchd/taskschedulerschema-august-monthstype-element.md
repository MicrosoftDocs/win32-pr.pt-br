---
title: Elemento de agosto (monthtype)
description: Especifica que a tarefa é executada em agosto.
ms.assetid: cd7e528c-d482-4bb4-a31f-fccdb19a441b
keywords:
- Elemento de agosto Agendador de Tarefas
topic_type:
- apiref
api_name:
- August
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4978ebd8f22da6e157461791c4c2000fce9db6ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824550"
---
# <a name="august-monthstype-element"></a><span data-ttu-id="a8c5a-104">Elemento de agosto (monthtype)</span><span class="sxs-lookup"><span data-stu-id="a8c5a-104">August (monthsType) Element</span></span>

<span data-ttu-id="a8c5a-105">Especifica que a tarefa é executada em agosto.</span><span class="sxs-lookup"><span data-stu-id="a8c5a-105">Specifies that the task runs in August.</span></span>

``` syntax
<xs:element name="August">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="a8c5a-106">O elemento de **agosto** é definido pelo tipo complexo [**monthtype**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a8c5a-106">The **August** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a8c5a-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a8c5a-107">Parent element</span></span>



| <span data-ttu-id="a8c5a-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="a8c5a-108">Element</span></span>                                                                                                          | <span data-ttu-id="a8c5a-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="a8c5a-109">Derived from</span></span>                                                     | <span data-ttu-id="a8c5a-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="a8c5a-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8c5a-111">**Meses (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="a8c5a-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="a8c5a-112">**monthtype**</span><span class="sxs-lookup"><span data-stu-id="a8c5a-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="a8c5a-113">Especifica os meses do ano durante os quais a tarefa é executada para uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="a8c5a-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="a8c5a-114">**Meses (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="a8c5a-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="a8c5a-115">**monthtype**</span><span class="sxs-lookup"><span data-stu-id="a8c5a-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="a8c5a-116">Especifica os meses do ano durante os quais a tarefa é executada por um agendamento mensal.</span><span class="sxs-lookup"><span data-stu-id="a8c5a-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="a8c5a-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a8c5a-117">Examples</span></span>

<span data-ttu-id="a8c5a-118">O XML a seguir define um calendário de meses que executa a tarefa em agosto.</span><span class="sxs-lookup"><span data-stu-id="a8c5a-118">The following XML defines a months calendar that runs the task in August.</span></span>


```XML
<Months>
    <August/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="a8c5a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8c5a-119">Requirements</span></span>



| <span data-ttu-id="a8c5a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8c5a-120">Requirement</span></span> | <span data-ttu-id="a8c5a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a8c5a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a8c5a-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8c5a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a8c5a-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8c5a-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a8c5a-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8c5a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a8c5a-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a8c5a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8c5a-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8c5a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8c5a-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="a8c5a-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="a8c5a-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="a8c5a-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





