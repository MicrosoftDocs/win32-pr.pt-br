---
description: 'Saiba mais sobre: Propriedades de JET_OPENTEMPORARYTABLE'
title: Propriedades de JET_OPENTEMPORARYTABLE (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: JET_OPENTEMPORARYTABLE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable_properties(v=EXCHG.10)
ms:contentKeyID: 55104127
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: e9c55afddd1128a517c27f6a86466b488e6924a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104570342"
---
# <a name="jet_opentemporarytable-properties"></a><span data-ttu-id="5d890-103">Propriedades de JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="5d890-103">JET_OPENTEMPORARYTABLE properties</span></span>

<span data-ttu-id="5d890-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="5d890-104">Include protected members</span></span>  
<span data-ttu-id="5d890-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="5d890-105">Include inherited members</span></span>  

<span data-ttu-id="5d890-106">O tipo de [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="5d890-106">The [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="5d890-107">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5d890-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="5d890-108">Nome</span><span class="sxs-lookup"><span data-stu-id="5d890-108">Name</span></span></th>
<th><span data-ttu-id="5d890-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d890-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="5d890-111"><a href="dn335290(v=exchg.10).md">cbKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="5d890-111"><a href="dn335290(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="5d890-112">Obtém ou define o tamanho máximo de uma chave que representa uma determinada linha.</span><span class="sxs-lookup"><span data-stu-id="5d890-112">Gets or sets the maximum size for a key representing a given row.</span></span> <span data-ttu-id="5d890-113">O tamanho máximo da chave pode ser definido para controlar como as chaves são truncadas.</span><span class="sxs-lookup"><span data-stu-id="5d890-113">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="5d890-114">O truncamento de chave é importante porque pode afetar quando as linhas são consideradas distintas.</span><span class="sxs-lookup"><span data-stu-id="5d890-114">Key truncation is important because it can affect when rows are considered to be distinct.</span></span> <span data-ttu-id="5d890-115">Se esse parâmetro for definido como 0 ou 255, o tamanho máximo da chave e sua semântica permanecerão idênticos ao tamanho máximo da chave com suporte do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5d890-115">If this parameter is set to 0 or 255 then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003.</span></span> <span data-ttu-id="5d890-116">Esse parâmetro também pode ser definido como um valor maior como uma função do tamanho da página do banco de dados para a instância <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span><span class="sxs-lookup"><span data-stu-id="5d890-116">This parameter may also be set to a larger value as a function of the database page size for the instance <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="5d890-117">Confira o <a href="dn335292(v=exchg.10).md">melhor</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="5d890-117">See <a href="dn335292(v=exchg.10).md">KeyMost</a> for more information.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="5d890-119"><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></span><span class="sxs-lookup"><span data-stu-id="5d890-119"><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="5d890-120">Obtém ou define a quantidade máxima de dados que serão usados de qualquer variável lengthcolumn para construir uma chave para uma determinada linha.</span><span class="sxs-lookup"><span data-stu-id="5d890-120">Gets or sets maximum amount of data that will be used from any variable lengthcolumn to construct a key for a given row.</span></span> <span data-ttu-id="5d890-121">Esse parâmetro pode ser usado para controlar a quantidade de espaço de chave consumida por qualquer coluna de chave fornecida.</span><span class="sxs-lookup"><span data-stu-id="5d890-121">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="5d890-122">Esse limite está em bytes.</span><span class="sxs-lookup"><span data-stu-id="5d890-122">This limit is in bytes.</span></span> <span data-ttu-id="5d890-123">Se esse parâmetro for zero ou for o mesmo que a propriedade <a href="dn335290(v=exchg.10).md">cbKeyMost</a> , nenhum limite estará em vigor.</span><span class="sxs-lookup"><span data-stu-id="5d890-123">If this parameter is zero or is the same as the <a href="dn335290(v=exchg.10).md">cbKeyMost</a> property then no limit is in effect.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="5d890-125"><a href="dn335287(v=exchg.10).md">ccolumn</a></span><span class="sxs-lookup"><span data-stu-id="5d890-125"><a href="dn335287(v=exchg.10).md">ccolumn</a></span></span></td>
<td><span data-ttu-id="5d890-126">Obtém ou define o número de colunas em <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span><span class="sxs-lookup"><span data-stu-id="5d890-126">Gets or sets the number of columns in <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="5d890-128"><a href="dn351232(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="5d890-128"><a href="dn351232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="5d890-129">Obtém ou define as opções para a tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="5d890-129">Gets or sets options for the temp table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="5d890-131"><a href="dn335288(v=exchg.10).md">pidxunicode</a></span><span class="sxs-lookup"><span data-stu-id="5d890-131"><a href="dn335288(v=exchg.10).md">pidxunicode</a></span></span></td>
<td><span data-ttu-id="5d890-132">Obtém ou define os sinalizadores de ID de localidade e normalização a serem usados para comparar quaisquer dados de coluna de chave Unicode na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="5d890-132">Gets or sets the locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="5d890-133">Quando esse parâmetro for NULL, o LCID padrão será usado para comparar todas as colunas de chave Unicode na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="5d890-133">When this parameter is null, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="5d890-134">O LCID padrão é a localidade inglês dos EUA.</span><span class="sxs-lookup"><span data-stu-id="5d890-134">The default LCID is the U.S. English locale.</span></span> <span data-ttu-id="5d890-135">Quando esse parâmetro é nulo, os sinalizadores de normalização padrão serão usados para comparar quaisquer dados de coluna de chave Unicode na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="5d890-135">When this parameter is null, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="5d890-136">Os sinalizadores de normalização padrão são: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="5d890-136">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="5d890-138"><a href="dn351228(v=exchg.10).md">prgcolumndef</a></span><span class="sxs-lookup"><span data-stu-id="5d890-138"><a href="dn351228(v=exchg.10).md">prgcolumndef</a></span></span></td>
<td><span data-ttu-id="5d890-139">Obtém ou define as definições de coluna para as colunas criadas na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="5d890-139">Gets or sets the column definitions for the columns created in the temporary table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="5d890-141"><a href="dn351233(v=exchg.10).md">prgcolumnid</a></span><span class="sxs-lookup"><span data-stu-id="5d890-141"><a href="dn351233(v=exchg.10).md">prgcolumnid</a></span></span></td>
<td><span data-ttu-id="5d890-142">Obtém ou define o buffer de saída que recebe a matriz de IDs de coluna geradas durante a criação da tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="5d890-142">Gets or sets the output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="5d890-143">As IDs de coluna nessa matriz correspondem exatamente à matriz de entrada de definições de coluna.</span><span class="sxs-lookup"><span data-stu-id="5d890-143">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="5d890-144">Como resultado, o tamanho desse buffer deve corresponder ao tamanho de <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span><span class="sxs-lookup"><span data-stu-id="5d890-144">As a result, the size of this buffer must correspond to the size of <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="5d890-146"><a href="dn335293(v=exchg.10).md">TableID</a></span><span class="sxs-lookup"><span data-stu-id="5d890-146"><a href="dn335293(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="5d890-147">Obtém o identificador de tabela para a tabela temporária criada como resultado de uma chamada bem-sucedida para JetOpenTemporaryTable.</span><span class="sxs-lookup"><span data-stu-id="5d890-147">Gets the table handle for the temporary table created as a result of a successful call to JetOpenTemporaryTable.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5d890-148">Parte superior</span><span class="sxs-lookup"><span data-stu-id="5d890-148">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="5d890-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d890-149">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5d890-150">Referência</span><span class="sxs-lookup"><span data-stu-id="5d890-150">Reference</span></span>

[<span data-ttu-id="5d890-151">Classe JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="5d890-151">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="5d890-152">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="5d890-152">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
