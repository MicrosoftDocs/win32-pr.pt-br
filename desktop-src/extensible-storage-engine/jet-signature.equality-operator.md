---
description: 'Saiba mais sobre: JET_SIGNATURE. Operador de igualdade'
title: JET_SIGNATURE. Operador de igualdade
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SIGNATURE.op_Equality(Microsoft.Isam.Esent.Interop.JET_SIGNATURE,Microsoft.Isam.Esent.Interop.JET_SIGNATURE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_signature.op_equality(v=EXCHG.10)
ms:contentKeyID: 39512803
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.op_Equality
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 011510343f79724c2c529c2b6b18537b43facbef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647391"
---
# <a name="jet_signatureequality-operator"></a><span data-ttu-id="7f6da-103">JET_SIGNATURE. Operador de igualdade</span><span class="sxs-lookup"><span data-stu-id="7f6da-103">JET_SIGNATURE.Equality operator</span></span>

<span data-ttu-id="7f6da-104">Determina se duas instâncias especificadas do JET_SIGNATURE são iguais.</span><span class="sxs-lookup"><span data-stu-id="7f6da-104">Determines whether two specified instances of JET_SIGNATURE are equal.</span></span>

<span data-ttu-id="7f6da-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7f6da-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7f6da-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7f6da-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7f6da-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f6da-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_SIGNATURE, _
    rhs As JET_SIGNATURE _
) As Boolean
'Usage
Dim lhs As JET_SIGNATURE
Dim rhs As JET_SIGNATURE
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_SIGNATURE lhs,
    JET_SIGNATURE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="7f6da-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f6da-108">Parameters</span></span>

  - <span data-ttu-id="7f6da-109">lhs</span><span class="sxs-lookup"><span data-stu-id="7f6da-109">lhs</span></span>  
    <span data-ttu-id="7f6da-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="7f6da-110">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="7f6da-111">A primeira instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="7f6da-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="7f6da-112">rhs</span><span class="sxs-lookup"><span data-stu-id="7f6da-112">rhs</span></span>  
    <span data-ttu-id="7f6da-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="7f6da-113">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="7f6da-114">A segunda instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="7f6da-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7f6da-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7f6da-115">Return value</span></span>

<span data-ttu-id="7f6da-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="7f6da-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="7f6da-117">True se as duas instâncias forem iguais.</span><span class="sxs-lookup"><span data-stu-id="7f6da-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7f6da-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f6da-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7f6da-119">Referência</span><span class="sxs-lookup"><span data-stu-id="7f6da-119">Reference</span></span>

[<span data-ttu-id="7f6da-120">Estrutura de JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="7f6da-120">JET_SIGNATURE structure</span></span>](./jet-signature-structure2.md)

[<span data-ttu-id="7f6da-121">Membros do JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="7f6da-121">JET_SIGNATURE members</span></span>](./jet-signature-members.md)

[<span data-ttu-id="7f6da-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7f6da-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
