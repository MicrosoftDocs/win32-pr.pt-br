---
description: 'Saiba mais sobre: JET_SESID. Operador de igualdade'
title: JET_SESID. Operador de igualdade
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SESID.op_Equality(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_sesid.op_equality(v=EXCHG.10)
ms:contentKeyID: 39511173
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SESID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SESID.Equality
- Microsoft.Isam.Esent.Interop.JET_SESID.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 19e0550452fb0053978cabcdb393222c814c85f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461002"
---
# <a name="jet_sesidequality-operator"></a><span data-ttu-id="b2cf3-103">JET_SESID. Operador de igualdade</span><span class="sxs-lookup"><span data-stu-id="b2cf3-103">JET_SESID.Equality operator</span></span>

<span data-ttu-id="b2cf3-104">Determina se duas instâncias especificadas do JET_SESID são iguais.</span><span class="sxs-lookup"><span data-stu-id="b2cf3-104">Determines whether two specified instances of JET_SESID are equal.</span></span>

<span data-ttu-id="b2cf3-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b2cf3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b2cf3-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b2cf3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b2cf3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2cf3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_SESID, _
    rhs As JET_SESID _
) As Boolean
'Usage
Dim lhs As JET_SESID
Dim rhs As JET_SESID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_SESID lhs,
    JET_SESID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="b2cf3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2cf3-108">Parameters</span></span>

  - <span data-ttu-id="b2cf3-109">lhs</span><span class="sxs-lookup"><span data-stu-id="b2cf3-109">lhs</span></span>  
    <span data-ttu-id="b2cf3-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b2cf3-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b2cf3-111">A primeira instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="b2cf3-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="b2cf3-112">rhs</span><span class="sxs-lookup"><span data-stu-id="b2cf3-112">rhs</span></span>  
    <span data-ttu-id="b2cf3-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b2cf3-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b2cf3-114">A segunda instância a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="b2cf3-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b2cf3-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b2cf3-115">Return value</span></span>

<span data-ttu-id="b2cf3-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="b2cf3-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="b2cf3-117">True se as duas instâncias forem iguais.</span><span class="sxs-lookup"><span data-stu-id="b2cf3-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b2cf3-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2cf3-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b2cf3-119">Referência</span><span class="sxs-lookup"><span data-stu-id="b2cf3-119">Reference</span></span>

[<span data-ttu-id="b2cf3-120">Estrutura de JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b2cf3-120">JET_SESID structure</span></span>](./jet-sesid-structure.md)

[<span data-ttu-id="b2cf3-121">Membros do JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b2cf3-121">JET_SESID members</span></span>](./jet-sesid-members.md)

[<span data-ttu-id="b2cf3-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b2cf3-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
