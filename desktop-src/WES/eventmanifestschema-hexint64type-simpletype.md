---
title: Tipo simples de UInt64type (esquema EventManifest)
description: Define um tipo longo sem sinal.
ms.assetid: 6f69dbde-8292-4f8e-bf49-3ef41ea7315e
keywords:
- Log de eventos de tipo simples de UInt64type
topic_type:
- apiref
api_name:
- UInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b375a8e452760f9e59bae9cae8449889483d9b4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009322"
---
# <a name="uint64type-simple-type"></a><span data-ttu-id="8013c-104">Tipo simples de UInt64type</span><span class="sxs-lookup"><span data-stu-id="8013c-104">UInt64Type Simple Type</span></span>

<span data-ttu-id="8013c-105">Define um tipo longo sem sinal.</span><span class="sxs-lookup"><span data-stu-id="8013c-105">Defines an unsigned long type.</span></span> <span data-ttu-id="8013c-106">O valor pode ser especificado como um inteiro de 8 bytes ou um valor hexadecimal no intervalo de 0 a 18446744073709551615.</span><span class="sxs-lookup"><span data-stu-id="8013c-106">The value can be specified as an 8-byte integer or hexadecimal value in the range from 0 through 18,446,744,073,709,551,615.</span></span>

``` syntax
<xs:simpleType name="UInt64Type">
    <xs:union
        memberValues="unsignedLong HexInt64Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="8013c-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8013c-107">Requirements</span></span>



| <span data-ttu-id="8013c-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="8013c-108">Requirement</span></span> | <span data-ttu-id="8013c-109">Valor</span><span class="sxs-lookup"><span data-stu-id="8013c-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8013c-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8013c-110">Minimum supported client</span></span><br/> | <span data-ttu-id="8013c-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8013c-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8013c-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8013c-112">Minimum supported server</span></span><br/> | <span data-ttu-id="8013c-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8013c-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





