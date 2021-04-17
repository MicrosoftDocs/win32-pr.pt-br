---
description: 'Saiba mais sobre: membros de tabela'
title: 'Membros da tabela '
TOCTitle: Table members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Table
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table_members(v=EXCHG.10)
ms:contentKeyID: 55104054
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: b4e5bd09cf1c450197978e3126dc63fe96ec6425
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104557311"
---
# <a name="table-members"></a><span data-ttu-id="5cf1c-103">Membros da tabela </span><span class="sxs-lookup"><span data-stu-id="5cf1c-103">Table members</span></span>

<span data-ttu-id="5cf1c-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="5cf1c-104">Include protected members</span></span>  
<span data-ttu-id="5cf1c-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="5cf1c-105">Include inherited members</span></span>  

<span data-ttu-id="5cf1c-106">Uma classe que encapsula um JET_TABLEID em um objeto descartável.</span><span class="sxs-lookup"><span data-stu-id="5cf1c-106">A class that encapsulates a JET_TABLEID in a disposable object.</span></span> <span data-ttu-id="5cf1c-107">Isso abre uma tabela existente.</span><span class="sxs-lookup"><span data-stu-id="5cf1c-107">This opens an existing table.</span></span> <span data-ttu-id="5cf1c-108">Para criar uma tabela, use o método JetCreateTable.</span><span class="sxs-lookup"><span data-stu-id="5cf1c-108">To create a table use the JetCreateTable method.</span></span>

