---
description: 'Saiba mais sobre: membros do JET_ENUMCOLUMNVALUE'
title: Membros do JET_ENUMCOLUMNVALUE
TOCTitle: JET_ENUMCOLUMNVALUE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnvalue_members(v=EXCHG.10)
ms:contentKeyID: 55103510
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 2950caf527af07312f4f27c9464ee4088830fe1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571059"
---
# <a name="jet_enumcolumnvalue-members"></a><span data-ttu-id="80d2f-103">Membros do JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="80d2f-103">JET_ENUMCOLUMNVALUE members</span></span>

<span data-ttu-id="80d2f-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="80d2f-104">Include protected members</span></span>  
<span data-ttu-id="80d2f-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="80d2f-105">Include inherited members</span></span>  

<span data-ttu-id="80d2f-106">Enumera os valores de coluna de um registro usando a função JetEnumerateColumns.</span><span class="sxs-lookup"><span data-stu-id="80d2f-106">Enumerates the column values of a record using the JetEnumerateColumns function.</span></span> <span data-ttu-id="80d2f-107">[JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, \[ \] int32, \[ \] , JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md) retorna uma matriz de estruturas de JET_ENUMCOLUMNVALUE.</span><span class="sxs-lookup"><span data-stu-id="80d2f-107">[JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, \[\], Int32, \[\], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md) returns an array of JET_ENUMCOLUMNVALUE structures.</span></span> <span data-ttu-id="80d2f-108">A matriz é retornada na memória que foi alocada usando o retorno de chamada que foi fornecido para essa função.</span><span class="sxs-lookup"><span data-stu-id="80d2f-108">The array is returned in memory that was allocated using the callback that was supplied to that function.</span></span>

<span data-ttu-id="80d2f-109">O tipo de [JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="80d2f-109">The [JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="80d2f-110">Construtores</span><span class="sxs-lookup"><span data-stu-id="80d2f-110">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="80d2f-111">Nome</span><span class="sxs-lookup"><span data-stu-id="80d2f-111">Name</span></span></th>
<th><span data-ttu-id="80d2f-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="80d2f-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="80d2f-114"><a href="dn335095(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a></span><span class="sxs-lookup"><span data-stu-id="80d2f-114"><a href="dn335095(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="80d2f-115">Parte superior</span><span class="sxs-lookup"><span data-stu-id="80d2f-115">Top</span></span>

## <a name="properties"></a><span data-ttu-id="80d2f-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="80d2f-116">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="80d2f-117">Nome</span><span class="sxs-lookup"><span data-stu-id="80d2f-117">Name</span></span></th>
<th><span data-ttu-id="80d2f-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="80d2f-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="80d2f-120"><a href="dn335097(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="80d2f-120"><a href="dn335097(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="80d2f-121">Obtém o tamanho do valor da coluna para a coluna.</span><span class="sxs-lookup"><span data-stu-id="80d2f-121">Gets the size of the column value for the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="80d2f-123"><a href="dn335144(v=exchg.10).md">erra</a></span><span class="sxs-lookup"><span data-stu-id="80d2f-123"><a href="dn335144(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="80d2f-124">Obtém o código de status da coluna resultante da enumeração do valor da coluna.</span><span class="sxs-lookup"><span data-stu-id="80d2f-124">Gets the column status code resulting from the enumeration of the column value.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="80d2f-126"><a href="dn335102(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="80d2f-126"><a href="dn335102(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="80d2f-127">Obtém o valor da coluna (por índice baseado em um) que foi enumerado.</span><span class="sxs-lookup"><span data-stu-id="80d2f-127">Gets the column value (by one-based index) that was enumerated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="80d2f-129"><a href="dn335149(v=exchg.10).md">pvData</a></span><span class="sxs-lookup"><span data-stu-id="80d2f-129"><a href="dn335149(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="80d2f-130">Obtém o valor que foi enumerado para a coluna.</span><span class="sxs-lookup"><span data-stu-id="80d2f-130">Gets the value that was enumerated for the column.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="80d2f-131">Parte superior</span><span class="sxs-lookup"><span data-stu-id="80d2f-131">Top</span></span>

## <a name="methods"></a><span data-ttu-id="80d2f-132">Métodos</span><span class="sxs-lookup"><span data-stu-id="80d2f-132">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="80d2f-133">Nome</span><span class="sxs-lookup"><span data-stu-id="80d2f-133">Name</span></span></th>
<th><span data-ttu-id="80d2f-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="80d2f-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="80d2f-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Igual a</a></span><span class="sxs-lookup"><span data-stu-id="80d2f-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="80d2f-137">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="80d2f-137">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="80d2f-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizar</a></span><span class="sxs-lookup"><span data-stu-id="80d2f-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="80d2f-140">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="80d2f-140">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="80d2f-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="80d2f-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="80d2f-143">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="80d2f-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="80d2f-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="80d2f-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="80d2f-146">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="80d2f-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="80d2f-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="80d2f-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="80d2f-149">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="80d2f-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="80d2f-151"><a href="dn335096(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="80d2f-151"><a href="dn335096(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="80d2f-152">Retorna uma <a href="/dotnet/api/system.string">cadeia de caracteres</a> que representa a <a href="dn335142(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>atual.</span><span class="sxs-lookup"><span data-stu-id="80d2f-152">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335142(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="80d2f-153">(Substitui <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="80d2f-153">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="80d2f-154">Parte superior</span><span class="sxs-lookup"><span data-stu-id="80d2f-154">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="80d2f-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="80d2f-155">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="80d2f-156">Referência</span><span class="sxs-lookup"><span data-stu-id="80d2f-156">Reference</span></span>

[<span data-ttu-id="80d2f-157">Classe JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="80d2f-157">JET_ENUMCOLUMNVALUE class</span></span>](./jet-enumcolumnvalue-class.md)

[<span data-ttu-id="80d2f-158">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="80d2f-158">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
