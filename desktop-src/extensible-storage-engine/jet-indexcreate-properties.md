---
description: 'Saiba mais sobre: Propriedades de JET_INDEXCREATE'
title: Propriedades de JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_properties(v=EXCHG.10)
ms:contentKeyID: 55103645
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 66b6ada105e6f6d12cb754f288478e85d75a07e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922576"
---
# <a name="jet_indexcreate-properties"></a><span data-ttu-id="8819c-103">Propriedades de JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="8819c-103">JET_INDEXCREATE properties</span></span>

<span data-ttu-id="8819c-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="8819c-104">Include protected members</span></span>  
<span data-ttu-id="8819c-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="8819c-105">Include inherited members</span></span>  

<span data-ttu-id="8819c-106">O tipo de [JET_INDEXCREATE](./jet-indexcreate-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="8819c-106">The [JET_INDEXCREATE](./jet-indexcreate-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="8819c-107">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8819c-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="8819c-108">Nome</span><span class="sxs-lookup"><span data-stu-id="8819c-108">Name</span></span></th>
<th><span data-ttu-id="8819c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="8819c-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="8819c-111"><a href="dn335122(v=exchg.10).md">cbKey</a></span><span class="sxs-lookup"><span data-stu-id="8819c-111"><a href="dn335122(v=exchg.10).md">cbKey</a></span></span></td>
<td><span data-ttu-id="8819c-112">Obtém ou define o comprimento, em caracteres, de szKey, incluindo os dois nulos de terminação.</span><span class="sxs-lookup"><span data-stu-id="8819c-112">Gets or sets the length, in characters, of szKey including the two terminating nulls.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="8819c-114"><a href="dn335156(v=exchg.10).md">cbKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="8819c-114"><a href="dn335156(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="8819c-115">Obtém ou define o tamanho máximo permitido, em bytes, para as chaves no índice.</span><span class="sxs-lookup"><span data-stu-id="8819c-115">Gets or sets the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="8819c-116">O tamanho mínimo de chave máximo suportado é JET_cbKeyMostMin (255), que é o tamanho de chave máximo herdado.</span><span class="sxs-lookup"><span data-stu-id="8819c-116">The minimum supported maximum key size is JET_cbKeyMostMin (255) which is the legacy maximum key size.</span></span> <span data-ttu-id="8819c-117">O tamanho máximo da chave depende do tamanho da página do banco de dados <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span><span class="sxs-lookup"><span data-stu-id="8819c-117">The maximum key size is dependent on the database page size <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="8819c-118">O tamanho máximo da chave pode ser recuperado com o <a href="dn351156(v=exchg.10).md">máximo</a>.</span><span class="sxs-lookup"><span data-stu-id="8819c-118">The maximum key size can be retrieved with <a href="dn351156(v=exchg.10).md">KeyMost</a>.</span></span> <span data-ttu-id="8819c-119">Esse parâmetro é ignorado no Windows XP e no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8819c-119">This parameter is ignored on Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="8819c-120">Diferentemente da API não gerenciada, <strong>IndexKeyMost ()</strong> (JET_bitIndexKeyMost) não é necessária, ela será adicionada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8819c-120">Unlike the unmanaged API, <strong>IndexKeyMost()</strong> (JET_bitIndexKeyMost) is not needed, it will be added automatically.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="8819c-122"><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></span><span class="sxs-lookup"><span data-stu-id="8819c-122"><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="8819c-123">Obtém ou define o comprimento máximo, em bytes, de cada coluna a ser armazenada no índice.</span><span class="sxs-lookup"><span data-stu-id="8819c-123">Gets or sets the maximum length, in bytes, of each column to store in the index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="8819c-125"><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></span><span class="sxs-lookup"><span data-stu-id="8819c-125"><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></span></span></td>
<td><span data-ttu-id="8819c-126">Obtém ou define o número de colunas condicionais.</span><span class="sxs-lookup"><span data-stu-id="8819c-126">Gets or sets the number of conditional columns.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="8819c-128"><a href="dn335157(v=exchg.10).md">erra</a></span><span class="sxs-lookup"><span data-stu-id="8819c-128"><a href="dn335157(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="8819c-129">Obtém ou define o código de erro da criação deste índice.</span><span class="sxs-lookup"><span data-stu-id="8819c-129">Gets or sets the error code from creating this index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="8819c-131"><a href="dn335119(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="8819c-131"><a href="dn335119(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="8819c-132">Obtém ou define as opções de criação de índice.</span><span class="sxs-lookup"><span data-stu-id="8819c-132">Gets or sets index creation options.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="8819c-134"><a href="dn335159(v=exchg.10).md">pidxUnicode</a></span><span class="sxs-lookup"><span data-stu-id="8819c-134"><a href="dn335159(v=exchg.10).md">pidxUnicode</a></span></span></td>
<td><span data-ttu-id="8819c-135">Obtém ou define as opções de comparação Unicode opcionais.</span><span class="sxs-lookup"><span data-stu-id="8819c-135">Gets or sets the optional unicode comparison options.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="8819c-137"><a href="dn335120(v=exchg.10).md">pSpaceHints</a></span><span class="sxs-lookup"><span data-stu-id="8819c-137"><a href="dn335120(v=exchg.10).md">pSpaceHints</a></span></span></td>
<td><span data-ttu-id="8819c-138">Obtém ou define as dicas de alocação, manutenção e uso de espaço.</span><span class="sxs-lookup"><span data-stu-id="8819c-138">Gets or sets space allocation, maintenance, and usage hints.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="8819c-140"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span><span class="sxs-lookup"><span data-stu-id="8819c-140"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span></span></td>
<td><span data-ttu-id="8819c-141">Obtém ou define as colunas condicionais opcionais.</span><span class="sxs-lookup"><span data-stu-id="8819c-141">Gets or sets the optional conditional columns.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="8819c-143"><a href="dn335121(v=exchg.10).md">szIndexName</a></span><span class="sxs-lookup"><span data-stu-id="8819c-143"><a href="dn335121(v=exchg.10).md">szIndexName</a></span></span></td>
<td><span data-ttu-id="8819c-144">Obtém ou define o nome do índice a ser criado.</span><span class="sxs-lookup"><span data-stu-id="8819c-144">Gets or sets the name of the index to create.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="8819c-146"><a href="dn335161(v=exchg.10).md">szKey</a></span><span class="sxs-lookup"><span data-stu-id="8819c-146"><a href="dn335161(v=exchg.10).md">szKey</a></span></span></td>
<td><span data-ttu-id="8819c-147">Obtém ou define a descrição da chave de índice.</span><span class="sxs-lookup"><span data-stu-id="8819c-147">Gets or sets the description of the index key.</span></span> <span data-ttu-id="8819c-148">Essa é uma cadeia de caracteres dupla com terminação nula de tokens delimitados por nulo.</span><span class="sxs-lookup"><span data-stu-id="8819c-148">This is a double null-terminated string of null-delimited tokens.</span></span> <span data-ttu-id="8819c-149">Cada token tem o formato [Direction-especificador] [nome-da-coluna], onde a especificação de direção é &quot; + &quot; ou &quot; - &quot; .</span><span class="sxs-lookup"><span data-stu-id="8819c-149">Each token is of the form [direction-specifier][column-name], where direction-specification is either &quot;+&quot; or &quot;-&quot;.</span></span> <span data-ttu-id="8819c-150">por exemplo, um szKey de &quot; + abc\0-def\0 + ghi\0 &quot; será indexado nas três colunas &quot; ABC &quot; (em ordem crescente), &quot; Def &quot; (em ordem decrescente) e &quot; GHI &quot; (em ordem crescente).</span><span class="sxs-lookup"><span data-stu-id="8819c-150">for example, a szKey of &quot;+abc\0-def\0+ghi\0&quot; will index over the three columns &quot;abc&quot; (in ascending order), &quot;def&quot; (in descending order), and &quot;ghi&quot; (in ascending order).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="8819c-152"><a href="dn335162(v=exchg.10).md">ulDensity</a></span><span class="sxs-lookup"><span data-stu-id="8819c-152"><a href="dn335162(v=exchg.10).md">ulDensity</a></span></span></td>
<td><span data-ttu-id="8819c-153">Obtém ou define a densidade do índice.</span><span class="sxs-lookup"><span data-stu-id="8819c-153">Gets or sets the density of the index.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8819c-154">Parte superior</span><span class="sxs-lookup"><span data-stu-id="8819c-154">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="8819c-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="8819c-155">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8819c-156">Referência</span><span class="sxs-lookup"><span data-stu-id="8819c-156">Reference</span></span>

[<span data-ttu-id="8819c-157">Classe JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="8819c-157">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="8819c-158">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="8819c-158">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
