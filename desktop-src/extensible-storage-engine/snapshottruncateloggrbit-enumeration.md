---
description: 'Saiba mais sobre: Enumeração SnapshotTruncateLogGrbit'
title: Enumeração SnapshotTruncateLogGrbit (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: SnapshotTruncateLogGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.snapshottruncateloggrbit(v=EXCHG.10)
ms:contentKeyID: 39516474
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit.AllDatabasesSnapshot
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit.AllDatabasesSnapshot
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit.None
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8baf9f9ec15e91183d2b01a07da9aeda0c7fec18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790618"
---
# <a name="snapshottruncateloggrbit-enumeration"></a><span data-ttu-id="a6956-103">Enumeração SnapshotTruncateLogGrbit</span><span class="sxs-lookup"><span data-stu-id="a6956-103">SnapshotTruncateLogGrbit enumeration</span></span>

<span data-ttu-id="a6956-104">Opções para [JetOSSnapshotTruncateLog (JET_OSSNAPID, SnapshotTruncateLogGrbit)](./vistaapi.jetossnapshottruncatelog-method.md) e [JetOSSnapshotTruncateLogInstance (JET_OSSNAPID, JET_INSTANCE, SnapshotTruncateLogGrbit)](./vistaapi.jetossnapshottruncateloginstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="a6956-104">Options for [JetOSSnapshotTruncateLog(JET_OSSNAPID, SnapshotTruncateLogGrbit)](./vistaapi.jetossnapshottruncatelog-method.md) and [JetOSSnapshotTruncateLogInstance(JET_OSSNAPID, JET_INSTANCE, SnapshotTruncateLogGrbit)](./vistaapi.jetossnapshottruncateloginstance-method.md).</span></span>

<span data-ttu-id="a6956-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="a6956-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="a6956-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a6956-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="a6956-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a6956-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a6956-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6956-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SnapshotTruncateLogGrbit
'Usage
Dim instance As SnapshotTruncateLogGrbit
```

``` csharp
[FlagsAttribute]
public enum SnapshotTruncateLogGrbit
```

## <a name="members"></a><span data-ttu-id="a6956-109">Membros</span><span class="sxs-lookup"><span data-stu-id="a6956-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="a6956-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="a6956-110">Member name</span></span></th>
<th><span data-ttu-id="a6956-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="a6956-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="a6956-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a6956-112">None</span></span></td>
<td><span data-ttu-id="a6956-113">Nenhum truncamento ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="a6956-113">No truncation will occur.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="a6956-114">AllDatabasesSnapshot</span><span class="sxs-lookup"><span data-stu-id="a6956-114">AllDatabasesSnapshot</span></span></td>
<td><span data-ttu-id="a6956-115">Todos os bancos de dados são anexados para que o mecanismo de armazenamento possa computar e fazer o truncamento de log.</span><span class="sxs-lookup"><span data-stu-id="a6956-115">All the databases are attached so the storage engine can compute and do the log truncation.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="a6956-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6956-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a6956-117">Referência</span><span class="sxs-lookup"><span data-stu-id="a6956-117">Reference</span></span>

[<span data-ttu-id="a6956-118">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="a6956-118">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
