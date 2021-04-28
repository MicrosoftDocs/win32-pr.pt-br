---
description: Tipo simples de UInt32type (contadores de desempenho) – define um tipo de inteiro sem sinal.
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: Tipo simples UInt32type (contadores de desempenho)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 32f8a4bbf00f569ba98dfc031f62717b1afc8734
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114574"
---
# <a name="uint32type-simple-type-performance-counters"></a><span data-ttu-id="3b091-103">Tipo simples UInt32type (contadores de desempenho)</span><span class="sxs-lookup"><span data-stu-id="3b091-103">UInt32Type Simple Type (Performance Counters)</span></span>

<span data-ttu-id="3b091-104">Define um tipo inteiro sem sinal.</span><span class="sxs-lookup"><span data-stu-id="3b091-104">Defines an unsigned integer type.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="xs:unsignedInt man:HexInt32Type"
     />
</xs:simpleType>
```

## <a name="remarks"></a><span data-ttu-id="3b091-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b091-105">Remarks</span></span>

<span data-ttu-id="3b091-106">Você pode especificar o valor como um inteiro de 4 bytes ou um valor hexadecimal no intervalo de 0 a 4.294.967.295.</span><span class="sxs-lookup"><span data-stu-id="3b091-106">You can specify the value as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b091-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b091-107">Requirements</span></span>



| <span data-ttu-id="3b091-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b091-108">Requirement</span></span> | <span data-ttu-id="3b091-109">Valor</span><span class="sxs-lookup"><span data-stu-id="3b091-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3b091-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b091-110">Minimum supported client</span></span><br/> | <span data-ttu-id="3b091-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3b091-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3b091-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b091-112">Minimum supported server</span></span><br/> | <span data-ttu-id="3b091-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3b091-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




