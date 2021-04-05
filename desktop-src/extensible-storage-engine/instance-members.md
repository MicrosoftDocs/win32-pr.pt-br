---
description: 'Saiba mais sobre: membros da instância'
title: 'Membros da Instância '
TOCTitle: Instance members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Instance
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance_members(v=EXCHG.10)
ms:contentKeyID: 55103299
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 8ba8dad079feba566dbb8fca873fcea19af778ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827430"
---
# <a name="instance-members"></a><span data-ttu-id="55f26-103">Membros da Instância </span><span class="sxs-lookup"><span data-stu-id="55f26-103">Instance members</span></span>

<span data-ttu-id="55f26-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="55f26-104">Include protected members</span></span>  
<span data-ttu-id="55f26-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="55f26-105">Include inherited members</span></span>  

<span data-ttu-id="55f26-106">Uma classe que encapsula um [JET_INSTANCE](./jet-instance-structure.md) em um objeto descartável.</span><span class="sxs-lookup"><span data-stu-id="55f26-106">A class that encapsulates a [JET_INSTANCE](./jet-instance-structure.md) in a disposable object.</span></span> <span data-ttu-id="55f26-107">A instância deve ser fechada por último e o fechamento da instância libera todos os outros recursos da instância.</span><span class="sxs-lookup"><span data-stu-id="55f26-107">The instance must be closed last and closing the instance releases all other resources for the instance.</span></span>

