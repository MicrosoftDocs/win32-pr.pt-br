---
description: 'Saiba mais sobre: Enumeração ObjectInfoFlags'
title: Enumeração ObjectInfoFlags
TOCTitle: ObjectInfoFlags enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ObjectInfoFlags
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.objectinfoflags(v=EXCHG.10)
ms:contentKeyID: 39515824
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.None
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.System
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableDerived
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableTemplate
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableFixedDDL
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableNoFixedVarColumnsInDerivedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.System
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableDerived
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.None
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableFixedDDL
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableNoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableTemplate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b3f301f1e786d126dbd57c071fe89356e0acc891
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828641"
---
# <a name="objectinfoflags-enumeration"></a><span data-ttu-id="e1e92-103">Enumeração ObjectInfoFlags</span><span class="sxs-lookup"><span data-stu-id="e1e92-103">ObjectInfoFlags enumeration</span></span>

<span data-ttu-id="e1e92-104">Sinalizadores para objetos ESENT (tabelas).</span><span class="sxs-lookup"><span data-stu-id="e1e92-104">Flags for ESENT objects (tables).</span></span> <span data-ttu-id="e1e92-105">Usado em [JET_OBJECTINFO](./jet-objectinfo-class.md).</span><span class="sxs-lookup"><span data-stu-id="e1e92-105">Used in [JET_OBJECTINFO](./jet-objectinfo-class.md).</span></span>

<span data-ttu-id="e1e92-106">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="e1e92-106">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="e1e92-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e1e92-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e1e92-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e1e92-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e1e92-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1e92-109">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ObjectInfoFlags
'Usage
Dim instance As ObjectInfoFlags
```

``` csharp
[FlagsAttribute]
public enum ObjectInfoFlags
```

## <a name="members"></a><span data-ttu-id="e1e92-110">Membros</span><span class="sxs-lookup"><span data-stu-id="e1e92-110">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="e1e92-111">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="e1e92-111">Member name</span></span></th>
<th><span data-ttu-id="e1e92-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1e92-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="e1e92-113">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e1e92-113">None</span></span></td>
<td><span data-ttu-id="e1e92-114">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="e1e92-114">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="e1e92-115">Sistema</span><span class="sxs-lookup"><span data-stu-id="e1e92-115">System</span></span></td>
<td><span data-ttu-id="e1e92-116">O objeto é somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="e1e92-116">Object is for internal use only.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="e1e92-117">TableFixedDDL</span><span class="sxs-lookup"><span data-stu-id="e1e92-117">TableFixedDDL</span></span></td>
<td><span data-ttu-id="e1e92-118">O DDL da tabela é fixo.</span><span class="sxs-lookup"><span data-stu-id="e1e92-118">Table's DDL is fixed.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="e1e92-119">Tabelatemplate</span><span class="sxs-lookup"><span data-stu-id="e1e92-119">TableTemplate</span></span></td>
<td><span data-ttu-id="e1e92-120">O DDL da tabela é herdável.</span><span class="sxs-lookup"><span data-stu-id="e1e92-120">Table's DDL is inheritable.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="e1e92-121">TableDerived</span><span class="sxs-lookup"><span data-stu-id="e1e92-121">TableDerived</span></span></td>
<td><span data-ttu-id="e1e92-122">A DDL da tabela é herdada de uma tabela de modelo.</span><span class="sxs-lookup"><span data-stu-id="e1e92-122">Table's DDL is inherited from a template table.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="e1e92-123">TableNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="e1e92-123">TableNoFixedVarColumnsInDerivedTables</span></span></td>
<td><span data-ttu-id="e1e92-124">Colunas fixas ou variáveis em tabelas derivadas (para que colunas fixas ou variáveis possam ser adicionadas ao modelo no futuro).</span><span class="sxs-lookup"><span data-stu-id="e1e92-124">Fixed or variable columns in derived tables (so that fixed or variable columns can be added to the template in the future).</span></span> <span data-ttu-id="e1e92-125">Usado em conjunto com TableTemplate.</span><span class="sxs-lookup"><span data-stu-id="e1e92-125">Used in conjunction with TableTemplate.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="e1e92-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1e92-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e1e92-127">Referência</span><span class="sxs-lookup"><span data-stu-id="e1e92-127">Reference</span></span>

[<span data-ttu-id="e1e92-128">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e1e92-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
