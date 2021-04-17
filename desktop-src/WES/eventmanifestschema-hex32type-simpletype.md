---
title: Tipo simples de HexInt32Type (esquema EventManifest)
description: Define um tipo hexadecimal de 4 bytes. | Tipo simples de HexInt32Type (esquema EventManifest)
ms.assetid: b1006593-c6f2-4669-b242-758ce9977565
keywords:
- Log de eventos de tipo simples HexInt32Type
topic_type:
- apiref
api_name:
- HexInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4630bc4d7d513a0fedad2191c63ca71571ce655a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105813407"
---
# <a name="hexint32type-simple-type-eventmanifest-schema"></a><span data-ttu-id="2e3b9-105">Tipo simples de HexInt32Type (esquema EventManifest)</span><span class="sxs-lookup"><span data-stu-id="2e3b9-105">HexInt32Type Simple Type (EventManifest Schema)</span></span>

<span data-ttu-id="2e3b9-106">Define um tipo hexadecimal de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="2e3b9-106">Defines a 4-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="2e3b9-107">Padrões</span><span class="sxs-lookup"><span data-stu-id="2e3b9-107">Patterns</span></span>

<span data-ttu-id="2e3b9-108">O tipo simples **HexInt32Type** é uma **cadeia de caracteres** que é restrita pelo seguinte padrão:</span><span class="sxs-lookup"><span data-stu-id="2e3b9-108">The **HexInt32Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,8}`

    <span data-ttu-id="2e3b9-109">O valor pode conter de um a oito caracteres hexadecimais (por exemplo, 0xA ou 0xac7bd361).</span><span class="sxs-lookup"><span data-stu-id="2e3b9-109">The value can contain from one to eight hexadecimal characters (for example, 0xa or 0xac7bd361).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e3b9-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e3b9-110">Requirements</span></span>



| <span data-ttu-id="2e3b9-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e3b9-111">Requirement</span></span> | <span data-ttu-id="2e3b9-112">Valor</span><span class="sxs-lookup"><span data-stu-id="2e3b9-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2e3b9-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e3b9-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2e3b9-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e3b9-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2e3b9-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e3b9-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2e3b9-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2e3b9-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





