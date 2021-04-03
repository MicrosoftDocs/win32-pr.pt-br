---
title: Elemento de junho (monthtype)
description: Especifica que a tarefa é executada em junho.
ms.assetid: 15b0e8c2-4dc1-4ca3-99c5-bd9a36718904
keywords:
- Elemento de junho Agendador de Tarefas
topic_type:
- apiref
api_name:
- June
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e6c21834348a70033af69a71534c60c1b08d91a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644880"
---
# <a name="june-monthstype-element"></a><span data-ttu-id="3f51f-104">Elemento de junho (monthtype)</span><span class="sxs-lookup"><span data-stu-id="3f51f-104">June (monthsType) Element</span></span>

<span data-ttu-id="3f51f-105">Especifica que a tarefa é executada em junho.</span><span class="sxs-lookup"><span data-stu-id="3f51f-105">Specifies that the task runs in June.</span></span>

``` syntax
<xs:element name="June">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="3f51f-106">O elemento de **junho** é definido pelo tipo complexo [**monthtype**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="3f51f-106">The **June** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="3f51f-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="3f51f-107">Parent element</span></span>



| <span data-ttu-id="3f51f-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="3f51f-108">Element</span></span>                                                                                                          | <span data-ttu-id="3f51f-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="3f51f-109">Derived from</span></span>                                                     | <span data-ttu-id="3f51f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="3f51f-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f51f-111">**Meses (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="3f51f-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="3f51f-112">**monthtype**</span><span class="sxs-lookup"><span data-stu-id="3f51f-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="3f51f-113">Especifica os meses do ano durante os quais a tarefa é executada para uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="3f51f-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="3f51f-114">**Meses (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="3f51f-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="3f51f-115">**monthtype**</span><span class="sxs-lookup"><span data-stu-id="3f51f-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="3f51f-116">Especifica os meses do ano durante os quais a tarefa é executada por um agendamento mensal.</span><span class="sxs-lookup"><span data-stu-id="3f51f-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="3f51f-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3f51f-117">Examples</span></span>

<span data-ttu-id="3f51f-118">O XML a seguir define um calendário de meses que executa a tarefa em junho.</span><span class="sxs-lookup"><span data-stu-id="3f51f-118">The following XML defines a months calendar that runs the task in June.</span></span>


```XML
<Months>
    <June/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="3f51f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f51f-119">Requirements</span></span>



| <span data-ttu-id="3f51f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f51f-120">Requirement</span></span> | <span data-ttu-id="3f51f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3f51f-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3f51f-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f51f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3f51f-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f51f-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3f51f-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f51f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3f51f-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3f51f-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3f51f-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f51f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f51f-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="3f51f-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="3f51f-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="3f51f-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





