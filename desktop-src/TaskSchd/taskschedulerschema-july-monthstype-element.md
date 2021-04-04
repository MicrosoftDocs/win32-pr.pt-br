---
title: Elemento de julho (monthtype)
description: Especifica que a tarefa é executada em julho.
ms.assetid: 6fcb06f1-0806-469c-a283-ba8f2ba2c256
keywords:
- Elemento de julho Agendador de Tarefas
topic_type:
- apiref
api_name:
- July
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6901ca83792ffd98269e26dc9cf24dd575025c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645000"
---
# <a name="july-monthstype-element"></a><span data-ttu-id="9add5-104">Elemento de julho (monthtype)</span><span class="sxs-lookup"><span data-stu-id="9add5-104">July (monthsType) Element</span></span>

<span data-ttu-id="9add5-105">Especifica que a tarefa é executada em julho.</span><span class="sxs-lookup"><span data-stu-id="9add5-105">Specifies that the task runs in July.</span></span>

``` syntax
<xs:element name="July">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="9add5-106">O elemento **julho** é definido pelo tipo complexo [**monthtype**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="9add5-106">The **July** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9add5-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="9add5-107">Parent element</span></span>



| <span data-ttu-id="9add5-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="9add5-108">Element</span></span>                                                                                                          | <span data-ttu-id="9add5-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="9add5-109">Derived from</span></span>                                                     | <span data-ttu-id="9add5-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="9add5-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9add5-111">**Meses (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="9add5-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="9add5-112">**monthtype**</span><span class="sxs-lookup"><span data-stu-id="9add5-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="9add5-113">Especifica os meses do ano durante os quais a tarefa é executada para uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="9add5-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="9add5-114">**Meses (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="9add5-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="9add5-115">**monthtype**</span><span class="sxs-lookup"><span data-stu-id="9add5-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="9add5-116">Especifica os meses do ano durante os quais a tarefa é executada por um agendamento mensal.</span><span class="sxs-lookup"><span data-stu-id="9add5-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="9add5-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9add5-117">Examples</span></span>

<span data-ttu-id="9add5-118">O XML a seguir define um calendário de meses que executa a tarefa em julho.</span><span class="sxs-lookup"><span data-stu-id="9add5-118">The following XML defines a months calendar that runs the task in July.</span></span>


```XML
<Months>
    <July/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="9add5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9add5-119">Requirements</span></span>



| <span data-ttu-id="9add5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9add5-120">Requirement</span></span> | <span data-ttu-id="9add5-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9add5-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9add5-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9add5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9add5-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9add5-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9add5-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9add5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9add5-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9add5-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9add5-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="9add5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9add5-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="9add5-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="9add5-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="9add5-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





