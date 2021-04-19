---
title: Tipo simples de HexInt64Type (esquema de evento)
description: Define um tipo hexadecimal de 8 bytes. | Tipo simples de HexInt64Type (esquema de evento)
ms.assetid: b4d8f416-d9e3-4a07-9b08-6f634c0de06c
keywords:
- Log de eventos de tipo simples HexInt64Type
topic_type:
- apiref
api_name:
- HexInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e290c2326415664fbbae3feed9628b86452b10c6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105783653"
---
# <a name="hexint64type-simple-type-event-schema"></a><span data-ttu-id="c882e-105">Tipo simples de HexInt64Type (esquema de evento)</span><span class="sxs-lookup"><span data-stu-id="c882e-105">HexInt64Type Simple Type (Event Schema)</span></span>

<span data-ttu-id="c882e-106">Define um tipo hexadecimal de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="c882e-106">Defines an 8-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt64Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,16}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="c882e-107">Padrões</span><span class="sxs-lookup"><span data-stu-id="c882e-107">Patterns</span></span>

<span data-ttu-id="c882e-108">O tipo simples **HexInt64Type** é uma **cadeia de caracteres** que é restrita pelo seguinte padrão:</span><span class="sxs-lookup"><span data-stu-id="c882e-108">The **HexInt64Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,16}`

    <span data-ttu-id="c882e-109">O valor pode conter de um a dezesseis caracteres hexadecimais (por exemplo, 0xA ou 0xac7bd361004fe190).</span><span class="sxs-lookup"><span data-stu-id="c882e-109">The value can contain from one to sixteen hexadecimal characters (for example, 0xa or 0xac7bd361004fe190).</span></span>

## <a name="requirements"></a><span data-ttu-id="c882e-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c882e-110">Requirements</span></span>



| <span data-ttu-id="c882e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c882e-111">Requirement</span></span> | <span data-ttu-id="c882e-112">Valor</span><span class="sxs-lookup"><span data-stu-id="c882e-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c882e-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c882e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c882e-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c882e-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c882e-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c882e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c882e-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c882e-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





