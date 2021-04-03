---
description: 'Saiba mais sobre: Enumeração CreateTableColumnIndexGrbit'
title: Enumeração CreateTableColumnIndexGrbit
TOCTitle: CreateTableColumnIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createtablecolumnindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39516657
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.FixedDDL
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.NoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.TemplateTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.TemplateTable
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.NoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.FixedDDL
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72f91c5d41b8262e3b2804159914b0a9ccaaaa7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922766"
---
# <a name="createtablecolumnindexgrbit-enumeration"></a><span data-ttu-id="5b5a0-103">Enumeração CreateTableColumnIndexGrbit</span><span class="sxs-lookup"><span data-stu-id="5b5a0-103">CreateTableColumnIndexGrbit enumeration</span></span>

<span data-ttu-id="5b5a0-104">Opções para JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="5b5a0-104">Options for JetCreateTableColumnIndex.</span></span>

<span data-ttu-id="5b5a0-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="5b5a0-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="5b5a0-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5b5a0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5b5a0-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5b5a0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5b5a0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b5a0-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateTableColumnIndexGrbit
'Usage
Dim instance As CreateTableColumnIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateTableColumnIndexGrbit
```

## <a name="members"></a><span data-ttu-id="5b5a0-109">Membros</span><span class="sxs-lookup"><span data-stu-id="5b5a0-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="5b5a0-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="5b5a0-110">Member name</span></span></th>
<th><span data-ttu-id="5b5a0-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b5a0-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="5b5a0-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5b5a0-112">None</span></span></td>
<td><span data-ttu-id="5b5a0-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="5b5a0-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="5b5a0-114">FixedDDL</span><span class="sxs-lookup"><span data-stu-id="5b5a0-114">FixedDDL</span></span></td>
<td><span data-ttu-id="5b5a0-115">O DDL é fixo.</span><span class="sxs-lookup"><span data-stu-id="5b5a0-115">The DDL is fixed.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="5b5a0-116">Modelotable</span><span class="sxs-lookup"><span data-stu-id="5b5a0-116">TemplateTable</span></span></td>
<td><span data-ttu-id="5b5a0-117">O DDL é herdável.</span><span class="sxs-lookup"><span data-stu-id="5b5a0-117">The DDL is inheritable.</span></span> <span data-ttu-id="5b5a0-118">Implica FixedDDL.</span><span class="sxs-lookup"><span data-stu-id="5b5a0-118">Implies FixedDDL.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="5b5a0-119">NoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="5b5a0-119">NoFixedVarColumnsInDerivedTables</span></span></td>
<td><span data-ttu-id="5b5a0-120">Usado em conjunto com Templatetable.</span><span class="sxs-lookup"><span data-stu-id="5b5a0-120">Used in conjunction with TemplateTable.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="5b5a0-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b5a0-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5b5a0-122">Referência</span><span class="sxs-lookup"><span data-stu-id="5b5a0-122">Reference</span></span>

[<span data-ttu-id="5b5a0-123">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5b5a0-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
