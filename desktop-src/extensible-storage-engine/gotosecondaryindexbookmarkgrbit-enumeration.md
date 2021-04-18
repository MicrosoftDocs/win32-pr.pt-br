---
description: 'Saiba mais sobre: Enumeração GotoSecondaryIndexBookmarkGrbit'
title: Enumeração GotoSecondaryIndexBookmarkGrbit
TOCTitle: GotoSecondaryIndexBookmarkGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.gotosecondaryindexbookmarkgrbit(v=EXCHG.10)
ms:contentKeyID: 39515224
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.BookmarkPermitVirtualCurrency
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.BookmarkPermitVirtualCurrency
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f38b5f26abc4dfafb95d5560b3ff1def4267527c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753066"
---
# <a name="gotosecondaryindexbookmarkgrbit-enumeration"></a><span data-ttu-id="f3ed0-103">Enumeração GotoSecondaryIndexBookmarkGrbit</span><span class="sxs-lookup"><span data-stu-id="f3ed0-103">GotoSecondaryIndexBookmarkGrbit enumeration</span></span>

<span data-ttu-id="f3ed0-104">Opções para [JetGotoSecondaryIndexBookmark (JET_SESID, JET_TABLEID, \[ \] , Int32, \[ \] Int32, GotoSecondaryIndexBookmarkGrbit)](./api.jetgotosecondaryindexbookmark-method.md).</span><span class="sxs-lookup"><span data-stu-id="f3ed0-104">Options for [JetGotoSecondaryIndexBookmark(JET_SESID, JET_TABLEID, \[\], Int32, \[\], Int32, GotoSecondaryIndexBookmarkGrbit)](./api.jetgotosecondaryindexbookmark-method.md).</span></span>

<span data-ttu-id="f3ed0-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="f3ed0-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="f3ed0-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f3ed0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f3ed0-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f3ed0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f3ed0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f3ed0-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GotoSecondaryIndexBookmarkGrbit
'Usage
Dim instance As GotoSecondaryIndexBookmarkGrbit
```

``` csharp
[FlagsAttribute]
public enum GotoSecondaryIndexBookmarkGrbit
```

## <a name="members"></a><span data-ttu-id="f3ed0-109">Membros</span><span class="sxs-lookup"><span data-stu-id="f3ed0-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f3ed0-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="f3ed0-110">Member name</span></span></th>
<th><span data-ttu-id="f3ed0-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3ed0-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f3ed0-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f3ed0-112">None</span></span></td>
<td><span data-ttu-id="f3ed0-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="f3ed0-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f3ed0-114">BookmarkPermitVirtualCurrency</span><span class="sxs-lookup"><span data-stu-id="f3ed0-114">BookmarkPermitVirtualCurrency</span></span></td>
<td><span data-ttu-id="f3ed0-115">Caso a entrada de índice não possa mais ser encontrada, o cursor será deixado posicionado onde essa entrada de índice foi encontrada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f3ed0-115">In the event that the index entry can no longer be found, the cursor will be left positioned where that index entry was previously found.</span></span> <span data-ttu-id="f3ed0-116">A operação ainda falhará com JET_errRecordDeleted; no entanto, será possível mover para a entrada de índice seguinte ou anterior em relação à entrada de índice que agora está ausente.</span><span class="sxs-lookup"><span data-stu-id="f3ed0-116">The operation will still fail with JET_errRecordDeleted; however, it will be possible to move to the next or previous index entry relative to the index entry that is now missing.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="f3ed0-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3ed0-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f3ed0-118">Referência</span><span class="sxs-lookup"><span data-stu-id="f3ed0-118">Reference</span></span>

[<span data-ttu-id="f3ed0-119">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f3ed0-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
