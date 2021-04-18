---
title: Tipo complexo monthlyDayOfWeekScheduleType
description: Define os elementos filho e as informações de sequenciamento para o elemento ScheduleByMonthDayOfWeek.
ms.assetid: fb4e5ba3-592b-47a4-bedf-5181d2b7a50f
keywords:
- Agendador de Tarefas tipo complexo monthlyDayOfWeekScheduleType
topic_type:
- apiref
api_name:
- monthlyDayOfWeekScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 782715aed5cbf59a98e996bfa18fdd7c1022227a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756978"
---
# <a name="monthlydayofweekscheduletype-complex-type"></a><span data-ttu-id="4791c-104">Tipo complexo monthlyDayOfWeekScheduleType</span><span class="sxs-lookup"><span data-stu-id="4791c-104">monthlyDayOfWeekScheduleType Complex Type</span></span>

<span data-ttu-id="4791c-105">Define os elementos filho e as informações de sequenciamento para o elemento [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="4791c-105">Defines the child elements and sequencing information for the [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="monthlyDayOfWeekScheduleType">
    <xs:all>
        <xs:element name="Weeks"
            type="weeksType"
            minOccurs="0"
         />
        <xs:element name="DaysOfWeek"
            type="daysOfWeekType"
         />
        <xs:element name="Months"
            type="monthsType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="4791c-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4791c-106">Child elements</span></span>



| <span data-ttu-id="4791c-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="4791c-107">Element</span></span>                                                                                   | <span data-ttu-id="4791c-108">Type</span><span class="sxs-lookup"><span data-stu-id="4791c-108">Type</span></span>                                                                     | <span data-ttu-id="4791c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4791c-109">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="4791c-110">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="4791c-110">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="4791c-111">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="4791c-111">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="4791c-112">Especifica os dias da semana durante os quais a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="4791c-112">Specifies the days of the week during which the task runs.</span></span><br/>   |
| [<span data-ttu-id="4791c-113">**Meses**</span><span class="sxs-lookup"><span data-stu-id="4791c-113">**Months**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [<span data-ttu-id="4791c-114">**monthtype**</span><span class="sxs-lookup"><span data-stu-id="4791c-114">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)         | <span data-ttu-id="4791c-115">Especifica os meses do ano durante os quais a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="4791c-115">Specifies the months of the year during which the task runs.</span></span><br/> |
| [<span data-ttu-id="4791c-116">**Semanas**</span><span class="sxs-lookup"><span data-stu-id="4791c-116">**Weeks**</span></span>](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | [<span data-ttu-id="4791c-117">**weektype**</span><span class="sxs-lookup"><span data-stu-id="4791c-117">**weeksType**</span></span>](taskschedulerschema-weekstype-complextype.md)           | <span data-ttu-id="4791c-118">Especifica as semanas do mês durante as quais a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="4791c-118">Specifies the weeks of the month during which the task runs.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4791c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4791c-119">Requirements</span></span>



| <span data-ttu-id="4791c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4791c-120">Requirement</span></span> | <span data-ttu-id="4791c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="4791c-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4791c-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4791c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4791c-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4791c-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4791c-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4791c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4791c-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4791c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4791c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="4791c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4791c-127">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="4791c-127">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="4791c-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="4791c-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





