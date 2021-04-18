---
title: Tipo simples de UInt8Type
description: Define um tipo de byte não assinado.
ms.assetid: bda12d06-683f-4183-a84b-2bc3159c4eff
keywords:
- Log de eventos de tipo simples UInt8Type
topic_type:
- apiref
api_name:
- UInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3236d7416cbb199037813a8ae870d4f87718081
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770540"
---
# <a name="uint8type-simple-type"></a><span data-ttu-id="9b17d-104">Tipo simples de UInt8Type</span><span class="sxs-lookup"><span data-stu-id="9b17d-104">UInt8Type Simple Type</span></span>

<span data-ttu-id="9b17d-105">Define um tipo de byte não assinado.</span><span class="sxs-lookup"><span data-stu-id="9b17d-105">Defines an unsigned byte type.</span></span> <span data-ttu-id="9b17d-106">O valor pode ser especificado como um inteiro de 1 byte ou um valor hexadecimal no intervalo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="9b17d-106">The value can be specified as a 1-byte integer or hexadecimal value in the range from 0 through 255.</span></span>

``` syntax
<xs:simpleType name="UInt8Type">
    <xs:union
        memberValues="unsignedByte HexInt8Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="9b17d-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b17d-107">Requirements</span></span>



| <span data-ttu-id="9b17d-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b17d-108">Requirement</span></span> | <span data-ttu-id="9b17d-109">Valor</span><span class="sxs-lookup"><span data-stu-id="9b17d-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9b17d-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b17d-110">Minimum supported client</span></span><br/> | <span data-ttu-id="9b17d-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9b17d-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9b17d-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b17d-112">Minimum supported server</span></span><br/> | <span data-ttu-id="9b17d-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9b17d-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





