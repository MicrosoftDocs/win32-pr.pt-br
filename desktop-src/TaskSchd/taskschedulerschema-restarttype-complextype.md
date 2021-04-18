---
title: Tipo complexo Restart
description: Define os elementos filho e as informações de sequência para o elemento RestartOnFailure.
ms.assetid: 3a192955-8a33-42b9-a974-faa9a3789f58
keywords:
- Restart tipo complexo Agendador de Tarefas
topic_type:
- apiref
api_name:
- restartType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f83dcac376fcdd8d2059649350502111f5a732f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499818"
---
# <a name="restarttype-complex-type"></a><span data-ttu-id="05c5f-104">Tipo complexo Restart</span><span class="sxs-lookup"><span data-stu-id="05c5f-104">restartType Complex Type</span></span>

<span data-ttu-id="05c5f-105">Define os elementos filho e as informações de sequência para o elemento [RestartOnFailure](taskschedulerschema-restartonfailure-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="05c5f-105">Defines the child elements and sequence information for the [RestartOnFailure](taskschedulerschema-restartonfailure-settingstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="restartType">
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
        <xs:element name="Count">
            <xs:simpleType>
                <xs:restriction
                    base="unsignedByte"
                >
                    <xs:minInclusive
                        value="1"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="05c5f-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="05c5f-106">Child elements</span></span>



| <span data-ttu-id="05c5f-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="05c5f-107">Element</span></span>                                                              | <span data-ttu-id="05c5f-108">Type</span><span class="sxs-lookup"><span data-stu-id="05c5f-108">Type</span></span> | <span data-ttu-id="05c5f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="05c5f-109">Description</span></span>                                        |
|----------------------------------------------------------------------|------|----------------------------------------------------|
| [<span data-ttu-id="05c5f-110">**Contar**</span><span class="sxs-lookup"><span data-stu-id="05c5f-110">**Count**</span></span>](taskschedulerschema-count-restarttype-element.md)       |      | <span data-ttu-id="05c5f-111">Número de tentativas para reiniciar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="05c5f-111">Number of attempts to restart the task.</span></span><br/> |
| [<span data-ttu-id="05c5f-112">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="05c5f-112">**Interval**</span></span>](taskschedulerschema-interval-restarttype-element.md) |      | <span data-ttu-id="05c5f-113">Por quanto tempo tentar iniciar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="05c5f-113">How long to try to start the task.</span></span><br/>      |



## <a name="requirements"></a><span data-ttu-id="05c5f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05c5f-114">Requirements</span></span>



| <span data-ttu-id="05c5f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="05c5f-115">Requirement</span></span> | <span data-ttu-id="05c5f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="05c5f-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="05c5f-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05c5f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="05c5f-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="05c5f-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="05c5f-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05c5f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="05c5f-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="05c5f-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="05c5f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="05c5f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05c5f-122">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="05c5f-122">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="05c5f-123">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="05c5f-123">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





