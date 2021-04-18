---
title: Tipo complexo monthlyScheduleType
description: Define os elementos filho e as informações de sequenciamento para o elemento ScheduleByMonth (calendarTriggerType).
ms.assetid: 3ade775c-ca44-403e-9602-80095c7dba1a
keywords:
- Agendador de Tarefas tipo complexo monthlyScheduleType
topic_type:
- apiref
api_name:
- monthlyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 132c2fafe2b05a01380c13aae2ab7cb3ddaa5330
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789445"
---
# <a name="monthlyscheduletype-complex-type"></a><span data-ttu-id="4adf6-104">Tipo complexo monthlyScheduleType</span><span class="sxs-lookup"><span data-stu-id="4adf6-104">monthlyScheduleType Complex Type</span></span>

<span data-ttu-id="4adf6-105">Define os elementos filho e as informações de sequenciamento para o elemento [**ScheduleByMonth (calendarTriggerType)**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="4adf6-105">Defines the child elements and sequencing information for the [**ScheduleByMonth (calendarTriggerType)**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="monthlyScheduleType">
    <xs:all>
        <xs:element name="DaysOfMonth"
            type="daysOfMonthType"
            minOccurs="0"
         />
        <xs:element name="Months"
            type="monthsType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="4adf6-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4adf6-106">Child elements</span></span>



| <span data-ttu-id="4adf6-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="4adf6-107">Element</span></span>                                                                            | <span data-ttu-id="4adf6-108">Type</span><span class="sxs-lookup"><span data-stu-id="4adf6-108">Type</span></span>                                                                       | <span data-ttu-id="4adf6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4adf6-109">Description</span></span>                                                                                    |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4adf6-110">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="4adf6-110">**DaysOfMonth**</span></span>](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [<span data-ttu-id="4adf6-111">**daysOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="4adf6-111">**daysOfMonthType**</span></span>](taskschedulerschema-daysofmonthtype-complextype.md) | <span data-ttu-id="4adf6-112">Especifica os dias do mês durante os quais a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="4adf6-112">Specifies the days of the month during which the task runs.</span></span><br/>                         |
| [<span data-ttu-id="4adf6-113">**Meses**</span><span class="sxs-lookup"><span data-stu-id="4adf6-113">**Months**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)           | [<span data-ttu-id="4adf6-114">**monthtype**</span><span class="sxs-lookup"><span data-stu-id="4adf6-114">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)           | <span data-ttu-id="4adf6-115">Especifica os meses do ano durante os quais a tarefa é executada por um agendamento mensal.</span><span class="sxs-lookup"><span data-stu-id="4adf6-115">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4adf6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4adf6-116">Requirements</span></span>



| <span data-ttu-id="4adf6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4adf6-117">Requirement</span></span> | <span data-ttu-id="4adf6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4adf6-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4adf6-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4adf6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4adf6-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4adf6-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4adf6-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4adf6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4adf6-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4adf6-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4adf6-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="4adf6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4adf6-124">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="4adf6-124">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="4adf6-125">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="4adf6-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





