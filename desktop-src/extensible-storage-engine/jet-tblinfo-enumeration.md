---
description: 'Saiba mais sobre: enumeração de JET_TblInfo'
title: Enumeração de JET_TblInfo
TOCTitle: JET_TblInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_TblInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tblinfo(v=EXCHG.10)
ms:contentKeyID: 39512198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad43dcecf65fdc9fb8dd53bdf686a077e6bdfa8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788905"
---
# <a name="jet_tblinfo-enumeration"></a><span data-ttu-id="2f81e-103">Enumeração de JET_TblInfo</span><span class="sxs-lookup"><span data-stu-id="2f81e-103">JET_TblInfo enumeration</span></span>

<span data-ttu-id="2f81e-104">Níveis de informações para recuperar informações de tabela com JetGetTableInfo.</span><span class="sxs-lookup"><span data-stu-id="2f81e-104">Info levels for retrieving table info with JetGetTableInfo.</span></span>

<span data-ttu-id="2f81e-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2f81e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2f81e-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2f81e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2f81e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f81e-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_TblInfo
'Usage
Dim instance As JET_TblInfo
```

``` csharp
public enum JET_TblInfo
```

## <a name="members"></a><span data-ttu-id="2f81e-108">Membros</span><span class="sxs-lookup"><span data-stu-id="2f81e-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="2f81e-109">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="2f81e-109">Member name</span></span></th>
<th><span data-ttu-id="2f81e-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="2f81e-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="2f81e-111">Padrão</span><span class="sxs-lookup"><span data-stu-id="2f81e-111">Default</span></span></td>
<td><span data-ttu-id="2f81e-112">Opção padrão.</span><span class="sxs-lookup"><span data-stu-id="2f81e-112">Default option.</span></span> <span data-ttu-id="2f81e-113">Recupera um <a href="dn335219(v=exchg.10).md">JET_OBJECTINFO</a> que contém informações sobre a tabela.</span><span class="sxs-lookup"><span data-stu-id="2f81e-113">Retrieves a <a href="dn335219(v=exchg.10).md">JET_OBJECTINFO</a> containing information about the table.</span></span> <span data-ttu-id="2f81e-114">Use essa opção com <a href="dn292198(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, JET_OBJECTINFO JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="2f81e-114">Use this option with <a href="dn292198(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="2f81e-115">Nome</span><span class="sxs-lookup"><span data-stu-id="2f81e-115">Name</span></span></td>
<td><span data-ttu-id="2f81e-116">Recupera o nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="2f81e-116">Retrieves the name of the table.</span></span> <span data-ttu-id="2f81e-117">Use essa opção com <a href="dn292204(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, String JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="2f81e-117">Use this option with <a href="dn292204(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="2f81e-118">DBID</span><span class="sxs-lookup"><span data-stu-id="2f81e-118">Dbid</span></span></td>
<td><span data-ttu-id="2f81e-119">Recupera o <a href="hh596176(v=exchg.10).md">JET_DBID</a> do banco de dados que contém a tabela.</span><span class="sxs-lookup"><span data-stu-id="2f81e-119">Retrieves the <a href="hh596176(v=exchg.10).md">JET_DBID</a> of the database containing the table.</span></span> <span data-ttu-id="2f81e-120">Use essa opção com <a href="dn292197(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, JET_DBID JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="2f81e-120">Use this option with <a href="dn292197(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="2f81e-121">SpaceUsage</span><span class="sxs-lookup"><span data-stu-id="2f81e-121">SpaceUsage</span></span></td>
<td><span data-ttu-id="2f81e-122">O comportamento do método depende do tamanho da matriz que é passada para o método.</span><span class="sxs-lookup"><span data-stu-id="2f81e-122">The behavior of the method depends on how large the array that is passed to the method is.</span></span> <span data-ttu-id="2f81e-123">A matriz deve ter pelo menos duas entradas.</span><span class="sxs-lookup"><span data-stu-id="2f81e-123">The array must have at least two entries.</span></span> <span data-ttu-id="2f81e-124">A primeira entrada conterá o número de extensões de propriedade na tabela.</span><span class="sxs-lookup"><span data-stu-id="2f81e-124">The first entry will contain the number of Owned Extents in the table.</span></span> <span data-ttu-id="2f81e-125">A segunda entrada conterá o número de extensões disponíveis na tabela.</span><span class="sxs-lookup"><span data-stu-id="2f81e-125">The second entry will contain the number of Available Extents in the table.</span></span> <span data-ttu-id="2f81e-126">Se a matriz tiver mais de duas entradas, os bytes restantes do buffer consistirão em uma matriz de estruturas que representa uma lista de extensões.</span><span class="sxs-lookup"><span data-stu-id="2f81e-126">If the array has more than two entries then the remaining bytes of the buffer will consist of an array of structures that represent a list of extents.</span></span> <span data-ttu-id="2f81e-127">Essa estrutura contém dois membros: o número da última página na extensão e o número de páginas na extensão.</span><span class="sxs-lookup"><span data-stu-id="2f81e-127">This structure contains two members: the last page number in the extent and the number of pages in the extent.</span></span> <span data-ttu-id="2f81e-128">Use essa opção com <a href="dn292202(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="2f81e-128">Use this option with <a href="dn292202(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="2f81e-129">SpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="2f81e-129">SpaceAlloc</span></span></td>
<td><span data-ttu-id="2f81e-130">A matriz passada para JetGetTableInfo deve ter duas entradas.</span><span class="sxs-lookup"><span data-stu-id="2f81e-130">The array passed to JetGetTableInfo must have two entries.</span></span> <span data-ttu-id="2f81e-131">A primeira entrada será definida como o número de páginas na tabela.</span><span class="sxs-lookup"><span data-stu-id="2f81e-131">The first entry will be set to the number of pages in the table.</span></span> <span data-ttu-id="2f81e-132">A segunda entrada será definida como a densidade de página de destino da tabela.</span><span class="sxs-lookup"><span data-stu-id="2f81e-132">The second entry will be set to the target density of pages for the table.</span></span> <span data-ttu-id="2f81e-133">Use essa opção com <a href="dn292202(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="2f81e-133">Use this option with <a href="dn292202(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="2f81e-134">SpaceOwned</span><span class="sxs-lookup"><span data-stu-id="2f81e-134">SpaceOwned</span></span></td>
<td><span data-ttu-id="2f81e-135">Obtém o número de páginas de propriedade da tabela.</span><span class="sxs-lookup"><span data-stu-id="2f81e-135">Gets the number of owned pages in the table.</span></span> <span data-ttu-id="2f81e-136">Use essa opção com <a href="dn292201(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, Int32 JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="2f81e-136">Use this option with <a href="dn292201(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="2f81e-137">SpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="2f81e-137">SpaceAvailable</span></span></td>
<td><span data-ttu-id="2f81e-138">Obtém o número de páginas disponíveis na tabela.</span><span class="sxs-lookup"><span data-stu-id="2f81e-138">Gets the number of available pages in the table.</span></span> <span data-ttu-id="2f81e-139">Use essa opção com <a href="dn292201(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, Int32 JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="2f81e-139">Use this option with <a href="dn292201(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="2f81e-140">TemplateTableName</span><span class="sxs-lookup"><span data-stu-id="2f81e-140">TemplateTableName</span></span></td>
<td><span data-ttu-id="2f81e-141">Se a tabela for uma tabela derivada, o resultado será preenchido com o nome da tabela da qual a tabela derivada herdou sua DDL.</span><span class="sxs-lookup"><span data-stu-id="2f81e-141">If the table is a derived table, the result will be filled in with the name of the table from which the derived table inherited its DDL.</span></span> <span data-ttu-id="2f81e-142">Se a tabela não for uma tabela derivada, o buffer será uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="2f81e-142">If the table is not a derived table, the buffer will an empty string.</span></span> <span data-ttu-id="2f81e-143">Use essa opção com <a href="dn292204(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, String JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="2f81e-143">Use this option with <a href="dn292204(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="2f81e-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f81e-144">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2f81e-145">Referência</span><span class="sxs-lookup"><span data-stu-id="2f81e-145">Reference</span></span>

[<span data-ttu-id="2f81e-146">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="2f81e-146">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
