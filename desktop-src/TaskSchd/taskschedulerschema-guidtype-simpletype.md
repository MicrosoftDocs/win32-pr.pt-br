---
title: tipo simples de guidtype (Agendador de Tarefas)
description: Define o padrão para GUIDs válidos.
ms.assetid: 1aa3f08b-4b3e-4e72-8ac4-d859a8da4c32
keywords:
- tipo simples de guidtype Agendador de Tarefas
topic_type:
- apiref
api_name:
- guidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 75b95d5b8ad7a4158dbe449fb28cf3324499488f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086120"
---
# <a name="guidtype-simple-type-task-scheduler"></a><span data-ttu-id="18a7e-104">tipo simples de guidtype (Agendador de Tarefas)</span><span class="sxs-lookup"><span data-stu-id="18a7e-104">guidType simple type (Task Scheduler)</span></span>

<span data-ttu-id="18a7e-105">Define o padrão para GUIDs válidos.</span><span class="sxs-lookup"><span data-stu-id="18a7e-105">Defines the pattern for valid GUIDs.</span></span>

``` syntax
<xs:simpleType name="guidType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\{([0-9a-fA-F]){8}(\-[0-9a-fA-F]{4}){3}\-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="18a7e-106">Padrões</span><span class="sxs-lookup"><span data-stu-id="18a7e-106">Patterns</span></span>

<span data-ttu-id="18a7e-107">O tipo simples **guidtype** é uma **cadeia de caracteres** que é restrita pelo seguinte padrão:</span><span class="sxs-lookup"><span data-stu-id="18a7e-107">The **guidType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `\{([0-9a-fA-F]){8}(\-[0-9a-fA-F]{4}){3}\-[0-9a-fA-F]{12}\}`

    <span data-ttu-id="18a7e-108">Um número de bits de 128 exclusivo.</span><span class="sxs-lookup"><span data-stu-id="18a7e-108">A unique 128-bit number.</span></span>

## <a name="requirements"></a><span data-ttu-id="18a7e-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18a7e-109">Requirements</span></span>



| <span data-ttu-id="18a7e-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="18a7e-110">Requirement</span></span> | <span data-ttu-id="18a7e-111">Valor</span><span class="sxs-lookup"><span data-stu-id="18a7e-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="18a7e-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18a7e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="18a7e-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="18a7e-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="18a7e-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18a7e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="18a7e-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="18a7e-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="18a7e-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="18a7e-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18a7e-117">Tipos simples de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="18a7e-117">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="18a7e-118">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="18a7e-118">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





