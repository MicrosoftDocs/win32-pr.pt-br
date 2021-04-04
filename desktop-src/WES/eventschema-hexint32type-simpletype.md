---
title: Tipo simples de HexInt32Type (esquema de evento)
description: Define um tipo hexadecimal de 4 bytes. | Tipo simples de HexInt32Type (esquema de evento)
ms.assetid: f4b5226d-2a5e-4756-b4c5-30cfbf13568e
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
ms.openlocfilehash: 5c9bd7a11d0e648cc451ec837f0f8711ca334d59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930364"
---
# <a name="hexint32type-simple-type-event-schema"></a><span data-ttu-id="f5b49-105">Tipo simples de HexInt32Type (esquema de evento)</span><span class="sxs-lookup"><span data-stu-id="f5b49-105">HexInt32Type Simple Type (Event Schema)</span></span>

<span data-ttu-id="f5b49-106">Define um tipo hexadecimal de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="f5b49-106">Defines a 4-byte hexadecimal type.</span></span>

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

## <a name="patterns"></a><span data-ttu-id="f5b49-107">Padrões</span><span class="sxs-lookup"><span data-stu-id="f5b49-107">Patterns</span></span>

<span data-ttu-id="f5b49-108">O tipo simples **HexInt32Type** é uma **cadeia de caracteres** que é restrita pelo seguinte padrão:</span><span class="sxs-lookup"><span data-stu-id="f5b49-108">The **HexInt32Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,8}`

    <span data-ttu-id="f5b49-109">O valor pode conter de um a oito caracteres hexadecimais (por exemplo, 0xA ou 0xac7bd361).</span><span class="sxs-lookup"><span data-stu-id="f5b49-109">The value can contain from one to eight hexadecimal characters (for example, 0xa or 0xac7bd361).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5b49-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5b49-110">Requirements</span></span>



| <span data-ttu-id="f5b49-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5b49-111">Requirement</span></span> | <span data-ttu-id="f5b49-112">Valor</span><span class="sxs-lookup"><span data-stu-id="f5b49-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f5b49-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5b49-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f5b49-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f5b49-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f5b49-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5b49-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f5b49-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f5b49-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





