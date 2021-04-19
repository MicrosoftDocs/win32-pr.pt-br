---
title: Elemento Week (weektype)
description: Especifica uma semana específica do mês.
ms.assetid: 0cec07da-e9e7-43ef-9f54-48d00114ba1f
keywords:
- Elemento Week Agendador de Tarefas
topic_type:
- apiref
api_name:
- Week
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0487aa07e1f1132c998b6cb2ba0f518a9db57ce2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105796305"
---
# <a name="week-weekstype-element"></a><span data-ttu-id="b8048-104">Elemento Week (weektype)</span><span class="sxs-lookup"><span data-stu-id="b8048-104">Week (weeksType) Element</span></span>

<span data-ttu-id="b8048-105">Especifica uma semana específica do mês.</span><span class="sxs-lookup"><span data-stu-id="b8048-105">Specifies a specific week of the month.</span></span>

``` syntax
<xs:element name="Week"
    type="weekType"
 />
```

<span data-ttu-id="b8048-106">O elemento **Week** é definido pelo tipo complexo [**weektype**](taskschedulerschema-weekstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b8048-106">The **Week** element is defined by the [**weeksType**](taskschedulerschema-weekstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b8048-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="b8048-107">Parent element</span></span>



| <span data-ttu-id="b8048-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b8048-108">Element</span></span>                                                                                                        | <span data-ttu-id="b8048-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="b8048-109">Derived from</span></span>                                                   | <span data-ttu-id="b8048-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b8048-110">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="b8048-111">**Semanas (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="b8048-111">**Weeks (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="b8048-112">**weektype**</span><span class="sxs-lookup"><span data-stu-id="b8048-112">**weeksType**</span></span>](taskschedulerschema-weekstype-complextype.md) | <span data-ttu-id="b8048-113">Especifica as semanas do mês em que a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="b8048-113">Specifies the weeks of the month in which the task is run.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b8048-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8048-114">Remarks</span></span>

<span data-ttu-id="b8048-115">Ao especificar as semanas do mês, use os números 1-4 para as primeiras quatro semanas do mês ou use a cadeia de caracteres "Last" para indicar que a última semana do mês.</span><span class="sxs-lookup"><span data-stu-id="b8048-115">When specifying the weeks of the month, use the numbers 1-4 for the first four weeks of the month or use the string "Last" to indicate that last week of the month.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8048-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8048-116">Requirements</span></span>



| <span data-ttu-id="b8048-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8048-117">Requirement</span></span> | <span data-ttu-id="b8048-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b8048-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b8048-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8048-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b8048-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8048-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b8048-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8048-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b8048-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b8048-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b8048-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8048-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8048-124">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="b8048-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="b8048-125">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="b8048-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





