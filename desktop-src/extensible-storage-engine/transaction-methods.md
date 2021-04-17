---
description: 'Saiba mais sobre: métodos de transação'
title: 'Métodos de transação '
TOCTitle: Transaction methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Transaction
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction_methods(v=EXCHG.10)
ms:contentKeyID: 55104163
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c926d00f785aab3a63cd8ebc7eebaf74ea5f0e23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104567810"
---
# <a name="transaction-methods"></a><span data-ttu-id="d54be-103">Métodos de transação </span><span class="sxs-lookup"><span data-stu-id="d54be-103">Transaction methods</span></span>

<span data-ttu-id="d54be-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="d54be-104">Include protected members</span></span>  
<span data-ttu-id="d54be-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="d54be-105">Include inherited members</span></span>  

<span data-ttu-id="d54be-106">O tipo de [transação](./transaction-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="d54be-106">The [Transaction](./transaction-class.md) type exposes the following members.</span></span>

## <a name="methods"></a><span data-ttu-id="d54be-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="d54be-107">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="d54be-108">Nome</span><span class="sxs-lookup"><span data-stu-id="d54be-108">Name</span></span></th>
<th><span data-ttu-id="d54be-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d54be-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="d54be-111"><a href="dn351172(v=exchg.10).md">Começar</a></span><span class="sxs-lookup"><span data-stu-id="d54be-111"><a href="dn351172(v=exchg.10).md">Begin</a></span></span></td>
<td><span data-ttu-id="d54be-112">Iniciar uma transação.</span><span class="sxs-lookup"><span data-stu-id="d54be-112">Begin a transaction.</span></span> <span data-ttu-id="d54be-113">Este objeto não deve estar em uma transação no momento.</span><span class="sxs-lookup"><span data-stu-id="d54be-113">This object should not currently be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="d54be-115"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span><span class="sxs-lookup"><span data-stu-id="d54be-115"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="d54be-116">Gerar uma exceção se esse objeto tiver sido descartado.</span><span class="sxs-lookup"><span data-stu-id="d54be-116">Throw an exception if this object has been disposed.</span></span> <span data-ttu-id="d54be-117">(Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="d54be-117">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="d54be-119"><a href="dn351179(v=exchg.10).md">Confirmar (CommitTransactionGrbit)</a></span><span class="sxs-lookup"><span data-stu-id="d54be-119"><a href="dn351179(v=exchg.10).md">Commit(CommitTransactionGrbit)</a></span></span></td>
<td><span data-ttu-id="d54be-120">Confirme uma transação.</span><span class="sxs-lookup"><span data-stu-id="d54be-120">Commit a transaction.</span></span> <span data-ttu-id="d54be-121">Esse objeto deve estar em uma transação.</span><span class="sxs-lookup"><span data-stu-id="d54be-121">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="d54be-123"><a href="dn351243(v=exchg.10).md">Commit (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</a></span><span class="sxs-lookup"><span data-stu-id="d54be-123"><a href="dn351243(v=exchg.10).md">Commit(CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</a></span></span></td>
<td><span data-ttu-id="d54be-124">Confirme uma transação.</span><span class="sxs-lookup"><span data-stu-id="d54be-124">Commit a transaction.</span></span> <span data-ttu-id="d54be-125">Esse objeto deve estar em uma transação.</span><span class="sxs-lookup"><span data-stu-id="d54be-125">This object should be in a transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="d54be-127"><a href="dn350553(v=exchg.10).md">Dispose ()</a></span><span class="sxs-lookup"><span data-stu-id="d54be-127"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="d54be-128">Descartar este objeto, liberando o recurso ESENT subjacente.</span><span class="sxs-lookup"><span data-stu-id="d54be-128">Dispose of this object, releasing the underlying Esent resource.</span></span> <span data-ttu-id="d54be-129">(Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="d54be-129">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="d54be-131"><a href="dn350543(v=exchg.10).md">Dispose (booliano)</a></span><span class="sxs-lookup"><span data-stu-id="d54be-131"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="d54be-132">Chamado por Dispose e o finalizador.</span><span class="sxs-lookup"><span data-stu-id="d54be-132">Called by Dispose and the finalizer.</span></span> <span data-ttu-id="d54be-133">(Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="d54be-133">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="d54be-135"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Igual a</a></span><span class="sxs-lookup"><span data-stu-id="d54be-135"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="d54be-136">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="d54be-136">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="d54be-138"><a href="dn350552(v=exchg.10).md">Finalizar</a></span><span class="sxs-lookup"><span data-stu-id="d54be-138"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="d54be-139">Finaliza uma instância da classe EsentResource.</span><span class="sxs-lookup"><span data-stu-id="d54be-139">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="d54be-140">(Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="d54be-140">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="d54be-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="d54be-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="d54be-143">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="d54be-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="d54be-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="d54be-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="d54be-146">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="d54be-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="d54be-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="d54be-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="d54be-149">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="d54be-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="d54be-151"><a href="dn351176(v=exchg.10).md">ReleaseResource</a></span><span class="sxs-lookup"><span data-stu-id="d54be-151"><a href="dn351176(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="d54be-152">Chamado quando a transação está sendo descartada enquanto ativa.</span><span class="sxs-lookup"><span data-stu-id="d54be-152">Called when the transaction is being disposed while active.</span></span> <span data-ttu-id="d54be-153">Isso deve reverter a transação.</span><span class="sxs-lookup"><span data-stu-id="d54be-153">This should rollback the transaction.</span></span> <span data-ttu-id="d54be-154">(Substitui <a href="dn350545(v=exchg.10).md">EsentResource. ReleaseResource ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="d54be-154">(Overrides <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="d54be-156"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span><span class="sxs-lookup"><span data-stu-id="d54be-156"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="d54be-157">Chamado por uma subclasse quando um recurso é alocado.</span><span class="sxs-lookup"><span data-stu-id="d54be-157">Called by a subclass when a resource is allocated.</span></span> <span data-ttu-id="d54be-158">(Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="d54be-158">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="d54be-160"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span><span class="sxs-lookup"><span data-stu-id="d54be-160"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="d54be-161">Chamado por uma subclasse quando um recurso é liberado.</span><span class="sxs-lookup"><span data-stu-id="d54be-161">Called by a subclass when a resource is freed.</span></span> <span data-ttu-id="d54be-162">(Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="d54be-162">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="d54be-164"><a href="dn351244(v=exchg.10).md">Reversão</a></span><span class="sxs-lookup"><span data-stu-id="d54be-164"><a href="dn351244(v=exchg.10).md">Rollback</a></span></span></td>
<td><span data-ttu-id="d54be-165">Reverter uma transação.</span><span class="sxs-lookup"><span data-stu-id="d54be-165">Rollback a transaction.</span></span> <span data-ttu-id="d54be-166">Esse objeto deve estar em uma transação.</span><span class="sxs-lookup"><span data-stu-id="d54be-166">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="d54be-168"><a href="dn351181(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="d54be-168"><a href="dn351181(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="d54be-169">Retorna uma <a href="/dotnet/api/system.string">cadeia de caracteres</a> que representa a <a href="dn351174(v=exchg.10).md">transação</a>atual.</span><span class="sxs-lookup"><span data-stu-id="d54be-169">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351174(v=exchg.10).md">Transaction</a>.</span></span> <span data-ttu-id="d54be-170">(Substitui <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="d54be-170">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d54be-171">Parte superior</span><span class="sxs-lookup"><span data-stu-id="d54be-171">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="d54be-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="d54be-172">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d54be-173">Referência</span><span class="sxs-lookup"><span data-stu-id="d54be-173">Reference</span></span>

[<span data-ttu-id="d54be-174">Classe de transação</span><span class="sxs-lookup"><span data-stu-id="d54be-174">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="d54be-175">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d54be-175">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
