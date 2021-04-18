---
title: Tipo complexo dailyScheduleType
description: Define os elementos filho e as informações de sequenciamento para o elemento ScheduleByDay.
ms.assetid: e0b1b09f-d72a-4a85-9059-4a917bc0104a
keywords:
- Agendador de Tarefas tipo complexo dailyScheduleType
topic_type:
- apiref
api_name:
- dailyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5982ab7e72a79dc909a4e91fafe363ca4703639d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105780107"
---
# <a name="dailyscheduletype-complex-type"></a><span data-ttu-id="01b30-104">Tipo complexo dailyScheduleType</span><span class="sxs-lookup"><span data-stu-id="01b30-104">dailyScheduleType Complex Type</span></span>

<span data-ttu-id="01b30-105">Define os elementos filho e as informações de sequenciamento para o elemento [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="01b30-105">Defines the child elements and sequencing information for the [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="dailyScheduleType">
    <xs:all>
        <xs:element name="DaysInterval"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="unsignedInt"
                >
                    <xs:minInclusive
                        value="1"
                     />
                    <xs:maxInclusive
                        value="365"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="01b30-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="01b30-106">Child elements</span></span>



| <span data-ttu-id="01b30-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="01b30-107">Element</span></span>                                                                            | <span data-ttu-id="01b30-108">Type</span><span class="sxs-lookup"><span data-stu-id="01b30-108">Type</span></span> | <span data-ttu-id="01b30-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="01b30-109">Description</span></span>                                                          |
|------------------------------------------------------------------------------------|------|----------------------------------------------------------------------|
| [<span data-ttu-id="01b30-110">**DaysInterval**</span><span class="sxs-lookup"><span data-stu-id="01b30-110">**DaysInterval**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |      | <span data-ttu-id="01b30-111">Especifica o intervalo entre os dias no agendamento.</span><span class="sxs-lookup"><span data-stu-id="01b30-111">Specifies the interval between the days in the schedule.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="01b30-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01b30-112">Requirements</span></span>



| <span data-ttu-id="01b30-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="01b30-113">Requirement</span></span> | <span data-ttu-id="01b30-114">Valor</span><span class="sxs-lookup"><span data-stu-id="01b30-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="01b30-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01b30-115">Minimum supported client</span></span><br/> | <span data-ttu-id="01b30-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01b30-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="01b30-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01b30-117">Minimum supported server</span></span><br/> | <span data-ttu-id="01b30-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="01b30-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="01b30-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="01b30-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01b30-120">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="01b30-120">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="01b30-121">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="01b30-121">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





