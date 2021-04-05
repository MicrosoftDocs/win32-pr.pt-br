---
title: Tipo simples UInt32type (log de eventos do Windows)
description: Define um tipo inteiro sem sinal.
ms.assetid: 11e99c26-3be7-4fac-b3e1-97cb0428a886
keywords:
- Log de eventos de tipo simples UInt32type
topic_type:
- apiref
api_name:
- UInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f2a24326197c72b08032f5144fea1a69fbe68089
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918399"
---
# <a name="uint32type-simple-type-windows-event-log"></a><span data-ttu-id="fbc56-104">Tipo simples UInt32type (log de eventos do Windows)</span><span class="sxs-lookup"><span data-stu-id="fbc56-104">UInt32Type Simple Type (Windows Event Log)</span></span>

<span data-ttu-id="fbc56-105">Define um tipo inteiro sem sinal.</span><span class="sxs-lookup"><span data-stu-id="fbc56-105">Defines an unsigned integer type.</span></span> <span data-ttu-id="fbc56-106">O valor pode ser especificado como um inteiro de 4 bytes ou um valor hexadecimal no intervalo de 0 a 4.294.967.295.</span><span class="sxs-lookup"><span data-stu-id="fbc56-106">The value can be specified as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="unsignedInt HexInt32Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="fbc56-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbc56-107">Requirements</span></span>



| <span data-ttu-id="fbc56-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbc56-108">Requirement</span></span> | <span data-ttu-id="fbc56-109">Valor</span><span class="sxs-lookup"><span data-stu-id="fbc56-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fbc56-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbc56-110">Minimum supported client</span></span><br/> | <span data-ttu-id="fbc56-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fbc56-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fbc56-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbc56-112">Minimum supported server</span></span><br/> | <span data-ttu-id="fbc56-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fbc56-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





