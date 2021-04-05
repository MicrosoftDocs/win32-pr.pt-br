---
description: 'Saiba mais sobre: membros do EsentStopwatch'
title: Membros do EsentStopwatch
TOCTitle: EsentStopwatch members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.EsentStopwatch
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstopwatch_members(v=EXCHG.10)
ms:contentKeyID: 55102990
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 36f9d619e104b7d271782c3765adea744beb950e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662651"
---
# <a name="esentstopwatch-members"></a><span data-ttu-id="e61f5-103">Membros do EsentStopwatch</span><span class="sxs-lookup"><span data-stu-id="e61f5-103">EsentStopwatch members</span></span>

<span data-ttu-id="e61f5-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="e61f5-104">Include protected members</span></span>  
<span data-ttu-id="e61f5-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="e61f5-105">Include inherited members</span></span>  

<span data-ttu-id="e61f5-106">Fornece um conjunto de métodos e propriedades que você pode usar para medir as estatísticas de trabalho de ESENT para um thread.</span><span class="sxs-lookup"><span data-stu-id="e61f5-106">Provides a set of methods and properties that you can use to measure ESENT work statistics for a thread.</span></span> <span data-ttu-id="e61f5-107">Se a versão atual do ESENT não oferecer suporte a [JetGetThreadStats (JET_THREADSTATS)](./vistaapi.jetgetthreadstats-method.md) , todas as estatísticas de ESENT serão 0.</span><span class="sxs-lookup"><span data-stu-id="e61f5-107">If the current version of ESENT doesn't support [JetGetThreadStats(JET_THREADSTATS)](./vistaapi.jetgetthreadstats-method.md) then all ESENT statistics will be 0.</span></span>

