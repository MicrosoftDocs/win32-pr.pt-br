---
title: Tipo complexo maintenanceSettingsType
description: Define os elementos filho e as informações de sequenciamento para o elemento MaintenanceSettings.
ms.assetid: CA4C452E-CA25-4E2D-B5E2-ED64C59AB3AD
keywords:
- Agendador de Tarefas tipo complexo maintenanceSettingsType
topic_type:
- apiref
api_name:
- maintenanceSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f261e84fe2af1239cce1bbd377e991ede6e8506
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644965"
---
# <a name="maintenancesettingstype-complex-type"></a><span data-ttu-id="48733-104">Tipo complexo maintenanceSettingsType</span><span class="sxs-lookup"><span data-stu-id="48733-104">maintenanceSettingsType Complex Type</span></span>

<span data-ttu-id="48733-105">Define os elementos filho e as informações de sequenciamento para o elemento [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="48733-105">Defines the child elements and sequencing information for the [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="maintenanceSettingsType">
    <xs:all>
        <xs:element name="Period"
            minOccurs="1"
            maxOccurs="1"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="P1D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Deadline"
            minOccurs="1"
            maxOccurs="1"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="P1D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Exclusive"
            type="boolean"
            maxOccurs="1"
            minOccurs="1"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="48733-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="48733-106">Child elements</span></span>



| <span data-ttu-id="48733-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="48733-107">Element</span></span>                                                                        | <span data-ttu-id="48733-108">Type</span><span class="sxs-lookup"><span data-stu-id="48733-108">Type</span></span>    | <span data-ttu-id="48733-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="48733-109">Description</span></span>                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48733-110">**Prazo**</span><span class="sxs-lookup"><span data-stu-id="48733-110">**Deadline**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |         | <span data-ttu-id="48733-111">Especifica o período de tempo após o qual o Agendador de tarefas tentará iniciar a tarefa durante a manutenção automática de emergência, se ela não for concluída durante a manutenção regular.</span><span class="sxs-lookup"><span data-stu-id="48733-111">Specifies the amount of time after which the Task scheduler will attempt to start task during emergency Automatic maintenance, if it failed to complete during regular maintenance.</span></span><br/> |
| <span data-ttu-id="48733-112">**Exclusive**</span><span class="sxs-lookup"><span data-stu-id="48733-112">**Exclusive**</span></span>                                                                  | <span data-ttu-id="48733-113">booleano</span><span class="sxs-lookup"><span data-stu-id="48733-113">boolean</span></span> | <span data-ttu-id="48733-114">Se definido como true, a tarefa será iniciada exclusivamente entre outras tarefas de manutenção.</span><span class="sxs-lookup"><span data-stu-id="48733-114">If set to true, the task will be started exclusively among other maintenance tasks.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="48733-115">**Período**</span><span class="sxs-lookup"><span data-stu-id="48733-115">**Period**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md)   |         | <span data-ttu-id="48733-116">Especifica com que frequência a tarefa precisa ser iniciada durante a manutenção automática.</span><span class="sxs-lookup"><span data-stu-id="48733-116">Specifies how often the task needs to be started during Automatic maintenance.</span></span><br/>                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="48733-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48733-117">Requirements</span></span>



| <span data-ttu-id="48733-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="48733-118">Requirement</span></span> | <span data-ttu-id="48733-119">Valor</span><span class="sxs-lookup"><span data-stu-id="48733-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="48733-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48733-120">Minimum supported client</span></span><br/> | <span data-ttu-id="48733-121">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="48733-121">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="48733-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48733-122">Minimum supported server</span></span><br/> | <span data-ttu-id="48733-123">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="48733-123">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="48733-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="48733-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48733-125">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="48733-125">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="48733-126">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="48733-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





