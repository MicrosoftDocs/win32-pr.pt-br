---
description: 'Saiba mais sobre: Enumeração SetIndexRangeGrbit'
title: Enumeração SetIndexRangeGrbit
TOCTitle: SetIndexRangeGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setindexrangegrbit(v=EXCHG.10)
ms:contentKeyID: 39515181
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.None
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInclusive
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInstantDuration
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeRemove
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeUpperLimit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInstantDuration
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeUpperLimit
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.None
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInclusive
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeRemove
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6cda73597f88d2c8fca911ebb96d7a3c6399ed9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760300"
---
# <a name="setindexrangegrbit-enumeration"></a><span data-ttu-id="dd5ed-103">Enumeração SetIndexRangeGrbit</span><span class="sxs-lookup"><span data-stu-id="dd5ed-103">SetIndexRangeGrbit enumeration</span></span>

<span data-ttu-id="dd5ed-104">Opções para JetSetIndexRange.</span><span class="sxs-lookup"><span data-stu-id="dd5ed-104">Options for JetSetIndexRange.</span></span>

<span data-ttu-id="dd5ed-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="dd5ed-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="dd5ed-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dd5ed-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dd5ed-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dd5ed-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dd5ed-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd5ed-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetIndexRangeGrbit
'Usage
Dim instance As SetIndexRangeGrbit
```

``` csharp
[FlagsAttribute]
public enum SetIndexRangeGrbit
```

## <a name="members"></a><span data-ttu-id="dd5ed-109">Membros</span><span class="sxs-lookup"><span data-stu-id="dd5ed-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="dd5ed-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="dd5ed-110">Member name</span></span></th>
<th><span data-ttu-id="dd5ed-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="dd5ed-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="dd5ed-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dd5ed-112">None</span></span></td>
<td><span data-ttu-id="dd5ed-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="dd5ed-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="dd5ed-114">RangeInclusive</span><span class="sxs-lookup"><span data-stu-id="dd5ed-114">RangeInclusive</span></span></td>
<td><span data-ttu-id="dd5ed-115">Essa opção indica que o limite do intervalo de índice é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="dd5ed-115">This option indicates that the limit of the index range is inclusive.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="dd5ed-116">RangeUpperLimit</span><span class="sxs-lookup"><span data-stu-id="dd5ed-116">RangeUpperLimit</span></span></td>
<td><span data-ttu-id="dd5ed-117">A chave de pesquisa no cursor representa os critérios de pesquisa para a entrada de índice mais próxima do final do índice que corresponderá ao intervalo de índice.</span><span class="sxs-lookup"><span data-stu-id="dd5ed-117">The search key in the cursor represents the search criteria for the index entry closest to the end of the index that will match the index range.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="dd5ed-118">RangeInstantDuration</span><span class="sxs-lookup"><span data-stu-id="dd5ed-118">RangeInstantDuration</span></span></td>
<td><span data-ttu-id="dd5ed-119">O intervalo de índice deve ser removido assim que tiver sido estabelecido.</span><span class="sxs-lookup"><span data-stu-id="dd5ed-119">The index range should be removed as soon as it has been established.</span></span> <span data-ttu-id="dd5ed-120">Isso é útil para testar a existência de entradas de índice que correspondam aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="dd5ed-120">This is useful for testing for the existence of index entries that match the search criteria.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="dd5ed-121">RangeRemove</span><span class="sxs-lookup"><span data-stu-id="dd5ed-121">RangeRemove</span></span></td>
<td><span data-ttu-id="dd5ed-122">Cancelar e intervalo de índice existente.</span><span class="sxs-lookup"><span data-stu-id="dd5ed-122">Cancel and existing index range.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="dd5ed-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd5ed-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dd5ed-124">Referência</span><span class="sxs-lookup"><span data-stu-id="dd5ed-124">Reference</span></span>

[<span data-ttu-id="dd5ed-125">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="dd5ed-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
