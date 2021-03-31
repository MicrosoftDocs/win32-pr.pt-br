---
description: 'Saiba mais sobre: JET_RECSIZE. Operador de igualdade'
title: JET_RECSIZE. Operador de igualdade (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Equality(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.op_equality(v=EXCHG.10)
ms:contentKeyID: 39515439
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Equality
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2f95ee6975a71e40d702b1f68c47ad6831881ffa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089896"
---
# <a name="jet_recsizeequality-operator"></a><span data-ttu-id="020f3-103">JET_RECSIZE. Operador de igualdade</span><span class="sxs-lookup"><span data-stu-id="020f3-103">JET_RECSIZE.Equality operator</span></span>

<span data-ttu-id="020f3-104">Determina se duas instâncias especificadas do JET_RECSIZE são iguais.</span><span class="sxs-lookup"><span data-stu-id="020f3-104">Determines whether two specified instances of JET_RECSIZE are equal.</span></span>

<span data-ttu-id="020f3-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="020f3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="020f3-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="020f3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="020f3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="020f3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_RECSIZE, _
    rhs As JET_RECSIZE _
) As Boolean
'Usage
Dim lhs As JET_RECSIZE
Dim rhs As JET_RECSIZE
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_RECSIZE lhs,
    JET_RECSIZE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="020f3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="020f3-108">Parameters</span></span>

  - <span data-ttu-id="020f3-109">lhs</span><span class="sxs-lookup"><span data-stu-id="020f3-109">lhs</span></span>  
    <span data-ttu-id="020f3-110">Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="020f3-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="020f3-111">A primeira instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="020f3-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="020f3-112">rhs</span><span class="sxs-lookup"><span data-stu-id="020f3-112">rhs</span></span>  
    <span data-ttu-id="020f3-113">Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="020f3-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="020f3-114">A segunda instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="020f3-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="020f3-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="020f3-115">Return value</span></span>

<span data-ttu-id="020f3-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="020f3-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="020f3-117">True se as duas instâncias forem iguais.</span><span class="sxs-lookup"><span data-stu-id="020f3-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="020f3-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="020f3-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="020f3-119">Referência</span><span class="sxs-lookup"><span data-stu-id="020f3-119">Reference</span></span>

[<span data-ttu-id="020f3-120">Estrutura de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="020f3-120">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="020f3-121">Membros do JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="020f3-121">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="020f3-122">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="020f3-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
