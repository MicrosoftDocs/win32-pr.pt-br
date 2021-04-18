---
title: Elemento de fevereiro (monthtype)
description: Especifica que a tarefa é executada em fevereiro.
ms.assetid: 871449f8-fa3a-4e1f-be36-bc5c98125721
keywords:
- Elemento de fevereiro Agendador de Tarefas
topic_type:
- apiref
api_name:
- February
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 727751964bfb9a752eb1190f8c7d3a86de2a9413
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766960"
---
# <a name="february-monthstype-element"></a><span data-ttu-id="dedcd-104">Elemento de fevereiro (monthtype)</span><span class="sxs-lookup"><span data-stu-id="dedcd-104">February (monthsType) Element</span></span>

<span data-ttu-id="dedcd-105">Especifica que a tarefa é executada em fevereiro.</span><span class="sxs-lookup"><span data-stu-id="dedcd-105">Specifies that the task runs in February.</span></span>

``` syntax
<xs:element name="February">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="dedcd-106">O elemento **fevereiro** é definido pelo tipo complexo [**monthtype**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="dedcd-106">The **February** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="dedcd-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="dedcd-107">Parent element</span></span>



| <span data-ttu-id="dedcd-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="dedcd-108">Element</span></span>                                                                                                          | <span data-ttu-id="dedcd-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="dedcd-109">Derived from</span></span>                                                     | <span data-ttu-id="dedcd-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="dedcd-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dedcd-111">**Meses (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="dedcd-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="dedcd-112">**monthtype**</span><span class="sxs-lookup"><span data-stu-id="dedcd-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="dedcd-113">Especifica os meses do ano durante os quais a tarefa é executada para uma agenda mensal de dia da semana.</span><span class="sxs-lookup"><span data-stu-id="dedcd-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="dedcd-114">**Meses (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="dedcd-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="dedcd-115">**monthtype**</span><span class="sxs-lookup"><span data-stu-id="dedcd-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="dedcd-116">Especifica os meses do ano durante os quais a tarefa é executada por um agendamento mensal.</span><span class="sxs-lookup"><span data-stu-id="dedcd-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="dedcd-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dedcd-117">Examples</span></span>

<span data-ttu-id="dedcd-118">O XML a seguir define um calendário de meses que executa a tarefa em fevereiro.</span><span class="sxs-lookup"><span data-stu-id="dedcd-118">The following XML defines a months calendar that runs the task in February.</span></span>


```XML
<Months>
    <February/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="dedcd-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dedcd-119">Requirements</span></span>



| <span data-ttu-id="dedcd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="dedcd-120">Requirement</span></span> | <span data-ttu-id="dedcd-121">Valor</span><span class="sxs-lookup"><span data-stu-id="dedcd-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dedcd-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dedcd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dedcd-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dedcd-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dedcd-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dedcd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dedcd-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dedcd-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dedcd-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="dedcd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dedcd-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="dedcd-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="dedcd-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="dedcd-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





