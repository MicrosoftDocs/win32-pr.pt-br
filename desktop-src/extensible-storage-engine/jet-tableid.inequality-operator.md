---
description: 'Saiba mais sobre: JET_TABLEID. Operador de desigualdade'
title: JET_TABLEID. Operador de desigualdade
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_TABLEID.op_Inequality(Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tableid.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39510333
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLEID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLEID.Inequality
- Microsoft.Isam.Esent.Interop.JET_TABLEID.op_Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7e1cfc9a43beb8478be287e1659883d49f62239
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505942"
---
# <a name="jet_tableidinequality-operator"></a><span data-ttu-id="f2dfd-103">JET_TABLEID. Operador de desigualdade</span><span class="sxs-lookup"><span data-stu-id="f2dfd-103">JET_TABLEID.Inequality operator</span></span>

<span data-ttu-id="f2dfd-104">Determina se duas instâncias especificadas do JET_TABLEID não são iguais.</span><span class="sxs-lookup"><span data-stu-id="f2dfd-104">Determines whether two specified instances of JET_TABLEID are not equal.</span></span>

<span data-ttu-id="f2dfd-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f2dfd-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f2dfd-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f2dfd-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f2dfd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2dfd-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_TABLEID, _
    rhs As JET_TABLEID _
) As Boolean
'Usage
Dim lhs As JET_TABLEID
Dim rhs As JET_TABLEID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_TABLEID lhs,
    JET_TABLEID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="f2dfd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2dfd-108">Parameters</span></span>

  - <span data-ttu-id="f2dfd-109">lhs</span><span class="sxs-lookup"><span data-stu-id="f2dfd-109">lhs</span></span>  
    <span data-ttu-id="f2dfd-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f2dfd-110">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f2dfd-111">A primeira instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="f2dfd-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2dfd-112">rhs</span><span class="sxs-lookup"><span data-stu-id="f2dfd-112">rhs</span></span>  
    <span data-ttu-id="f2dfd-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f2dfd-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f2dfd-114">A segunda instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="f2dfd-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f2dfd-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f2dfd-115">Return value</span></span>

<span data-ttu-id="f2dfd-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="f2dfd-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="f2dfd-117">True se as duas instâncias não forem iguais.</span><span class="sxs-lookup"><span data-stu-id="f2dfd-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f2dfd-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2dfd-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f2dfd-119">Referência</span><span class="sxs-lookup"><span data-stu-id="f2dfd-119">Reference</span></span>

[<span data-ttu-id="f2dfd-120">Estrutura de JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="f2dfd-120">JET_TABLEID structure</span></span>](./jet-tableid-structure.md)

[<span data-ttu-id="f2dfd-121">Membros do JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="f2dfd-121">JET_TABLEID members</span></span>](./jet-tableid-members.md)

[<span data-ttu-id="f2dfd-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f2dfd-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
