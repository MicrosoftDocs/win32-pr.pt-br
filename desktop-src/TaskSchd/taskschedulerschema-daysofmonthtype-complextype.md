---
title: Tipo complexo daysOfMonthType
description: Define o elemento filho e as informações de sequenciamento para o elemento DaysOfMonth (monthlyScheduleType).
ms.assetid: 8258c090-c836-497e-8e5b-db4782277822
keywords:
- Agendador de Tarefas tipo complexo daysOfMonthType
topic_type:
- apiref
api_name:
- daysOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1459528b47bf01a9e336b758b739c3f5751ee1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369823"
---
# <a name="daysofmonthtype-complex-type"></a><span data-ttu-id="f0bef-104">Tipo complexo daysOfMonthType</span><span class="sxs-lookup"><span data-stu-id="f0bef-104">daysOfMonthType Complex Type</span></span>

<span data-ttu-id="f0bef-105">Define o elemento filho e as informações de sequenciamento para o elemento [**DaysOfMonth (monthlyScheduleType)**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f0bef-105">Defines the child element and sequencing information for the [**DaysOfMonth (monthlyScheduleType)**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) element.</span></span>

``` syntax
<xs:complexType name="daysOfMonthType">
    <xs:sequence>
        <xs:element name="Day"
            type="dayOfMonthType"
            minOccurs="0"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="f0bef-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f0bef-106">Child elements</span></span>



| <span data-ttu-id="f0bef-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="f0bef-107">Element</span></span>                                                        | <span data-ttu-id="f0bef-108">Type</span><span class="sxs-lookup"><span data-stu-id="f0bef-108">Type</span></span>                                                                    | <span data-ttu-id="f0bef-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f0bef-109">Description</span></span>                                                          |
|----------------------------------------------------------------|-------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="f0bef-110">**Dia**</span><span class="sxs-lookup"><span data-stu-id="f0bef-110">**Day**</span></span>](taskschedulerschema-day-daysofmonthtype-element.md) | [<span data-ttu-id="f0bef-111">**dayOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="f0bef-111">**dayOfMonthType**</span></span>](taskschedulerschema-dayofmonthtype-simpletype.md) | <span data-ttu-id="f0bef-112">Especifica um dia do mês durante o qual a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="f0bef-112">Specifies a day of the month during which the task runs.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="f0bef-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0bef-113">Requirements</span></span>



| <span data-ttu-id="f0bef-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0bef-114">Requirement</span></span> | <span data-ttu-id="f0bef-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f0bef-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f0bef-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0bef-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f0bef-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f0bef-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f0bef-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0bef-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f0bef-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f0bef-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f0bef-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0bef-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0bef-121">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f0bef-121">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="f0bef-122">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f0bef-122">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





