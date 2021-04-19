---
title: Tipo complexo idleSettingsType
description: Define os elementos filho e as informações de sequenciamento para o elemento IdleSettings (settingstype).
ms.assetid: 0f50c4d6-fda9-42cc-8dab-4c9439fbea4b
keywords:
- Agendador de Tarefas tipo complexo idleSettingsType
topic_type:
- apiref
api_name:
- idleSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba5ffa3acb879aad095b5b136d882bb817eb0ab0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105782887"
---
# <a name="idlesettingstype-complex-type"></a><span data-ttu-id="524c1-104">Tipo complexo idleSettingsType</span><span class="sxs-lookup"><span data-stu-id="524c1-104">idleSettingsType Complex Type</span></span>

<span data-ttu-id="524c1-105">Define os elementos filho e as informações de sequenciamento para o elemento [**IdleSettings (settingstype)**](taskschedulerschema-idlesettings-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="524c1-105">Defines the child elements and sequencing information for the [**IdleSettings (settingsType)**](taskschedulerschema-idlesettings-settingstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="idleSettingsType">
    <xs:all>
        <xs:element name="Duration"
            default="PT10M"
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
        <xs:element name="WaitTimeout"
            default="PT1H"
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
        <xs:element name="StopOnIdleEnd"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="524c1-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="524c1-106">Child elements</span></span>



| <span data-ttu-id="524c1-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="524c1-107">Element</span></span>                                                                                  | <span data-ttu-id="524c1-108">Type</span><span class="sxs-lookup"><span data-stu-id="524c1-108">Type</span></span>    | <span data-ttu-id="524c1-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="524c1-109">Description</span></span>                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="524c1-110">**Duration**</span><span class="sxs-lookup"><span data-stu-id="524c1-110">**Duration**</span></span>](taskschedulerschema-duration-idlesettingstype-element.md)                |         | <span data-ttu-id="524c1-111">Especifica a quantidade de tempo permitido para iniciar a tarefa enquanto estiver em uma condição ociosa.</span><span class="sxs-lookup"><span data-stu-id="524c1-111">Specifies the amount of time allowed to start the task while in an idle condition.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="524c1-112">**RestartOnIdle**</span><span class="sxs-lookup"><span data-stu-id="524c1-112">**RestartOnIdle**</span></span>](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | <span data-ttu-id="524c1-113">booleano</span><span class="sxs-lookup"><span data-stu-id="524c1-113">boolean</span></span> | <span data-ttu-id="524c1-114">A tarefa é reiniciada assim que uma condição ociosa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="524c1-114">The task is restarted as soon as an idle condition starts.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="524c1-115">**StopOnIdleEnd**</span><span class="sxs-lookup"><span data-stu-id="524c1-115">**StopOnIdleEnd**</span></span>](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | <span data-ttu-id="524c1-116">booleano</span><span class="sxs-lookup"><span data-stu-id="524c1-116">boolean</span></span> | <span data-ttu-id="524c1-117">Especifica que a tarefa será encerrada se a condição de ociosidade terminar antes que a duração de ociosidade seja excedida.</span><span class="sxs-lookup"><span data-stu-id="524c1-117">Specifies that the task is terminated if the idle condition ends before the idle duration is exceeded.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="524c1-118">**WaitTimeout**</span><span class="sxs-lookup"><span data-stu-id="524c1-118">**WaitTimeout**</span></span>](taskschedulerschema-waittimeout-idlesettingstype-element.md)          |         | <span data-ttu-id="524c1-119">Especifica a quantidade de tempo de espera para que uma condição ociosa seja iniciada.</span><span class="sxs-lookup"><span data-stu-id="524c1-119">Specifies the amount of time to wait for an idle condition to start.</span></span> <span data-ttu-id="524c1-120">Se nenhum valor for especificado para esse elemento, o serviço de Agendador de Tarefas aguardará indefinidamente se uma condição ociosa ocorrer.</span><span class="sxs-lookup"><span data-stu-id="524c1-120">If no value is specified for this element, then the Task Scheduler service will wait indefinitely for an idle condition to occur.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="524c1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="524c1-121">Requirements</span></span>



| <span data-ttu-id="524c1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="524c1-122">Requirement</span></span> | <span data-ttu-id="524c1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="524c1-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="524c1-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="524c1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="524c1-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="524c1-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="524c1-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="524c1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="524c1-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="524c1-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="524c1-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="524c1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="524c1-129">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="524c1-129">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="524c1-130">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="524c1-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





