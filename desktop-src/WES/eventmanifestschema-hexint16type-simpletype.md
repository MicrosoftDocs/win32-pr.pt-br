---
title: Tipo simples de UInt16type
description: Define um tipo curto sem sinal.
ms.assetid: 2200bb14-8f38-43fd-aed3-2a6b3ac33ed5
keywords:
- Log de eventos de tipo simples UInt16type
topic_type:
- apiref
api_name:
- UInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e687f42a43a12266267a0531ce078e8c6b5d1031
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645082"
---
# <a name="uint16type-simple-type"></a><span data-ttu-id="6c30c-104">Tipo simples de UInt16type</span><span class="sxs-lookup"><span data-stu-id="6c30c-104">UInt16Type Simple Type</span></span>

<span data-ttu-id="6c30c-105">Define um tipo curto sem sinal.</span><span class="sxs-lookup"><span data-stu-id="6c30c-105">Defines an unsigned short type.</span></span> <span data-ttu-id="6c30c-106">O valor pode ser especificado como um inteiro de 2 bytes ou um valor hexadecimal no intervalo de 0 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="6c30c-106">The value can be specified as a 2-byte integer or hexadecimal value in the range from 0 through 65,535.</span></span>

``` syntax
<xs:simpleType name="UInt16Type">
    <xs:union
        memberValues="unsignedShort HexInt16Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="6c30c-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c30c-107">Requirements</span></span>



| <span data-ttu-id="6c30c-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c30c-108">Requirement</span></span> | <span data-ttu-id="6c30c-109">Valor</span><span class="sxs-lookup"><span data-stu-id="6c30c-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6c30c-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c30c-110">Minimum supported client</span></span><br/> | <span data-ttu-id="6c30c-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6c30c-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6c30c-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c30c-112">Minimum supported server</span></span><br/> | <span data-ttu-id="6c30c-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6c30c-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





