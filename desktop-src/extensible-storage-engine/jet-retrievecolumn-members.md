---
description: 'Saiba mais sobre: membros do JET_RETRIEVECOLUMN'
title: Membros do JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn_members(v=EXCHG.10)
ms:contentKeyID: 55103877
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 9a5eda1d671cfe6225a8419314b2f53558294754
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104561009"
---
# <a name="jet_retrievecolumn-members"></a><span data-ttu-id="14766-103">Membros do JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="14766-103">JET_RETRIEVECOLUMN members</span></span>

<span data-ttu-id="14766-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="14766-104">Include protected members</span></span>  
<span data-ttu-id="14766-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="14766-105">Include inherited members</span></span>  

<span data-ttu-id="14766-106">Contém parâmetros de entrada e saída para [JetRetrieveColumns (JET_SESID, JET_TABLEID, \[ \] , Int32)](./api.jetretrievecolumns-method.md).</span><span class="sxs-lookup"><span data-stu-id="14766-106">Contains input and output parameters for [JetRetrieveColumns(JET_SESID, JET_TABLEID, \[\], Int32)](./api.jetretrievecolumns-method.md).</span></span> <span data-ttu-id="14766-107">Os campos na estrutura descrevem o valor da coluna a ser recuperado, como recuperá-lo e onde salvar os resultados.</span><span class="sxs-lookup"><span data-stu-id="14766-107">Fields in the structure describe what column value to retrieve, how to retrieve it, and where to save results.</span></span>

