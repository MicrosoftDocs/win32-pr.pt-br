---
description: 'Saiba mais sobre: JET_LOGTIME. Operador de igualdade'
title: JET_LOGTIME. Operador de igualdade
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LOGTIME.op_Equality(Microsoft.Isam.Esent.Interop.JET_LOGTIME,Microsoft.Isam.Esent.Interop.JET_LOGTIME)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_logtime.op_equality(v=EXCHG.10)
ms:contentKeyID: 39514101
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.Equality
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d7f346a1331200b18c2fc9e51d8eebc1ddaef105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797559"
---
# <a name="jet_logtimeequality-operator"></a><span data-ttu-id="381d0-103">JET_LOGTIME. Operador de igualdade</span><span class="sxs-lookup"><span data-stu-id="381d0-103">JET_LOGTIME.Equality operator</span></span>

<span data-ttu-id="381d0-104">Determina se duas instâncias especificadas do JET_LOGTIME são iguais.</span><span class="sxs-lookup"><span data-stu-id="381d0-104">Determines whether two specified instances of JET_LOGTIME are equal.</span></span>

<span data-ttu-id="381d0-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="381d0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="381d0-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="381d0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="381d0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="381d0-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_LOGTIME, _
    rhs As JET_LOGTIME _
) As Boolean
'Usage
Dim lhs As JET_LOGTIME
Dim rhs As JET_LOGTIME
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_LOGTIME lhs,
    JET_LOGTIME rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="381d0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="381d0-108">Parameters</span></span>

  - <span data-ttu-id="381d0-109">lhs</span><span class="sxs-lookup"><span data-stu-id="381d0-109">lhs</span></span>  
    <span data-ttu-id="381d0-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="381d0-110">Type: [Microsoft.Isam.Esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span></span>  
    
    <span data-ttu-id="381d0-111">A primeira instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="381d0-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="381d0-112">rhs</span><span class="sxs-lookup"><span data-stu-id="381d0-112">rhs</span></span>  
    <span data-ttu-id="381d0-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="381d0-113">Type: [Microsoft.Isam.Esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span></span>  
    
    <span data-ttu-id="381d0-114">A segunda instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="381d0-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="381d0-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="381d0-115">Return value</span></span>

<span data-ttu-id="381d0-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="381d0-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="381d0-117">True se as duas instâncias forem iguais.</span><span class="sxs-lookup"><span data-stu-id="381d0-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="381d0-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="381d0-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="381d0-119">Referência</span><span class="sxs-lookup"><span data-stu-id="381d0-119">Reference</span></span>

[<span data-ttu-id="381d0-120">Estrutura de JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="381d0-120">JET_LOGTIME structure</span></span>](./jet-logtime-structure2.md)

[<span data-ttu-id="381d0-121">Membros do JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="381d0-121">JET_LOGTIME members</span></span>](./jet-logtime-members.md)

[<span data-ttu-id="381d0-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="381d0-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
