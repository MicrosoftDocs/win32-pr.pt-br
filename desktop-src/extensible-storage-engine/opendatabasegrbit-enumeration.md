---
description: 'Saiba mais sobre: Enumeração OpenDatabaseGrbit'
title: Enumeração OpenDatabaseGrbit
TOCTitle: OpenDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.opendatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39514563
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.Exclusive
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.ReadOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.Exclusive
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d14fb779ec02137f6a4fce1cfdd92f46dedcb832
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169780"
---
# <a name="opendatabasegrbit-enumeration"></a><span data-ttu-id="6a608-103">Enumeração OpenDatabaseGrbit</span><span class="sxs-lookup"><span data-stu-id="6a608-103">OpenDatabaseGrbit enumeration</span></span>

<span data-ttu-id="6a608-104">Opções para [JetOpenDatabase (JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="6a608-104">Options for [JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span></span>

<span data-ttu-id="6a608-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="6a608-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="6a608-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6a608-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6a608-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6a608-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6a608-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a608-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration OpenDatabaseGrbit
'Usage
Dim instance As OpenDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum OpenDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="6a608-109">Membros</span><span class="sxs-lookup"><span data-stu-id="6a608-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="6a608-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="6a608-110">Member name</span></span></th>
<th><span data-ttu-id="6a608-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="6a608-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="6a608-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6a608-112">None</span></span></td>
<td><span data-ttu-id="6a608-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="6a608-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="6a608-114">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6a608-114">ReadOnly</span></span></td>
<td><span data-ttu-id="6a608-115">Impede modificações no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6a608-115">Prevents modifications to the database.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="6a608-116">Exclusivo</span><span class="sxs-lookup"><span data-stu-id="6a608-116">Exclusive</span></span></td>
<td><span data-ttu-id="6a608-117">Permite que apenas uma única sessão anexe um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6a608-117">Allows only a single session to attach a database.</span></span> <span data-ttu-id="6a608-118">Normalmente, várias sessões podem abrir um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6a608-118">Normally, several sessions can open a database.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="6a608-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a608-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6a608-120">Referência</span><span class="sxs-lookup"><span data-stu-id="6a608-120">Reference</span></span>

[<span data-ttu-id="6a608-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6a608-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
