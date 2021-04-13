---
title: Tipo complexo de repetição
description: Define os elementos filho e as informações de sequência para o elemento repetition (triggerBaseType).
ms.assetid: d2b4b840-3a69-4ff8-ac32-6ec76e7e8788
keywords:
- tipo complexo de repetiçãotype Agendador de Tarefas
topic_type:
- apiref
api_name:
- repetitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aa9ee8c08a79f5db053b772c86929f98a72f011c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369785"
---
# <a name="repetitiontype-complex-type"></a><span data-ttu-id="22058-104">Tipo complexo de repetição</span><span class="sxs-lookup"><span data-stu-id="22058-104">repetitionType Complex Type</span></span>

<span data-ttu-id="22058-105">Define os elementos filho e as informações de sequência para o elemento [**repetition (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="22058-105">Defines the child elements and sequence information for the [**Repetition (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md) element.</span></span>

``` syntax
<xs:complexType name="repetitionType">
    <xs:all>
        <xs:element name="Interval">
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                    <xs:maxInclusive
                        value="P31D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Duration"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="StopAtDurationEnd"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="22058-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="22058-106">Child elements</span></span>



| <span data-ttu-id="22058-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="22058-107">Element</span></span>                                                                                   | <span data-ttu-id="22058-108">Type</span><span class="sxs-lookup"><span data-stu-id="22058-108">Type</span></span>    | <span data-ttu-id="22058-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="22058-109">Description</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22058-110">**Duration**</span><span class="sxs-lookup"><span data-stu-id="22058-110">**Duration**</span></span>](taskschedulerschema-duration-repetitiontype-element.md)                   |         | <span data-ttu-id="22058-111">Especifica por quanto tempo o padrão é repetido.</span><span class="sxs-lookup"><span data-stu-id="22058-111">Specifies how long the pattern is repeated.</span></span> <span data-ttu-id="22058-112">Se nenhum valor for especificado, o padrão será repetido indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="22058-112">If no value is specified, the pattern is repeated indefinitely.</span></span><br/> |
| [<span data-ttu-id="22058-113">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="22058-113">**Interval**</span></span>](taskschedulerschema-interval-repetitiontype-element.md)                   |         | <span data-ttu-id="22058-114">Especifica a quantidade de tempo entre cada reinicialização da tarefa.</span><span class="sxs-lookup"><span data-stu-id="22058-114">Specifies the amount of time between each restart of the task.</span></span><br/>                                              |
| [<span data-ttu-id="22058-115">**StopAtDurationEnd**</span><span class="sxs-lookup"><span data-stu-id="22058-115">**StopAtDurationEnd**</span></span>](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | <span data-ttu-id="22058-116">booleano</span><span class="sxs-lookup"><span data-stu-id="22058-116">boolean</span></span> | <span data-ttu-id="22058-117">Especifica que uma instância em execução da tarefa é interrompida no final da duração do padrão de repetição.</span><span class="sxs-lookup"><span data-stu-id="22058-117">Specifies that a running instance of the task is stopped at the end of the repetition pattern duration.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="22058-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22058-118">Requirements</span></span>



| <span data-ttu-id="22058-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="22058-119">Requirement</span></span> | <span data-ttu-id="22058-120">Valor</span><span class="sxs-lookup"><span data-stu-id="22058-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="22058-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22058-121">Minimum supported client</span></span><br/> | <span data-ttu-id="22058-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="22058-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="22058-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22058-123">Minimum supported server</span></span><br/> | <span data-ttu-id="22058-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="22058-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="22058-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="22058-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22058-126">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="22058-126">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="22058-127">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="22058-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





