---
description: 'Saiba mais sobre: Enumeração JetRelop'
title: Enumeração JetRelop (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: JetRelop enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JetRelop
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jetrelop(v=EXCHG.10)
ms:contentKeyID: 55104456
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskNotEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.Equals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.NotEquals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.PrefixEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.PrefixEquals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskNotEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.NotEquals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7839e0223eb9dd773ca9a5d10b5210b10b0a944a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297732"
---
# <a name="jetrelop-enumeration"></a><span data-ttu-id="43c87-103">Enumeração JetRelop</span><span class="sxs-lookup"><span data-stu-id="43c87-103">JetRelop enumeration</span></span>

<span data-ttu-id="43c87-104">Operação de comparação para o filtro definido como [JET_INDEX_COLUMN](./jet-index-column-class.md).</span><span class="sxs-lookup"><span data-stu-id="43c87-104">Comparison operation for filter defined as [JET_INDEX_COLUMN](./jet-index-column-class.md).</span></span>

<span data-ttu-id="43c87-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="43c87-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="43c87-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="43c87-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="43c87-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43c87-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JetRelop
'Usage
Dim instance As JetRelop
```

``` csharp
public enum JetRelop
```

## <a name="members"></a><span data-ttu-id="43c87-108">Membros</span><span class="sxs-lookup"><span data-stu-id="43c87-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="43c87-109">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="43c87-109">Member name</span></span></th>
<th><span data-ttu-id="43c87-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="43c87-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="43c87-111">É igual a</span><span class="sxs-lookup"><span data-stu-id="43c87-111">Equals</span></span></td>
<td><span data-ttu-id="43c87-112">Aceite somente linhas que tenham valor de coluna igual ao valor especificado.</span><span class="sxs-lookup"><span data-stu-id="43c87-112">Accept only rows which have column value equal to the given value.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="43c87-113">PrefixEquals</span><span class="sxs-lookup"><span data-stu-id="43c87-113">PrefixEquals</span></span></td>
<td><span data-ttu-id="43c87-114">Aceite somente as linhas que têm colunas cujo prefixo corresponde ao valor especificado.</span><span class="sxs-lookup"><span data-stu-id="43c87-114">Accept only rows which have columns whose prefix matches the given value.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="43c87-115">NotEquals</span><span class="sxs-lookup"><span data-stu-id="43c87-115">NotEquals</span></span></td>
<td><span data-ttu-id="43c87-116">Aceitar somente as linhas que têm valor de coluna diferente do valor especificado.</span><span class="sxs-lookup"><span data-stu-id="43c87-116">Accept only rows which have column value not equal to the given value.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="43c87-117">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="43c87-117">LessThanOrEqual</span></span></td>
<td><span data-ttu-id="43c87-118">Aceite somente linhas com valor de coluna menor ou igual a um determinado valor.</span><span class="sxs-lookup"><span data-stu-id="43c87-118">Accept only rows which have column value less than or equal a given value.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="43c87-119">LessThan</span><span class="sxs-lookup"><span data-stu-id="43c87-119">LessThan</span></span></td>
<td><span data-ttu-id="43c87-120">Aceite somente linhas que tenham valor de coluna menor que um determinado valor.</span><span class="sxs-lookup"><span data-stu-id="43c87-120">Accept only rows which have column value less than a given value.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="43c87-121">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="43c87-121">GreaterThanOrEqual</span></span></td>
<td><span data-ttu-id="43c87-122">Aceite apenas as linhas com valor de coluna maior ou igual a um determinado valor.</span><span class="sxs-lookup"><span data-stu-id="43c87-122">Accept only rows which have column value greater than or equal a given value.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="43c87-123">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="43c87-123">GreaterThan</span></span></td>
<td><span data-ttu-id="43c87-124">Aceite somente linhas que tenham valor de coluna maior que um determinado valor.</span><span class="sxs-lookup"><span data-stu-id="43c87-124">Accept only rows which have column value greater than a given value.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="43c87-125">BitmaskEqualsZero</span><span class="sxs-lookup"><span data-stu-id="43c87-125">BitmaskEqualsZero</span></span></td>
<td><span data-ttu-id="43c87-126">Aceite somente as linhas que têm o valor de coluna ANDed com uma determinada bitmask, gerando zero.</span><span class="sxs-lookup"><span data-stu-id="43c87-126">Accept only rows which have column value ANDed with a given bitmask yielding zero.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="43c87-127">BitmaskNotEqualsZero</span><span class="sxs-lookup"><span data-stu-id="43c87-127">BitmaskNotEqualsZero</span></span></td>
<td><span data-ttu-id="43c87-128">Aceitar somente as linhas que têm o valor de coluna ANDed com uma determinada bitmask, gerando diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="43c87-128">Accept only rows which have column value ANDed with a given bitmask yielding non-zero.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="43c87-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="43c87-129">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="43c87-130">Referência</span><span class="sxs-lookup"><span data-stu-id="43c87-130">Reference</span></span>

[<span data-ttu-id="43c87-131">Namespace Microsoft. ISAM. ESENT. Interop. windows8</span><span class="sxs-lookup"><span data-stu-id="43c87-131">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
