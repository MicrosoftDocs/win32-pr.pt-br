---
title: Tipo simples de HexInt16Type
description: Define um tipo hexadecimal de 2 bytes.
ms.assetid: d33d24e7-d260-49ea-a8ba-187b9b7a3a9c
keywords:
- Log de eventos de tipo simples HexInt16Type
topic_type:
- apiref
api_name:
- HexInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6aaa5021fbc5a7de5c16083c0f7744bc4a154c50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455795"
---
# <a name="hexint16type-simple-type"></a><span data-ttu-id="837fe-104">Tipo simples de HexInt16Type</span><span class="sxs-lookup"><span data-stu-id="837fe-104">HexInt16Type Simple Type</span></span>

<span data-ttu-id="837fe-105">Define um tipo hexadecimal de 2 bytes.</span><span class="sxs-lookup"><span data-stu-id="837fe-105">Defines a 2-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt16Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,4}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="837fe-106">Padrões</span><span class="sxs-lookup"><span data-stu-id="837fe-106">Patterns</span></span>

<span data-ttu-id="837fe-107">O tipo simples **HexInt16Type** é uma **cadeia de caracteres** que é restrita pelo seguinte padrão:</span><span class="sxs-lookup"><span data-stu-id="837fe-107">The **HexInt16Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,4}`

    <span data-ttu-id="837fe-108">O valor pode conter de um a quatro caracteres hexadecimais (por exemplo, 0xA ou 0xac7b).</span><span class="sxs-lookup"><span data-stu-id="837fe-108">The value can contain from one to four hexadecimal characters (for example, 0xa or 0xac7b).</span></span>

## <a name="requirements"></a><span data-ttu-id="837fe-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="837fe-109">Requirements</span></span>



| <span data-ttu-id="837fe-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="837fe-110">Requirement</span></span> | <span data-ttu-id="837fe-111">Valor</span><span class="sxs-lookup"><span data-stu-id="837fe-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="837fe-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="837fe-112">Minimum supported client</span></span><br/> | <span data-ttu-id="837fe-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="837fe-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="837fe-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="837fe-114">Minimum supported server</span></span><br/> | <span data-ttu-id="837fe-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="837fe-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





