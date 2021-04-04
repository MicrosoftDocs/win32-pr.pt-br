---
description: 'Saiba mais sobre: enumeração de JET_dbstate'
title: Enumeração de JET_dbstate
TOCTitle: JET_dbstate enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_dbstate
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbstate(v=EXCHG.10)
ms:contentKeyID: 39511841
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_dbstate
- Microsoft.Isam.Esent.Interop.JET_dbstate.BeingConverted
- Microsoft.Isam.Esent.Interop.JET_dbstate.CleanShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.DirtyShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.ForceDetach
- Microsoft.Isam.Esent.Interop.JET_dbstate.JustCreated
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_dbstate.JustCreated
- Microsoft.Isam.Esent.Interop.JET_dbstate.BeingConverted
- Microsoft.Isam.Esent.Interop.JET_dbstate.CleanShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.ForceDetach
- Microsoft.Isam.Esent.Interop.JET_dbstate.DirtyShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a83c8a4313e5e6f21ee885ee7936c90503bfbd3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646745"
---
# <a name="jet_dbstate-enumeration"></a><span data-ttu-id="00ea6-103">Enumeração de JET_dbstate</span><span class="sxs-lookup"><span data-stu-id="00ea6-103">JET_dbstate enumeration</span></span>

<span data-ttu-id="00ea6-104">Estados de banco de dados (usados em [JET_DBINFOMISC](./jet-dbinfomisc-class.md)).</span><span class="sxs-lookup"><span data-stu-id="00ea6-104">Database states (used in [JET_DBINFOMISC](./jet-dbinfomisc-class.md)).</span></span>

<span data-ttu-id="00ea6-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="00ea6-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="00ea6-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="00ea6-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="00ea6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00ea6-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_dbstate
'Usage
Dim instance As JET_dbstate
```

``` csharp
public enum JET_dbstate
```

## <a name="members"></a><span data-ttu-id="00ea6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="00ea6-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="00ea6-109">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="00ea6-109">Member name</span></span></th>
<th><span data-ttu-id="00ea6-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="00ea6-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="00ea6-111">JustCreated</span><span class="sxs-lookup"><span data-stu-id="00ea6-111">JustCreated</span></span></td>
<td><span data-ttu-id="00ea6-112">O banco de dados acabou de ser criado.</span><span class="sxs-lookup"><span data-stu-id="00ea6-112">The database was just created.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="00ea6-113">DirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="00ea6-113">DirtyShutdown</span></span></td>
<td><span data-ttu-id="00ea6-114">Banco de dados de desligamento anormal (inconsistente).</span><span class="sxs-lookup"><span data-stu-id="00ea6-114">Dirty shutdown (inconsistent) database.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="00ea6-115">CleanShutdown</span><span class="sxs-lookup"><span data-stu-id="00ea6-115">CleanShutdown</span></span></td>
<td><span data-ttu-id="00ea6-116">Banco de dados de desligamento normal (consistente).</span><span class="sxs-lookup"><span data-stu-id="00ea6-116">Clean shutdown (consistent) database.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="00ea6-117">BeingConverted</span><span class="sxs-lookup"><span data-stu-id="00ea6-117">BeingConverted</span></span></td>
<td><span data-ttu-id="00ea6-118">O banco de dados está sendo convertido.</span><span class="sxs-lookup"><span data-stu-id="00ea6-118">Database is being converted.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="00ea6-119">ForceDetach</span><span class="sxs-lookup"><span data-stu-id="00ea6-119">ForceDetach</span></span></td>
<td><span data-ttu-id="00ea6-120">O banco de dados foi desanexado.</span><span class="sxs-lookup"><span data-stu-id="00ea6-120">Database was force-detached.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="00ea6-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="00ea6-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="00ea6-122">Referência</span><span class="sxs-lookup"><span data-stu-id="00ea6-122">Reference</span></span>

[<span data-ttu-id="00ea6-123">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="00ea6-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
