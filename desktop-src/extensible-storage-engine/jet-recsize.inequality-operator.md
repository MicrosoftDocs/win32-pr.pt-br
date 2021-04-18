---
description: 'Saiba mais sobre: JET_RECSIZE. Operador de desigualdade'
title: JET_RECSIZE. Operador de desigualdade (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Inequality(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39512584
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Inequality
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 724009d5f4e816a5613b2fb6344b0a5388dea819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793704"
---
# <a name="jet_recsizeinequality-operator"></a><span data-ttu-id="d78e0-103">JET_RECSIZE. Operador de desigualdade</span><span class="sxs-lookup"><span data-stu-id="d78e0-103">JET_RECSIZE.Inequality operator</span></span>

<span data-ttu-id="d78e0-104">Determina se duas instâncias especificadas do JET_RECSIZE não são iguais.</span><span class="sxs-lookup"><span data-stu-id="d78e0-104">Determines whether two specified instances of JET_RECSIZE are not equal.</span></span>

<span data-ttu-id="d78e0-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d78e0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="d78e0-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d78e0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d78e0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d78e0-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_RECSIZE, _
    rhs As JET_RECSIZE _
) As Boolean
'Usage
Dim lhs As JET_RECSIZE
Dim rhs As JET_RECSIZE
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_RECSIZE lhs,
    JET_RECSIZE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="d78e0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d78e0-108">Parameters</span></span>

  - <span data-ttu-id="d78e0-109">lhs</span><span class="sxs-lookup"><span data-stu-id="d78e0-109">lhs</span></span>  
    <span data-ttu-id="d78e0-110">Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="d78e0-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="d78e0-111">A primeira instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="d78e0-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="d78e0-112">rhs</span><span class="sxs-lookup"><span data-stu-id="d78e0-112">rhs</span></span>  
    <span data-ttu-id="d78e0-113">Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="d78e0-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="d78e0-114">A segunda instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="d78e0-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d78e0-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d78e0-115">Return value</span></span>

<span data-ttu-id="d78e0-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="d78e0-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="d78e0-117">True se as duas instâncias não forem iguais.</span><span class="sxs-lookup"><span data-stu-id="d78e0-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d78e0-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="d78e0-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d78e0-119">Referência</span><span class="sxs-lookup"><span data-stu-id="d78e0-119">Reference</span></span>

[<span data-ttu-id="d78e0-120">Estrutura de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="d78e0-120">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="d78e0-121">Membros do JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="d78e0-121">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="d78e0-122">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="d78e0-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
