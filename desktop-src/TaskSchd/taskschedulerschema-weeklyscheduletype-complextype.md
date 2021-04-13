---
title: Tipo complexo weeklyScheduleType
description: Define os elementos filho e as informações de sequenciamento para o elemento ScheduleByWeek.
ms.assetid: 048832fa-2262-4461-9cfc-823a4eb7a1df
keywords:
- Agendador de Tarefas tipo complexo weeklyScheduleType
topic_type:
- apiref
api_name:
- weeklyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 797e01c20e749593d64bad12f017af8be613992e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369461"
---
# <a name="weeklyscheduletype-complex-type"></a><span data-ttu-id="44eda-104">Tipo complexo weeklyScheduleType</span><span class="sxs-lookup"><span data-stu-id="44eda-104">weeklyScheduleType Complex Type</span></span>

<span data-ttu-id="44eda-105">Define os elementos filho e as informações de sequenciamento para o elemento [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="44eda-105">Defines the child elements and sequencing information for the [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="weeklyScheduleType">
    <xs:all>
        <xs:element name="WeeksInterval"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="unsignedByte"
                >
                    <xs:minInclusive
                        value="1"
                     />
                    <xs:maxInclusive
                        value="52"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="DaysOfWeek"
            type="daysOfWeekType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="44eda-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="44eda-106">Child elements</span></span>



| <span data-ttu-id="44eda-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="44eda-107">Element</span></span>                                                                               | <span data-ttu-id="44eda-108">Type</span><span class="sxs-lookup"><span data-stu-id="44eda-108">Type</span></span>                                                                     | <span data-ttu-id="44eda-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="44eda-109">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="44eda-110">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="44eda-110">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [<span data-ttu-id="44eda-111">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="44eda-111">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="44eda-112">Especifica os dias da semana em que a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="44eda-112">Specifies the days of the week in which the task runs.</span></span><br/>    |
| [<span data-ttu-id="44eda-113">**WeeksInterval**</span><span class="sxs-lookup"><span data-stu-id="44eda-113">**WeeksInterval**</span></span>](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) |                                                                          | <span data-ttu-id="44eda-114">Especifica o intervalo entre as semanas no agendamento.</span><span class="sxs-lookup"><span data-stu-id="44eda-114">Specifies the interval between the weeks in the schedule.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="44eda-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44eda-115">Requirements</span></span>



| <span data-ttu-id="44eda-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="44eda-116">Requirement</span></span> | <span data-ttu-id="44eda-117">Valor</span><span class="sxs-lookup"><span data-stu-id="44eda-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="44eda-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44eda-118">Minimum supported client</span></span><br/> | <span data-ttu-id="44eda-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="44eda-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="44eda-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44eda-120">Minimum supported server</span></span><br/> | <span data-ttu-id="44eda-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="44eda-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="44eda-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="44eda-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44eda-123">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="44eda-123">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





