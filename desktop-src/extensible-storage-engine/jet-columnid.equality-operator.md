---
description: 'Saiba mais sobre: JET_COLUMNID. Operador de igualdade'
title: JET_COLUMNID. Operador de igualdade
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_Equality(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_equality(v=EXCHG.10)
ms:contentKeyID: 39514850
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.Equality
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 79d6d376d9a574587e5e3fc5329a7c092da73a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297417"
---
# <a name="jet_columnidequality-operator"></a><span data-ttu-id="43d95-103">JET_COLUMNID. Operador de igualdade</span><span class="sxs-lookup"><span data-stu-id="43d95-103">JET_COLUMNID.Equality operator</span></span>

<span data-ttu-id="43d95-104">Determina se duas instâncias especificadas do JET_COLUMNID são iguais.</span><span class="sxs-lookup"><span data-stu-id="43d95-104">Determines whether two specified instances of JET_COLUMNID are equal.</span></span>

<span data-ttu-id="43d95-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="43d95-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="43d95-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="43d95-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="43d95-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43d95-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="43d95-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43d95-108">Parameters</span></span>

  - <span data-ttu-id="43d95-109">lhs</span><span class="sxs-lookup"><span data-stu-id="43d95-109">lhs</span></span>  
    <span data-ttu-id="43d95-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="43d95-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="43d95-111">A primeira instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="43d95-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="43d95-112">rhs</span><span class="sxs-lookup"><span data-stu-id="43d95-112">rhs</span></span>  
    <span data-ttu-id="43d95-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="43d95-113">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="43d95-114">A segunda instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="43d95-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="43d95-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43d95-115">Return value</span></span>

<span data-ttu-id="43d95-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="43d95-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="43d95-117">True se as duas instâncias forem iguais.</span><span class="sxs-lookup"><span data-stu-id="43d95-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="43d95-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="43d95-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="43d95-119">Referência</span><span class="sxs-lookup"><span data-stu-id="43d95-119">Reference</span></span>

[<span data-ttu-id="43d95-120">Estrutura de JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="43d95-120">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="43d95-121">Membros do JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="43d95-121">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="43d95-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="43d95-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
