---
description: 'Saiba mais sobre: JET_BKLOGTIME. Operador de igualdade'
title: JET_BKLOGTIME. Operador de igualdade
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Equality(Microsoft.Isam.Esent.Interop.JET_BKLOGTIME,Microsoft.Isam.Esent.Interop.JET_BKLOGTIME)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bklogtime.op_equality(v=EXCHG.10)
ms:contentKeyID: 39515956
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Equality
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f5a75a1fc55159fc5ea71dba09dc1ed54194b940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763527"
---
# <a name="jet_bklogtimeequality-operator"></a><span data-ttu-id="1a639-103">JET_BKLOGTIME. Operador de igualdade</span><span class="sxs-lookup"><span data-stu-id="1a639-103">JET_BKLOGTIME.Equality operator</span></span>

<span data-ttu-id="1a639-104">Determina se duas instâncias especificadas do JET_BKLOGTIME são iguais.</span><span class="sxs-lookup"><span data-stu-id="1a639-104">Determines whether two specified instances of JET_BKLOGTIME are equal.</span></span>

<span data-ttu-id="1a639-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1a639-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1a639-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1a639-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1a639-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a639-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_BKLOGTIME, _
    rhs As JET_BKLOGTIME _
) As Boolean
'Usage
Dim lhs As JET_BKLOGTIME
Dim rhs As JET_BKLOGTIME
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_BKLOGTIME lhs,
    JET_BKLOGTIME rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="1a639-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a639-108">Parameters</span></span>

  - <span data-ttu-id="1a639-109">lhs</span><span class="sxs-lookup"><span data-stu-id="1a639-109">lhs</span></span>  
    <span data-ttu-id="1a639-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="1a639-110">Type: [Microsoft.Isam.Esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span></span>  
    
    <span data-ttu-id="1a639-111">A primeira instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="1a639-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="1a639-112">rhs</span><span class="sxs-lookup"><span data-stu-id="1a639-112">rhs</span></span>  
    <span data-ttu-id="1a639-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="1a639-113">Type: [Microsoft.Isam.Esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span></span>  
    
    <span data-ttu-id="1a639-114">A segunda instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="1a639-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="1a639-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1a639-115">Return value</span></span>

<span data-ttu-id="1a639-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="1a639-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="1a639-117">True se as duas instâncias forem iguais.</span><span class="sxs-lookup"><span data-stu-id="1a639-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1a639-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a639-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1a639-119">Referência</span><span class="sxs-lookup"><span data-stu-id="1a639-119">Reference</span></span>

[<span data-ttu-id="1a639-120">Estrutura de JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="1a639-120">JET_BKLOGTIME structure</span></span>](./jet-bklogtime-structure2.md)

[<span data-ttu-id="1a639-121">Membros do JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="1a639-121">JET_BKLOGTIME members</span></span>](./jet-bklogtime-members.md)

[<span data-ttu-id="1a639-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="1a639-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
