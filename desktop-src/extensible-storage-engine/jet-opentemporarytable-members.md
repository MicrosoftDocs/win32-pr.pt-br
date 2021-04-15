---
description: 'Saiba mais sobre: membros do JET_OPENTEMPORARYTABLE'
title: Membros de JET_OPENTEMPORARYTABLE (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: JET_OPENTEMPORARYTABLE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable_members(v=EXCHG.10)
ms:contentKeyID: 55104223
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: af149ecba6858aca4b4877fc9446872386406838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104562059"
---
# <a name="jet_opentemporarytable-members"></a><span data-ttu-id="7aa8b-103">Membros do JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="7aa8b-103">JET_OPENTEMPORARYTABLE members</span></span>

<span data-ttu-id="7aa8b-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="7aa8b-104">Include protected members</span></span>  
<span data-ttu-id="7aa8b-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="7aa8b-105">Include inherited members</span></span>  

<span data-ttu-id="7aa8b-106">Uma coleção de parâmetros para o método JetOpenTemporaryTable.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-106">A collection of parameters for the JetOpenTemporaryTable method.</span></span>

<span data-ttu-id="7aa8b-107">O tipo de [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-107">The [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="7aa8b-108">Construtores</span><span class="sxs-lookup"><span data-stu-id="7aa8b-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="7aa8b-109">Nome</span><span class="sxs-lookup"><span data-stu-id="7aa8b-109">Name</span></span></th>
<th><span data-ttu-id="7aa8b-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7aa8b-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="7aa8b-112"><a href="dn351224(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a></span><span class="sxs-lookup"><span data-stu-id="7aa8b-112"><a href="dn351224(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7aa8b-113">Parte superior</span><span class="sxs-lookup"><span data-stu-id="7aa8b-113">Top</span></span>

## <a name="properties"></a><span data-ttu-id="7aa8b-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7aa8b-114">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="7aa8b-115">Nome</span><span class="sxs-lookup"><span data-stu-id="7aa8b-115">Name</span></span></th>
<th><span data-ttu-id="7aa8b-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="7aa8b-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="7aa8b-118"><a href="dn335290(v=exchg.10).md">cbKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="7aa8b-118"><a href="dn335290(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="7aa8b-119">Obtém ou define o tamanho máximo de uma chave que representa uma determinada linha.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-119">Gets or sets the maximum size for a key representing a given row.</span></span> <span data-ttu-id="7aa8b-120">O tamanho máximo da chave pode ser definido para controlar como as chaves são truncadas.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-120">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="7aa8b-121">O truncamento de chave é importante porque pode afetar quando as linhas são consideradas distintas.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-121">Key truncation is important because it can affect when rows are considered to be distinct.</span></span> <span data-ttu-id="7aa8b-122">Se esse parâmetro for definido como 0 ou 255, o tamanho máximo da chave e sua semântica permanecerão idênticos ao tamanho máximo da chave com suporte do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-122">If this parameter is set to 0 or 255 then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003.</span></span> <span data-ttu-id="7aa8b-123">Esse parâmetro também pode ser definido como um valor maior como uma função do tamanho da página do banco de dados para a instância <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-123">This parameter may also be set to a larger value as a function of the database page size for the instance <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="7aa8b-124">Confira o <a href="dn335292(v=exchg.10).md">melhor</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-124">See <a href="dn335292(v=exchg.10).md">KeyMost</a> for more information.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="7aa8b-126"><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></span><span class="sxs-lookup"><span data-stu-id="7aa8b-126"><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="7aa8b-127">Obtém ou define a quantidade máxima de dados que serão usados de qualquer variável lengthcolumn para construir uma chave para uma determinada linha.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-127">Gets or sets maximum amount of data that will be used from any variable lengthcolumn to construct a key for a given row.</span></span> <span data-ttu-id="7aa8b-128">Esse parâmetro pode ser usado para controlar a quantidade de espaço de chave consumida por qualquer coluna de chave fornecida.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-128">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="7aa8b-129">Esse limite está em bytes.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-129">This limit is in bytes.</span></span> <span data-ttu-id="7aa8b-130">Se esse parâmetro for zero ou for o mesmo que a propriedade <a href="dn335290(v=exchg.10).md">cbKeyMost</a> , nenhum limite estará em vigor.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-130">If this parameter is zero or is the same as the <a href="dn335290(v=exchg.10).md">cbKeyMost</a> property then no limit is in effect.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="7aa8b-132"><a href="dn335287(v=exchg.10).md">ccolumn</a></span><span class="sxs-lookup"><span data-stu-id="7aa8b-132"><a href="dn335287(v=exchg.10).md">ccolumn</a></span></span></td>
<td><span data-ttu-id="7aa8b-133">Obtém ou define o número de colunas em <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-133">Gets or sets the number of columns in <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="7aa8b-135"><a href="dn351232(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="7aa8b-135"><a href="dn351232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="7aa8b-136">Obtém ou define as opções para a tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-136">Gets or sets options for the temp table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="7aa8b-138"><a href="dn335288(v=exchg.10).md">pidxunicode</a></span><span class="sxs-lookup"><span data-stu-id="7aa8b-138"><a href="dn335288(v=exchg.10).md">pidxunicode</a></span></span></td>
<td><span data-ttu-id="7aa8b-139">Obtém ou define os sinalizadores de ID de localidade e normalização a serem usados para comparar quaisquer dados de coluna de chave Unicode na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-139">Gets or sets the locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="7aa8b-140">Quando esse parâmetro for NULL, o LCID padrão será usado para comparar todas as colunas de chave Unicode na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-140">When this parameter is null, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="7aa8b-141">O LCID padrão é a localidade inglês dos EUA.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-141">The default LCID is the U.S. English locale.</span></span> <span data-ttu-id="7aa8b-142">Quando esse parâmetro é nulo, os sinalizadores de normalização padrão serão usados para comparar quaisquer dados de coluna de chave Unicode na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-142">When this parameter is null, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="7aa8b-143">Os sinalizadores de normalização padrão são: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-143">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="7aa8b-145"><a href="dn351228(v=exchg.10).md">prgcolumndef</a></span><span class="sxs-lookup"><span data-stu-id="7aa8b-145"><a href="dn351228(v=exchg.10).md">prgcolumndef</a></span></span></td>
<td><span data-ttu-id="7aa8b-146">Obtém ou define as definições de coluna para as colunas criadas na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-146">Gets or sets the column definitions for the columns created in the temporary table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="7aa8b-148"><a href="dn351233(v=exchg.10).md">prgcolumnid</a></span><span class="sxs-lookup"><span data-stu-id="7aa8b-148"><a href="dn351233(v=exchg.10).md">prgcolumnid</a></span></span></td>
<td><span data-ttu-id="7aa8b-149">Obtém ou define o buffer de saída que recebe a matriz de IDs de coluna geradas durante a criação da tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-149">Gets or sets the output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="7aa8b-150">As IDs de coluna nessa matriz correspondem exatamente à matriz de entrada de definições de coluna.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-150">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="7aa8b-151">Como resultado, o tamanho desse buffer deve corresponder ao tamanho de <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-151">As a result, the size of this buffer must correspond to the size of <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="7aa8b-153"><a href="dn335293(v=exchg.10).md">TableID</a></span><span class="sxs-lookup"><span data-stu-id="7aa8b-153"><a href="dn335293(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="7aa8b-154">Obtém o identificador de tabela para a tabela temporária criada como resultado de uma chamada bem-sucedida para JetOpenTemporaryTable.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-154">Gets the table handle for the temporary table created as a result of a successful call to JetOpenTemporaryTable.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7aa8b-155">Parte superior</span><span class="sxs-lookup"><span data-stu-id="7aa8b-155">Top</span></span>

## <a name="methods"></a><span data-ttu-id="7aa8b-156">Métodos</span><span class="sxs-lookup"><span data-stu-id="7aa8b-156">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="7aa8b-157">Nome</span><span class="sxs-lookup"><span data-stu-id="7aa8b-157">Name</span></span></th>
<th><span data-ttu-id="7aa8b-158">Descrição</span><span class="sxs-lookup"><span data-stu-id="7aa8b-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="7aa8b-160"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Igual a</a></span><span class="sxs-lookup"><span data-stu-id="7aa8b-160"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="7aa8b-161">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="7aa8b-161">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="7aa8b-163"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizar</a></span><span class="sxs-lookup"><span data-stu-id="7aa8b-163"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="7aa8b-164">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="7aa8b-164">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="7aa8b-166"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="7aa8b-166"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="7aa8b-167">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="7aa8b-167">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="7aa8b-169"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="7aa8b-169"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="7aa8b-170">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="7aa8b-170">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="7aa8b-172"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="7aa8b-172"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="7aa8b-173">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="7aa8b-173">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="7aa8b-175"><a href="dn335286(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="7aa8b-175"><a href="dn335286(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="7aa8b-176">Retorna uma <a href="/dotnet/api/system.string">cadeia de caracteres</a> que representa a <a href="dn351217(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>atual.</span><span class="sxs-lookup"><span data-stu-id="7aa8b-176">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351217(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>.</span></span> <span data-ttu-id="7aa8b-177">(Substitui <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="7aa8b-177">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7aa8b-178">Parte superior</span><span class="sxs-lookup"><span data-stu-id="7aa8b-178">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="7aa8b-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="7aa8b-179">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7aa8b-180">Referência</span><span class="sxs-lookup"><span data-stu-id="7aa8b-180">Reference</span></span>

[<span data-ttu-id="7aa8b-181">Classe JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="7aa8b-181">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="7aa8b-182">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="7aa8b-182">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
