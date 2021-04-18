---
description: 'Saiba mais sobre: enumeração de JET_IdxInfo'
title: Enumeração de JET_IdxInfo
TOCTitle: JET_IdxInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_IdxInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_idxinfo(v=EXCHG.10)
ms:contentKeyID: 39512789
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.VarSegMac
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.KeyMost
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.IndexId
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SysTabCursor
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.OLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Default
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.ResetOLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Langid
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.List
- Microsoft.Isam.Esent.Interop.JET_IdxInfo
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Count
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.IndexId
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_IdxInfo
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.List
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.VarSegMac
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.KeyMost
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.OLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.ResetOLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SysTabCursor
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Count
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Default
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Langid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e1f2cb50537ed492a428c82fd9a6f6541c5fad2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798195"
---
# <a name="jet_idxinfo-enumeration"></a><span data-ttu-id="ab257-103">Enumeração de JET_IdxInfo</span><span class="sxs-lookup"><span data-stu-id="ab257-103">JET_IdxInfo enumeration</span></span>

<span data-ttu-id="ab257-104">Níveis de informações para recuperar informações de índice com JetGetIndexInfo.</span><span class="sxs-lookup"><span data-stu-id="ab257-104">Info levels for retrieve index information with JetGetIndexInfo.</span></span> <span data-ttu-id="ab257-105">e JetGetTableIndexInfo.</span><span class="sxs-lookup"><span data-stu-id="ab257-105">and JetGetTableIndexInfo.</span></span>

<span data-ttu-id="ab257-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ab257-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ab257-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ab257-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ab257-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab257-108">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_IdxInfo
'Usage
Dim instance As JET_IdxInfo
```

``` csharp
public enum JET_IdxInfo
```

## <a name="members"></a><span data-ttu-id="ab257-109">Membros</span><span class="sxs-lookup"><span data-stu-id="ab257-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="ab257-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="ab257-110">Member name</span></span></th>
<th><span data-ttu-id="ab257-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab257-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ab257-112">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab257-112">Default</span></span></td>
<td><span data-ttu-id="ab257-113">Retorna uma estrutura de <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> com informações sobre o índice.</span><span class="sxs-lookup"><span data-stu-id="ab257-113">Returns a <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> structure with information about the index.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ab257-114">Lista</span><span class="sxs-lookup"><span data-stu-id="ab257-114">List</span></span></td>
<td><span data-ttu-id="ab257-115">Retorna uma estrutura de <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> com informações sobre o índice.</span><span class="sxs-lookup"><span data-stu-id="ab257-115">Returns a <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> structure with information about the index.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ab257-116">SysTabCursor</span><span class="sxs-lookup"><span data-stu-id="ab257-116">SysTabCursor</span></span></td>
<td><span data-ttu-id="ab257-117"><strong>Obsoleto.</strong></span><span class="sxs-lookup"><span data-stu-id="ab257-117"><strong>Obsolete.</strong></span></span> <span data-ttu-id="ab257-118">SysTabCursor é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="ab257-118">SysTabCursor is obsolete.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ab257-119">OLC</span><span class="sxs-lookup"><span data-stu-id="ab257-119">OLC</span></span></td>
<td><span data-ttu-id="ab257-120"><strong>Obsoleto.</strong></span><span class="sxs-lookup"><span data-stu-id="ab257-120"><strong>Obsolete.</strong></span></span> <span data-ttu-id="ab257-121">OLC é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="ab257-121">OLC is obsolete.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ab257-122">ResetOLC</span><span class="sxs-lookup"><span data-stu-id="ab257-122">ResetOLC</span></span></td>
<td><span data-ttu-id="ab257-123"><strong>Obsoleto.</strong></span><span class="sxs-lookup"><span data-stu-id="ab257-123"><strong>Obsolete.</strong></span></span> <span data-ttu-id="ab257-124">Reset OLC é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="ab257-124">Reset OLC is obsolete.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ab257-125">SpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="ab257-125">SpaceAlloc</span></span></td>
<td><span data-ttu-id="ab257-126">Retorna um inteiro com o uso de espaço do índice.</span><span class="sxs-lookup"><span data-stu-id="ab257-126">Returns an integer with the space usage of the index.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ab257-127">LCID</span><span class="sxs-lookup"><span data-stu-id="ab257-127">LCID</span></span></td>
<td><span data-ttu-id="ab257-128">Retorna um inteiro com o LCID do índice.</span><span class="sxs-lookup"><span data-stu-id="ab257-128">Returns an integer with the LCID of the index.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ab257-129">LangID</span><span class="sxs-lookup"><span data-stu-id="ab257-129">Langid</span></span></td>
<td><span data-ttu-id="ab257-130"><strong>Obsoleto.</strong></span><span class="sxs-lookup"><span data-stu-id="ab257-130"><strong>Obsolete.</strong></span></span> <span data-ttu-id="ab257-131">O LANGID está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="ab257-131">Langid is obsolete.</span></span> <span data-ttu-id="ab257-132">Em vez disso, use LCID.</span><span class="sxs-lookup"><span data-stu-id="ab257-132">Use LCID instead.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ab257-133">Contagem</span><span class="sxs-lookup"><span data-stu-id="ab257-133">Count</span></span></td>
<td><span data-ttu-id="ab257-134">Retorna um inteiro com a contagem de índices na tabela.</span><span class="sxs-lookup"><span data-stu-id="ab257-134">Returns an integer with the count of indexes in the table.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ab257-135">VarSegMac</span><span class="sxs-lookup"><span data-stu-id="ab257-135">VarSegMac</span></span></td>
<td><span data-ttu-id="ab257-136">Retorna um UShort com o valor de cbVarSegMac com o qual o índice foi criado.</span><span class="sxs-lookup"><span data-stu-id="ab257-136">Returns a ushort with the value of cbVarSegMac the index was created with.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ab257-137">IndexId</span><span class="sxs-lookup"><span data-stu-id="ab257-137">IndexId</span></span></td>
<td><span data-ttu-id="ab257-138">Retorna um <a href="hh557060(v=exchg.10).md">JET_INDEXID</a> identificando o índice.</span><span class="sxs-lookup"><span data-stu-id="ab257-138">Returns a <a href="hh557060(v=exchg.10).md">JET_INDEXID</a> identifying the index.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ab257-139">Mais</span><span class="sxs-lookup"><span data-stu-id="ab257-139">KeyMost</span></span></td>
<td><span data-ttu-id="ab257-140">Introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ab257-140">Introduced in Windows Vista.</span></span> <span data-ttu-id="ab257-141">Retorna um UShort com o valor de cbKeyMost com o qual o índice foi criado.</span><span class="sxs-lookup"><span data-stu-id="ab257-141">Returns a ushort with the value of cbKeyMost the index was created with.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="ab257-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab257-142">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ab257-143">Referência</span><span class="sxs-lookup"><span data-stu-id="ab257-143">Reference</span></span>

[<span data-ttu-id="ab257-144">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ab257-144">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
