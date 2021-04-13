---
description: 'Saiba mais sobre: Propriedades de JET_INDEXLIST'
title: Propriedades de JET_INDEXLIST
TOCTitle: JET_INDEXLIST properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_INDEXLIST
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist_properties(v=EXCHG.10)
ms:contentKeyID: 55103599
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 7a1f500f5d51c0487ea490d2051bfc5e4639afbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104555101"
---
# <a name="jet_indexlist-properties"></a><span data-ttu-id="58e84-103">Propriedades de JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="58e84-103">JET_INDEXLIST properties</span></span>

<span data-ttu-id="58e84-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="58e84-104">Include protected members</span></span>  
<span data-ttu-id="58e84-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="58e84-105">Include inherited members</span></span>  

<span data-ttu-id="58e84-106">O tipo de [JET_INDEXLIST](./jet-indexlist-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="58e84-106">The [JET_INDEXLIST](./jet-indexlist-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="58e84-107">Propriedades</span><span class="sxs-lookup"><span data-stu-id="58e84-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="58e84-108">Nome</span><span class="sxs-lookup"><span data-stu-id="58e84-108">Name</span></span></th>
<th><span data-ttu-id="58e84-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="58e84-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="58e84-111"><a href="dn335125(v=exchg.10).md">columnidcColumn</a></span><span class="sxs-lookup"><span data-stu-id="58e84-111"><a href="dn335125(v=exchg.10).md">columnidcColumn</a></span></span></td>
<td><span data-ttu-id="58e84-112">Obtém o columnid da coluna na tabela temporária que armazena o número de colunas na chave de índice.</span><span class="sxs-lookup"><span data-stu-id="58e84-112">Gets the columnid of the column in the temporary table which stores the number of columns in the index key.</span></span> <span data-ttu-id="58e84-113">A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="58e84-113">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="58e84-115"><a href="dn335126(v=exchg.10).md">columnidcEntry</a></span><span class="sxs-lookup"><span data-stu-id="58e84-115"><a href="dn335126(v=exchg.10).md">columnidcEntry</a></span></span></td>
<td><span data-ttu-id="58e84-116">Obtém o columnid da coluna na tabela temporária que armazena o número de entradas no índice.</span><span class="sxs-lookup"><span data-stu-id="58e84-116">Gets the columnid of the column in the temporary table which stores the number of entries in the index.</span></span> <span data-ttu-id="58e84-117">Esse valor não é atual e só é atualizado por &quot; API. JetComputeStats &quot; .</span><span class="sxs-lookup"><span data-stu-id="58e84-117">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="58e84-118">A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="58e84-118">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="58e84-120"><a href="dn335127(v=exchg.10).md">columnidcKey</a></span><span class="sxs-lookup"><span data-stu-id="58e84-120"><a href="dn335127(v=exchg.10).md">columnidcKey</a></span></span></td>
<td><span data-ttu-id="58e84-121">Obtém o columnid da coluna na tabela temporária que armazena o número de chaves exclusivas no índice.</span><span class="sxs-lookup"><span data-stu-id="58e84-121">Gets the columnid of the column in the temporary table which stores the number of unique keys in the index.</span></span> <span data-ttu-id="58e84-122">Esse valor não é atual e só é atualizado por &quot; API. JetComputeStats &quot; .</span><span class="sxs-lookup"><span data-stu-id="58e84-122">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="58e84-123">A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="58e84-123">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="58e84-125"><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></span><span class="sxs-lookup"><span data-stu-id="58e84-125"><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></span></span></td>
<td><span data-ttu-id="58e84-126">Obtém o columnid da coluna na tabela temporária que armazena o tipo de coluna da coluna que está sendo indexada.</span><span class="sxs-lookup"><span data-stu-id="58e84-126">Gets the columnid of the column in the temporary table which stores the column type of the column being indexed.</span></span> <span data-ttu-id="58e84-127">A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="58e84-127">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="58e84-129"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span><span class="sxs-lookup"><span data-stu-id="58e84-129"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span></span></td>
<td><span data-ttu-id="58e84-130">Obtém o columnid da coluna na tabela temporária que armazena o columnid da coluna que está sendo indexada.</span><span class="sxs-lookup"><span data-stu-id="58e84-130">Gets the columnid of the column in the temporary table which stores the columnid of the column being indexed.</span></span> <span data-ttu-id="58e84-131">A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="58e84-131">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="58e84-133"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span><span class="sxs-lookup"><span data-stu-id="58e84-133"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span></span></td>
<td><span data-ttu-id="58e84-134">Obtém o columnid da coluna na tabela temporária que armazena o grbit que se aplica à coluna indexada.</span><span class="sxs-lookup"><span data-stu-id="58e84-134">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="58e84-135">Consulte <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="58e84-135">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="58e84-136">A coluna é do tipo <a href="hh577895(v=exchg.10).md">texto</a>.</span><span class="sxs-lookup"><span data-stu-id="58e84-136">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="58e84-138"><a href="dn335168(v=exchg.10).md">columnidCp</a></span><span class="sxs-lookup"><span data-stu-id="58e84-138"><a href="dn335168(v=exchg.10).md">columnidCp</a></span></span></td>
<td><span data-ttu-id="58e84-139">Obtém o columnid da coluna na tabela temporária que armazena a página de código da coluna indexada.</span><span class="sxs-lookup"><span data-stu-id="58e84-139">Gets the columnid of the column in the temporary table which stores the code page of the indexed column.</span></span> <span data-ttu-id="58e84-140">A coluna é do tipo <a href="hh577895(v=exchg.10).md">Short</a>.</span><span class="sxs-lookup"><span data-stu-id="58e84-140">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="58e84-142"><a href="dn335136(v=exchg.10).md">columnidcPage</a></span><span class="sxs-lookup"><span data-stu-id="58e84-142"><a href="dn335136(v=exchg.10).md">columnidcPage</a></span></span></td>
<td><span data-ttu-id="58e84-143">Obtém o columnid da coluna na tabela temporária que armazena o número de páginas no índice.</span><span class="sxs-lookup"><span data-stu-id="58e84-143">Gets the columnid of the column in the temporary table which stores the number of pages in the index.</span></span> <span data-ttu-id="58e84-144">Esse valor não é atual e só é atualizado por &quot; API. JetComputeStats &quot; .</span><span class="sxs-lookup"><span data-stu-id="58e84-144">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="58e84-145">A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="58e84-145">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="58e84-147"><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></span><span class="sxs-lookup"><span data-stu-id="58e84-147"><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></span></span></td>
<td><span data-ttu-id="58e84-148">Obtém o columnid da coluna na tabela temporária que armazena o grbit que se aplica à coluna indexada.</span><span class="sxs-lookup"><span data-stu-id="58e84-148">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="58e84-149">Consulte <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="58e84-149">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="58e84-150">A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="58e84-150">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="58e84-152"><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></span><span class="sxs-lookup"><span data-stu-id="58e84-152"><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></span></span></td>
<td><span data-ttu-id="58e84-153">Obtém o columnid da coluna na tabela temporária que armazena o grbits usado no índice.</span><span class="sxs-lookup"><span data-stu-id="58e84-153">Gets the columnid of the column in the temporary table which stores the grbits used on the index.</span></span> <span data-ttu-id="58e84-154">Consulte <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="58e84-154">See <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>.</span></span> <span data-ttu-id="58e84-155">A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="58e84-155">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="58e84-157"><a href="dn335170(v=exchg.10).md">columnidiColumn</a></span><span class="sxs-lookup"><span data-stu-id="58e84-157"><a href="dn335170(v=exchg.10).md">columnidiColumn</a></span></span></td>
<td><span data-ttu-id="58e84-158">Obtém o columnid da coluna na tabela temporária que armazena o índice dessa coluna na chave de índice.</span><span class="sxs-lookup"><span data-stu-id="58e84-158">Gets the columnid of the column in the temporary table which stores the index of of this column in the index key.</span></span> <span data-ttu-id="58e84-159">A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="58e84-159">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="58e84-161"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span><span class="sxs-lookup"><span data-stu-id="58e84-161"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span></span></td>
<td><span data-ttu-id="58e84-162">Obtém o columnid da coluna na tabela temporária que armazena o nome do índice.</span><span class="sxs-lookup"><span data-stu-id="58e84-162">Gets the columnid of the column in the temporary table which stores the name of the index.</span></span> <span data-ttu-id="58e84-163">A coluna é do tipo <a href="hh577895(v=exchg.10).md">texto</a>.</span><span class="sxs-lookup"><span data-stu-id="58e84-163">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="58e84-165"><a href="dn335171(v=exchg.10).md">columnidLangid</a></span><span class="sxs-lookup"><span data-stu-id="58e84-165"><a href="dn335171(v=exchg.10).md">columnidLangid</a></span></span></td>
<td><span data-ttu-id="58e84-166">Obtém o columnid da coluna na tabela temporária que armazena a ID de idioma (LCID) do índice.</span><span class="sxs-lookup"><span data-stu-id="58e84-166">Gets the columnid of the column in the temporary table which stores the language id (LCID) of the index.</span></span> <span data-ttu-id="58e84-167">A coluna é do tipo <a href="hh577895(v=exchg.10).md">Short</a>.</span><span class="sxs-lookup"><span data-stu-id="58e84-167">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="58e84-169"><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></span><span class="sxs-lookup"><span data-stu-id="58e84-169"><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></span></span></td>
<td><span data-ttu-id="58e84-170">Obtém o columnid da coluna na tabela temporária que armazena os sinalizadores de normalização Unicode para o índice.</span><span class="sxs-lookup"><span data-stu-id="58e84-170">Gets the columnid of the column in the temporary table which stores the unicode normalization flags for the index.</span></span> <span data-ttu-id="58e84-171">A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="58e84-171">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="58e84-173"><a href="dn335173(v=exchg.10).md">cRecord</a></span><span class="sxs-lookup"><span data-stu-id="58e84-173"><a href="dn335173(v=exchg.10).md">cRecord</a></span></span></td>
<td><span data-ttu-id="58e84-174">Obtém o número de registros na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="58e84-174">Gets the number of records in the temporary table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="58e84-176"><a href="dn335174(v=exchg.10).md">TableID</a></span><span class="sxs-lookup"><span data-stu-id="58e84-176"><a href="dn335174(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="58e84-177">Obtém TableName da tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="58e84-177">Gets tableid of the temporary table.</span></span> <span data-ttu-id="58e84-178">Isso deve ser fechado quando a tabela não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="58e84-178">This should be closed when the table is no longer needed.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="58e84-179">Parte superior</span><span class="sxs-lookup"><span data-stu-id="58e84-179">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="58e84-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="58e84-180">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="58e84-181">Referência</span><span class="sxs-lookup"><span data-stu-id="58e84-181">Reference</span></span>

[<span data-ttu-id="58e84-182">Classe JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="58e84-182">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="58e84-183">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="58e84-183">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
