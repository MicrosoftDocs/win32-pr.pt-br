---
description: 'Saiba mais sobre: membros da transação'
title: 'Membros da transação '
TOCTitle: Transaction members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Transaction
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction_members(v=EXCHG.10)
ms:contentKeyID: 55104159
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4a11aba5d3ffdc8a0e02bd166aa0a433d4860af5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563167"
---
# <a name="transaction-members"></a><span data-ttu-id="a7129-103">Membros da transação </span><span class="sxs-lookup"><span data-stu-id="a7129-103">Transaction members</span></span>

<span data-ttu-id="a7129-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="a7129-104">Include protected members</span></span>  
<span data-ttu-id="a7129-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="a7129-105">Include inherited members</span></span>  

<span data-ttu-id="a7129-106">Uma classe que encapsula uma transação em um JET_SESID.</span><span class="sxs-lookup"><span data-stu-id="a7129-106">A class that encapsulates a transaction on a JET_SESID.</span></span>

<span data-ttu-id="a7129-107">O tipo de [transação](./transaction-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="a7129-107">The [Transaction](./transaction-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="a7129-108">Construtores</span><span class="sxs-lookup"><span data-stu-id="a7129-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a7129-109">Nome</span><span class="sxs-lookup"><span data-stu-id="a7129-109">Name</span></span></th>
<th><span data-ttu-id="a7129-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7129-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="a7129-112"><a href="dn351177(v=exchg.10).md">Transação</a></span><span class="sxs-lookup"><span data-stu-id="a7129-112"><a href="dn351177(v=exchg.10).md">Transaction</a></span></span></td>
<td><span data-ttu-id="a7129-113">Inicializa uma nova instância da classe Transaction.</span><span class="sxs-lookup"><span data-stu-id="a7129-113">Initializes a new instance of the Transaction class.</span></span> <span data-ttu-id="a7129-114">Isso inicia automaticamente uma transação.</span><span class="sxs-lookup"><span data-stu-id="a7129-114">This automatically begins a transaction.</span></span> <span data-ttu-id="a7129-115">A transação será revertida se não confirmada explicitamente.</span><span class="sxs-lookup"><span data-stu-id="a7129-115">The transaction will be rolled back if not explicitly committed.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a7129-116">Parte superior</span><span class="sxs-lookup"><span data-stu-id="a7129-116">Top</span></span>

## <a name="properties"></a><span data-ttu-id="a7129-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a7129-117">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a7129-118">Nome</span><span class="sxs-lookup"><span data-stu-id="a7129-118">Name</span></span></th>
<th><span data-ttu-id="a7129-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7129-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Propriedade protegida" alt="Protected property" /></td>
<td><span data-ttu-id="a7129-121"><a href="dn350578(v=exchg.10).md">HasResource</a></span><span class="sxs-lookup"><span data-stu-id="a7129-121"><a href="dn350578(v=exchg.10).md">HasResource</a></span></span></td>
<td><span data-ttu-id="a7129-122">Obtém um valor que indica se o recurso subjacente está alocado no momento.</span><span class="sxs-lookup"><span data-stu-id="a7129-122">Gets a value indicating whether the underlying resource is currently allocated.</span></span> <span data-ttu-id="a7129-123">(Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="a7129-123">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="a7129-125"><a href="dn351180(v=exchg.10).md">IsInTransaction</a></span><span class="sxs-lookup"><span data-stu-id="a7129-125"><a href="dn351180(v=exchg.10).md">IsInTransaction</a></span></span></td>
<td><span data-ttu-id="a7129-126">Obtém um valor que indica se este objeto está em uma transação no momento.</span><span class="sxs-lookup"><span data-stu-id="a7129-126">Gets a value indicating whether this object is currently in a transaction.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a7129-127">Parte superior</span><span class="sxs-lookup"><span data-stu-id="a7129-127">Top</span></span>

## <a name="methods"></a><span data-ttu-id="a7129-128">Métodos</span><span class="sxs-lookup"><span data-stu-id="a7129-128">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a7129-129">Nome</span><span class="sxs-lookup"><span data-stu-id="a7129-129">Name</span></span></th>
<th><span data-ttu-id="a7129-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7129-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="a7129-132"><a href="dn351172(v=exchg.10).md">Começar</a></span><span class="sxs-lookup"><span data-stu-id="a7129-132"><a href="dn351172(v=exchg.10).md">Begin</a></span></span></td>
<td><span data-ttu-id="a7129-133">Iniciar uma transação.</span><span class="sxs-lookup"><span data-stu-id="a7129-133">Begin a transaction.</span></span> <span data-ttu-id="a7129-134">Este objeto não deve estar em uma transação no momento.</span><span class="sxs-lookup"><span data-stu-id="a7129-134">This object should not currently be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="a7129-136"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span><span class="sxs-lookup"><span data-stu-id="a7129-136"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="a7129-137">Gerar uma exceção se esse objeto tiver sido descartado.</span><span class="sxs-lookup"><span data-stu-id="a7129-137">Throw an exception if this object has been disposed.</span></span> <span data-ttu-id="a7129-138">(Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="a7129-138">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="a7129-140"><a href="dn351179(v=exchg.10).md">Confirmar (CommitTransactionGrbit)</a></span><span class="sxs-lookup"><span data-stu-id="a7129-140"><a href="dn351179(v=exchg.10).md">Commit(CommitTransactionGrbit)</a></span></span></td>
<td><span data-ttu-id="a7129-141">Confirme uma transação.</span><span class="sxs-lookup"><span data-stu-id="a7129-141">Commit a transaction.</span></span> <span data-ttu-id="a7129-142">Esse objeto deve estar em uma transação.</span><span class="sxs-lookup"><span data-stu-id="a7129-142">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="a7129-144"><a href="dn351243(v=exchg.10).md">Commit (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</a></span><span class="sxs-lookup"><span data-stu-id="a7129-144"><a href="dn351243(v=exchg.10).md">Commit(CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</a></span></span></td>
<td><span data-ttu-id="a7129-145">Confirme uma transação.</span><span class="sxs-lookup"><span data-stu-id="a7129-145">Commit a transaction.</span></span> <span data-ttu-id="a7129-146">Esse objeto deve estar em uma transação.</span><span class="sxs-lookup"><span data-stu-id="a7129-146">This object should be in a transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="a7129-148"><a href="dn350553(v=exchg.10).md">Dispose ()</a></span><span class="sxs-lookup"><span data-stu-id="a7129-148"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="a7129-149">Descartar este objeto, liberando o recurso ESENT subjacente.</span><span class="sxs-lookup"><span data-stu-id="a7129-149">Dispose of this object, releasing the underlying Esent resource.</span></span> <span data-ttu-id="a7129-150">(Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="a7129-150">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="a7129-152"><a href="dn350543(v=exchg.10).md">Dispose (booliano)</a></span><span class="sxs-lookup"><span data-stu-id="a7129-152"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="a7129-153">Chamado por Dispose e o finalizador.</span><span class="sxs-lookup"><span data-stu-id="a7129-153">Called by Dispose and the finalizer.</span></span> <span data-ttu-id="a7129-154">(Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="a7129-154">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="a7129-156"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Igual a</a></span><span class="sxs-lookup"><span data-stu-id="a7129-156"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="a7129-157">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="a7129-157">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="a7129-159"><a href="dn350552(v=exchg.10).md">Finalizar</a></span><span class="sxs-lookup"><span data-stu-id="a7129-159"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="a7129-160">Finaliza uma instância da classe EsentResource.</span><span class="sxs-lookup"><span data-stu-id="a7129-160">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="a7129-161">(Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="a7129-161">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="a7129-163"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="a7129-163"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="a7129-164">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="a7129-164">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="a7129-166"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="a7129-166"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="a7129-167">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="a7129-167">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="a7129-169"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="a7129-169"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="a7129-170">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="a7129-170">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="a7129-172"><a href="dn351176(v=exchg.10).md">ReleaseResource</a></span><span class="sxs-lookup"><span data-stu-id="a7129-172"><a href="dn351176(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="a7129-173">Chamado quando a transação está sendo descartada enquanto ativa.</span><span class="sxs-lookup"><span data-stu-id="a7129-173">Called when the transaction is being disposed while active.</span></span> <span data-ttu-id="a7129-174">Isso deve reverter a transação.</span><span class="sxs-lookup"><span data-stu-id="a7129-174">This should rollback the transaction.</span></span> <span data-ttu-id="a7129-175">(Substitui <a href="dn350545(v=exchg.10).md">EsentResource. ReleaseResource ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="a7129-175">(Overrides <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="a7129-177"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span><span class="sxs-lookup"><span data-stu-id="a7129-177"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="a7129-178">Chamado por uma subclasse quando um recurso é alocado.</span><span class="sxs-lookup"><span data-stu-id="a7129-178">Called by a subclass when a resource is allocated.</span></span> <span data-ttu-id="a7129-179">(Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="a7129-179">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="a7129-181"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span><span class="sxs-lookup"><span data-stu-id="a7129-181"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="a7129-182">Chamado por uma subclasse quando um recurso é liberado.</span><span class="sxs-lookup"><span data-stu-id="a7129-182">Called by a subclass when a resource is freed.</span></span> <span data-ttu-id="a7129-183">(Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="a7129-183">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="a7129-185"><a href="dn351244(v=exchg.10).md">Reversão</a></span><span class="sxs-lookup"><span data-stu-id="a7129-185"><a href="dn351244(v=exchg.10).md">Rollback</a></span></span></td>
<td><span data-ttu-id="a7129-186">Reverter uma transação.</span><span class="sxs-lookup"><span data-stu-id="a7129-186">Rollback a transaction.</span></span> <span data-ttu-id="a7129-187">Esse objeto deve estar em uma transação.</span><span class="sxs-lookup"><span data-stu-id="a7129-187">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="a7129-189"><a href="dn351181(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="a7129-189"><a href="dn351181(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="a7129-190">Retorna uma <a href="/dotnet/api/system.string">cadeia de caracteres</a> que representa a <a href="dn351174(v=exchg.10).md">transação</a>atual.</span><span class="sxs-lookup"><span data-stu-id="a7129-190">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351174(v=exchg.10).md">Transaction</a>.</span></span> <span data-ttu-id="a7129-191">(Substitui <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="a7129-191">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a7129-192">Parte superior</span><span class="sxs-lookup"><span data-stu-id="a7129-192">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="a7129-193">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7129-193">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a7129-194">Referência</span><span class="sxs-lookup"><span data-stu-id="a7129-194">Reference</span></span>

[<span data-ttu-id="a7129-195">Classe de transação</span><span class="sxs-lookup"><span data-stu-id="a7129-195">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="a7129-196">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a7129-196">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
