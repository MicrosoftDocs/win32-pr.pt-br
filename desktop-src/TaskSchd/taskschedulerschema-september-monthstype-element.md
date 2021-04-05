---
title: Elemento de setembro (monthtype)
description: Especifica que a tarefa é executada em setembro.
ms.assetid: b1ad2221-ca22-4808-bf20-ecf3cbb930f2
keywords:
- Agendador de Tarefas de elemento de setembro
topic_type:
- apiref
api_name:
- September
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdd7e18ba9ae1cc7653589710fb9529281e84ccb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919051"
---
# <a name="september-monthstype-element"></a><span data-ttu-id="1e970-104">Elemento de setembro (monthtype)</span><span class="sxs-lookup"><span data-stu-id="1e970-104">September (monthsType) Element</span></span>

<span data-ttu-id="1e970-105">Especifica que a tarefa é executada em setembro.</span><span class="sxs-lookup"><span data-stu-id="1e970-105">Specifies that the task runs in September.</span></span>

``` syntax
<xs:element name="September">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="1e970-106">O elemento de **setembro** é definido pelo tipo complexo [**monthtype**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1e970-106">The **September** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1e970-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="1e970-107">Parent element</span></span>



| <span data-ttu-id="1e970-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="1e970-108">Element</span></span>                                                                                                          | <span data-ttu-id="1e970-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="1e970-109">Derived from</span></span>                                                     | <span data-ttu-id="1e970-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e970-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e970-111">**Meses (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="1e970-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="1e970-112">**monthtype**</span><span class="sxs-lookup"><span data-stu-id="1e970-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="1e970-113">Especifica os meses do ano durante os quais a tarefa é executada para uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="1e970-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="1e970-114">**Meses (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="1e970-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="1e970-115">**monthtype**</span><span class="sxs-lookup"><span data-stu-id="1e970-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="1e970-116">Especifica os meses do ano durante os quais a tarefa é executada por um agendamento mensal.</span><span class="sxs-lookup"><span data-stu-id="1e970-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="1e970-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1e970-117">Examples</span></span>

<span data-ttu-id="1e970-118">O XML a seguir define um calendário de meses que executa a tarefa em setembro.</span><span class="sxs-lookup"><span data-stu-id="1e970-118">The following XML defines a months calendar that runs the task in September.</span></span>


```XML
<Months>
    <September/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="1e970-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e970-119">Requirements</span></span>



| <span data-ttu-id="1e970-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e970-120">Requirement</span></span> | <span data-ttu-id="1e970-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1e970-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1e970-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e970-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1e970-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1e970-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1e970-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e970-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1e970-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1e970-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1e970-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e970-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e970-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="1e970-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="1e970-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="1e970-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





