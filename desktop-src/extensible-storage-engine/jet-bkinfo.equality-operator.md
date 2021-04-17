---
description: 'Saiba mais sobre: JET_BKINFO. Operador de igualdade'
title: JET_BKINFO. Operador de igualdade
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKINFO.op_Equality(Microsoft.Isam.Esent.Interop.JET_BKINFO,Microsoft.Isam.Esent.Interop.JET_BKINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bkinfo.op_equality(v=EXCHG.10)
ms:contentKeyID: 39510688
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKINFO.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKINFO.op_Equality
- Microsoft.Isam.Esent.Interop.JET_BKINFO.Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a20cc09e55ce2bbb194561d4e371b81f9bcb2a6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811899"
---
# <a name="jet_bkinfoequality-operator"></a><span data-ttu-id="201d8-103">JET_BKINFO. Operador de igualdade</span><span class="sxs-lookup"><span data-stu-id="201d8-103">JET_BKINFO.Equality operator</span></span>

<span data-ttu-id="201d8-104">Determina se duas instâncias especificadas do JET_BKINFO são iguais.</span><span class="sxs-lookup"><span data-stu-id="201d8-104">Determines whether two specified instances of JET_BKINFO are equal.</span></span>

<span data-ttu-id="201d8-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="201d8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="201d8-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="201d8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="201d8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="201d8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_BKINFO, _
    rhs As JET_BKINFO _
) As Boolean
'Usage
Dim lhs As JET_BKINFO
Dim rhs As JET_BKINFO
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_BKINFO lhs,
    JET_BKINFO rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="201d8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="201d8-108">Parameters</span></span>

  - <span data-ttu-id="201d8-109">lhs</span><span class="sxs-lookup"><span data-stu-id="201d8-109">lhs</span></span>  
    <span data-ttu-id="201d8-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="201d8-110">Type: [Microsoft.Isam.Esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span></span>  
    
    <span data-ttu-id="201d8-111">A primeira instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="201d8-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="201d8-112">rhs</span><span class="sxs-lookup"><span data-stu-id="201d8-112">rhs</span></span>  
    <span data-ttu-id="201d8-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="201d8-113">Type: [Microsoft.Isam.Esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span></span>  
    
    <span data-ttu-id="201d8-114">A segunda instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="201d8-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="201d8-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="201d8-115">Return value</span></span>

<span data-ttu-id="201d8-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="201d8-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="201d8-117">True se as duas instâncias forem iguais.</span><span class="sxs-lookup"><span data-stu-id="201d8-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="201d8-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="201d8-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="201d8-119">Referência</span><span class="sxs-lookup"><span data-stu-id="201d8-119">Reference</span></span>

[<span data-ttu-id="201d8-120">Estrutura de JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="201d8-120">JET_BKINFO structure</span></span>](./jet-bkinfo-structure2.md)

[<span data-ttu-id="201d8-121">Membros do JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="201d8-121">JET_BKINFO members</span></span>](./jet-bkinfo-members.md)

[<span data-ttu-id="201d8-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="201d8-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