<span data-ttu-id="14766-108">O tipo de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="14766-108">The [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="14766-109">Construtores</span><span class="sxs-lookup"><span data-stu-id="14766-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="14766-110">Nome</span><span class="sxs-lookup"><span data-stu-id="14766-110">Name</span></span></th>
<th><span data-ttu-id="14766-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="14766-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="14766-113"><a href="dn351036(v=exchg.10).md">JET_RETRIEVECOLUMN</a></span><span class="sxs-lookup"><span data-stu-id="14766-113"><a href="dn351036(v=exchg.10).md">JET_RETRIEVECOLUMN</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="14766-114">Parte superior</span><span class="sxs-lookup"><span data-stu-id="14766-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="14766-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="14766-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="14766-116">Nome</span><span class="sxs-lookup"><span data-stu-id="14766-116">Name</span></span></th>
<th><span data-ttu-id="14766-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="14766-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="14766-119"><a href="dn335226(v=exchg.10).md">cbActual</a></span><span class="sxs-lookup"><span data-stu-id="14766-119"><a href="dn335226(v=exchg.10).md">cbActual</a></span></span></td>
<td><span data-ttu-id="14766-120">Obtém o tamanho, em bytes, dos dados recuperados por uma operação de recuperação de coluna.</span><span class="sxs-lookup"><span data-stu-id="14766-120">Gets the size, in bytes, of data that is retrieved by a retrieve column operation.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="14766-122"><a href="dn335228(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="14766-122"><a href="dn335228(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="14766-123">Obtém ou define o tamanho do buffer <a href="dn351040(v=exchg.10).md">pvData</a> , em bytes.</span><span class="sxs-lookup"><span data-stu-id="14766-123">Gets or sets the size of the <a href="dn351040(v=exchg.10).md">pvData</a> buffer, in bytes.</span></span> <span data-ttu-id="14766-124">A operação de recuperação de coluna não armazenará mais dados em pvData do que cbData.</span><span class="sxs-lookup"><span data-stu-id="14766-124">The retrieve column operation will not store more data in pvData than cbData.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="14766-126"><a href="dn335230(v=exchg.10).md">columnid</a></span><span class="sxs-lookup"><span data-stu-id="14766-126"><a href="dn335230(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="14766-127">Obtém ou define o identificador de coluna da coluna a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="14766-127">Gets or sets the column identifier for the column to retrieve.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="14766-129"><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></span><span class="sxs-lookup"><span data-stu-id="14766-129"><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></span></span></td>
<td><span data-ttu-id="14766-130">Obtém o columnid da coluna marcada, com vários valores ou esparsos quando todas as colunas marcadas são recuperadas passando 0 como columnid.</span><span class="sxs-lookup"><span data-stu-id="14766-130">Gets the columnid of the tagged, multi-valued, or sparse column when all tagged columns are retrieved by passing 0 as the columnid.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="14766-132"><a href="dn335231(v=exchg.10).md">erra</a></span><span class="sxs-lookup"><span data-stu-id="14766-132"><a href="dn335231(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="14766-133">Obtém o aviso retornado da recuperação da coluna.</span><span class="sxs-lookup"><span data-stu-id="14766-133">Gets the warning returned from the retrieval of the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="14766-135"><a href="dn335232(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="14766-135"><a href="dn335232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="14766-136">Obtém ou define as opções de recuperação de coluna.</span><span class="sxs-lookup"><span data-stu-id="14766-136">Gets or sets the options for column retrieval.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="14766-138"><a href="dn335233(v=exchg.10).md">ibData</a></span><span class="sxs-lookup"><span data-stu-id="14766-138"><a href="dn335233(v=exchg.10).md">ibData</a></span></span></td>
<td><span data-ttu-id="14766-139">Obtém ou define o deslocamento no buffer no qual os dados serão armazenados.</span><span class="sxs-lookup"><span data-stu-id="14766-139">Gets or sets the offset in the buffer that data will be stored in.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="14766-141"><a href="dn335234(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="14766-141"><a href="dn335234(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="14766-142">Obtém ou define o deslocamento para o primeiro byte a ser recuperado de uma coluna do tipo <a href="hh577895(v=exchg.10).md">LongBinary</a> ou <a href="hh577895(v=exchg.10).md">LONGTEXT</a>.</span><span class="sxs-lookup"><span data-stu-id="14766-142">Gets or sets the offset to the first byte to be retrieved from a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="14766-144"><a href="dn351039(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="14766-144"><a href="dn351039(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="14766-145">Obtém ou define o número de sequência dos valores contidos em uma coluna com vários valores.</span><span class="sxs-lookup"><span data-stu-id="14766-145">Gets or sets the sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="14766-146">Se itagSequence for 0, o número de instâncias de uma coluna com vários valores será retornado em vez de quaisquer dados de coluna.</span><span class="sxs-lookup"><span data-stu-id="14766-146">If the itagSequence is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="14766-148"><a href="dn351040(v=exchg.10).md">pvData</a></span><span class="sxs-lookup"><span data-stu-id="14766-148"><a href="dn351040(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="14766-149">Obtém ou define o buffer que armazenará os dados que serão recuperados da coluna.</span><span class="sxs-lookup"><span data-stu-id="14766-149">Gets or sets the buffer that will store data that is retrieved from the column.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="14766-150">Parte superior</span><span class="sxs-lookup"><span data-stu-id="14766-150">Top</span></span>

## <a name="methods"></a><span data-ttu-id="14766-151">Métodos</span><span class="sxs-lookup"><span data-stu-id="14766-151">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="14766-152">Nome</span><span class="sxs-lookup"><span data-stu-id="14766-152">Name</span></span></th>
<th><span data-ttu-id="14766-153">Descrição</span><span class="sxs-lookup"><span data-stu-id="14766-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="14766-155"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Igual a</a></span><span class="sxs-lookup"><span data-stu-id="14766-155"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="14766-156">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="14766-156">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="14766-158"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizar</a></span><span class="sxs-lookup"><span data-stu-id="14766-158"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="14766-159">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="14766-159">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="14766-161"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="14766-161"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="14766-162">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="14766-162">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="14766-164"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="14766-164"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="14766-165">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="14766-165">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="14766-167"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="14766-167"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="14766-168">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="14766-168">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="14766-170"><a href="dn335224(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="14766-170"><a href="dn335224(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="14766-171">Retorna uma <a href="/dotnet/api/system.string">cadeia de caracteres</a> que representa a <a href="dn351033(v=exchg.10).md">JET_RETRIEVECOLUMN</a>atual.</span><span class="sxs-lookup"><span data-stu-id="14766-171">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351033(v=exchg.10).md">JET_RETRIEVECOLUMN</a>.</span></span> <span data-ttu-id="14766-172">(Substitui <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="14766-172">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="14766-173">Parte superior</span><span class="sxs-lookup"><span data-stu-id="14766-173">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="14766-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="14766-174">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="14766-175">Referência</span><span class="sxs-lookup"><span data-stu-id="14766-175">Reference</span></span>

[<span data-ttu-id="14766-176">Classe JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="14766-176">JET_RETRIEVECOLUMN class</span></span>](./jet-retrievecolumn-class.md)

[<span data-ttu-id="14766-177">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="14766-177">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