<span data-ttu-id="5cf1c-109">O tipo de [tabela](./table-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="5cf1c-109">The [Table](./table-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="5cf1c-110">Construtores</span><span class="sxs-lookup"><span data-stu-id="5cf1c-110">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="5cf1c-111">Nome</span><span class="sxs-lookup"><span data-stu-id="5cf1c-111">Name</span></span></th>
<th><span data-ttu-id="5cf1c-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="5cf1c-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5cf1c-114"><a href="dn351234(v=exchg.10).md">Table</a></span><span class="sxs-lookup"><span data-stu-id="5cf1c-114"><a href="dn351234(v=exchg.10).md">Table</a></span></span></td>
<td><span data-ttu-id="5cf1c-115">Inicializa uma nova instância da classe da tabela.</span><span class="sxs-lookup"><span data-stu-id="5cf1c-115">Initializes a new instance of the Table class.</span></span> <span data-ttu-id="5cf1c-116">A tabela é aberta do banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="5cf1c-116">The table is opened from the given database.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5cf1c-117">Parte superior</span><span class="sxs-lookup"><span data-stu-id="5cf1c-117">Top</span></span>

## <a name="properties"></a><span data-ttu-id="5cf1c-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5cf1c-118">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="5cf1c-119">Nome</span><span class="sxs-lookup"><span data-stu-id="5cf1c-119">Name</span></span></th>
<th><span data-ttu-id="5cf1c-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="5cf1c-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Propriedade protegida" alt="Protected property" /></td>
<td><span data-ttu-id="5cf1c-122"><a href="dn350578(v=exchg.10).md">HasResource</a></span><span class="sxs-lookup"><span data-stu-id="5cf1c-122"><a href="dn350578(v=exchg.10).md">HasResource</a></span></span></td>
<td><span data-ttu-id="5cf1c-123">Obtém um valor que indica se o recurso subjacente está alocado no momento.</span><span class="sxs-lookup"><span data-stu-id="5cf1c-123">Gets a value indicating whether the underlying resource is currently allocated.</span></span> <span data-ttu-id="5cf1c-124">(Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="5cf1c-124">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="5cf1c-126"><a href="dn351171(v=exchg.10).md">JetTableid</a></span><span class="sxs-lookup"><span data-stu-id="5cf1c-126"><a href="dn351171(v=exchg.10).md">JetTableid</a></span></span></td>
<td><span data-ttu-id="5cf1c-127">Obtém o JET_TABLEID que esta tabela contém.</span><span class="sxs-lookup"><span data-stu-id="5cf1c-127">Gets the JET_TABLEID that this table contains.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="5cf1c-129"><a href="dn351170(v=exchg.10).md">Nome</a></span><span class="sxs-lookup"><span data-stu-id="5cf1c-129"><a href="dn351170(v=exchg.10).md">Name</a></span></span></td>
<td><span data-ttu-id="5cf1c-130">Obtém o nome desta tabela.</span><span class="sxs-lookup"><span data-stu-id="5cf1c-130">Gets the name of this table.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5cf1c-131">Parte superior</span><span class="sxs-lookup"><span data-stu-id="5cf1c-131">Top</span></span>

## <a name="methods"></a><span data-ttu-id="5cf1c-132">Métodos</span><span class="sxs-lookup"><span data-stu-id="5cf1c-132">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="5cf1c-133">Nome</span><span class="sxs-lookup"><span data-stu-id="5cf1c-133">Name</span></span></th>
<th><span data-ttu-id="5cf1c-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="5cf1c-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="5cf1c-136"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span><span class="sxs-lookup"><span data-stu-id="5cf1c-136"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="5cf1c-137">Gerar uma exceção se esse objeto tiver sido descartado.</span><span class="sxs-lookup"><span data-stu-id="5cf1c-137">Throw an exception if this object has been disposed.</span></span> <span data-ttu-id="5cf1c-138">(Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="5cf1c-138">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5cf1c-140"><a href="dn351235(v=exchg.10).md">Close</a></span><span class="sxs-lookup"><span data-stu-id="5cf1c-140"><a href="dn351235(v=exchg.10).md">Close</a></span></span></td>
<td><span data-ttu-id="5cf1c-141">Feche a tabela.</span><span class="sxs-lookup"><span data-stu-id="5cf1c-141">Close the table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5cf1c-143"><a href="dn350553(v=exchg.10).md">Dispose ()</a></span><span class="sxs-lookup"><span data-stu-id="5cf1c-143"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="5cf1c-144">Descartar este objeto, liberando o recurso ESENT subjacente.</span><span class="sxs-lookup"><span data-stu-id="5cf1c-144">Dispose of this object, releasing the underlying Esent resource.</span></span> <span data-ttu-id="5cf1c-145">(Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="5cf1c-145">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="5cf1c-147"><a href="dn350543(v=exchg.10).md">Dispose (booliano)</a></span><span class="sxs-lookup"><span data-stu-id="5cf1c-147"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="5cf1c-148">Chamado por Dispose e o finalizador.</span><span class="sxs-lookup"><span data-stu-id="5cf1c-148">Called by Dispose and the finalizer.</span></span> <span data-ttu-id="5cf1c-149">(Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="5cf1c-149">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5cf1c-151"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Igual a</a></span><span class="sxs-lookup"><span data-stu-id="5cf1c-151"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="5cf1c-152">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="5cf1c-152">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="5cf1c-154"><a href="dn350552(v=exchg.10).md">Finalizar</a></span><span class="sxs-lookup"><span data-stu-id="5cf1c-154"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="5cf1c-155">Finaliza uma instância da classe EsentResource.</span><span class="sxs-lookup"><span data-stu-id="5cf1c-155">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="5cf1c-156">(Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="5cf1c-156">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5cf1c-158"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="5cf1c-158"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="5cf1c-159">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="5cf1c-159">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5cf1c-161"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="5cf1c-161"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="5cf1c-162">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="5cf1c-162">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="5cf1c-164"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="5cf1c-164"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="5cf1c-165">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="5cf1c-165">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="5cf1c-167"><a href="dn351168(v=exchg.10).md">ReleaseResource</a></span><span class="sxs-lookup"><span data-stu-id="5cf1c-167"><a href="dn351168(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="5cf1c-168">Libere o JET_TABLEID subjacente.</span><span class="sxs-lookup"><span data-stu-id="5cf1c-168">Free the underlying JET_TABLEID.</span></span> <span data-ttu-id="5cf1c-169">(Substitui <a href="dn350545(v=exchg.10).md">EsentResource. ReleaseResource ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="5cf1c-169">(Overrides <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="5cf1c-171"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span><span class="sxs-lookup"><span data-stu-id="5cf1c-171"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="5cf1c-172">Chamado por uma subclasse quando um recurso é alocado.</span><span class="sxs-lookup"><span data-stu-id="5cf1c-172">Called by a subclass when a resource is allocated.</span></span> <span data-ttu-id="5cf1c-173">(Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="5cf1c-173">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="5cf1c-175"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span><span class="sxs-lookup"><span data-stu-id="5cf1c-175"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="5cf1c-176">Chamado por uma subclasse quando um recurso é liberado.</span><span class="sxs-lookup"><span data-stu-id="5cf1c-176">Called by a subclass when a resource is freed.</span></span> <span data-ttu-id="5cf1c-177">(Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="5cf1c-177">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5cf1c-179"><a href="dn351237(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="5cf1c-179"><a href="dn351237(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="5cf1c-180">Retorna uma <a href="/dotnet/api/system.string">cadeia de caracteres</a> que representa a <a href="dn351163(v=exchg.10).md">tabela</a>atual.</span><span class="sxs-lookup"><span data-stu-id="5cf1c-180">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351163(v=exchg.10).md">Table</a>.</span></span> <span data-ttu-id="5cf1c-181">(Substitui <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="5cf1c-181">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5cf1c-182">Parte superior</span><span class="sxs-lookup"><span data-stu-id="5cf1c-182">Top</span></span>

## <a name="operators"></a><span data-ttu-id="5cf1c-183">Operadores</span><span class="sxs-lookup"><span data-stu-id="5cf1c-183">Operators</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="5cf1c-184">Nome</span><span class="sxs-lookup"><span data-stu-id="5cf1c-184">Name</span></span></th>
<th><span data-ttu-id="5cf1c-185">Descrição</span><span class="sxs-lookup"><span data-stu-id="5cf1c-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operador público" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="5cf1c-188"><a href="dn351239(v=exchg.10).md">Implícito (tabela para JET_TABLEID)</a></span><span class="sxs-lookup"><span data-stu-id="5cf1c-188"><a href="dn351239(v=exchg.10).md">Implicit(Table to JET_TABLEID)</a></span></span></td>
<td><span data-ttu-id="5cf1c-189">Operador de conversão implícita de uma tabela para um JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="5cf1c-189">Implicit conversion operator from a Table to a JET_TABLEID.</span></span> <span data-ttu-id="5cf1c-190">Isso permite que uma tabela seja usada com APIs que esperam um JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="5cf1c-190">This allows a Table to be used with APIs which expect a JET_TABLEID.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5cf1c-191">Parte superior</span><span class="sxs-lookup"><span data-stu-id="5cf1c-191">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="5cf1c-192">Confira também</span><span class="sxs-lookup"><span data-stu-id="5cf1c-192">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5cf1c-193">Referência</span><span class="sxs-lookup"><span data-stu-id="5cf1c-193">Reference</span></span>

[<span data-ttu-id="5cf1c-194">Classe de tabela</span><span class="sxs-lookup"><span data-stu-id="5cf1c-194">Table class</span></span>](./table-class.md)

[<span data-ttu-id="5cf1c-195">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5cf1c-195">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
