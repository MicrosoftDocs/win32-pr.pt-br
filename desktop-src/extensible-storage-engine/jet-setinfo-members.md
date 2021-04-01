---
description: 'Saiba mais sobre: membros do JET_SETINFO'
title: Membros do JET_SETINFO
TOCTitle: JET_SETINFO members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_SETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo_members(v=EXCHG.10)
ms:contentKeyID: 55103871
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c782eace916b3871ade67870b08e1766faeafd28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646897"
---
# <a name="jet_setinfo-members"></a><span data-ttu-id="3b260-103">Membros do JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="3b260-103">JET_SETINFO members</span></span>

<span data-ttu-id="3b260-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="3b260-104">Include protected members</span></span>  
<span data-ttu-id="3b260-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="3b260-105">Include inherited members</span></span>  

<span data-ttu-id="3b260-106">Configurações para JetSetColumn.</span><span class="sxs-lookup"><span data-stu-id="3b260-106">Settings for JetSetColumn.</span></span>

<span data-ttu-id="3b260-107">O tipo de [JET_SETINFO](./jet-setinfo-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="3b260-107">The [JET_SETINFO](./jet-setinfo-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="3b260-108">Construtores</span><span class="sxs-lookup"><span data-stu-id="3b260-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3b260-109">Nome</span><span class="sxs-lookup"><span data-stu-id="3b260-109">Name</span></span></th>
<th><span data-ttu-id="3b260-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b260-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="3b260-112"><a href="dn351031(v=exchg.10).md">JET_SETINFO</a></span><span class="sxs-lookup"><span data-stu-id="3b260-112"><a href="dn351031(v=exchg.10).md">JET_SETINFO</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3b260-113">Parte superior</span><span class="sxs-lookup"><span data-stu-id="3b260-113">Top</span></span>

## <a name="properties"></a><span data-ttu-id="3b260-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3b260-114">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3b260-115">Nome</span><span class="sxs-lookup"><span data-stu-id="3b260-115">Name</span></span></th>
<th><span data-ttu-id="3b260-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b260-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="3b260-118"><a href="dn351064(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="3b260-118"><a href="dn351064(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="3b260-119">Obtém ou define o deslocamento para o primeiro byte a ser definido em uma coluna do tipo <a href="hh577895(v=exchg.10).md">LongBinary</a> ou <a href="hh577895(v=exchg.10).md">LONGTEXT</a>.</span><span class="sxs-lookup"><span data-stu-id="3b260-119">Gets or sets offset to the first byte to be set in a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="3b260-121"><a href="dn351037(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="3b260-121"><a href="dn351037(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="3b260-122">Obtém ou define o número de sequência do valor em uma coluna de valores múltiplos a ser definida.</span><span class="sxs-lookup"><span data-stu-id="3b260-122">Gets or sets the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="3b260-123">A matriz de valores é baseada em um.</span><span class="sxs-lookup"><span data-stu-id="3b260-123">The array of values is one-based.</span></span> <span data-ttu-id="3b260-124">O primeiro valor é Sequence 1, não 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="3b260-124">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="3b260-125">Se a coluna de registro tiver apenas um valor, 1 deverá ser passado como itagSequence se esse valor estiver sendo substituído.</span><span class="sxs-lookup"><span data-stu-id="3b260-125">If the record column has only one value then 1 should be passed as the itagSequence if that value is being replaced.</span></span> <span data-ttu-id="3b260-126">Um valor de 0 (zero) significa adicionar uma nova instância de valor de coluna ao final da sequência de valores de coluna.</span><span class="sxs-lookup"><span data-stu-id="3b260-126">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3b260-127">Parte superior</span><span class="sxs-lookup"><span data-stu-id="3b260-127">Top</span></span>

## <a name="methods"></a><span data-ttu-id="3b260-128">Métodos</span><span class="sxs-lookup"><span data-stu-id="3b260-128">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3b260-129">Nome</span><span class="sxs-lookup"><span data-stu-id="3b260-129">Name</span></span></th>
<th><span data-ttu-id="3b260-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b260-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="3b260-132"><a href="dn351060(v=exchg.10).md">ContentEquals</a></span><span class="sxs-lookup"><span data-stu-id="3b260-132"><a href="dn351060(v=exchg.10).md">ContentEquals</a></span></span></td>
<td><span data-ttu-id="3b260-133">Retorna um valor que indica se essa instância é igual a outra instância.</span><span class="sxs-lookup"><span data-stu-id="3b260-133">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="3b260-135"><a href="dn351032(v=exchg.10).md">DeepClone</a></span><span class="sxs-lookup"><span data-stu-id="3b260-135"><a href="dn351032(v=exchg.10).md">DeepClone</a></span></span></td>
<td><span data-ttu-id="3b260-136">Retorna uma cópia profunda do objeto.</span><span class="sxs-lookup"><span data-stu-id="3b260-136">Returns a deep copy of the object.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="3b260-138"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Igual a</a></span><span class="sxs-lookup"><span data-stu-id="3b260-138"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="3b260-139">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="3b260-139">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="3b260-141"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizar</a></span><span class="sxs-lookup"><span data-stu-id="3b260-141"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="3b260-142">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="3b260-142">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="3b260-144"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="3b260-144"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="3b260-145">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="3b260-145">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="3b260-147"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="3b260-147"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="3b260-148">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="3b260-148">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="3b260-150"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="3b260-150"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="3b260-151">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="3b260-151">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="3b260-153"><a href="dn351062(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="3b260-153"><a href="dn351062(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="3b260-154">Retorna uma <a href="/dotnet/api/system.string">cadeia de caracteres</a> que representa a <a href="dn351059(v=exchg.10).md">JET_SETINFO</a>atual.</span><span class="sxs-lookup"><span data-stu-id="3b260-154">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351059(v=exchg.10).md">JET_SETINFO</a>.</span></span> <span data-ttu-id="3b260-155">(Substitui <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="3b260-155">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3b260-156">Parte superior</span><span class="sxs-lookup"><span data-stu-id="3b260-156">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="3b260-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b260-157">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3b260-158">Referência</span><span class="sxs-lookup"><span data-stu-id="3b260-158">Reference</span></span>

[<span data-ttu-id="3b260-159">Classe JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="3b260-159">JET_SETINFO class</span></span>](./jet-setinfo-class.md)

[<span data-ttu-id="3b260-160">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3b260-160">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
