---
description: 'Saiba mais sobre: membros do ColumnStream'
title: 'Membros ColumnStream '
TOCTitle: ColumnStream members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.ColumnStream
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream_members(v=EXCHG.10)
ms:contentKeyID: 55101147
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 9f35c0e000329bc98e2f9fd5873cd724516271d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104565197"
---
# <a name="columnstream-members"></a><span data-ttu-id="5f02f-103">Membros ColumnStream </span><span class="sxs-lookup"><span data-stu-id="5f02f-103">ColumnStream members</span></span>

<span data-ttu-id="5f02f-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="5f02f-104">Include protected members</span></span>  
<span data-ttu-id="5f02f-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="5f02f-105">Include inherited members</span></span>  

<span data-ttu-id="5f02f-106">Essa classe fornece uma interface de streaming para uma coluna de valor longo (ou seja, uma coluna do tipo [LongBinary](./jet-coltyp-enumeration.md) ou [LONGTEXT](./jet-coltyp-enumeration.md)).</span><span class="sxs-lookup"><span data-stu-id="5f02f-106">This class provides a streaming interface to a long-value column (i.e. a column of type [LongBinary](./jet-coltyp-enumeration.md) or [LongText](./jet-coltyp-enumeration.md)).</span></span>

<span data-ttu-id="5f02f-107">O tipo [ColumnStream](./columnstream-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="5f02f-107">The [ColumnStream](./columnstream-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="5f02f-108">Construtores</span><span class="sxs-lookup"><span data-stu-id="5f02f-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="5f02f-109">Nome</span><span class="sxs-lookup"><span data-stu-id="5f02f-109">Name</span></span></th>
<th><span data-ttu-id="5f02f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f02f-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5f02f-112"><a href="dn334142(v=exchg.10).md">ColumnStream</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-112"><a href="dn334142(v=exchg.10).md">ColumnStream</a></span></span></td>
<td><span data-ttu-id="5f02f-113">Inicializa uma nova instância da classe ColumnStream.</span><span class="sxs-lookup"><span data-stu-id="5f02f-113">Initializes a new instance of the ColumnStream class.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5f02f-114">Parte superior</span><span class="sxs-lookup"><span data-stu-id="5f02f-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="5f02f-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5f02f-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="5f02f-116">Nome</span><span class="sxs-lookup"><span data-stu-id="5f02f-116">Name</span></span></th>
<th><span data-ttu-id="5f02f-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f02f-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="5f02f-119"><a href="dn334201(v=exchg.10).md">CanRead</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-119"><a href="dn334201(v=exchg.10).md">CanRead</a></span></span></td>
<td><span data-ttu-id="5f02f-120">Obtém um valor que indica se o fluxo dá suporte à leitura.</span><span class="sxs-lookup"><span data-stu-id="5f02f-120">Gets a value indicating whether the stream supports reading.</span></span> <span data-ttu-id="5f02f-121">(Substitui <a href="/dotnet/api/system.io.stream.canread#System_IO_Stream_CanRead">Stream. CanRead</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-121">(Overrides <a href="/dotnet/api/system.io.stream.canread#System_IO_Stream_CanRead">Stream.CanRead</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="5f02f-123"><a href="dn334153(v=exchg.10).md">CanSeek</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-123"><a href="dn334153(v=exchg.10).md">CanSeek</a></span></span></td>
<td><span data-ttu-id="5f02f-124">Obtém um valor que indica se o fluxo dá suporte à busca.</span><span class="sxs-lookup"><span data-stu-id="5f02f-124">Gets a value indicating whether the stream supports seeking.</span></span> <span data-ttu-id="5f02f-125">(Substitui <a href="/dotnet/api/system.io.stream.canseek#System_IO_Stream_CanSeek">Stream. CanSeek</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-125">(Overrides <a href="/dotnet/api/system.io.stream.canseek#System_IO_Stream_CanSeek">Stream.CanSeek</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="5f02f-127"><a href="/dotnet/api/system.io.stream.cantimeout#System_IO_Stream_CanTimeout">CanTimeout</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-127"><a href="/dotnet/api/system.io.stream.cantimeout#System_IO_Stream_CanTimeout">CanTimeout</a></span></span></td>
<td><span data-ttu-id="5f02f-128">(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-128">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="5f02f-130"><a href="dn334204(v=exchg.10).md">CanWrite</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-130"><a href="dn334204(v=exchg.10).md">CanWrite</a></span></span></td>
<td><span data-ttu-id="5f02f-131">Obtém um valor que indica se o fluxo dá suporte à gravação.</span><span class="sxs-lookup"><span data-stu-id="5f02f-131">Gets a value indicating whether the stream supports writing.</span></span> <span data-ttu-id="5f02f-132">(Substitui <a href="/dotnet/api/system.io.stream.canwrite#System_IO_Stream_CanWrite">Stream. CanWrite</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-132">(Overrides <a href="/dotnet/api/system.io.stream.canwrite#System_IO_Stream_CanWrite">Stream.CanWrite</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="5f02f-134"><a href="dn334159(v=exchg.10).md">Itag</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-134"><a href="dn334159(v=exchg.10).md">Itag</a></span></span></td>
<td><span data-ttu-id="5f02f-135">Obtém ou define o iTag da coluna.</span><span class="sxs-lookup"><span data-stu-id="5f02f-135">Gets or sets the itag of the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="5f02f-137"><a href="dn334205(v=exchg.10).md">Comprimento</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-137"><a href="dn334205(v=exchg.10).md">Length</a></span></span></td>
<td><span data-ttu-id="5f02f-138">Obtém o comprimento atual do fluxo.</span><span class="sxs-lookup"><span data-stu-id="5f02f-138">Gets the current length of the stream.</span></span> <span data-ttu-id="5f02f-139">(Substitui <a href="/dotnet/api/system.io.stream.length#System_IO_Stream_Length">Stream. Length</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-139">(Overrides <a href="/dotnet/api/system.io.stream.length#System_IO_Stream_Length">Stream.Length</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="5f02f-141"><a href="dn334161(v=exchg.10).md">Posição</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-141"><a href="dn334161(v=exchg.10).md">Position</a></span></span></td>
<td><span data-ttu-id="5f02f-142">Obtém ou define a posição atual no fluxo.</span><span class="sxs-lookup"><span data-stu-id="5f02f-142">Gets or sets the current position in the stream.</span></span> <span data-ttu-id="5f02f-143">(Substitui <a href="/dotnet/api/system.io.stream.position#System_IO_Stream_Position">Stream. Position</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-143">(Overrides <a href="/dotnet/api/system.io.stream.position#System_IO_Stream_Position">Stream.Position</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="5f02f-145"><a href="/dotnet/api/system.io.stream.readtimeout#System_IO_Stream_ReadTimeout">ReadTimeout</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-145"><a href="/dotnet/api/system.io.stream.readtimeout#System_IO_Stream_ReadTimeout">ReadTimeout</a></span></span></td>
<td><span data-ttu-id="5f02f-146">(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-146">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="5f02f-148"><a href="/dotnet/api/system.io.stream.writetimeout#System_IO_Stream_WriteTimeout">WriteTimeout</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-148"><a href="/dotnet/api/system.io.stream.writetimeout#System_IO_Stream_WriteTimeout">WriteTimeout</a></span></span></td>
<td><span data-ttu-id="5f02f-149">(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-149">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5f02f-150">Parte superior</span><span class="sxs-lookup"><span data-stu-id="5f02f-150">Top</span></span>

## <a name="methods"></a><span data-ttu-id="5f02f-151">Métodos</span><span class="sxs-lookup"><span data-stu-id="5f02f-151">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="5f02f-152">Nome</span><span class="sxs-lookup"><span data-stu-id="5f02f-152">Name</span></span></th>
<th><span data-ttu-id="5f02f-153">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f02f-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5f02f-155"><a href="/dotnet/api/system.io.stream.beginread#System_IO_Stream_BeginRead_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginRead</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-155"><a href="/dotnet/api/system.io.stream.beginread#System_IO_Stream_BeginRead_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginRead</a></span></span></td>
<td><span data-ttu-id="5f02f-156">(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-156">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5f02f-158"><a href="/dotnet/api/system.io.stream.beginwrite#System_IO_Stream_BeginWrite_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginWrite</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-158"><a href="/dotnet/api/system.io.stream.beginwrite#System_IO_Stream_BeginWrite_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginWrite</a></span></span></td>
<td><span data-ttu-id="5f02f-159">(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-159">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5f02f-161"><a href="/dotnet/api/system.io.stream.close#System_IO_Stream_Close">Close</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-161"><a href="/dotnet/api/system.io.stream.close#System_IO_Stream_Close">Close</a></span></span></td>
<td><span data-ttu-id="5f02f-162">(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-162">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5f02f-164"><a href="/dotnet/api/system.marshalbyrefobject.createobjref#System_MarshalByRefObject_CreateObjRef_System_Type_">CreateObjRef</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-164"><a href="/dotnet/api/system.marshalbyrefobject.createobjref#System_MarshalByRefObject_CreateObjRef_System_Type_">CreateObjRef</a></span></span></td>
<td><span data-ttu-id="5f02f-165">(Herdado de <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-165">(Inherited from <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="5f02f-167"><a href="/dotnet/api/system.io.stream.createwaithandle#System_IO_Stream_CreateWaitHandle">CreateWaitHandle</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-167"><a href="/dotnet/api/system.io.stream.createwaithandle#System_IO_Stream_CreateWaitHandle">CreateWaitHandle</a></span></span></td>
<td><span data-ttu-id="5f02f-168"><strong>Obsoleto.</strong></span><span class="sxs-lookup"><span data-stu-id="5f02f-168"><strong>Obsolete.</strong></span></span> <span data-ttu-id="5f02f-169">(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-169">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5f02f-171"><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose">Dispose ()</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-171"><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose">Dispose()</a></span></span></td>
<td><span data-ttu-id="5f02f-172">(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-172">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="5f02f-174"><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose_System_Boolean_">Dispose (booliano)</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-174"><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose_System_Boolean_">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="5f02f-175">(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-175">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5f02f-177"><a href="/dotnet/api/system.io.stream.endread#System_IO_Stream_EndRead_System_IAsyncResult_">EndRead</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-177"><a href="/dotnet/api/system.io.stream.endread#System_IO_Stream_EndRead_System_IAsyncResult_">EndRead</a></span></span></td>
<td><span data-ttu-id="5f02f-178">(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-178">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5f02f-180"><a href="/dotnet/api/system.io.stream.endwrite#System_IO_Stream_EndWrite_System_IAsyncResult_">EndWrite</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-180"><a href="/dotnet/api/system.io.stream.endwrite#System_IO_Stream_EndWrite_System_IAsyncResult_">EndWrite</a></span></span></td>
<td><span data-ttu-id="5f02f-181">(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-181">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5f02f-183"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Igual a</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-183"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="5f02f-184">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-184">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="5f02f-186"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizar</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-186"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="5f02f-187">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-187">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5f02f-189"><a href="dn334193(v=exchg.10).md">Liberar</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-189"><a href="dn334193(v=exchg.10).md">Flush</a></span></span></td>
<td><span data-ttu-id="5f02f-190">Libere o fluxo.</span><span class="sxs-lookup"><span data-stu-id="5f02f-190">Flush the stream.</span></span> <span data-ttu-id="5f02f-191">(Substitui <a href="/dotnet/api/system.io.stream.flush#System_IO_Stream_Flush">Stream. Flush ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-191">(Overrides <a href="/dotnet/api/system.io.stream.flush#System_IO_Stream_Flush">Stream.Flush()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5f02f-193"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-193"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="5f02f-194">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-194">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5f02f-196"><a href="/dotnet/api/system.marshalbyrefobject.getlifetimeservice#System_MarshalByRefObject_GetLifetimeService">GetLifetimeService</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-196"><a href="/dotnet/api/system.marshalbyrefobject.getlifetimeservice#System_MarshalByRefObject_GetLifetimeService">GetLifetimeService</a></span></span></td>
<td><span data-ttu-id="5f02f-197">(Herdado de <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-197">(Inherited from <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5f02f-199"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-199"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="5f02f-200">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-200">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5f02f-202"><a href="/dotnet/api/system.marshalbyrefobject.initializelifetimeservice#System_MarshalByRefObject_InitializeLifetimeService">InitializeLifetimeService</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-202"><a href="/dotnet/api/system.marshalbyrefobject.initializelifetimeservice#System_MarshalByRefObject_InitializeLifetimeService">InitializeLifetimeService</a></span></span></td>
<td><span data-ttu-id="5f02f-203">(Herdado de <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-203">(Inherited from <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="5f02f-205"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone()</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-205"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone()</a></span></span></td>
<td><span data-ttu-id="5f02f-206">(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-206">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="5f02f-208"><a href="/dotnet/api/system.marshalbyrefobject.memberwiseclone#System_MarshalByRefObject_MemberwiseClone_System_Boolean_">MemberwiseClone (booliano)</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-208"><a href="/dotnet/api/system.marshalbyrefobject.memberwiseclone#System_MarshalByRefObject_MemberwiseClone_System_Boolean_">MemberwiseClone(Boolean)</a></span></span></td>
<td><span data-ttu-id="5f02f-209">(Herdado de <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-209">(Inherited from <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5f02f-211"><a href="dn334198(v=exchg.10).md">Ler</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-211"><a href="dn334198(v=exchg.10).md">Read</a></span></span></td>
<td><span data-ttu-id="5f02f-212">Lê uma sequência de bytes do fluxo atual e avança a posição no fluxo até o número de bytes lidos.</span><span class="sxs-lookup"><span data-stu-id="5f02f-212">Reads a sequence of bytes from the current stream and advances the position within the stream by the number of bytes read.</span></span> <span data-ttu-id="5f02f-213">(Substitui <a href="/dotnet/api/system.io.stream.read#System_IO_Stream_Read_System_Byte___System_Int32_System_Int32_">Stream. Read ([], Int32, Int32)</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-213">(Overrides <a href="/dotnet/api/system.io.stream.read#System_IO_Stream_Read_System_Byte___System_Int32_System_Int32_">Stream.Read([], Int32, Int32)</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5f02f-215"><a href="/dotnet/api/system.io.stream.readbyte#System_IO_Stream_ReadByte">ReadByte</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-215"><a href="/dotnet/api/system.io.stream.readbyte#System_IO_Stream_ReadByte">ReadByte</a></span></span></td>
<td><span data-ttu-id="5f02f-216">(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-216">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5f02f-218"><a href="dn334154(v=exchg.10).md">Seek</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-218"><a href="dn334154(v=exchg.10).md">Seek</a></span></span></td>
<td><span data-ttu-id="5f02f-219">Define a posição no fluxo atual.</span><span class="sxs-lookup"><span data-stu-id="5f02f-219">Sets the position in the current stream.</span></span> <span data-ttu-id="5f02f-220">(Substitui <a href="/dotnet/api/system.io.stream.seek#System_IO_Stream_Seek_System_Int64_System_IO_SeekOrigin_">Stream. Seek (Int64, SeekOrigin)</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-220">(Overrides <a href="/dotnet/api/system.io.stream.seek#System_IO_Stream_Seek_System_Int64_System_IO_SeekOrigin_">Stream.Seek(Int64, SeekOrigin)</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5f02f-222"><a href="dn334196(v=exchg.10).md">SetLength</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-222"><a href="dn334196(v=exchg.10).md">SetLength</a></span></span></td>
<td><span data-ttu-id="5f02f-223">Define o comprimento do fluxo.</span><span class="sxs-lookup"><span data-stu-id="5f02f-223">Sets the length of the stream.</span></span> <span data-ttu-id="5f02f-224">(Substitui <a href="/dotnet/api/system.io.stream.setlength#System_IO_Stream_SetLength_System_Int64_">Stream. SetLength (Int64)</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-224">(Overrides <a href="/dotnet/api/system.io.stream.setlength#System_IO_Stream_SetLength_System_Int64_">Stream.SetLength(Int64)</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5f02f-226"><a href="dn334149(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-226"><a href="dn334149(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="5f02f-227">Retorna uma <a href="/dotnet/api/system.string">cadeia de caracteres</a> que representa o <a href="dn334143(v=exchg.10).md">ColumnStream</a>atual.</span><span class="sxs-lookup"><span data-stu-id="5f02f-227">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn334143(v=exchg.10).md">ColumnStream</a>.</span></span> <span data-ttu-id="5f02f-228">(Substitui <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-228">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5f02f-230"><a href="dn334197(v=exchg.10).md">Gravar</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-230"><a href="dn334197(v=exchg.10).md">Write</a></span></span></td>
<td><span data-ttu-id="5f02f-231">Grava uma sequência de bytes no fluxo atual e avança a posição atual dentro desse fluxo pelo número de bytes gravados.</span><span class="sxs-lookup"><span data-stu-id="5f02f-231">Writes a sequence of bytes to the current stream and advances the current position within this stream by the number of bytes written.</span></span> <span data-ttu-id="5f02f-232">(Substitui <a href="/dotnet/api/system.io.stream.write#System_IO_Stream_Write_System_Byte___System_Int32_System_Int32_">Stream. Write ([], Int32, Int32)</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-232">(Overrides <a href="/dotnet/api/system.io.stream.write#System_IO_Stream_Write_System_Byte___System_Int32_System_Int32_">Stream.Write([], Int32, Int32)</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="5f02f-234"><a href="/dotnet/api/system.io.stream.writebyte#System_IO_Stream_WriteByte_System_Byte_">WriteByte</a></span><span class="sxs-lookup"><span data-stu-id="5f02f-234"><a href="/dotnet/api/system.io.stream.writebyte#System_IO_Stream_WriteByte_System_Byte_">WriteByte</a></span></span></td>
<td><span data-ttu-id="5f02f-235">(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</span><span class="sxs-lookup"><span data-stu-id="5f02f-235">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5f02f-236">Parte superior</span><span class="sxs-lookup"><span data-stu-id="5f02f-236">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="5f02f-237">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f02f-237">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5f02f-238">Referência</span><span class="sxs-lookup"><span data-stu-id="5f02f-238">Reference</span></span>

[<span data-ttu-id="5f02f-239">Classe ColumnStream</span><span class="sxs-lookup"><span data-stu-id="5f02f-239">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="5f02f-240">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5f02f-240">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
