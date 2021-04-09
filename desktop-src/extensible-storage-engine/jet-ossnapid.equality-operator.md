---
description: 'Saiba mais sobre: JET_OSSNAPID. Operador de igualdade'
title: JET_OSSNAPID. Operador de igualdade
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_OSSNAPID.op_Equality(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.JET_OSSNAPID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ossnapid.op_equality(v=EXCHG.10)
ms:contentKeyID: 39513985
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.op_Equality
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a0fcd5d1edba1a0c3d05fe2b1778741626832d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171040"
---
# <a name="jet_ossnapidequality-operator"></a><span data-ttu-id="31598-103">JET_OSSNAPID. Operador de igualdade</span><span class="sxs-lookup"><span data-stu-id="31598-103">JET_OSSNAPID.Equality operator</span></span>

<span data-ttu-id="31598-104">Determina se duas instâncias especificadas do JET_OSSNAPID são iguais.</span><span class="sxs-lookup"><span data-stu-id="31598-104">Determines whether two specified instances of JET_OSSNAPID are equal.</span></span>

<span data-ttu-id="31598-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="31598-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="31598-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="31598-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="31598-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31598-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_OSSNAPID, _
    rhs As JET_OSSNAPID _
) As Boolean
'Usage
Dim lhs As JET_OSSNAPID
Dim rhs As JET_OSSNAPID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_OSSNAPID lhs,
    JET_OSSNAPID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="31598-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31598-108">Parameters</span></span>

  - <span data-ttu-id="31598-109">lhs</span><span class="sxs-lookup"><span data-stu-id="31598-109">lhs</span></span>  
    <span data-ttu-id="31598-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="31598-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="31598-111">A primeira instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="31598-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="31598-112">rhs</span><span class="sxs-lookup"><span data-stu-id="31598-112">rhs</span></span>  
    <span data-ttu-id="31598-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="31598-113">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="31598-114">A segunda instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="31598-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31598-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31598-115">Return value</span></span>

<span data-ttu-id="31598-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="31598-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="31598-117">True se as duas instâncias forem iguais.</span><span class="sxs-lookup"><span data-stu-id="31598-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="31598-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="31598-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="31598-119">Referência</span><span class="sxs-lookup"><span data-stu-id="31598-119">Reference</span></span>

[<span data-ttu-id="31598-120">Estrutura de JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="31598-120">JET_OSSNAPID structure</span></span>](./jet-ossnapid-structure.md)

[<span data-ttu-id="31598-121">Membros do JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="31598-121">JET_OSSNAPID members</span></span>](./jet-ossnapid-members.md)

[<span data-ttu-id="31598-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="31598-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
