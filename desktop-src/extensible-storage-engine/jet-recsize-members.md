---
description: 'Saiba mais sobre: membros do JET_RECSIZE'
title: Membros de JET_RECSIZE (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: JET_RECSIZE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize_members(v=EXCHG.10)
ms:contentKeyID: 39510137
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 224d22b5dea0447297163fb6b5e1a70fe62a6396
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104561625"
---
# <a name="jet_recsize-members"></a><span data-ttu-id="b1d31-103">Membros do JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="b1d31-103">JET_RECSIZE members</span></span>

<span data-ttu-id="b1d31-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="b1d31-104">Include protected members</span></span>  
<span data-ttu-id="b1d31-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="b1d31-105">Include inherited members</span></span>  

<span data-ttu-id="b1d31-106">Usado por [JetGetRecordSize (JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md) para retornar informações sobre os requisitos de uso de um registro no espaço de dados do usuário, o número de colunas definidas, o número de valores e o espaço de sobrecarga da estrutura do registro ESENT.</span><span class="sxs-lookup"><span data-stu-id="b1d31-106">Used by [JetGetRecordSize(JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESENT record structure overhead space.</span></span>

<span data-ttu-id="b1d31-107">O tipo de [JET_RECSIZE](./jet-recsize-structure2.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1d31-107">The [JET_RECSIZE](./jet-recsize-structure2.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="b1d31-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b1d31-108">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="b1d31-109">Nome</span><span class="sxs-lookup"><span data-stu-id="b1d31-109">Name</span></span></th>
<th><span data-ttu-id="b1d31-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1d31-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b1d31-112"><a href="hh557581(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="b1d31-112"><a href="hh557581(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="b1d31-113">Obtém o conjunto de dados do usuário no registro.</span><span class="sxs-lookup"><span data-stu-id="b1d31-113">Gets the user data set in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b1d31-115"><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></span><span class="sxs-lookup"><span data-stu-id="b1d31-115"><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></span></span></td>
<td><span data-ttu-id="b1d31-116">Obtém o tamanho compactado dos dados do usuário no registro.</span><span class="sxs-lookup"><span data-stu-id="b1d31-116">Gets the compressed size of user data in record.</span></span> <span data-ttu-id="b1d31-117">Isso é o mesmo que <a href="hh557581(v=exchg.10).md">cbData</a> se nenhum valor longo intrínseco for compactado).</span><span class="sxs-lookup"><span data-stu-id="b1d31-117">This is the same as <a href="hh557581(v=exchg.10).md">cbData</a> if no intrinsic long-values are compressed).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b1d31-119"><a href="hh557913(v=exchg.10).md">cbLongValueData</a></span><span class="sxs-lookup"><span data-stu-id="b1d31-119"><a href="hh557913(v=exchg.10).md">cbLongValueData</a></span></span></td>
<td><span data-ttu-id="b1d31-120">Obtém o conjunto de dados do usuário no registro, mas armazenado na árvore de valor longo.</span><span class="sxs-lookup"><span data-stu-id="b1d31-120">Gets the user data set in the record, but stored in the long-value tree.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b1d31-122"><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></span><span class="sxs-lookup"><span data-stu-id="b1d31-122"><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></span></span></td>
<td><span data-ttu-id="b1d31-123">Obtém o tamanho compactado dos dados do usuário na árvore de valor longo.</span><span class="sxs-lookup"><span data-stu-id="b1d31-123">Gets the compressed size of user data in the long-value tree.</span></span> <span data-ttu-id="b1d31-124">Isso é o mesmo que <a href="hh557913(v=exchg.10).md">cbLongValueData</a> se nenhum valor longo separado for compactado.</span><span class="sxs-lookup"><span data-stu-id="b1d31-124">This is the same as <a href="hh557913(v=exchg.10).md">cbLongValueData</a> if no separated long values are compressed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b1d31-126"><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></span><span class="sxs-lookup"><span data-stu-id="b1d31-126"><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></span></span></td>
<td><span data-ttu-id="b1d31-127">Obtém a sobrecarga dos dados de valor longo.</span><span class="sxs-lookup"><span data-stu-id="b1d31-127">Gets the overhead of the long-value data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b1d31-129"><a href="hh565836(v=exchg.10).md">cbOverhead</a></span><span class="sxs-lookup"><span data-stu-id="b1d31-129"><a href="hh565836(v=exchg.10).md">cbOverhead</a></span></span></td>
<td><span data-ttu-id="b1d31-130">Obtém a sobrecarga da estrutura de registro ESENT para este registro.</span><span class="sxs-lookup"><span data-stu-id="b1d31-130">Gets the overhead of the ESENT record structure for this record.</span></span> <span data-ttu-id="b1d31-131">Isso inclui o tamanho da chave do registro.</span><span class="sxs-lookup"><span data-stu-id="b1d31-131">This includes the record's key size.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b1d31-133"><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></span><span class="sxs-lookup"><span data-stu-id="b1d31-133"><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></span></span></td>
<td><span data-ttu-id="b1d31-134">Obtém o número total de colunas no registro que estão compactadas.</span><span class="sxs-lookup"><span data-stu-id="b1d31-134">Gets the total number of columns in the record which are compressed.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b1d31-136"><a href="hh596288(v=exchg.10).md">cLongValues</a></span><span class="sxs-lookup"><span data-stu-id="b1d31-136"><a href="hh596288(v=exchg.10).md">cLongValues</a></span></span></td>
<td><span data-ttu-id="b1d31-137">Obtém o número total de valores longos armazenados na árvore de valor longo para esse registro.</span><span class="sxs-lookup"><span data-stu-id="b1d31-137">Gets the total number of long values stored in the long-value tree for this record.</span></span> <span data-ttu-id="b1d31-138">Isso não inclui valores longos intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="b1d31-138">This does not include intrinsic long values.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b1d31-140"><a href="hh577486(v=exchg.10).md">cMultiValues</a></span><span class="sxs-lookup"><span data-stu-id="b1d31-140"><a href="hh577486(v=exchg.10).md">cMultiValues</a></span></span></td>
<td><span data-ttu-id="b1d31-141">Obtém a acumulação do número total de valores além do primeiro para todas as colunas no registro.</span><span class="sxs-lookup"><span data-stu-id="b1d31-141">Gets the accumulation of the total number of values beyond the first for all columns in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b1d31-143"><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></span><span class="sxs-lookup"><span data-stu-id="b1d31-143"><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></span></span></td>
<td><span data-ttu-id="b1d31-144">Obtém o número total de colunas fixas e variáveis definidas neste registro.</span><span class="sxs-lookup"><span data-stu-id="b1d31-144">Gets the total number of fixed and variable columns set in this record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="b1d31-146"><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></span><span class="sxs-lookup"><span data-stu-id="b1d31-146"><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></span></span></td>
<td><span data-ttu-id="b1d31-147">Obtém o número total de colunas marcadas definidas neste registro.</span><span class="sxs-lookup"><span data-stu-id="b1d31-147">Gets the total number of tagged columns set in this record.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b1d31-148">Parte superior</span><span class="sxs-lookup"><span data-stu-id="b1d31-148">Top</span></span>

## <a name="methods"></a><span data-ttu-id="b1d31-149">Métodos</span><span class="sxs-lookup"><span data-stu-id="b1d31-149">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="b1d31-150">Nome</span><span class="sxs-lookup"><span data-stu-id="b1d31-150">Name</span></span></th>
<th><span data-ttu-id="b1d31-151">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1d31-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="b1d31-154"><a href="hh538879(v=exchg.10).md">Adicionar</a></span><span class="sxs-lookup"><span data-stu-id="b1d31-154"><a href="hh538879(v=exchg.10).md">Add</a></span></span></td>
<td><span data-ttu-id="b1d31-155">Adicione os tamanhos em duas estruturas de JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="b1d31-155">Add the sizes in two JET_RECSIZE structures.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="b1d31-157"><a href="hh558506(v=exchg.10).md">Equals (Object)</a></span><span class="sxs-lookup"><span data-stu-id="b1d31-157"><a href="hh558506(v=exchg.10).md">Equals(Object)</a></span></span></td>
<td><span data-ttu-id="b1d31-158">Retorna um valor que indica se essa instância é igual a outra instância.</span><span class="sxs-lookup"><span data-stu-id="b1d31-158">Returns a value indicating whether this instance is equal to another instance.</span></span> <span data-ttu-id="b1d31-159">(Substitui <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType. Equals (Object)</a>.)</span><span class="sxs-lookup"><span data-stu-id="b1d31-159">(Overrides <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType.Equals(Object)</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="b1d31-161"><a href="hh577992(v=exchg.10).md">Equals (JET_RECSIZE)</a></span><span class="sxs-lookup"><span data-stu-id="b1d31-161"><a href="hh577992(v=exchg.10).md">Equals(JET_RECSIZE)</a></span></span></td>
<td><span data-ttu-id="b1d31-162">Retorna um valor que indica se essa instância é igual a outra instância.</span><span class="sxs-lookup"><span data-stu-id="b1d31-162">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="b1d31-164"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizar</a></span><span class="sxs-lookup"><span data-stu-id="b1d31-164"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="b1d31-165">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="b1d31-165">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="b1d31-167"><a href="hh557078(v=exchg.10).md">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="b1d31-167"><a href="hh557078(v=exchg.10).md">GetHashCode</a></span></span></td>
<td><span data-ttu-id="b1d31-168">Retorna o código hash para a instância.</span><span class="sxs-lookup"><span data-stu-id="b1d31-168">Returns the hash code for this instance.</span></span> <span data-ttu-id="b1d31-169">(Substitui <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType. GetHashCode ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="b1d31-169">(Overrides <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType.GetHashCode()</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="b1d31-171"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="b1d31-171"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="b1d31-172">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="b1d31-172">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="b1d31-174"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="b1d31-174"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="b1d31-175">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="b1d31-175">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="b1d31-178"><a href="hh579561(v=exchg.10).md">Subtrair</a></span><span class="sxs-lookup"><span data-stu-id="b1d31-178"><a href="hh579561(v=exchg.10).md">Subtract</a></span></span></td>
<td><span data-ttu-id="b1d31-179">Calcule a diferença em tamanhos entre duas estruturas de JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="b1d31-179">Calculate the difference in sizes between two JET_RECSIZE structures.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="b1d31-181"><a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ToString</a></span><span class="sxs-lookup"><span data-stu-id="b1d31-181"><a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ToString</a></span></span></td>
<td><span data-ttu-id="b1d31-182">(Herdado de <a href="/dotnet/api/system.valuetype">ValueType</a>.)</span><span class="sxs-lookup"><span data-stu-id="b1d31-182">(Inherited from <a href="/dotnet/api/system.valuetype">ValueType</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b1d31-183">Parte superior</span><span class="sxs-lookup"><span data-stu-id="b1d31-183">Top</span></span>

## <a name="operators"></a><span data-ttu-id="b1d31-184">Operadores</span><span class="sxs-lookup"><span data-stu-id="b1d31-184">Operators</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="b1d31-185">Nome</span><span class="sxs-lookup"><span data-stu-id="b1d31-185">Name</span></span></th>
<th><span data-ttu-id="b1d31-186">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1d31-186">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operador público" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="b1d31-189"><a href="hh578675(v=exchg.10).md">Além</a></span><span class="sxs-lookup"><span data-stu-id="b1d31-189"><a href="hh578675(v=exchg.10).md">Addition</a></span></span></td>
<td><span data-ttu-id="b1d31-190">Adicione os tamanhos em duas estruturas de JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="b1d31-190">Add the sizes in two JET_RECSIZE structures.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operador público" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="b1d31-193"><a href="hh596362(v=exchg.10).md">Igualitário</a></span><span class="sxs-lookup"><span data-stu-id="b1d31-193"><a href="hh596362(v=exchg.10).md">Equality</a></span></span></td>
<td><span data-ttu-id="b1d31-194">Determina se duas instâncias especificadas do JET_RECSIZE são iguais.</span><span class="sxs-lookup"><span data-stu-id="b1d31-194">Determines whether two specified instances of JET_RECSIZE are equal.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operador público" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="b1d31-197"><a href="hh578809(v=exchg.10).md">Desigualdade</a></span><span class="sxs-lookup"><span data-stu-id="b1d31-197"><a href="hh578809(v=exchg.10).md">Inequality</a></span></span></td>
<td><span data-ttu-id="b1d31-198">Determina se duas instâncias especificadas do JET_RECSIZE não são iguais.</span><span class="sxs-lookup"><span data-stu-id="b1d31-198">Determines whether two specified instances of JET_RECSIZE are not equal.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operador público" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="b1d31-201"><a href="hh596696(v=exchg.10).md">Subtração</a></span><span class="sxs-lookup"><span data-stu-id="b1d31-201"><a href="hh596696(v=exchg.10).md">Subtraction</a></span></span></td>
<td><span data-ttu-id="b1d31-202">Calcule a diferença em tamanhos entre duas estruturas de JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="b1d31-202">Calculate the difference in sizes between two JET_RECSIZE structures.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b1d31-203">Parte superior</span><span class="sxs-lookup"><span data-stu-id="b1d31-203">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="b1d31-204">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1d31-204">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b1d31-205">Referência</span><span class="sxs-lookup"><span data-stu-id="b1d31-205">Reference</span></span>

[<span data-ttu-id="b1d31-206">Estrutura de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="b1d31-206">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="b1d31-207">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="b1d31-207">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
