---
description: 'Saiba mais sobre: JET_LS. Operador de desigualdade'
title: JET_LS. Operador de desigualdade
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LS.op_Inequality(Microsoft.Isam.Esent.Interop.JET_LS,Microsoft.Isam.Esent.Interop.JET_LS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ls.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39512483
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LS.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LS.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_LS.Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: da167f0deda8254d279e7d81c7219b6e9920673f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011423"
---
# <a name="jet_lsinequality-operator"></a><span data-ttu-id="249f6-103">JET_LS. Operador de desigualdade</span><span class="sxs-lookup"><span data-stu-id="249f6-103">JET_LS.Inequality operator</span></span>

<span data-ttu-id="249f6-104">Determina se duas instâncias especificadas do JET_LS não são iguais.</span><span class="sxs-lookup"><span data-stu-id="249f6-104">Determines whether two specified instances of JET_LS are not equal.</span></span>

<span data-ttu-id="249f6-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="249f6-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="249f6-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="249f6-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="249f6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="249f6-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_LS, _
    rhs As JET_LS _
) As Boolean
'Usage
Dim lhs As JET_LS
Dim rhs As JET_LS
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_LS lhs,
    JET_LS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="249f6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="249f6-108">Parameters</span></span>

  - <span data-ttu-id="249f6-109">lhs</span><span class="sxs-lookup"><span data-stu-id="249f6-109">lhs</span></span>  
    <span data-ttu-id="249f6-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_LS](./jet-ls-structure.md)</span><span class="sxs-lookup"><span data-stu-id="249f6-110">Type: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span></span>  
    
    <span data-ttu-id="249f6-111">A primeira instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="249f6-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="249f6-112">rhs</span><span class="sxs-lookup"><span data-stu-id="249f6-112">rhs</span></span>  
    <span data-ttu-id="249f6-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_LS](./jet-ls-structure.md)</span><span class="sxs-lookup"><span data-stu-id="249f6-113">Type: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span></span>  
    
    <span data-ttu-id="249f6-114">A segunda instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="249f6-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="249f6-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="249f6-115">Return value</span></span>

<span data-ttu-id="249f6-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="249f6-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="249f6-117">True se as duas instâncias não forem iguais.</span><span class="sxs-lookup"><span data-stu-id="249f6-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="249f6-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="249f6-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="249f6-119">Referência</span><span class="sxs-lookup"><span data-stu-id="249f6-119">Reference</span></span>

[<span data-ttu-id="249f6-120">Estrutura de JET_LS</span><span class="sxs-lookup"><span data-stu-id="249f6-120">JET_LS structure</span></span>](./jet-ls-structure.md)

[<span data-ttu-id="249f6-121">Membros do JET_LS</span><span class="sxs-lookup"><span data-stu-id="249f6-121">JET_LS members</span></span>](./jet-ls-members.md)

[<span data-ttu-id="249f6-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="249f6-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
