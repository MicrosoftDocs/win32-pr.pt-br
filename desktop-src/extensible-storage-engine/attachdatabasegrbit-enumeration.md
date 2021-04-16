---
description: 'Saiba mais sobre: Enumeração AttachDatabaseGrbit'
title: Enumeração AttachDatabaseGrbit
TOCTitle: AttachDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.attachdatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39514410
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.DeleteCorruptIndexes
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.ReadOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.DeleteCorruptIndexes
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81525e97f1b6266ba15baab50168404566bd7bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757580"
---
# <a name="attachdatabasegrbit-enumeration"></a><span data-ttu-id="b0565-103">Enumeração AttachDatabaseGrbit</span><span class="sxs-lookup"><span data-stu-id="b0565-103">AttachDatabaseGrbit enumeration</span></span>

<span data-ttu-id="b0565-104">Opções para JetAttachDatabase.</span><span class="sxs-lookup"><span data-stu-id="b0565-104">Options for JetAttachDatabase.</span></span>

<span data-ttu-id="b0565-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="b0565-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="b0565-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b0565-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b0565-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b0565-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b0565-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0565-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration AttachDatabaseGrbit
'Usage
Dim instance As AttachDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum AttachDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="b0565-109">Membros</span><span class="sxs-lookup"><span data-stu-id="b0565-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="b0565-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="b0565-110">Member name</span></span></th>
<th><span data-ttu-id="b0565-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0565-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b0565-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b0565-112">None</span></span></td>
<td><span data-ttu-id="b0565-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="b0565-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="b0565-114">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b0565-114">ReadOnly</span></span></td>
<td><span data-ttu-id="b0565-115">Impede modificações no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b0565-115">Prevents modifications to the database.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b0565-116">DeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="b0565-116">DeleteCorruptIndexes</span></span></td>
<td><span data-ttu-id="b0565-117">Se JET_paramEnableIndexChecking tiver sido definido, todos os índices sobre dados Unicode serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="b0565-117">If JET_paramEnableIndexChecking has been set, all indexes over Unicode data will be deleted.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="b0565-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0565-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b0565-119">Referência</span><span class="sxs-lookup"><span data-stu-id="b0565-119">Reference</span></span>

[<span data-ttu-id="b0565-120">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b0565-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
