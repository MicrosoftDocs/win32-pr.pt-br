---
description: Define uma lista de estruturas que contêm valores de contadores.
ms.assetid: 6f6b33ed-6440-456c-8379-61a37798c95f
title: Tipo complexo de structs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c36de698d1e0eb136f17034e0740851fc751d157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783251"
---
# <a name="structs-complex-type"></a><span data-ttu-id="6e4c8-103">Tipo complexo de structs</span><span class="sxs-lookup"><span data-stu-id="6e4c8-103">structs Complex Type</span></span>

<span data-ttu-id="6e4c8-104">Define uma lista de estruturas que contêm valores de contadores.</span><span class="sxs-lookup"><span data-stu-id="6e4c8-104">Defines a list of structures that contain counter values.</span></span>

``` syntax
<xs:complexType name="structs">
    <xs:choice
        minOccurs="1"
        maxOccurs="unbounded"
    >
        <xs:element name="struct"
            type="man:struct"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="6e4c8-105">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6e4c8-105">Child elements</span></span>



| <span data-ttu-id="6e4c8-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="6e4c8-106">Element</span></span>    | <span data-ttu-id="6e4c8-107">Type</span><span class="sxs-lookup"><span data-stu-id="6e4c8-107">Type</span></span>                                                           | <span data-ttu-id="6e4c8-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6e4c8-108">Description</span></span>                                                      |
|------------|----------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="6e4c8-109">**struct**</span><span class="sxs-lookup"><span data-stu-id="6e4c8-109">**struct**</span></span> | [<span data-ttu-id="6e4c8-110">**homem: struct**</span><span class="sxs-lookup"><span data-stu-id="6e4c8-110">**man:struct**</span></span>](performance-counters-struct-complex-type.md) | <span data-ttu-id="6e4c8-111">O nome de uma estrutura que contém valores de contador.</span><span class="sxs-lookup"><span data-stu-id="6e4c8-111">The name of a structure that contains counter values.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="6e4c8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e4c8-112">Requirements</span></span>



| <span data-ttu-id="6e4c8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e4c8-113">Requirement</span></span> | <span data-ttu-id="6e4c8-114">Valor</span><span class="sxs-lookup"><span data-stu-id="6e4c8-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6e4c8-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e4c8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6e4c8-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6e4c8-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6e4c8-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e4c8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6e4c8-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6e4c8-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




