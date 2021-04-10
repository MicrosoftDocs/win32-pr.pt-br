---
description: 'Saiba mais sobre: membros do JET_INDEXCREATE'
title: Membros do JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_members(v=EXCHG.10)
ms:contentKeyID: 55103641
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: cbe9ce962221db30c8cdae90461fa55fc0baea19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171349"
---
# <a name="jet_indexcreate-members"></a><span data-ttu-id="1bef6-103">Membros do JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="1bef6-103">JET_INDEXCREATE members</span></span>

<span data-ttu-id="1bef6-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="1bef6-104">Include protected members</span></span>  
<span data-ttu-id="1bef6-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="1bef6-105">Include inherited members</span></span>  

<span data-ttu-id="1bef6-106">Contém as informações necessárias para criar um índice sobre os dados em um banco de dado ESE.</span><span class="sxs-lookup"><span data-stu-id="1bef6-106">Contains the information needed to create an index over data in an ESE database.</span></span> <span data-ttu-id="1bef6-107">Contém as informações necessárias para criar um índice sobre os dados em um banco de dado ESE.</span><span class="sxs-lookup"><span data-stu-id="1bef6-107">Contains the information needed to create an index over data in an ESE database.</span></span>

<span data-ttu-id="1bef6-108">O tipo de [JET_INDEXCREATE](./jet-indexcreate-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="1bef6-108">The [JET_INDEXCREATE](./jet-indexcreate-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="1bef6-109">Construtores</span><span class="sxs-lookup"><span data-stu-id="1bef6-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="1bef6-110">Nome</span><span class="sxs-lookup"><span data-stu-id="1bef6-110">Name</span></span></th>
<th><span data-ttu-id="1bef6-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="1bef6-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="1bef6-113"><a href="dn335115(v=exchg.10).md">JET_INDEXCREATE</a></span><span class="sxs-lookup"><span data-stu-id="1bef6-113"><a href="dn335115(v=exchg.10).md">JET_INDEXCREATE</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1bef6-114">Parte superior</span><span class="sxs-lookup"><span data-stu-id="1bef6-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="1bef6-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1bef6-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="1bef6-116">Nome</span><span class="sxs-lookup"><span data-stu-id="1bef6-116">Name</span></span></th>
<th><span data-ttu-id="1bef6-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="1bef6-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="1bef6-119"><a href="dn335122(v=exchg.10).md">cbKey</a></span><span class="sxs-lookup"><span data-stu-id="1bef6-119"><a href="dn335122(v=exchg.10).md">cbKey</a></span></span></td>
<td><span data-ttu-id="1bef6-120">Obtém ou define o comprimento, em caracteres, de szKey, incluindo os dois nulos de terminação.</span><span class="sxs-lookup"><span data-stu-id="1bef6-120">Gets or sets the length, in characters, of szKey including the two terminating nulls.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="1bef6-122"><a href="dn335156(v=exchg.10).md">cbKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="1bef6-122"><a href="dn335156(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="1bef6-123">Obtém ou define o tamanho máximo permitido, em bytes, para as chaves no índice.</span><span class="sxs-lookup"><span data-stu-id="1bef6-123">Gets or sets the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="1bef6-124">O tamanho mínimo de chave máximo suportado é JET_cbKeyMostMin (255), que é o tamanho de chave máximo herdado.</span><span class="sxs-lookup"><span data-stu-id="1bef6-124">The minimum supported maximum key size is JET_cbKeyMostMin (255) which is the legacy maximum key size.</span></span> <span data-ttu-id="1bef6-125">O tamanho máximo da chave depende do tamanho da página do banco de dados <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span><span class="sxs-lookup"><span data-stu-id="1bef6-125">The maximum key size is dependent on the database page size <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="1bef6-126">O tamanho máximo da chave pode ser recuperado com o <a href="dn351156(v=exchg.10).md">máximo</a>.</span><span class="sxs-lookup"><span data-stu-id="1bef6-126">The maximum key size can be retrieved with <a href="dn351156(v=exchg.10).md">KeyMost</a>.</span></span> <span data-ttu-id="1bef6-127">Esse parâmetro é ignorado no Windows XP e no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1bef6-127">This parameter is ignored on Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="1bef6-128">Diferentemente da API não gerenciada, <strong>IndexKeyMost ()</strong> (JET_bitIndexKeyMost) não é necessária, ela será adicionada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="1bef6-128">Unlike the unmanaged API, <strong>IndexKeyMost()</strong> (JET_bitIndexKeyMost) is not needed, it will be added automatically.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="1bef6-130"><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></span><span class="sxs-lookup"><span data-stu-id="1bef6-130"><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="1bef6-131">Obtém ou define o comprimento máximo, em bytes, de cada coluna a ser armazenada no índice.</span><span class="sxs-lookup"><span data-stu-id="1bef6-131">Gets or sets the maximum length, in bytes, of each column to store in the index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="1bef6-133"><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></span><span class="sxs-lookup"><span data-stu-id="1bef6-133"><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></span></span></td>
<td><span data-ttu-id="1bef6-134">Obtém ou define o número de colunas condicionais.</span><span class="sxs-lookup"><span data-stu-id="1bef6-134">Gets or sets the number of conditional columns.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="1bef6-136"><a href="dn335157(v=exchg.10).md">erra</a></span><span class="sxs-lookup"><span data-stu-id="1bef6-136"><a href="dn335157(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="1bef6-137">Obtém ou define o código de erro da criação deste índice.</span><span class="sxs-lookup"><span data-stu-id="1bef6-137">Gets or sets the error code from creating this index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="1bef6-139"><a href="dn335119(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="1bef6-139"><a href="dn335119(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="1bef6-140">Obtém ou define as opções de criação de índice.</span><span class="sxs-lookup"><span data-stu-id="1bef6-140">Gets or sets index creation options.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="1bef6-142"><a href="dn335159(v=exchg.10).md">pidxUnicode</a></span><span class="sxs-lookup"><span data-stu-id="1bef6-142"><a href="dn335159(v=exchg.10).md">pidxUnicode</a></span></span></td>
<td><span data-ttu-id="1bef6-143">Obtém ou define as opções de comparação Unicode opcionais.</span><span class="sxs-lookup"><span data-stu-id="1bef6-143">Gets or sets the optional unicode comparison options.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="1bef6-145"><a href="dn335120(v=exchg.10).md">pSpaceHints</a></span><span class="sxs-lookup"><span data-stu-id="1bef6-145"><a href="dn335120(v=exchg.10).md">pSpaceHints</a></span></span></td>
<td><span data-ttu-id="1bef6-146">Obtém ou define as dicas de alocação, manutenção e uso de espaço.</span><span class="sxs-lookup"><span data-stu-id="1bef6-146">Gets or sets space allocation, maintenance, and usage hints.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="1bef6-148"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span><span class="sxs-lookup"><span data-stu-id="1bef6-148"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span></span></td>
<td><span data-ttu-id="1bef6-149">Obtém ou define as colunas condicionais opcionais.</span><span class="sxs-lookup"><span data-stu-id="1bef6-149">Gets or sets the optional conditional columns.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="1bef6-151"><a href="dn335121(v=exchg.10).md">szIndexName</a></span><span class="sxs-lookup"><span data-stu-id="1bef6-151"><a href="dn335121(v=exchg.10).md">szIndexName</a></span></span></td>
<td><span data-ttu-id="1bef6-152">Obtém ou define o nome do índice a ser criado.</span><span class="sxs-lookup"><span data-stu-id="1bef6-152">Gets or sets the name of the index to create.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="1bef6-154"><a href="dn335161(v=exchg.10).md">szKey</a></span><span class="sxs-lookup"><span data-stu-id="1bef6-154"><a href="dn335161(v=exchg.10).md">szKey</a></span></span></td>
<td><span data-ttu-id="1bef6-155">Obtém ou define a descrição da chave de índice.</span><span class="sxs-lookup"><span data-stu-id="1bef6-155">Gets or sets the description of the index key.</span></span> <span data-ttu-id="1bef6-156">Essa é uma cadeia de caracteres dupla com terminação nula de tokens delimitados por nulo.</span><span class="sxs-lookup"><span data-stu-id="1bef6-156">This is a double null-terminated string of null-delimited tokens.</span></span> <span data-ttu-id="1bef6-157">Cada token tem o formato [Direction-especificador] [nome-da-coluna], onde a especificação de direção é &quot; + &quot; ou &quot; - &quot; .</span><span class="sxs-lookup"><span data-stu-id="1bef6-157">Each token is of the form [direction-specifier][column-name], where direction-specification is either &quot;+&quot; or &quot;-&quot;.</span></span> <span data-ttu-id="1bef6-158">por exemplo, um szKey de &quot; + abc\0-def\0 + ghi\0 &quot; será indexado nas três colunas &quot; ABC &quot; (em ordem crescente), &quot; Def &quot; (em ordem decrescente) e &quot; GHI &quot; (em ordem crescente).</span><span class="sxs-lookup"><span data-stu-id="1bef6-158">for example, a szKey of &quot;+abc\0-def\0+ghi\0&quot; will index over the three columns &quot;abc&quot; (in ascending order), &quot;def&quot; (in descending order), and &quot;ghi&quot; (in ascending order).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="1bef6-160"><a href="dn335162(v=exchg.10).md">ulDensity</a></span><span class="sxs-lookup"><span data-stu-id="1bef6-160"><a href="dn335162(v=exchg.10).md">ulDensity</a></span></span></td>
<td><span data-ttu-id="1bef6-161">Obtém ou define a densidade do índice.</span><span class="sxs-lookup"><span data-stu-id="1bef6-161">Gets or sets the density of the index.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1bef6-162">Parte superior</span><span class="sxs-lookup"><span data-stu-id="1bef6-162">Top</span></span>

## <a name="methods"></a><span data-ttu-id="1bef6-163">Métodos</span><span class="sxs-lookup"><span data-stu-id="1bef6-163">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="1bef6-164">Nome</span><span class="sxs-lookup"><span data-stu-id="1bef6-164">Name</span></span></th>
<th><span data-ttu-id="1bef6-165">Descrição</span><span class="sxs-lookup"><span data-stu-id="1bef6-165">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="1bef6-167"><a href="dn335116(v=exchg.10).md">ContentEquals</a></span><span class="sxs-lookup"><span data-stu-id="1bef6-167"><a href="dn335116(v=exchg.10).md">ContentEquals</a></span></span></td>
<td><span data-ttu-id="1bef6-168">Retorna um valor que indica se essa instância é igual a outra instância.</span><span class="sxs-lookup"><span data-stu-id="1bef6-168">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="1bef6-170"><a href="dn335153(v=exchg.10).md">DeepClone</a></span><span class="sxs-lookup"><span data-stu-id="1bef6-170"><a href="dn335153(v=exchg.10).md">DeepClone</a></span></span></td>
<td><span data-ttu-id="1bef6-171">Retorna uma cópia profunda do objeto.</span><span class="sxs-lookup"><span data-stu-id="1bef6-171">Returns a deep copy of the object.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="1bef6-173"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Igual a</a></span><span class="sxs-lookup"><span data-stu-id="1bef6-173"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="1bef6-174">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="1bef6-174">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="1bef6-176"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizar</a></span><span class="sxs-lookup"><span data-stu-id="1bef6-176"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="1bef6-177">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="1bef6-177">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="1bef6-179"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="1bef6-179"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="1bef6-180">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="1bef6-180">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="1bef6-182"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="1bef6-182"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="1bef6-183">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="1bef6-183">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="1bef6-185"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="1bef6-185"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="1bef6-186">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="1bef6-186">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="1bef6-188"><a href="dn335154(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="1bef6-188"><a href="dn335154(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="1bef6-189">Gere uma representação de cadeia de caracteres da instância.</span><span class="sxs-lookup"><span data-stu-id="1bef6-189">Generate a string representation of the instance.</span></span> <span data-ttu-id="1bef6-190">(Substitui <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="1bef6-190">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1bef6-191">Parte superior</span><span class="sxs-lookup"><span data-stu-id="1bef6-191">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="1bef6-192">Confira também</span><span class="sxs-lookup"><span data-stu-id="1bef6-192">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1bef6-193">Referência</span><span class="sxs-lookup"><span data-stu-id="1bef6-193">Reference</span></span>

[<span data-ttu-id="1bef6-194">Classe JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="1bef6-194">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="1bef6-195">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="1bef6-195">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
