---
description: 'Saiba mais sobre: membros do JET_ENUMCOLUMN'
title: Membros do JET_ENUMCOLUMN
TOCTitle: JET_ENUMCOLUMN members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn_members(v=EXCHG.10)
ms:contentKeyID: 55103614
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: a1281d7d81fc4e0db476c4ca0f9ac688a7a7b055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564840"
---
# <a name="jet_enumcolumn-members"></a><span data-ttu-id="3132c-103">Membros do JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="3132c-103">JET_ENUMCOLUMN members</span></span>

<span data-ttu-id="3132c-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="3132c-104">Include protected members</span></span>  
<span data-ttu-id="3132c-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="3132c-105">Include inherited members</span></span>  

<span data-ttu-id="3132c-106">Enumera os valores de coluna de um registro usando a função JetEnumerateColumns.</span><span class="sxs-lookup"><span data-stu-id="3132c-106">Enumerates the column values of a record using the JetEnumerateColumns function.</span></span> <span data-ttu-id="3132c-107">JetEnumerateColumns retorna uma matriz de estruturas de JET_ENUMCOLUMNVALUE.</span><span class="sxs-lookup"><span data-stu-id="3132c-107">JetEnumerateColumns returns an array of JET_ENUMCOLUMNVALUE structures.</span></span> <span data-ttu-id="3132c-108">A matriz é retornada na memória que foi alocada usando o retorno de chamada que foi fornecido para essa função.</span><span class="sxs-lookup"><span data-stu-id="3132c-108">The array is returned in memory that was allocated using the callback that was supplied to that function.</span></span>

