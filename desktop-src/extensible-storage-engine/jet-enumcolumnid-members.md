---
description: 'Saiba mais sobre: membros do JET_ENUMCOLUMNID'
title: Membros do JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_members(v=EXCHG.10)
ms:contentKeyID: 55103504
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: f852541d8e16a1a9edfd87afe59a0a8a4c4c4af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010360"
---
# <a name="jet_enumcolumnid-members"></a><span data-ttu-id="0d4e5-103">Membros do JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="0d4e5-103">JET_ENUMCOLUMNID members</span></span>

<span data-ttu-id="0d4e5-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="0d4e5-104">Include protected members</span></span>  
<span data-ttu-id="0d4e5-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="0d4e5-105">Include inherited members</span></span>  

<span data-ttu-id="0d4e5-106">Enumera um conjunto específico de colunas e, opcionalmente, um conjunto específico de vários valores para essas colunas quando a função JetEnumerateColumns é usada.</span><span class="sxs-lookup"><span data-stu-id="0d4e5-106">Enumerates a specific set of columns and, optionally, a specific set of multiple values for those columns when the JetEnumerateColumns function is used.</span></span> <span data-ttu-id="0d4e5-107">O JetEnumerateColumns, opcionalmente, usa uma matriz de estruturas JET_ENUMCOLUMNID.</span><span class="sxs-lookup"><span data-stu-id="0d4e5-107">JetEnumerateColumns optionally takes an array of JET_ENUMCOLUMNID structures.</span></span>

<span data-ttu-id="0d4e5-108">O tipo de [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="0d4e5-108">The [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="0d4e5-109">Construtores</span><span class="sxs-lookup"><span data-stu-id="0d4e5-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="0d4e5-110">Nome</span><span class="sxs-lookup"><span data-stu-id="0d4e5-110">Name</span></span></th>
<th><span data-ttu-id="0d4e5-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d4e5-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="0d4e5-113"><a href="dn335140(v=exchg.10).md">JET_ENUMCOLUMNID</a></span><span class="sxs-lookup"><span data-stu-id="0d4e5-113"><a href="dn335140(v=exchg.10).md">JET_ENUMCOLUMNID</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0d4e5-114">Parte superior</span><span class="sxs-lookup"><span data-stu-id="0d4e5-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="0d4e5-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0d4e5-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="0d4e5-116">Nome</span><span class="sxs-lookup"><span data-stu-id="0d4e5-116">Name</span></span></th>
<th><span data-ttu-id="0d4e5-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d4e5-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="0d4e5-119"><a href="dn335141(v=exchg.10).md">columnid</a></span><span class="sxs-lookup"><span data-stu-id="0d4e5-119"><a href="dn335141(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="0d4e5-120">Obtém ou define a ID de columnid a ser enumerada.</span><span class="sxs-lookup"><span data-stu-id="0d4e5-120">Gets or sets the columnid ID to enumerate.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="0d4e5-122"><a href="dn335092(v=exchg.10).md">ctagSequence</a></span><span class="sxs-lookup"><span data-stu-id="0d4e5-122"><a href="dn335092(v=exchg.10).md">ctagSequence</a></span></span></td>
<td><span data-ttu-id="0d4e5-123">Obtém ou define a contagem de valores de coluna (por índice baseado em um) para enumerar para a ID de coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="0d4e5-123">Gets or sets the count of column values (by one-based index) to enumerate for the specified column ID.</span></span> <span data-ttu-id="0d4e5-124">Se ctagSequence for 0 (zero), rgtagSequence será ignorado e todos os valores de coluna para a ID de coluna especificada serão enumerados.</span><span class="sxs-lookup"><span data-stu-id="0d4e5-124">If ctagSequence is 0 (zero) then rgtagSequence is ignored and all column values for the specified column ID will be enumerated.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="0d4e5-126"><a href="dn335093(v=exchg.10).md">rgtagSequence</a></span><span class="sxs-lookup"><span data-stu-id="0d4e5-126"><a href="dn335093(v=exchg.10).md">rgtagSequence</a></span></span></td>
<td><span data-ttu-id="0d4e5-127">Obtém ou define a matriz de índices com base em um na matriz de valores de coluna para uma determinada coluna.</span><span class="sxs-lookup"><span data-stu-id="0d4e5-127">Gets or sets the array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="0d4e5-128">Um único elemento é um itagSequence que é definido em JET_RETRIEVECOLUMN.</span><span class="sxs-lookup"><span data-stu-id="0d4e5-128">A single element is an itagSequence which is defined in JET_RETRIEVECOLUMN.</span></span> <span data-ttu-id="0d4e5-129">Um itagSequence de 0 (zero) significa &quot; ignorar &quot; .</span><span class="sxs-lookup"><span data-stu-id="0d4e5-129">An itagSequence of 0 (zero) means &quot;skip&quot;.</span></span> <span data-ttu-id="0d4e5-130">Um itagSequence de 1 significa retornar o primeiro valor de coluna da coluna, 2 significa o segundo e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="0d4e5-130">An itagSequence of 1 means return the first column value of the column, 2 means the second, and so on.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0d4e5-131">Parte superior</span><span class="sxs-lookup"><span data-stu-id="0d4e5-131">Top</span></span>

## <a name="methods"></a><span data-ttu-id="0d4e5-132">Métodos</span><span class="sxs-lookup"><span data-stu-id="0d4e5-132">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="0d4e5-133">Nome</span><span class="sxs-lookup"><span data-stu-id="0d4e5-133">Name</span></span></th>
<th><span data-ttu-id="0d4e5-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d4e5-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="0d4e5-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Igual a</a></span><span class="sxs-lookup"><span data-stu-id="0d4e5-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="0d4e5-137">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="0d4e5-137">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="0d4e5-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizar</a></span><span class="sxs-lookup"><span data-stu-id="0d4e5-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="0d4e5-140">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="0d4e5-140">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="0d4e5-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="0d4e5-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="0d4e5-143">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="0d4e5-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="0d4e5-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="0d4e5-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="0d4e5-146">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="0d4e5-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="0d4e5-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="0d4e5-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="0d4e5-149">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="0d4e5-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="0d4e5-151"><a href="dn335091(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="0d4e5-151"><a href="dn335091(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="0d4e5-152">Retorna uma <a href="/dotnet/api/system.string">cadeia de caracteres</a> que representa a <a href="dn335139(v=exchg.10).md">JET_ENUMCOLUMNID</a>atual.</span><span class="sxs-lookup"><span data-stu-id="0d4e5-152">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335139(v=exchg.10).md">JET_ENUMCOLUMNID</a>.</span></span> <span data-ttu-id="0d4e5-153">(Substitui <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="0d4e5-153">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0d4e5-154">Parte superior</span><span class="sxs-lookup"><span data-stu-id="0d4e5-154">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="0d4e5-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d4e5-155">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0d4e5-156">Referência</span><span class="sxs-lookup"><span data-stu-id="0d4e5-156">Reference</span></span>

[<span data-ttu-id="0d4e5-157">Classe JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="0d4e5-157">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="0d4e5-158">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0d4e5-158">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