<span data-ttu-id="e61f5-108">O tipo [EsentStopwatch](./esentstopwatch-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="e61f5-108">The [EsentStopwatch](./esentstopwatch-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="e61f5-109">Construtores</span><span class="sxs-lookup"><span data-stu-id="e61f5-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e61f5-110">Nome</span><span class="sxs-lookup"><span data-stu-id="e61f5-110">Name</span></span></th>
<th><span data-ttu-id="e61f5-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="e61f5-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="e61f5-113"><a href="dn334872(v=exchg.10).md">EsentStopwatch</a></span><span class="sxs-lookup"><span data-stu-id="e61f5-113"><a href="dn334872(v=exchg.10).md">EsentStopwatch</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e61f5-114">Parte superior</span><span class="sxs-lookup"><span data-stu-id="e61f5-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="e61f5-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e61f5-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e61f5-116">Nome</span><span class="sxs-lookup"><span data-stu-id="e61f5-116">Name</span></span></th>
<th><span data-ttu-id="e61f5-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="e61f5-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="e61f5-119"><a href="dn334934(v=exchg.10).md">Decorrido</a></span><span class="sxs-lookup"><span data-stu-id="e61f5-119"><a href="dn334934(v=exchg.10).md">Elapsed</a></span></span></td>
<td><span data-ttu-id="e61f5-120">Obtém o tempo total decorrido, medido pela instância atual.</span><span class="sxs-lookup"><span data-stu-id="e61f5-120">Gets the total elapsed time measured by the current instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="e61f5-122"><a href="dn334933(v=exchg.10).md">Isexecute</a></span><span class="sxs-lookup"><span data-stu-id="e61f5-122"><a href="dn334933(v=exchg.10).md">IsRunning</a></span></span></td>
<td><span data-ttu-id="e61f5-123">Obtém um valor que indica se o temporizador EsentStopwatch está em execução.</span><span class="sxs-lookup"><span data-stu-id="e61f5-123">Gets a value indicating whether the EsentStopwatch timer is running.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="e61f5-125"><a href="dn334930(v=exchg.10).md">ThreadStats</a></span><span class="sxs-lookup"><span data-stu-id="e61f5-125"><a href="dn334930(v=exchg.10).md">ThreadStats</a></span></span></td>
<td><span data-ttu-id="e61f5-126">Obtém o total de estatísticas de trabalho de ESENT medido pela instância atual.</span><span class="sxs-lookup"><span data-stu-id="e61f5-126">Gets the total ESENT work stats measured by the current instance.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e61f5-127">Parte superior</span><span class="sxs-lookup"><span data-stu-id="e61f5-127">Top</span></span>

## <a name="methods"></a><span data-ttu-id="e61f5-128">Métodos</span><span class="sxs-lookup"><span data-stu-id="e61f5-128">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e61f5-129">Nome</span><span class="sxs-lookup"><span data-stu-id="e61f5-129">Name</span></span></th>
<th><span data-ttu-id="e61f5-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="e61f5-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="e61f5-132"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Igual a</a></span><span class="sxs-lookup"><span data-stu-id="e61f5-132"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="e61f5-133">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="e61f5-133">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="e61f5-135"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizar</a></span><span class="sxs-lookup"><span data-stu-id="e61f5-135"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="e61f5-136">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="e61f5-136">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="e61f5-138"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="e61f5-138"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="e61f5-139">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="e61f5-139">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="e61f5-141"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="e61f5-141"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="e61f5-142">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="e61f5-142">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="e61f5-144"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="e61f5-144"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="e61f5-145">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="e61f5-145">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="e61f5-147"><a href="dn334869(v=exchg.10).md">Redefinir</a></span><span class="sxs-lookup"><span data-stu-id="e61f5-147"><a href="dn334869(v=exchg.10).md">Reset</a></span></span></td>
<td><span data-ttu-id="e61f5-148">Interrompe a medição do intervalo de tempo e redefine as estatísticas de thread.</span><span class="sxs-lookup"><span data-stu-id="e61f5-148">Stops time interval measurement and resets the thread statistics.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="e61f5-150"><a href="dn334931(v=exchg.10).md">Iniciar</a></span><span class="sxs-lookup"><span data-stu-id="e61f5-150"><a href="dn334931(v=exchg.10).md">Start</a></span></span></td>
<td><span data-ttu-id="e61f5-151">Começa a medir o trabalho de ESENT.</span><span class="sxs-lookup"><span data-stu-id="e61f5-151">Starts measuring ESENT work.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="e61f5-154"><a href="dn334877(v=exchg.10).md">StartNew</a></span><span class="sxs-lookup"><span data-stu-id="e61f5-154"><a href="dn334877(v=exchg.10).md">StartNew</a></span></span></td>
<td><span data-ttu-id="e61f5-155">Inicializa uma nova instância de EsentStopwatch e começa a medir o tempo decorrido.</span><span class="sxs-lookup"><span data-stu-id="e61f5-155">Initializes a new EsentStopwatch instance and starts measuring elapsed time.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="e61f5-157"><a href="dn334932(v=exchg.10).md">Parar</a></span><span class="sxs-lookup"><span data-stu-id="e61f5-157"><a href="dn334932(v=exchg.10).md">Stop</a></span></span></td>
<td><span data-ttu-id="e61f5-158">Interrompe a medição do trabalho ESENT.</span><span class="sxs-lookup"><span data-stu-id="e61f5-158">Stops measuring ESENT work.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="e61f5-160"><a href="dn334873(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="e61f5-160"><a href="dn334873(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="e61f5-161">Retorna uma <a href="/dotnet/api/system.string">cadeia de caracteres</a> que representa o <a href="/dotnet/api/system.diagnostics.stopwatch">cronômetro</a>atual.</span><span class="sxs-lookup"><span data-stu-id="e61f5-161">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="/dotnet/api/system.diagnostics.stopwatch">Stopwatch</a>.</span></span> <span data-ttu-id="e61f5-162">(Substitui <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="e61f5-162">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e61f5-163">Parte superior</span><span class="sxs-lookup"><span data-stu-id="e61f5-163">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="e61f5-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="e61f5-164">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e61f5-165">Referência</span><span class="sxs-lookup"><span data-stu-id="e61f5-165">Reference</span></span>

[<span data-ttu-id="e61f5-166">Classe EsentStopwatch</span><span class="sxs-lookup"><span data-stu-id="e61f5-166">EsentStopwatch class</span></span>](./esentstopwatch-class.md)

[<span data-ttu-id="e61f5-167">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e61f5-167">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
