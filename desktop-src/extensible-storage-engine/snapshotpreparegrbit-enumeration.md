---
description: 'Saiba mais sobre: Enumeração SnapshotPrepareGrbit'
title: Enumeração SnapshotPrepareGrbit
TOCTitle: SnapshotPrepareGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.snapshotpreparegrbit(v=EXCHG.10)
ms:contentKeyID: 39515688
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.CopySnapshot
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.IncrementalSnapshot
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.CopySnapshot
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.IncrementalSnapshot
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.None
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 32c11c609f78cc96862f9c2f15d93266f40ae941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296440"
---
# <a name="snapshotpreparegrbit-enumeration"></a><span data-ttu-id="25eea-103">Enumeração SnapshotPrepareGrbit</span><span class="sxs-lookup"><span data-stu-id="25eea-103">SnapshotPrepareGrbit enumeration</span></span>

<span data-ttu-id="25eea-104">Opções para [JetOSSnapshotPrepare (JET_OSSNAPID, SnapshotPrepareGrbit)](./api.jetossnapshotprepare-method.md).</span><span class="sxs-lookup"><span data-stu-id="25eea-104">Options for [JetOSSnapshotPrepare(JET_OSSNAPID, SnapshotPrepareGrbit)](./api.jetossnapshotprepare-method.md).</span></span>

<span data-ttu-id="25eea-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="25eea-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="25eea-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="25eea-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="25eea-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="25eea-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="25eea-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25eea-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SnapshotPrepareGrbit
'Usage
Dim instance As SnapshotPrepareGrbit
```

``` csharp
[FlagsAttribute]
public enum SnapshotPrepareGrbit
```

## <a name="members"></a><span data-ttu-id="25eea-109">Membros</span><span class="sxs-lookup"><span data-stu-id="25eea-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="25eea-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="25eea-110">Member name</span></span></th>
<th><span data-ttu-id="25eea-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="25eea-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="25eea-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="25eea-112">None</span></span></td>
<td><span data-ttu-id="25eea-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="25eea-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="25eea-114">IncrementalSnapshot</span><span class="sxs-lookup"><span data-stu-id="25eea-114">IncrementalSnapshot</span></span></td>
<td><span data-ttu-id="25eea-115">Somente os arquivos de log serão feitos.</span><span class="sxs-lookup"><span data-stu-id="25eea-115">Only logfiles will be taken.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="25eea-116">CopySnapshot</span><span class="sxs-lookup"><span data-stu-id="25eea-116">CopySnapshot</span></span></td>
<td><span data-ttu-id="25eea-117">Um instantâneo de cópia (normal ou incremental) sem truncamento de log.</span><span class="sxs-lookup"><span data-stu-id="25eea-117">A copy snapshot (normal or incremental) with no log truncation.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="25eea-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="25eea-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="25eea-119">Referência</span><span class="sxs-lookup"><span data-stu-id="25eea-119">Reference</span></span>

[<span data-ttu-id="25eea-120">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="25eea-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
