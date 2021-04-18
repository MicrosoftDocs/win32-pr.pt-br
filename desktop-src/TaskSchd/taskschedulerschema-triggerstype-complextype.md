---
title: Tipo complexo TriggerType
description: Define o grupo (Trigger) para todos os elementos de gatilho.
ms.assetid: ceabc332-e028-491e-8fd8-c02ac23a2635
keywords:
- tipo complexo de TriggerType Agendador de Tarefas
topic_type:
- apiref
api_name:
- triggersType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9903fdc292fe832cc6931d794a4c1f39fd91f83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789442"
---
# <a name="triggerstype-complex-type"></a><span data-ttu-id="97886-104">Tipo complexo TriggerType</span><span class="sxs-lookup"><span data-stu-id="97886-104">triggersType Complex Type</span></span>

<span data-ttu-id="97886-105">Define o grupo ([**Trigger**](taskschedulerschema-triggergroup-group.md)) para todos os elementos de gatilho.</span><span class="sxs-lookup"><span data-stu-id="97886-105">Defines the group ([**triggerGroup**](taskschedulerschema-triggergroup-group.md)) for all trigger elements.</span></span> <span data-ttu-id="97886-106">O grupo de [**disparadores**](taskschedulerschema-triggergroup-group.md) contém a lista de gatilhos que podem ser usados em uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="97886-106">The [**triggerGroup**](taskschedulerschema-triggergroup-group.md) group contains the list of triggers that can be used in a task.</span></span>

``` syntax
<xs:complexType name="triggersType">
    <xs:group
        minOccurs="0"
        maxOccurs="48"
        ref="triggerGroup"
     />
</xs:complexType>
```

## <a name="requirements"></a><span data-ttu-id="97886-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97886-107">Requirements</span></span>



| <span data-ttu-id="97886-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="97886-108">Requirement</span></span> | <span data-ttu-id="97886-109">Valor</span><span class="sxs-lookup"><span data-stu-id="97886-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="97886-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97886-110">Minimum supported client</span></span><br/> | <span data-ttu-id="97886-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="97886-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="97886-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97886-112">Minimum supported server</span></span><br/> | <span data-ttu-id="97886-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="97886-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="97886-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="97886-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97886-115">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="97886-115">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





