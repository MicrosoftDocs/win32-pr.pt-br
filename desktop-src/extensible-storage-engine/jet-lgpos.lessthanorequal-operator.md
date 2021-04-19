---
description: 'Saiba mais sobre: JET_LGPOS. Operador LessThanOrEqual'
title: JET_LGPOS. Operador LessThanOrEqual
TOCTitle: 'LessThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.op_LessThanOrEqual(Microsoft.Isam.Esent.Interop.JET_LGPOS,Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.op_lessthanorequal(v=EXCHG.10)
ms:contentKeyID: 39510104
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.LessThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.JET_LGPOS.op_LessThanOrEqual
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57eb2f9383b218409ebee927cc4d6ad1283f3e8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770636"
---
# <a name="jet_lgposlessthanorequal-operator"></a><span data-ttu-id="00f8e-103">JET_LGPOS. Operador LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="00f8e-103">JET_LGPOS.LessThanOrEqual operator</span></span>

<span data-ttu-id="00f8e-104">Determine se uma posição de log é anterior ou igual a outra posição de log.</span><span class="sxs-lookup"><span data-stu-id="00f8e-104">Determine whether one log position is before or equal to another log position.</span></span>

<span data-ttu-id="00f8e-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="00f8e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="00f8e-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="00f8e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="00f8e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00f8e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <= ( _
    lhs As JET_LGPOS, _
    rhs As JET_LGPOS _
) As Boolean
'Usage
Dim lhs As JET_LGPOS
Dim rhs As JET_LGPOS
Dim returnValue As Boolean

returnValue = (lhs <= rhs)
```

``` csharp
public static bool operator <=(
    JET_LGPOS lhs,
    JET_LGPOS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="00f8e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00f8e-108">Parameters</span></span>

  - <span data-ttu-id="00f8e-109">lhs</span><span class="sxs-lookup"><span data-stu-id="00f8e-109">lhs</span></span>  
    <span data-ttu-id="00f8e-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="00f8e-110">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="00f8e-111">A primeira posição de log a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="00f8e-111">The first log position to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="00f8e-112">rhs</span><span class="sxs-lookup"><span data-stu-id="00f8e-112">rhs</span></span>  
    <span data-ttu-id="00f8e-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="00f8e-113">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="00f8e-114">A segunda posição de log para comparar.</span><span class="sxs-lookup"><span data-stu-id="00f8e-114">The second log position to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="00f8e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="00f8e-115">Return value</span></span>

<span data-ttu-id="00f8e-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="00f8e-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="00f8e-117">True se o LHS vier antes ou for igual ao RHS.</span><span class="sxs-lookup"><span data-stu-id="00f8e-117">True if lhs comes before or is equal to rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="00f8e-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="00f8e-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="00f8e-119">Referência</span><span class="sxs-lookup"><span data-stu-id="00f8e-119">Reference</span></span>

[<span data-ttu-id="00f8e-120">Estrutura de JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="00f8e-120">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="00f8e-121">Membros do JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="00f8e-121">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="00f8e-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="00f8e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
