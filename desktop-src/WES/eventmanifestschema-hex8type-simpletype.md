---
title: Tipo simples de HexInt8Type
description: Define um tipo hexadecimal de 1 byte.
ms.assetid: 390acf84-7b5c-45e7-83bd-9f3115099568
keywords:
- Log de eventos de tipo simples HexInt8Type
topic_type:
- apiref
api_name:
- HexInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e68e56340ee535531fb6711dcf01a72d92665cbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455975"
---
# <a name="hexint8type-simple-type"></a><span data-ttu-id="7cb3e-104">Tipo simples de HexInt8Type</span><span class="sxs-lookup"><span data-stu-id="7cb3e-104">HexInt8Type Simple Type</span></span>

<span data-ttu-id="7cb3e-105">Define um tipo hexadecimal de 1 byte.</span><span class="sxs-lookup"><span data-stu-id="7cb3e-105">Defines a 1-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt8Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,2}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="7cb3e-106">Padrões</span><span class="sxs-lookup"><span data-stu-id="7cb3e-106">Patterns</span></span>

<span data-ttu-id="7cb3e-107">O tipo simples **HexInt8Type** é uma [cadeia de caracteres](/dotnet/api/system.string) que é restrita pelo seguinte padrão:</span><span class="sxs-lookup"><span data-stu-id="7cb3e-107">The **HexInt8Type** simple type is a [string](/dotnet/api/system.string) that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,2}`

    <span data-ttu-id="7cb3e-108">O valor pode conter de um a dois caracteres hexadecimais (por exemplo, 0xA ou 0xAC).</span><span class="sxs-lookup"><span data-stu-id="7cb3e-108">The value can contain from one to two hexadecimal characters (for example, 0xa or 0xac).</span></span>

## <a name="requirements"></a><span data-ttu-id="7cb3e-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cb3e-109">Requirements</span></span>



| <span data-ttu-id="7cb3e-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cb3e-110">Requirement</span></span> | <span data-ttu-id="7cb3e-111">Valor</span><span class="sxs-lookup"><span data-stu-id="7cb3e-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7cb3e-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cb3e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="7cb3e-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7cb3e-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7cb3e-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cb3e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="7cb3e-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7cb3e-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

