---
description: 'Saiba mais sobre: JET_COLUMNID. Operador GreaterThanOrEqual'
title: JET_COLUMNID. Operador GreaterThanOrEqual
TOCTitle: 'GreaterThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_GreaterThanOrEqual(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_greaterthanorequal(v=EXCHG.10)
ms:contentKeyID: 39509674
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.GreaterThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.GreaterThanOrEqual
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 344d1ed95ebc6a4a79d17f8b664f3f8a76740367
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790514"
---
# <a name="jet_columnidgreaterthanorequal-operator"></a><span data-ttu-id="33e39-103">JET_COLUMNID. Operador GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="33e39-103">JET_COLUMNID.GreaterThanOrEqual operator</span></span>

<span data-ttu-id="33e39-104">Determine se um columnid é posterior ou igual a outro columnid.</span><span class="sxs-lookup"><span data-stu-id="33e39-104">Determine whether one columnid is after or equal to another columnid.</span></span>

<span data-ttu-id="33e39-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="33e39-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="33e39-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="33e39-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="33e39-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33e39-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator >= ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs >= rhs)
```

``` csharp
public static bool operator >=(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="33e39-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33e39-108">Parameters</span></span>

  - <span data-ttu-id="33e39-109">lhs</span><span class="sxs-lookup"><span data-stu-id="33e39-109">lhs</span></span>  
    <span data-ttu-id="33e39-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="33e39-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="33e39-111">O primeiro columnid a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="33e39-111">The first columnid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="33e39-112">rhs</span><span class="sxs-lookup"><span data-stu-id="33e39-112">rhs</span></span>  
    <span data-ttu-id="33e39-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="33e39-113">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="33e39-114">O segundo columnid a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="33e39-114">The second columnid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="33e39-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33e39-115">Return value</span></span>

<span data-ttu-id="33e39-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="33e39-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="33e39-117">True se o LHS vier após ou for igual ao RHS.</span><span class="sxs-lookup"><span data-stu-id="33e39-117">True if lhs comes after or is equal to rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="33e39-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="33e39-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="33e39-119">Referência</span><span class="sxs-lookup"><span data-stu-id="33e39-119">Reference</span></span>

[<span data-ttu-id="33e39-120">Estrutura de JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="33e39-120">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="33e39-121">Membros do JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="33e39-121">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="33e39-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="33e39-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
