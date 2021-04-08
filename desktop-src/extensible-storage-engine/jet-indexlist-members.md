---
description: 'Saiba mais sobre: membros do JET_INDEXLIST'
title: Membros do JET_INDEXLIST
TOCTitle: JET_INDEXLIST members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INDEXLIST
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist_members(v=EXCHG.10)
ms:contentKeyID: 55103660
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d7800ef911366bad40b2d02ee60e23b5d138d30c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011576"
---
# <a name="jet_indexlist-members"></a><span data-ttu-id="b0e95-103">Membros do JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="b0e95-103">JET_INDEXLIST members</span></span>

<span data-ttu-id="b0e95-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="b0e95-104">Include protected members</span></span>  
<span data-ttu-id="b0e95-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="b0e95-105">Include inherited members</span></span>  

<span data-ttu-id="b0e95-106">Informações sobre uma tabela temporária que contém informações sobre todos os índices de uma determinada tabela.</span><span class="sxs-lookup"><span data-stu-id="b0e95-106">Information about a temporary table containing information about all indexes for a given table.</span></span>

<span data-ttu-id="b0e95-107">O tipo de [JET_INDEXLIST](./jet-indexlist-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="b0e95-107">The [JET_INDEXLIST](./jet-indexlist-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="b0e95-108">Construtores</span><span class="sxs-lookup"><span data-stu-id="b0e95-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="b0e95-109">Nome</span><span class="sxs-lookup"><span data-stu-id="b0e95-109">Name</span></span></th>
<th><span data-ttu-id="b0e95-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0e95-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="b0e95-112"><a href="dn335166(v=exchg.10).md">JET_INDEXLIST</a></span><span class="sxs-lookup"><span data-stu-id="b0e95-112"><a href="dn335166(v=exchg.10).md">JET_INDEXLIST</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b0e95-113">Parte superior</span><span class="sxs-lookup"><span data-stu-id="b0e95-113">Top</span></span>

## <a name="properties"></a><span data-ttu-id="b0e95-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b0e95-114">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="b0e95-115">Nome</span><span class="sxs-lookup"><span data-stu-id="b0e95-115">Name</span></span></th>
<th><span data-ttu-id="b0e95-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0e95-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b0e95-118"><a href="dn335125(v=exchg.10).md">columnidcColumn</a></span><span class="sxs-lookup"><span data-stu-id="b0e95-118"><a href="dn335125(v=exchg.10).md">columnidcColumn</a></span></span></td>
<td><span data-ttu-id="b0e95-119">Obtém o columnid da coluna na tabela temporária que armazena o número de colunas na chave de índice.</span><span class="sxs-lookup"><span data-stu-id="b0e95-119">Gets the columnid of the column in the temporary table which stores the number of columns in the index key.</span></span> <span data-ttu-id="b0e95-120">A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="b0e95-120">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b0e95-122"><a href="dn335126(v=exchg.10).md">columnidcEntry</a></span><span class="sxs-lookup"><span data-stu-id="b0e95-122"><a href="dn335126(v=exchg.10).md">columnidcEntry</a></span></span></td>
<td><span data-ttu-id="b0e95-123">Obtém o columnid da coluna na tabela temporária que armazena o número de entradas no índice.</span><span class="sxs-lookup"><span data-stu-id="b0e95-123">Gets the columnid of the column in the temporary table which stores the number of entries in the index.</span></span> <span data-ttu-id="b0e95-124">Esse valor não é atual e só é atualizado por &quot; API. JetComputeStats &quot; .</span><span class="sxs-lookup"><span data-stu-id="b0e95-124">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="b0e95-125">A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="b0e95-125">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b0e95-127"><a href="dn335127(v=exchg.10).md">columnidcKey</a></span><span class="sxs-lookup"><span data-stu-id="b0e95-127"><a href="dn335127(v=exchg.10).md">columnidcKey</a></span></span></td>
<td><span data-ttu-id="b0e95-128">Obtém o columnid da coluna na tabela temporária que armazena o número de chaves exclusivas no índice.</span><span class="sxs-lookup"><span data-stu-id="b0e95-128">Gets the columnid of the column in the temporary table which stores the number of unique keys in the index.</span></span> <span data-ttu-id="b0e95-129">Esse valor não é atual e só é atualizado por &quot; API. JetComputeStats &quot; .</span><span class="sxs-lookup"><span data-stu-id="b0e95-129">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="b0e95-130">A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="b0e95-130">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b0e95-132"><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></span><span class="sxs-lookup"><span data-stu-id="b0e95-132"><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></span></span></td>
<td><span data-ttu-id="b0e95-133">Obtém o columnid da coluna na tabela temporária que armazena o tipo de coluna da coluna que está sendo indexada.</span><span class="sxs-lookup"><span data-stu-id="b0e95-133">Gets the columnid of the column in the temporary table which stores the column type of the column being indexed.</span></span> <span data-ttu-id="b0e95-134">A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="b0e95-134">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b0e95-136"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span><span class="sxs-lookup"><span data-stu-id="b0e95-136"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span></span></td>
<td><span data-ttu-id="b0e95-137">Obtém o columnid da coluna na tabela temporária que armazena o columnid da coluna que está sendo indexada.</span><span class="sxs-lookup"><span data-stu-id="b0e95-137">Gets the columnid of the column in the temporary table which stores the columnid of the column being indexed.</span></span> <span data-ttu-id="b0e95-138">A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="b0e95-138">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b0e95-140"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span><span class="sxs-lookup"><span data-stu-id="b0e95-140"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span></span></td>
<td><span data-ttu-id="b0e95-141">Obtém o columnid da coluna na tabela temporária que armazena o grbit que se aplica à coluna indexada.</span><span class="sxs-lookup"><span data-stu-id="b0e95-141">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="b0e95-142">Consulte <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="b0e95-142">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="b0e95-143">A coluna é do tipo <a href="hh577895(v=exchg.10).md">texto</a>.</span><span class="sxs-lookup"><span data-stu-id="b0e95-143">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b0e95-145"><a href="dn335168(v=exchg.10).md">columnidCp</a></span><span class="sxs-lookup"><span data-stu-id="b0e95-145"><a href="dn335168(v=exchg.10).md">columnidCp</a></span></span></td>
<td><span data-ttu-id="b0e95-146">Obtém o columnid da coluna na tabela temporária que armazena a página de código da coluna indexada.</span><span class="sxs-lookup"><span data-stu-id="b0e95-146">Gets the columnid of the column in the temporary table which stores the code page of the indexed column.</span></span> <span data-ttu-id="b0e95-147">A coluna é do tipo <a href="hh577895(v=exchg.10).md">Short</a>.</span><span class="sxs-lookup"><span data-stu-id="b0e95-147">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b0e95-149"><a href="dn335136(v=exchg.10).md">columnidcPage</a></span><span class="sxs-lookup"><span data-stu-id="b0e95-149"><a href="dn335136(v=exchg.10).md">columnidcPage</a></span></span></td>
<td><span data-ttu-id="b0e95-150">Obtém o columnid da coluna na tabela temporária que armazena o número de páginas no índice.</span><span class="sxs-lookup"><span data-stu-id="b0e95-150">Gets the columnid of the column in the temporary table which stores the number of pages in the index.</span></span> <span data-ttu-id="b0e95-151">Esse valor não é atual e só é atualizado por &quot; API. JetComputeStats &quot; .</span><span class="sxs-lookup"><span data-stu-id="b0e95-151">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="b0e95-152">A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="b0e95-152">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b0e95-154"><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></span><span class="sxs-lookup"><span data-stu-id="b0e95-154"><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></span></span></td>
<td><span data-ttu-id="b0e95-155">Obtém o columnid da coluna na tabela temporária que armazena o grbit que se aplica à coluna indexada.</span><span class="sxs-lookup"><span data-stu-id="b0e95-155">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="b0e95-156">Consulte <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="b0e95-156">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="b0e95-157">A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="b0e95-157">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b0e95-159"><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></span><span class="sxs-lookup"><span data-stu-id="b0e95-159"><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></span></span></td>
<td><span data-ttu-id="b0e95-160">Obtém o columnid da coluna na tabela temporária que armazena o grbits usado no índice.</span><span class="sxs-lookup"><span data-stu-id="b0e95-160">Gets the columnid of the column in the temporary table which stores the grbits used on the index.</span></span> <span data-ttu-id="b0e95-161">Consulte <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="b0e95-161">See <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>.</span></span> <span data-ttu-id="b0e95-162">A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="b0e95-162">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b0e95-164"><a href="dn335170(v=exchg.10).md">columnidiColumn</a></span><span class="sxs-lookup"><span data-stu-id="b0e95-164"><a href="dn335170(v=exchg.10).md">columnidiColumn</a></span></span></td>
<td><span data-ttu-id="b0e95-165">Obtém o columnid da coluna na tabela temporária que armazena o índice dessa coluna na chave de índice.</span><span class="sxs-lookup"><span data-stu-id="b0e95-165">Gets the columnid of the column in the temporary table which stores the index of of this column in the index key.</span></span> <span data-ttu-id="b0e95-166">A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="b0e95-166">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b0e95-168"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span><span class="sxs-lookup"><span data-stu-id="b0e95-168"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span></span></td>
<td><span data-ttu-id="b0e95-169">Obtém o columnid da coluna na tabela temporária que armazena o nome do índice.</span><span class="sxs-lookup"><span data-stu-id="b0e95-169">Gets the columnid of the column in the temporary table which stores the name of the index.</span></span> <span data-ttu-id="b0e95-170">A coluna é do tipo <a href="hh577895(v=exchg.10).md">texto</a>.</span><span class="sxs-lookup"><span data-stu-id="b0e95-170">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b0e95-172"><a href="dn335171(v=exchg.10).md">columnidLangid</a></span><span class="sxs-lookup"><span data-stu-id="b0e95-172"><a href="dn335171(v=exchg.10).md">columnidLangid</a></span></span></td>
<td><span data-ttu-id="b0e95-173">Obtém o columnid da coluna na tabela temporária que armazena a ID de idioma (LCID) do índice.</span><span class="sxs-lookup"><span data-stu-id="b0e95-173">Gets the columnid of the column in the temporary table which stores the language id (LCID) of the index.</span></span> <span data-ttu-id="b0e95-174">A coluna é do tipo <a href="hh577895(v=exchg.10).md">Short</a>.</span><span class="sxs-lookup"><span data-stu-id="b0e95-174">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b0e95-176"><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></span><span class="sxs-lookup"><span data-stu-id="b0e95-176"><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></span></span></td>
<td><span data-ttu-id="b0e95-177">Obtém o columnid da coluna na tabela temporária que armazena os sinalizadores de normalização Unicode para o índice.</span><span class="sxs-lookup"><span data-stu-id="b0e95-177">Gets the columnid of the column in the temporary table which stores the unicode normalization flags for the index.</span></span> <span data-ttu-id="b0e95-178">A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="b0e95-178">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b0e95-180"><a href="dn335173(v=exchg.10).md">cRecord</a></span><span class="sxs-lookup"><span data-stu-id="b0e95-180"><a href="dn335173(v=exchg.10).md">cRecord</a></span></span></td>
<td><span data-ttu-id="b0e95-181">Obtém o número de registros na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="b0e95-181">Gets the number of records in the temporary table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b0e95-183"><a href="dn335174(v=exchg.10).md">TableID</a></span><span class="sxs-lookup"><span data-stu-id="b0e95-183"><a href="dn335174(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="b0e95-184">Obtém TableName da tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="b0e95-184">Gets tableid of the temporary table.</span></span> <span data-ttu-id="b0e95-185">Isso deve ser fechado quando a tabela não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="b0e95-185">This should be closed when the table is no longer needed.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b0e95-186">Parte superior</span><span class="sxs-lookup"><span data-stu-id="b0e95-186">Top</span></span>

## <a name="methods"></a><span data-ttu-id="b0e95-187">Métodos</span><span class="sxs-lookup"><span data-stu-id="b0e95-187">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="b0e95-188">Nome</span><span class="sxs-lookup"><span data-stu-id="b0e95-188">Name</span></span></th>
<th><span data-ttu-id="b0e95-189">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0e95-189">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="b0e95-191"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Igual a</a></span><span class="sxs-lookup"><span data-stu-id="b0e95-191"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="b0e95-192">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="b0e95-192">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="b0e95-194"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizar</a></span><span class="sxs-lookup"><span data-stu-id="b0e95-194"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="b0e95-195">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="b0e95-195">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="b0e95-197"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="b0e95-197"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="b0e95-198">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="b0e95-198">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="b0e95-200"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="b0e95-200"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="b0e95-201">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="b0e95-201">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="b0e95-203"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="b0e95-203"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="b0e95-204">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="b0e95-204">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="b0e95-206"><a href="dn335165(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="b0e95-206"><a href="dn335165(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="b0e95-207">Retorna uma <a href="/dotnet/api/system.string">cadeia de caracteres</a> que representa a <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a>atual.</span><span class="sxs-lookup"><span data-stu-id="b0e95-207">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a>.</span></span> <span data-ttu-id="b0e95-208">(Substitui <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="b0e95-208">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b0e95-209">Parte superior</span><span class="sxs-lookup"><span data-stu-id="b0e95-209">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="b0e95-210">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0e95-210">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b0e95-211">Referência</span><span class="sxs-lookup"><span data-stu-id="b0e95-211">Reference</span></span>

[<span data-ttu-id="b0e95-212">Classe JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="b0e95-212">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="b0e95-213">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b0e95-213">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
