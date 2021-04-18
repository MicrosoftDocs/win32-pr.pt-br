---
description: 'Saiba mais sobre: JET_LGPOS. Operador de igualdade'
title: JET_LGPOS. Operador de igualdade
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.op_Equality(Microsoft.Isam.Esent.Interop.JET_LGPOS,Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.op_equality(v=EXCHG.10)
ms:contentKeyID: 39510144
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.Equality
- Microsoft.Isam.Esent.Interop.JET_LGPOS.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ffdde1ee34cb60761d55dd52f2145a6b9bdd0a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766564"
---
# <a name="jet_lgposequality-operator"></a><span data-ttu-id="4f846-103">JET_LGPOS. Operador de igualdade</span><span class="sxs-lookup"><span data-stu-id="4f846-103">JET_LGPOS.Equality operator</span></span>

<span data-ttu-id="4f846-104">Determina se duas instâncias especificadas do JET_LGPOS são iguais.</span><span class="sxs-lookup"><span data-stu-id="4f846-104">Determines whether two specified instances of JET_LGPOS are equal.</span></span>

<span data-ttu-id="4f846-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4f846-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4f846-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4f846-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4f846-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f846-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_LGPOS, _
    rhs As JET_LGPOS _
) As Boolean
'Usage
Dim lhs As JET_LGPOS
Dim rhs As JET_LGPOS
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_LGPOS lhs,
    JET_LGPOS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="4f846-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f846-108">Parameters</span></span>

  - <span data-ttu-id="4f846-109">lhs</span><span class="sxs-lookup"><span data-stu-id="4f846-109">lhs</span></span>  
    <span data-ttu-id="4f846-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="4f846-110">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="4f846-111">A primeira instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="4f846-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="4f846-112">rhs</span><span class="sxs-lookup"><span data-stu-id="4f846-112">rhs</span></span>  
    <span data-ttu-id="4f846-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="4f846-113">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="4f846-114">A segunda instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="4f846-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4f846-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4f846-115">Return value</span></span>

<span data-ttu-id="4f846-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="4f846-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="4f846-117">True se as duas instâncias forem iguais.</span><span class="sxs-lookup"><span data-stu-id="4f846-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4f846-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f846-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4f846-119">Referência</span><span class="sxs-lookup"><span data-stu-id="4f846-119">Reference</span></span>

[<span data-ttu-id="4f846-120">Estrutura de JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="4f846-120">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="4f846-121">Membros do JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="4f846-121">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="4f846-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4f846-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
