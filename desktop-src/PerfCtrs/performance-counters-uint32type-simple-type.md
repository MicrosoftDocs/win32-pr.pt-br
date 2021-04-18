---
description: Define um tipo inteiro sem sinal.
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: Tipo simples UInt32type (contadores de desempenho)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4c32901167bcf181e5400ddb1d3b91ed7383965c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769298"
---
# <a name="uint32type-simple-type-performance-counters"></a><span data-ttu-id="01a6e-103">Tipo simples UInt32type (contadores de desempenho)</span><span class="sxs-lookup"><span data-stu-id="01a6e-103">UInt32Type Simple Type (Performance Counters)</span></span>

<span data-ttu-id="01a6e-104">Define um tipo inteiro sem sinal.</span><span class="sxs-lookup"><span data-stu-id="01a6e-104">Defines an unsigned integer type.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="xs:unsignedInt man:HexInt32Type"
     />
</xs:simpleType>
```

## <a name="remarks"></a><span data-ttu-id="01a6e-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="01a6e-105">Remarks</span></span>

<span data-ttu-id="01a6e-106">Você pode especificar o valor como um inteiro de 4 bytes ou um valor hexadecimal no intervalo de 0 a 4.294.967.295.</span><span class="sxs-lookup"><span data-stu-id="01a6e-106">You can specify the value as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

## <a name="requirements"></a><span data-ttu-id="01a6e-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01a6e-107">Requirements</span></span>



| <span data-ttu-id="01a6e-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="01a6e-108">Requirement</span></span> | <span data-ttu-id="01a6e-109">Valor</span><span class="sxs-lookup"><span data-stu-id="01a6e-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="01a6e-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01a6e-110">Minimum supported client</span></span><br/> | <span data-ttu-id="01a6e-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01a6e-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="01a6e-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01a6e-112">Minimum supported server</span></span><br/> | <span data-ttu-id="01a6e-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="01a6e-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




