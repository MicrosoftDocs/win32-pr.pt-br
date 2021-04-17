---
description: 'Saiba mais sobre: Enumeração DefragGrbit'
title: Enumeração DefragGrbit
TOCTitle: DefragGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.DefragGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.defraggrbit(v=EXCHG.10)
ms:contentKeyID: 39516122
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DefragGrbit
- Microsoft.Isam.Esent.Interop.DefragGrbit.AvailSpaceTreesOnly
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStart
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStop
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DefragGrbit
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStart
- Microsoft.Isam.Esent.Interop.DefragGrbit.AvailSpaceTreesOnly
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStop
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5da047fbdad20ac40d780dc5b0bba9e986e7672
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787632"
---
# <a name="defraggrbit-enumeration"></a><span data-ttu-id="410bc-103">Enumeração DefragGrbit</span><span class="sxs-lookup"><span data-stu-id="410bc-103">DefragGrbit enumeration</span></span>

<span data-ttu-id="410bc-104">Opções para [JetDefragment (JET_SESID, JET_DBID, String, Int32, Int32, DefragGrbit)](./api.jetdefragment-method.md).</span><span class="sxs-lookup"><span data-stu-id="410bc-104">Options for [JetDefragment(JET_SESID, JET_DBID, String, Int32, Int32, DefragGrbit)](./api.jetdefragment-method.md).</span></span>

<span data-ttu-id="410bc-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="410bc-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="410bc-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="410bc-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="410bc-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="410bc-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="410bc-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="410bc-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration DefragGrbit
'Usage
Dim instance As DefragGrbit
```

``` csharp
[FlagsAttribute]
public enum DefragGrbit
```

## <a name="members"></a><span data-ttu-id="410bc-109">Membros</span><span class="sxs-lookup"><span data-stu-id="410bc-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="410bc-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="410bc-110">Member name</span></span></th>
<th><span data-ttu-id="410bc-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="410bc-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="410bc-112">AvailSpaceTreesOnly</span><span class="sxs-lookup"><span data-stu-id="410bc-112">AvailSpaceTreesOnly</span></span></td>
<td><span data-ttu-id="410bc-113">Desfragmenta a parte de espaço disponível da alocação de espaço do banco de dados ESE.</span><span class="sxs-lookup"><span data-stu-id="410bc-113">Defragments the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="410bc-114">O espaço do banco de dados é dividido em dois tipos, espaço de propriedade e espaço disponível.</span><span class="sxs-lookup"><span data-stu-id="410bc-114">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="410bc-115">O espaço de propriedade é alocado para uma tabela ou índice enquanto o espaço disponível está pronto para uso dentro da tabela ou índice, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="410bc-115">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="410bc-116">O espaço disponível é muito mais dinâmico no comportamento e requer a desfragmentação online mais do que o espaço de propriedade ou os dados de índice ou de tabela.</span><span class="sxs-lookup"><span data-stu-id="410bc-116">Available space is much more dynamic in behavior and requires on-line defragmentation more so than owned space or table or index data.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="410bc-117">BatchStart</span><span class="sxs-lookup"><span data-stu-id="410bc-117">BatchStart</span></span></td>
<td><span data-ttu-id="410bc-118">Inicia uma nova tarefa de desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="410bc-118">Starts a new defragmentation task.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="410bc-119">BatchStop</span><span class="sxs-lookup"><span data-stu-id="410bc-119">BatchStop</span></span></td>
<td><span data-ttu-id="410bc-120">Interrompe uma tarefa de desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="410bc-120">Stops a defragmentation task.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="410bc-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="410bc-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="410bc-122">Referência</span><span class="sxs-lookup"><span data-stu-id="410bc-122">Reference</span></span>

[<span data-ttu-id="410bc-123">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="410bc-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
