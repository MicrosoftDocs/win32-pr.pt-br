---
title: Tipo simples prioritytype
description: Define os valores mínimo e máximo para o elemento de prioridade (settingstype).
ms.assetid: 44e97d78-f035-4db9-a557-f24960518628
keywords:
- tipo simples de prioritytype Agendador de Tarefas
topic_type:
- apiref
api_name:
- priorityType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05b3c6d04adf557242438c813dab4f10d48cdb9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009611"
---
# <a name="prioritytype-simple-type"></a><span data-ttu-id="cf288-104">Tipo simples prioritytype</span><span class="sxs-lookup"><span data-stu-id="cf288-104">priorityType Simple Type</span></span>

<span data-ttu-id="cf288-105">Define os valores mínimo e máximo para o elemento de [**prioridade (settingstype)**](taskschedulerschema-priority-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="cf288-105">Defines the minimum and maximum values for the [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="priorityType">
    <xs:restriction
        base="byte"
    >
        <xs:enumeration
            value="0"
         />
        <xs:enumeration
            value="10"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="cf288-106">Valores de enumeração</span><span class="sxs-lookup"><span data-stu-id="cf288-106">Enumeration values</span></span>

<span data-ttu-id="cf288-107">O tipo simples **prioritytype** define os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="cf288-107">The **priorityType** simple type defines the following values.</span></span>



| <span data-ttu-id="cf288-108">Valor</span><span class="sxs-lookup"><span data-stu-id="cf288-108">Value</span></span> | <span data-ttu-id="cf288-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf288-109">Description</span></span>                         |
|-------|-------------------------------------|
| <span data-ttu-id="cf288-110">0</span><span class="sxs-lookup"><span data-stu-id="cf288-110">0</span></span>     | <span data-ttu-id="cf288-111">Inteiro mínimo permitido.</span><span class="sxs-lookup"><span data-stu-id="cf288-111">Minimum integer allowed.</span></span><br/> |
| <span data-ttu-id="cf288-112">10</span><span class="sxs-lookup"><span data-stu-id="cf288-112">10</span></span>    | <span data-ttu-id="cf288-113">Inteiro máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="cf288-113">Maximum integer allowed.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="cf288-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf288-114">Requirements</span></span>



| <span data-ttu-id="cf288-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf288-115">Requirement</span></span> | <span data-ttu-id="cf288-116">Valor</span><span class="sxs-lookup"><span data-stu-id="cf288-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cf288-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf288-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cf288-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cf288-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cf288-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf288-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cf288-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cf288-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cf288-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf288-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf288-122">Tipos simples de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="cf288-122">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="cf288-123">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="cf288-123">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





