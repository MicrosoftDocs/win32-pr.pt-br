---
title: Tipo simples de GUIDtype (esquema EventManifest)
description: Define um tipo de identificador global exclusivo, no formato de registro. | Tipo simples de GUIDtype (esquema EventManifest)
ms.assetid: c35fa54b-5a2e-46de-a1c7-fc408b00ee68
keywords:
- Tipo de log de tipos simples GUIDtype
topic_type:
- apiref
api_name:
- GUIDType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 474715cf4e9c11536ca227ecdb5609b13be7e222
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105763756"
---
# <a name="guidtype-simple-type-eventmanifest-schema"></a><span data-ttu-id="a9d00-105">Tipo simples de GUIDtype (esquema EventManifest)</span><span class="sxs-lookup"><span data-stu-id="a9d00-105">GUIDType Simple Type (EventManifest Schema)</span></span>

<span data-ttu-id="a9d00-106">Define um tipo de identificador global exclusivo, no formato de registro.</span><span class="sxs-lookup"><span data-stu-id="a9d00-106">Defines a globally unique identifier type, in Registry format.</span></span>

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="a9d00-107">Padrões</span><span class="sxs-lookup"><span data-stu-id="a9d00-107">Patterns</span></span>

<span data-ttu-id="a9d00-108">O tipo simples **guidtype** é uma cadeia de caracteres que é restrita pelo seguinte padrão:</span><span class="sxs-lookup"><span data-stu-id="a9d00-108">The **GUIDType** simple type is a string that is restricted by the following pattern:</span></span>

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    <span data-ttu-id="a9d00-109">O valor deve ser um tipo de identificador globalmente exclusivo no formato do registro.</span><span class="sxs-lookup"><span data-stu-id="a9d00-109">The value must be a globally unique identifier type in Registry format.</span></span> <span data-ttu-id="a9d00-110">Por exemplo, {5b2fc63a-8af4-44cb-960C-aefdced908d6}.</span><span class="sxs-lookup"><span data-stu-id="a9d00-110">For example, {5b2fc63a-8af4-44cb-960c-aefdced908d6}.</span></span> <span data-ttu-id="a9d00-111">Use GUIDGen.exe ou UUIDGen.exe para criar um GUID.</span><span class="sxs-lookup"><span data-stu-id="a9d00-111">Use GUIDGen.exe or UUIDGen.exe to create a GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9d00-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9d00-112">Requirements</span></span>



| <span data-ttu-id="a9d00-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9d00-113">Requirement</span></span> | <span data-ttu-id="a9d00-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a9d00-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a9d00-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9d00-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a9d00-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a9d00-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a9d00-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9d00-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a9d00-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a9d00-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





