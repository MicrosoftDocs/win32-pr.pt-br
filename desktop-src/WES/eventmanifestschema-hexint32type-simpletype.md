---
title: Tipo simples UInt32type (log de eventos do Windows)
description: Tipo simples de UInt32type (log de eventos do Windows) – define um tipo inteiro sem sinal.
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
ms.openlocfilehash: 631bb3e8424db8a5d781aaa43df6096730aaa4d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090564"
---
# <a name="uint32type-simple-type-windows-event-log"></a><span data-ttu-id="4c88c-104">Tipo simples UInt32type (log de eventos do Windows)</span><span class="sxs-lookup"><span data-stu-id="4c88c-104">UInt32Type Simple Type (Windows Event Log)</span></span>

<span data-ttu-id="4c88c-105">Define um tipo inteiro sem sinal.</span><span class="sxs-lookup"><span data-stu-id="4c88c-105">Defines an unsigned integer type.</span></span> <span data-ttu-id="4c88c-106">O valor pode ser especificado como um inteiro de 4 bytes ou um valor hexadecimal no intervalo de 0 a 4.294.967.295.</span><span class="sxs-lookup"><span data-stu-id="4c88c-106">The value can be specified as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="unsignedInt HexInt32Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="4c88c-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c88c-107">Requirements</span></span>



| <span data-ttu-id="4c88c-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c88c-108">Requirement</span></span> | <span data-ttu-id="4c88c-109">Valor</span><span class="sxs-lookup"><span data-stu-id="4c88c-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4c88c-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c88c-110">Minimum supported client</span></span><br/> | <span data-ttu-id="4c88c-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4c88c-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4c88c-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c88c-112">Minimum supported server</span></span><br/> | <span data-ttu-id="4c88c-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4c88c-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





