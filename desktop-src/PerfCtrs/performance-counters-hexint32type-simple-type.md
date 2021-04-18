---
description: Define um tipo hexadecimal de 4 bytes.
ms.assetid: d0e538c1-f22e-4905-ba73-b670fa7eb174
title: Tipo simples de HexInt32Type (contadores de desempenho)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d2392f2240ca9ca61525b27993e16bcab979a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766839"
---
# <a name="hexint32type-simple-type-performance-counters"></a><span data-ttu-id="e4759-103">Tipo simples de HexInt32Type (contadores de desempenho)</span><span class="sxs-lookup"><span data-stu-id="e4759-103">HexInt32Type Simple Type (Performance Counters)</span></span>

<span data-ttu-id="e4759-104">Define um tipo hexadecimal de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="e4759-104">Defines a 4-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="e4759-105">Padrões</span><span class="sxs-lookup"><span data-stu-id="e4759-105">Patterns</span></span>

<span data-ttu-id="e4759-106">O tipo simples **HexInt32Type** é um **xs: String** que é restrito pelo seguinte padrão:</span><span class="sxs-lookup"><span data-stu-id="e4759-106">The **HexInt32Type** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,8}`

    <span data-ttu-id="e4759-107">O valor pode conter de um a oito caracteres hexadecimais (por exemplo, 0xA ou 0xac7bd361).</span><span class="sxs-lookup"><span data-stu-id="e4759-107">The value can contain from one to eight hexadecimal characters (for example, 0xa or 0xac7bd361).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4759-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4759-108">Requirements</span></span>



| <span data-ttu-id="e4759-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4759-109">Requirement</span></span> | <span data-ttu-id="e4759-110">Valor</span><span class="sxs-lookup"><span data-stu-id="e4759-110">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e4759-111">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4759-111">Minimum supported client</span></span><br/> | <span data-ttu-id="e4759-112">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e4759-112">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e4759-113">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4759-113">Minimum supported server</span></span><br/> | <span data-ttu-id="e4759-114">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e4759-114">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