<span data-ttu-id="3132c-109">O tipo de [JET_ENUMCOLUMN](./jet-enumcolumn-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="3132c-109">The [JET_ENUMCOLUMN](./jet-enumcolumn-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="3132c-110">Construtores</span><span class="sxs-lookup"><span data-stu-id="3132c-110">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3132c-111">Nome</span><span class="sxs-lookup"><span data-stu-id="3132c-111">Name</span></span></th>
<th><span data-ttu-id="3132c-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="3132c-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="3132c-114"><a href="dn335131(v=exchg.10).md">JET_ENUMCOLUMN</a></span><span class="sxs-lookup"><span data-stu-id="3132c-114"><a href="dn335131(v=exchg.10).md">JET_ENUMCOLUMN</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3132c-115">Parte superior</span><span class="sxs-lookup"><span data-stu-id="3132c-115">Top</span></span>

## <a name="properties"></a><span data-ttu-id="3132c-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3132c-116">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3132c-117">Nome</span><span class="sxs-lookup"><span data-stu-id="3132c-117">Name</span></span></th>
<th><span data-ttu-id="3132c-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="3132c-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="3132c-120"><a href="dn335137(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="3132c-120"><a href="dn335137(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="3132c-121">Obtém o tamanho do valor que foi enumerado para a coluna.</span><span class="sxs-lookup"><span data-stu-id="3132c-121">Gets the size of the value that was enumerated for the column.</span></span> <span data-ttu-id="3132c-122">Esse membro só será usado se <a href="dn335086(v=exchg.10).md">Err</a> for igual a <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span><span class="sxs-lookup"><span data-stu-id="3132c-122">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is equal to <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="3132c-124"><a href="dn335085(v=exchg.10).md">cEnumColumnValue</a></span><span class="sxs-lookup"><span data-stu-id="3132c-124"><a href="dn335085(v=exchg.10).md">cEnumColumnValue</a></span></span></td>
<td><span data-ttu-id="3132c-125">Obtém o número de valores de coluna enumerados para a coluna.</span><span class="sxs-lookup"><span data-stu-id="3132c-125">Gets the number of column values enumerated for the column.</span></span> <span data-ttu-id="3132c-126">Esse membro só será usado se <a href="dn335086(v=exchg.10).md">Err</a> não for <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span><span class="sxs-lookup"><span data-stu-id="3132c-126">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is not <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="3132c-128"><a href="dn335135(v=exchg.10).md">columnid</a></span><span class="sxs-lookup"><span data-stu-id="3132c-128"><a href="dn335135(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="3132c-129">Obtém a ID de columnid que foi enumerada.</span><span class="sxs-lookup"><span data-stu-id="3132c-129">Gets the columnid ID that was enumerated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="3132c-131"><a href="dn335086(v=exchg.10).md">erra</a></span><span class="sxs-lookup"><span data-stu-id="3132c-131"><a href="dn335086(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="3132c-132">Obtém o código de status da coluna que resulta da enumeração.</span><span class="sxs-lookup"><span data-stu-id="3132c-132">Gets the column status code that results from the enumeration.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="3132c-134"><a href="dn335087(v=exchg.10).md">pvData</a></span><span class="sxs-lookup"><span data-stu-id="3132c-134"><a href="dn335087(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="3132c-135">Obtém o valor que foi enumerado para a coluna.</span><span class="sxs-lookup"><span data-stu-id="3132c-135">Gets the value that was enumerated for the column.</span></span> <span data-ttu-id="3132c-136">Esse membro só será usado se <a href="dn335086(v=exchg.10).md">Err</a> for igual a <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span><span class="sxs-lookup"><span data-stu-id="3132c-136">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is equal to <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span> <span data-ttu-id="3132c-137">Isso aponta para a memória alocada com o retorno de chamada de alocador de <a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a> passado para <a href="dn292148(v=exchg.10).md">JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a>.</span><span class="sxs-lookup"><span data-stu-id="3132c-137">This points to memory allocated with the <a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a> allocator callback passed to <a href="dn292148(v=exchg.10).md">JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a>.</span></span> <span data-ttu-id="3132c-138">Lembre-se de liberar a memória quando terminar.</span><span class="sxs-lookup"><span data-stu-id="3132c-138">Remember to release the memory when finished.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="3132c-140"><a href="dn335089(v=exchg.10).md">rgEnumColumnValue</a></span><span class="sxs-lookup"><span data-stu-id="3132c-140"><a href="dn335089(v=exchg.10).md">rgEnumColumnValue</a></span></span></td>
<td><span data-ttu-id="3132c-141">Obtém os valores da coluna enumerada para a coluna.</span><span class="sxs-lookup"><span data-stu-id="3132c-141">Gets the enumerated column values for the column.</span></span> <span data-ttu-id="3132c-142">Esse membro só será usado se <a href="dn335086(v=exchg.10).md">Err</a> não for <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span><span class="sxs-lookup"><span data-stu-id="3132c-142">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is not <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3132c-143">Parte superior</span><span class="sxs-lookup"><span data-stu-id="3132c-143">Top</span></span>

## <a name="methods"></a><span data-ttu-id="3132c-144">Métodos</span><span class="sxs-lookup"><span data-stu-id="3132c-144">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3132c-145">Nome</span><span class="sxs-lookup"><span data-stu-id="3132c-145">Name</span></span></th>
<th><span data-ttu-id="3132c-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="3132c-146">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="3132c-148"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Igual a</a></span><span class="sxs-lookup"><span data-stu-id="3132c-148"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="3132c-149">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="3132c-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="3132c-151"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizar</a></span><span class="sxs-lookup"><span data-stu-id="3132c-151"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="3132c-152">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="3132c-152">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="3132c-154"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="3132c-154"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="3132c-155">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="3132c-155">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="3132c-157"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="3132c-157"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="3132c-158">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="3132c-158">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="3132c-160"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="3132c-160"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="3132c-161">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="3132c-161">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="3132c-163"><a href="dn335132(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="3132c-163"><a href="dn335132(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="3132c-164">Retorna uma <a href="/dotnet/api/system.string">cadeia de caracteres</a> que representa a <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a>atual.</span><span class="sxs-lookup"><span data-stu-id="3132c-164">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a>.</span></span> <span data-ttu-id="3132c-165">(Substitui <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="3132c-165">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3132c-166">Parte superior</span><span class="sxs-lookup"><span data-stu-id="3132c-166">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="3132c-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="3132c-167">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3132c-168">Referência</span><span class="sxs-lookup"><span data-stu-id="3132c-168">Reference</span></span>

[<span data-ttu-id="3132c-169">Classe JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="3132c-169">JET_ENUMCOLUMN class</span></span>](./jet-enumcolumn-class.md)

[<span data-ttu-id="3132c-170">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3132c-170">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
