---
description: 'Saiba mais sobre: membros do JET_INSTANCE_INFO'
title: Membros do JET_INSTANCE_INFO
TOCTitle: JET_INSTANCE_INFO members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info_members(v=EXCHG.10)
ms:contentKeyID: 55103693
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 42d9bcd2c078766875fc8230eaf83dc07fdb4b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104553528"
---
# <a name="jet_instance_info-members"></a><span data-ttu-id="a5e4c-103">Membros do JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="a5e4c-103">JET_INSTANCE_INFO members</span></span>

<span data-ttu-id="a5e4c-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="a5e4c-104">Include protected members</span></span>  
<span data-ttu-id="a5e4c-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="a5e4c-105">Include inherited members</span></span>  

<span data-ttu-id="a5e4c-106">Recebe informações sobre a execução de instâncias de banco de dados quando usadas com as funções JetGetInstanceInfo e JetOSSnapshotFreeze.</span><span class="sxs-lookup"><span data-stu-id="a5e4c-106">Receives information about running database instances when used with the JetGetInstanceInfo and JetOSSnapshotFreeze functions.</span></span>

<span data-ttu-id="a5e4c-107">O tipo de [JET_INSTANCE_INFO](./jet-instance-info-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5e4c-107">The [JET_INSTANCE_INFO](./jet-instance-info-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="a5e4c-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a5e4c-108">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a5e4c-109">Nome</span><span class="sxs-lookup"><span data-stu-id="a5e4c-109">Name</span></span></th>
<th><span data-ttu-id="a5e4c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="a5e4c-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="a5e4c-112"><a href="dn335189(v=exchg.10).md">cDatabases</a></span><span class="sxs-lookup"><span data-stu-id="a5e4c-112"><a href="dn335189(v=exchg.10).md">cDatabases</a></span></span></td>
<td><span data-ttu-id="a5e4c-113">Obtém o número de bancos de dados que estão anexados à instância de Database.</span><span class="sxs-lookup"><span data-stu-id="a5e4c-113">Gets the number of databases that are attached to the database instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="a5e4c-115"><a href="dn335190(v=exchg.10).md">hInstanceId</a></span><span class="sxs-lookup"><span data-stu-id="a5e4c-115"><a href="dn335190(v=exchg.10).md">hInstanceId</a></span></span></td>
<td><span data-ttu-id="a5e4c-116">Obtém a JET_INSTANCE da instância fornecida.</span><span class="sxs-lookup"><span data-stu-id="a5e4c-116">Gets the JET_INSTANCE of the given instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="a5e4c-118"><a href="dn335193(v=exchg.10).md">szDatabaseFileName</a></span><span class="sxs-lookup"><span data-stu-id="a5e4c-118"><a href="dn335193(v=exchg.10).md">szDatabaseFileName</a></span></span></td>
<td><span data-ttu-id="a5e4c-119">Obtém uma coleção de cadeias de caracteres, cada uma mantendo o nome de arquivo de um banco de dados anexado à instância do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a5e4c-119">Gets a collection of strings, each holding the file name of a database that is attached to the database instance.</span></span> <span data-ttu-id="a5e4c-120">A matriz tem elementos cDatabases.</span><span class="sxs-lookup"><span data-stu-id="a5e4c-120">The array has cDatabases elements.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="a5e4c-122"><a href="dn335194(v=exchg.10).md">szInstanceName</a></span><span class="sxs-lookup"><span data-stu-id="a5e4c-122"><a href="dn335194(v=exchg.10).md">szInstanceName</a></span></span></td>
<td><span data-ttu-id="a5e4c-123">Obtém o nome da instância do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a5e4c-123">Gets the name of the database instance.</span></span> <span data-ttu-id="a5e4c-124">Esse valor pode ser nulo se a instância não tiver um nome.</span><span class="sxs-lookup"><span data-stu-id="a5e4c-124">This value can be null if the instance does not have a name.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a5e4c-125">Parte superior</span><span class="sxs-lookup"><span data-stu-id="a5e4c-125">Top</span></span>

## <a name="methods"></a><span data-ttu-id="a5e4c-126">Métodos</span><span class="sxs-lookup"><span data-stu-id="a5e4c-126">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a5e4c-127">Nome</span><span class="sxs-lookup"><span data-stu-id="a5e4c-127">Name</span></span></th>
<th><span data-ttu-id="a5e4c-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="a5e4c-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="a5e4c-130"><a href="dn335184(v=exchg.10).md">Equals (Object)</a></span><span class="sxs-lookup"><span data-stu-id="a5e4c-130"><a href="dn335184(v=exchg.10).md">Equals(Object)</a></span></span></td>
<td><span data-ttu-id="a5e4c-131">Retorna um valor que indica se essa instância é igual a outra instância.</span><span class="sxs-lookup"><span data-stu-id="a5e4c-131">Returns a value indicating whether this instance is equal to another instance.</span></span> <span data-ttu-id="a5e4c-132">(Substitui <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Object. Equals (Object)</a>.)</span><span class="sxs-lookup"><span data-stu-id="a5e4c-132">(Overrides <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Object.Equals(Object)</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="a5e4c-134"><a href="dn335187(v=exchg.10).md">Equals (JET_INSTANCE_INFO)</a></span><span class="sxs-lookup"><span data-stu-id="a5e4c-134"><a href="dn335187(v=exchg.10).md">Equals(JET_INSTANCE_INFO)</a></span></span></td>
<td><span data-ttu-id="a5e4c-135">Retorna um valor que indica se essa instância é igual a outra instância.</span><span class="sxs-lookup"><span data-stu-id="a5e4c-135">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="a5e4c-137"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizar</a></span><span class="sxs-lookup"><span data-stu-id="a5e4c-137"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="a5e4c-138">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="a5e4c-138">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="a5e4c-140"><a href="dn335191(v=exchg.10).md">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="a5e4c-140"><a href="dn335191(v=exchg.10).md">GetHashCode</a></span></span></td>
<td><span data-ttu-id="a5e4c-141">Retorna o código hash para a instância.</span><span class="sxs-lookup"><span data-stu-id="a5e4c-141">Returns the hash code for this instance.</span></span> <span data-ttu-id="a5e4c-142">(Substitui <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">Object. GetHashCode ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="a5e4c-142">(Overrides <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">Object.GetHashCode()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="a5e4c-144"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="a5e4c-144"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="a5e4c-145">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="a5e4c-145">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="a5e4c-147"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="a5e4c-147"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="a5e4c-148">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="a5e4c-148">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="a5e4c-150"><a href="dn335192(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="a5e4c-150"><a href="dn335192(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="a5e4c-151">Gere uma representação de cadeia de caracteres da instância.</span><span class="sxs-lookup"><span data-stu-id="a5e4c-151">Generate a string representation of the instance.</span></span> <span data-ttu-id="a5e4c-152">(Substitui <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="a5e4c-152">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a5e4c-153">Parte superior</span><span class="sxs-lookup"><span data-stu-id="a5e4c-153">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="a5e4c-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5e4c-154">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a5e4c-155">Referência</span><span class="sxs-lookup"><span data-stu-id="a5e4c-155">Reference</span></span>

[<span data-ttu-id="a5e4c-156">Classe JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="a5e4c-156">JET_INSTANCE_INFO class</span></span>](./jet-instance-info-class.md)

[<span data-ttu-id="a5e4c-157">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a5e4c-157">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
