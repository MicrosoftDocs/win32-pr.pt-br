---
title: Tipo simples de weektype
description: Define os valores que podem ser usados no elemento Week.
ms.assetid: 83a525ae-020b-4528-9e14-1e7d9df7b8c0
keywords:
- tipo simples de semanatype Agendador de Tarefas
topic_type:
- apiref
api_name:
- weekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6513efe0fe0ef4fcbf6b849627d09ec9da6feb82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085362"
---
# <a name="weektype-simple-type"></a><span data-ttu-id="4edd9-104">Tipo simples de weektype</span><span class="sxs-lookup"><span data-stu-id="4edd9-104">weekType Simple Type</span></span>

<span data-ttu-id="4edd9-105">Define os valores que podem ser usados no elemento [**Week**](taskschedulerschema-week-weekstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="4edd9-105">Defines the values that can be used in the [**Week**](taskschedulerschema-week-weekstype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="weekType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-4]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="4edd9-106">Padrões</span><span class="sxs-lookup"><span data-stu-id="4edd9-106">Patterns</span></span>

<span data-ttu-id="4edd9-107">O tipo simples **weektype** é uma **cadeia de caracteres** que é restrita pelo seguinte padrão:</span><span class="sxs-lookup"><span data-stu-id="4edd9-107">The **weekType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `[1-4]|Last`

    <span data-ttu-id="4edd9-108">Especifica o primeiro na quarta semana do mês (1-4) ou sempre na última semana do mês.</span><span class="sxs-lookup"><span data-stu-id="4edd9-108">Specifies the first through the fourth week of the month (1-4) or always the last week of the month.</span></span>

## <a name="requirements"></a><span data-ttu-id="4edd9-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4edd9-109">Requirements</span></span>



| <span data-ttu-id="4edd9-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="4edd9-110">Requirement</span></span> | <span data-ttu-id="4edd9-111">Valor</span><span class="sxs-lookup"><span data-stu-id="4edd9-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4edd9-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4edd9-112">Minimum supported client</span></span><br/> | <span data-ttu-id="4edd9-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4edd9-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4edd9-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4edd9-114">Minimum supported server</span></span><br/> | <span data-ttu-id="4edd9-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4edd9-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4edd9-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="4edd9-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4edd9-117">Tipos simples de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="4edd9-117">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="4edd9-118">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="4edd9-118">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





