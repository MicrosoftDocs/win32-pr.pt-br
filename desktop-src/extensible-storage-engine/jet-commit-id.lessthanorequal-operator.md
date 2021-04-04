---
description: 'Saiba mais sobre: operador JET_COMMIT_ID. LessThanOrEqual'
title: Operador JET_COMMIT_ID. LessThanOrEqual (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'LessThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_LessThanOrEqual(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.op_lessthanorequal(v=EXCHG.10)
ms:contentKeyID: 55104413
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.LessThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_LessThanOrEqual
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 872ded299fc36295ea56500605f23af37feb0962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662636"
---
# <a name="jet_commit_idlessthanorequal-operator"></a><span data-ttu-id="cb10e-103">Operador JET_COMMIT_ID. LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="cb10e-103">JET_COMMIT_ID.LessThanOrEqual operator</span></span>

<span data-ttu-id="cb10e-104">Determine se uma commitid é anterior a outra commitid.</span><span class="sxs-lookup"><span data-stu-id="cb10e-104">Determine whether one commitid is before another commitid.</span></span>

<span data-ttu-id="cb10e-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cb10e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="cb10e-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cb10e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cb10e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cb10e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <= ( _
    lhs As JET_COMMIT_ID, _
    rhs As JET_COMMIT_ID _
) As Boolean
'Usage
Dim lhs As JET_COMMIT_ID
Dim rhs As JET_COMMIT_ID
Dim returnValue As Boolean

returnValue = (lhs <= rhs)
```

``` csharp
public static bool operator <=(
    JET_COMMIT_ID lhs,
    JET_COMMIT_ID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="cb10e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cb10e-108">Parameters</span></span>

  - <span data-ttu-id="cb10e-109">lhs</span><span class="sxs-lookup"><span data-stu-id="cb10e-109">lhs</span></span>  
    <span data-ttu-id="cb10e-110">Tipo: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="cb10e-110">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="cb10e-111">A primeira confirmação de comparação a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="cb10e-111">The first commitid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="cb10e-112">rhs</span><span class="sxs-lookup"><span data-stu-id="cb10e-112">rhs</span></span>  
    <span data-ttu-id="cb10e-113">Tipo: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="cb10e-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="cb10e-114">A segunda confirmação de comparação a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="cb10e-114">The second commitid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="cb10e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cb10e-115">Return value</span></span>

<span data-ttu-id="cb10e-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="cb10e-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="cb10e-117">True se o LHS vier antes ou igual ao RHS.</span><span class="sxs-lookup"><span data-stu-id="cb10e-117">True if lhs comes before or equal to rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cb10e-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb10e-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cb10e-119">Referência</span><span class="sxs-lookup"><span data-stu-id="cb10e-119">Reference</span></span>

[<span data-ttu-id="cb10e-120">Classe JET_COMMIT_ID</span><span class="sxs-lookup"><span data-stu-id="cb10e-120">JET_COMMIT_ID class</span></span>](./jet-commit-id-class.md)

[<span data-ttu-id="cb10e-121">Membros do JET_COMMIT_ID</span><span class="sxs-lookup"><span data-stu-id="cb10e-121">JET_COMMIT_ID members</span></span>](./jet-commit-id-members.md)

[<span data-ttu-id="cb10e-122">Namespace Microsoft. ISAM. ESENT. Interop. windows8</span><span class="sxs-lookup"><span data-stu-id="cb10e-122">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