<span data-ttu-id="55f26-108">O tipo de [instância](./instance-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="55f26-108">The [Instance](./instance-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="55f26-109">Construtores</span><span class="sxs-lookup"><span data-stu-id="55f26-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="55f26-110">Nome</span><span class="sxs-lookup"><span data-stu-id="55f26-110">Name</span></span></th>
<th><span data-ttu-id="55f26-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="55f26-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="55f26-113"><a href="dn350924(v=exchg.10).md">Instância (cadeia de caracteres)</a></span><span class="sxs-lookup"><span data-stu-id="55f26-113"><a href="dn350924(v=exchg.10).md">Instance(String)</a></span></span></td>
<td><span data-ttu-id="55f26-114">Inicializa uma nova instância da classe de instância.</span><span class="sxs-lookup"><span data-stu-id="55f26-114">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="55f26-115">O JET_INSTANCE subjacente é alocado, mas não inicializado.</span><span class="sxs-lookup"><span data-stu-id="55f26-115">The underlying JET_INSTANCE is allocated, but not initialized.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="55f26-117"><a href="dn350927(v=exchg.10).md">Instância (cadeia de caracteres, Cadeia de caracteres)</a></span><span class="sxs-lookup"><span data-stu-id="55f26-117"><a href="dn350927(v=exchg.10).md">Instance(String, String)</a></span></span></td>
<td><span data-ttu-id="55f26-118">Inicializa uma nova instância da classe de instância.</span><span class="sxs-lookup"><span data-stu-id="55f26-118">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="55f26-119">O JET_INSTANCE subjacente é alocado, mas não inicializado.</span><span class="sxs-lookup"><span data-stu-id="55f26-119">The underlying JET_INSTANCE is allocated, but not initialized.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="55f26-121"><a href="dn350948(v=exchg.10).md">Instance (cadeia de caracteres, Cadeia de caracteres, TermGrbit)</a></span><span class="sxs-lookup"><span data-stu-id="55f26-121"><a href="dn350948(v=exchg.10).md">Instance(String, String, TermGrbit)</a></span></span></td>
<td><span data-ttu-id="55f26-122">Inicializa uma nova instância da classe de instância.</span><span class="sxs-lookup"><span data-stu-id="55f26-122">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="55f26-123">O JET_INSTANCE subjacente é alocado, mas não inicializado.</span><span class="sxs-lookup"><span data-stu-id="55f26-123">The underlying JET_INSTANCE is allocated, but not initialized.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="55f26-124">Parte superior</span><span class="sxs-lookup"><span data-stu-id="55f26-124">Top</span></span>

## <a name="properties"></a><span data-ttu-id="55f26-125">Propriedades</span><span class="sxs-lookup"><span data-stu-id="55f26-125">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="55f26-126">Nome</span><span class="sxs-lookup"><span data-stu-id="55f26-126">Name</span></span></th>
<th><span data-ttu-id="55f26-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="55f26-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="55f26-129"><a href="/dotnet/api/system.runtime.interopservices.safehandle.isclosed#System_Runtime_InteropServices_SafeHandle_IsClosed">IsClosed</a></span><span class="sxs-lookup"><span data-stu-id="55f26-129"><a href="/dotnet/api/system.runtime.interopservices.safehandle.isclosed#System_Runtime_InteropServices_SafeHandle_IsClosed">IsClosed</a></span></span></td>
<td><span data-ttu-id="55f26-130">(Herdado de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="55f26-130">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="55f26-132"><a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid.isinvalid#Microsoft_Win32_SafeHandles_SafeHandleZeroOrMinusOneIsInvalid_IsInvalid">Não inválido</a></span><span class="sxs-lookup"><span data-stu-id="55f26-132"><a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid.isinvalid#Microsoft_Win32_SafeHandles_SafeHandleZeroOrMinusOneIsInvalid_IsInvalid">IsInvalid</a></span></span></td>
<td><span data-ttu-id="55f26-133">(Herdado de <a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid">SafeHandleZeroOrMinusOneIsInvalid</a>.)</span><span class="sxs-lookup"><span data-stu-id="55f26-133">(Inherited from <a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid">SafeHandleZeroOrMinusOneIsInvalid</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="55f26-135"><a href="dn350941(v=exchg.10).md">JetInstance</a></span><span class="sxs-lookup"><span data-stu-id="55f26-135"><a href="dn350941(v=exchg.10).md">JetInstance</a></span></span></td>
<td><span data-ttu-id="55f26-136">Obtém o JET_INSTANCE que essa instância contém.</span><span class="sxs-lookup"><span data-stu-id="55f26-136">Gets the JET_INSTANCE that this instance contains.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="55f26-138"><a href="dn350962(v=exchg.10).md">Parâmetros</a></span><span class="sxs-lookup"><span data-stu-id="55f26-138"><a href="dn350962(v=exchg.10).md">Parameters</a></span></span></td>
<td><span data-ttu-id="55f26-139">Obtém Instanceparameters para esta instância.</span><span class="sxs-lookup"><span data-stu-id="55f26-139">Gets the InstanceParameters for this instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="55f26-141"><a href="dn350964(v=exchg.10).md">TermGrbit</a></span><span class="sxs-lookup"><span data-stu-id="55f26-141"><a href="dn350964(v=exchg.10).md">TermGrbit</a></span></span></td>
<td><span data-ttu-id="55f26-142">Obtém ou define o TermGrbit para esta instância.</span><span class="sxs-lookup"><span data-stu-id="55f26-142">Gets or sets the TermGrbit for this instance.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="55f26-143">Parte superior</span><span class="sxs-lookup"><span data-stu-id="55f26-143">Top</span></span>

## <a name="methods"></a><span data-ttu-id="55f26-144">Métodos</span><span class="sxs-lookup"><span data-stu-id="55f26-144">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="55f26-145">Nome</span><span class="sxs-lookup"><span data-stu-id="55f26-145">Name</span></span></th>
<th><span data-ttu-id="55f26-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="55f26-146">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="55f26-148"><a href="/dotnet/api/system.runtime.interopservices.safehandle.close#System_Runtime_InteropServices_SafeHandle_Close">Close</a></span><span class="sxs-lookup"><span data-stu-id="55f26-148"><a href="/dotnet/api/system.runtime.interopservices.safehandle.close#System_Runtime_InteropServices_SafeHandle_Close">Close</a></span></span></td>
<td><span data-ttu-id="55f26-149">(Herdado de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="55f26-149">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="55f26-151"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousaddref#System_Runtime_InteropServices_SafeHandle_DangerousAddRef_System_Boolean__">DangerousAddRef</a></span><span class="sxs-lookup"><span data-stu-id="55f26-151"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousaddref#System_Runtime_InteropServices_SafeHandle_DangerousAddRef_System_Boolean__">DangerousAddRef</a></span></span></td>
<td><span data-ttu-id="55f26-152">(Herdado de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="55f26-152">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="55f26-154"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousgethandle#System_Runtime_InteropServices_SafeHandle_DangerousGetHandle">DangerousGetHandle</a></span><span class="sxs-lookup"><span data-stu-id="55f26-154"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousgethandle#System_Runtime_InteropServices_SafeHandle_DangerousGetHandle">DangerousGetHandle</a></span></span></td>
<td><span data-ttu-id="55f26-155">(Herdado de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="55f26-155">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="55f26-157"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousrelease#System_Runtime_InteropServices_SafeHandle_DangerousRelease">DangerousRelease</a></span><span class="sxs-lookup"><span data-stu-id="55f26-157"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousrelease#System_Runtime_InteropServices_SafeHandle_DangerousRelease">DangerousRelease</a></span></span></td>
<td><span data-ttu-id="55f26-158">(Herdado de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="55f26-158">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="55f26-160"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose">Dispose ()</a></span><span class="sxs-lookup"><span data-stu-id="55f26-160"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose">Dispose()</a></span></span></td>
<td><span data-ttu-id="55f26-161">(Herdado de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="55f26-161">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="55f26-163"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose_System_Boolean_">Dispose (booliano)</a></span><span class="sxs-lookup"><span data-stu-id="55f26-163"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose_System_Boolean_">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="55f26-164">(Herdado de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="55f26-164">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="55f26-166"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Igual a</a></span><span class="sxs-lookup"><span data-stu-id="55f26-166"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="55f26-167">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="55f26-167">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="55f26-169"><a href="/dotnet/api/system.runtime.interopservices.safehandle.finalize#System_Runtime_InteropServices_SafeHandle_Finalize">Finalizar</a></span><span class="sxs-lookup"><span data-stu-id="55f26-169"><a href="/dotnet/api/system.runtime.interopservices.safehandle.finalize#System_Runtime_InteropServices_SafeHandle_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="55f26-170">(Herdado de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="55f26-170">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="55f26-172"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="55f26-172"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="55f26-173">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="55f26-173">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="55f26-175"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="55f26-175"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="55f26-176">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="55f26-176">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="55f26-178"><a href="dn350932(v=exchg.10).md">Init ()</a></span><span class="sxs-lookup"><span data-stu-id="55f26-178"><a href="dn350932(v=exchg.10).md">Init()</a></span></span></td>
<td><span data-ttu-id="55f26-179">Inicialize o JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="55f26-179">Initialize the JET_INSTANCE.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="55f26-181"><a href="dn350954(v=exchg.10).md">Init (InitGrbit)</a></span><span class="sxs-lookup"><span data-stu-id="55f26-181"><a href="dn350954(v=exchg.10).md">Init(InitGrbit)</a></span></span></td>
<td><span data-ttu-id="55f26-182">Inicialize o JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="55f26-182">Initialize the JET_INSTANCE.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="55f26-184"><a href="dn350934(v=exchg.10).md">Init (JET_RSTINFO, InitGrbit)</a></span><span class="sxs-lookup"><span data-stu-id="55f26-184"><a href="dn350934(v=exchg.10).md">Init(JET_RSTINFO, InitGrbit)</a></span></span></td>
<td><span data-ttu-id="55f26-185">Inicialize o JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="55f26-185">Initialize the JET_INSTANCE.</span></span> <span data-ttu-id="55f26-186">Essa API requer pelo menos a versão vista do ESENT.</span><span class="sxs-lookup"><span data-stu-id="55f26-186">This API requires at least the Vista version of ESENT.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="55f26-188"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="55f26-188"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="55f26-189">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="55f26-189">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="55f26-191"><a href="dn350956(v=exchg.10).md">ReleaseHandle</a></span><span class="sxs-lookup"><span data-stu-id="55f26-191"><a href="dn350956(v=exchg.10).md">ReleaseHandle</a></span></span></td>
<td><span data-ttu-id="55f26-192">Libere o identificador para esta instância.</span><span class="sxs-lookup"><span data-stu-id="55f26-192">Release the handle for this instance.</span></span> <span data-ttu-id="55f26-193">(Substitui <a href="/dotnet/api/system.runtime.interopservices.safehandle.releasehandle#System_Runtime_InteropServices_SafeHandle_ReleaseHandle">SafeHandle. ReleaseHandle ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="55f26-193">(Overrides <a href="/dotnet/api/system.runtime.interopservices.safehandle.releasehandle#System_Runtime_InteropServices_SafeHandle_ReleaseHandle">SafeHandle.ReleaseHandle()</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="55f26-195"><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandle#System_Runtime_InteropServices_SafeHandle_SetHandle_System_IntPtr_">SetHandle</a></span><span class="sxs-lookup"><span data-stu-id="55f26-195"><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandle#System_Runtime_InteropServices_SafeHandle_SetHandle_System_IntPtr_">SetHandle</a></span></span></td>
<td><span data-ttu-id="55f26-196">(Herdado de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="55f26-196">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="55f26-198"><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandleasinvalid#System_Runtime_InteropServices_SafeHandle_SetHandleAsInvalid">SetHandleAsInvalid</a></span><span class="sxs-lookup"><span data-stu-id="55f26-198"><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandleasinvalid#System_Runtime_InteropServices_SafeHandle_SetHandleAsInvalid">SetHandleAsInvalid</a></span></span></td>
<td><span data-ttu-id="55f26-199">(Herdado de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="55f26-199">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="55f26-201"><a href="dn350935(v=exchg.10).md">Termo</a></span><span class="sxs-lookup"><span data-stu-id="55f26-201"><a href="dn350935(v=exchg.10).md">Term</a></span></span></td>
<td><span data-ttu-id="55f26-202">Encerre o JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="55f26-202">Terminate the JET_INSTANCE.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="55f26-204"><a href="dn350960(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="55f26-204"><a href="dn350960(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="55f26-205">Retorna uma <a href="/dotnet/api/system.string">cadeia de caracteres</a> que representa a <a href="dn350923(v=exchg.10).md">instância</a>atual.</span><span class="sxs-lookup"><span data-stu-id="55f26-205">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn350923(v=exchg.10).md">Instance</a>.</span></span> <span data-ttu-id="55f26-206">(Substitui <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="55f26-206">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="55f26-207">Parte superior</span><span class="sxs-lookup"><span data-stu-id="55f26-207">Top</span></span>

## <a name="operators"></a><span data-ttu-id="55f26-208">Operadores</span><span class="sxs-lookup"><span data-stu-id="55f26-208">Operators</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="55f26-209">Nome</span><span class="sxs-lookup"><span data-stu-id="55f26-209">Name</span></span></th>
<th><span data-ttu-id="55f26-210">Descrição</span><span class="sxs-lookup"><span data-stu-id="55f26-210">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operador público" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="55f26-213"><a href="dn350950(v=exchg.10).md">Implícito (instância para JET_INSTANCE)</a></span><span class="sxs-lookup"><span data-stu-id="55f26-213"><a href="dn350950(v=exchg.10).md">Implicit(Instance to JET_INSTANCE)</a></span></span></td>
<td><span data-ttu-id="55f26-214">Forneça conversão implícita de um objeto de instância para uma estrutura de JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="55f26-214">Provide implicit conversion of an Instance object to a JET_INSTANCE structure.</span></span> <span data-ttu-id="55f26-215">Isso é feito para que uma instância possa ser usada em qualquer lugar em que um JET_INSTANCE é necessário.</span><span class="sxs-lookup"><span data-stu-id="55f26-215">This is done so that an Instance can be used anywhere a JET_INSTANCE is required.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="55f26-216">Parte superior</span><span class="sxs-lookup"><span data-stu-id="55f26-216">Top</span></span>

## <a name="fields"></a><span data-ttu-id="55f26-217">Campos</span><span class="sxs-lookup"><span data-stu-id="55f26-217">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="55f26-218">Nome</span><span class="sxs-lookup"><span data-stu-id="55f26-218">Name</span></span></th>
<th><span data-ttu-id="55f26-219">Descrição</span><span class="sxs-lookup"><span data-stu-id="55f26-219">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.protfield(exchg.10).gif" title="Campo protegido" alt="Protected field" /></td>
<td><span data-ttu-id="55f26-221"><a href="/dotnet/api/system.runtime.interopservices.safehandle.handle">processamento</a></span><span class="sxs-lookup"><span data-stu-id="55f26-221"><a href="/dotnet/api/system.runtime.interopservices.safehandle.handle">handle</a></span></span></td>
<td><span data-ttu-id="55f26-222">(Herdado de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="55f26-222">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="55f26-223">Parte superior</span><span class="sxs-lookup"><span data-stu-id="55f26-223">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="55f26-224">Confira também</span><span class="sxs-lookup"><span data-stu-id="55f26-224">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="55f26-225">Referência</span><span class="sxs-lookup"><span data-stu-id="55f26-225">Reference</span></span>

[<span data-ttu-id="55f26-226">Classe de instância</span><span class="sxs-lookup"><span data-stu-id="55f26-226">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="55f26-227">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="55f26-227">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
