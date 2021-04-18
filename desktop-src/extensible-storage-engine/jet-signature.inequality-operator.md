---
description: 'Saiba mais sobre: JET_SIGNATURE. Operador de desigualdade'
title: JET_SIGNATURE. Operador de desigualdade
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SIGNATURE.op_Inequality(Microsoft.Isam.Esent.Interop.JET_SIGNATURE,Microsoft.Isam.Esent.Interop.JET_SIGNATURE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_signature.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39516073
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 646b97f37aea55ee3e9d1aa24e80b9d26ea82469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789002"
---
# <a name="jet_signatureinequality-operator"></a><span data-ttu-id="a1bb3-103">JET_SIGNATURE. Operador de desigualdade</span><span class="sxs-lookup"><span data-stu-id="a1bb3-103">JET_SIGNATURE.Inequality operator</span></span>

<span data-ttu-id="a1bb3-104">Determina se duas instâncias especificadas do JET_SIGNATURE não são iguais.</span><span class="sxs-lookup"><span data-stu-id="a1bb3-104">Determines whether two specified instances of JET_SIGNATURE are not equal.</span></span>

<span data-ttu-id="a1bb3-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a1bb3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a1bb3-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a1bb3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a1bb3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1bb3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_SIGNATURE, _
    rhs As JET_SIGNATURE _
) As Boolean
'Usage
Dim lhs As JET_SIGNATURE
Dim rhs As JET_SIGNATURE
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_SIGNATURE lhs,
    JET_SIGNATURE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="a1bb3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1bb3-108">Parameters</span></span>

  - <span data-ttu-id="a1bb3-109">lhs</span><span class="sxs-lookup"><span data-stu-id="a1bb3-109">lhs</span></span>  
    <span data-ttu-id="a1bb3-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="a1bb3-110">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="a1bb3-111">A primeira instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="a1bb3-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="a1bb3-112">rhs</span><span class="sxs-lookup"><span data-stu-id="a1bb3-112">rhs</span></span>  
    <span data-ttu-id="a1bb3-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="a1bb3-113">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="a1bb3-114">A segunda instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="a1bb3-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="a1bb3-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a1bb3-115">Return value</span></span>

<span data-ttu-id="a1bb3-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="a1bb3-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="a1bb3-117">True se as duas instâncias não forem iguais.</span><span class="sxs-lookup"><span data-stu-id="a1bb3-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a1bb3-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1bb3-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a1bb3-119">Referência</span><span class="sxs-lookup"><span data-stu-id="a1bb3-119">Reference</span></span>

[<span data-ttu-id="a1bb3-120">Estrutura de JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="a1bb3-120">JET_SIGNATURE structure</span></span>](./jet-signature-structure2.md)

[<span data-ttu-id="a1bb3-121">Membros do JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="a1bb3-121">JET_SIGNATURE members</span></span>](./jet-signature-members.md)

[<span data-ttu-id="a1bb3-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a1bb3-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
