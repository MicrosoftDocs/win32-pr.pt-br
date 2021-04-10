---
description: 'Saiba mais sobre: Enumeração DetachDatabaseGrbit'
title: Enumeração DetachDatabaseGrbit
TOCTitle: DetachDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.detachdatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 55100985
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceClose
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceCloseAndDetach
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceDetach
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceClose
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceCloseAndDetach
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceDetach
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e67962420ee0179571da8262f17ea5279f59016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171758"
---
# <a name="detachdatabasegrbit-enumeration"></a><span data-ttu-id="aadd2-103">Enumeração DetachDatabaseGrbit</span><span class="sxs-lookup"><span data-stu-id="aadd2-103">DetachDatabaseGrbit enumeration</span></span>

<span data-ttu-id="aadd2-104">Opções para [JetDetachDatabase2 (JET_SESID, String, DetachDatabaseGrbit)](./api.jetdetachdatabase2-method.md).</span><span class="sxs-lookup"><span data-stu-id="aadd2-104">Options for [JetDetachDatabase2(JET_SESID, String, DetachDatabaseGrbit)](./api.jetdetachdatabase2-method.md).</span></span>

<span data-ttu-id="aadd2-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="aadd2-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="aadd2-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="aadd2-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="aadd2-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="aadd2-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="aadd2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aadd2-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration DetachDatabaseGrbit
'Usage
Dim instance As DetachDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum DetachDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="aadd2-109">Membros</span><span class="sxs-lookup"><span data-stu-id="aadd2-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="aadd2-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="aadd2-110">Member name</span></span></th>
<th><span data-ttu-id="aadd2-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="aadd2-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="aadd2-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="aadd2-112">None</span></span></td>
<td><span data-ttu-id="aadd2-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="aadd2-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="aadd2-114">ForceDetach</span><span class="sxs-lookup"><span data-stu-id="aadd2-114">ForceDetach</span></span></td>
<td><span data-ttu-id="aadd2-115"><strong>Obsoleto.</strong></span><span class="sxs-lookup"><span data-stu-id="aadd2-115"><strong>Obsolete.</strong></span></span> <span data-ttu-id="aadd2-116">Se ForceDetach for usado, <a href="dn350463(v=exchg.10).md">EsentForceDetachNotAllowedException</a> será retornado.</span><span class="sxs-lookup"><span data-stu-id="aadd2-116">If ForceDetach is used, <a href="dn350463(v=exchg.10).md">EsentForceDetachNotAllowedException</a> will be returned.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="aadd2-117">Fechamento forçado</span><span class="sxs-lookup"><span data-stu-id="aadd2-117">ForceClose</span></span></td>
<td><span data-ttu-id="aadd2-118"><strong>Obsoleto.</strong></span><span class="sxs-lookup"><span data-stu-id="aadd2-118"><strong>Obsolete.</strong></span></span> <span data-ttu-id="aadd2-119">Fechamento forçado não é mais usado.</span><span class="sxs-lookup"><span data-stu-id="aadd2-119">ForceClose is no longer used.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="aadd2-120">ForceCloseAndDetach</span><span class="sxs-lookup"><span data-stu-id="aadd2-120">ForceCloseAndDetach</span></span></td>
<td><span data-ttu-id="aadd2-121"><strong>Obsoleto.</strong></span><span class="sxs-lookup"><span data-stu-id="aadd2-121"><strong>Obsolete.</strong></span></span> <span data-ttu-id="aadd2-122">Se ForceCloseAndDetach for usado, <a href="dn350463(v=exchg.10).md">EsentForceDetachNotAllowedException</a> será retornado.</span><span class="sxs-lookup"><span data-stu-id="aadd2-122">If ForceCloseAndDetach is used, <a href="dn350463(v=exchg.10).md">EsentForceDetachNotAllowedException</a> will be returned.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="aadd2-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="aadd2-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="aadd2-124">Referência</span><span class="sxs-lookup"><span data-stu-id="aadd2-124">Reference</span></span>

[<span data-ttu-id="aadd2-125">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="aadd2-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
