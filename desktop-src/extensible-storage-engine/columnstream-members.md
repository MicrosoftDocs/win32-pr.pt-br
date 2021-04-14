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
# <a name="columnstream-members"></a>Membros ColumnStream 

Incluir membros protegidos  
Incluir membros herdados  

Essa classe fornece uma interface de streaming para uma coluna de valor longo (ou seja, uma coluna do tipo [LongBinary](./jet-coltyp-enumeration.md) ou [LONGTEXT](./jet-coltyp-enumeration.md)).

O tipo [ColumnStream](./columnstream-class.md) expõe os membros a seguir.

## <a name="constructors"></a>Construtores

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nome</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn334142(v=exchg.10).md">ColumnStream</a></td>
<td>Inicializa uma nova instância da classe ColumnStream.</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="properties"></a>Propriedades

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nome</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334201(v=exchg.10).md">CanRead</a></td>
<td>Obtém um valor que indica se o fluxo dá suporte à leitura. (Substitui <a href="/dotnet/api/system.io.stream.canread#System_IO_Stream_CanRead">Stream. CanRead</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334153(v=exchg.10).md">CanSeek</a></td>
<td>Obtém um valor que indica se o fluxo dá suporte à busca. (Substitui <a href="/dotnet/api/system.io.stream.canseek#System_IO_Stream_CanSeek">Stream. CanSeek</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="/dotnet/api/system.io.stream.cantimeout#System_IO_Stream_CanTimeout">CanTimeout</a></td>
<td>(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334204(v=exchg.10).md">CanWrite</a></td>
<td>Obtém um valor que indica se o fluxo dá suporte à gravação. (Substitui <a href="/dotnet/api/system.io.stream.canwrite#System_IO_Stream_CanWrite">Stream. CanWrite</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334159(v=exchg.10).md">Itag</a></td>
<td>Obtém ou define o iTag da coluna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334205(v=exchg.10).md">Comprimento</a></td>
<td>Obtém o comprimento atual do fluxo. (Substitui <a href="/dotnet/api/system.io.stream.length#System_IO_Stream_Length">Stream. Length</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334161(v=exchg.10).md">Posição</a></td>
<td>Obtém ou define a posição atual no fluxo. (Substitui <a href="/dotnet/api/system.io.stream.position#System_IO_Stream_Position">Stream. Position</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="/dotnet/api/system.io.stream.readtimeout#System_IO_Stream_ReadTimeout">ReadTimeout</a></td>
<td>(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="/dotnet/api/system.io.stream.writetimeout#System_IO_Stream_WriteTimeout">WriteTimeout</a></td>
<td>(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="methods"></a>Métodos

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nome</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.io.stream.beginread#System_IO_Stream_BeginRead_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginRead</a></td>
<td>(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.io.stream.beginwrite#System_IO_Stream_BeginWrite_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginWrite</a></td>
<td>(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.io.stream.close#System_IO_Stream_Close">Close</a></td>
<td>(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.marshalbyrefobject.createobjref#System_MarshalByRefObject_CreateObjRef_System_Type_">CreateObjRef</a></td>
<td>(Herdado de <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.io.stream.createwaithandle#System_IO_Stream_CreateWaitHandle">CreateWaitHandle</a></td>
<td><strong>Obsoleto.</strong> (Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose">Dispose ()</a></td>
<td>(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose_System_Boolean_">Dispose (booliano)</a></td>
<td>(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.io.stream.endread#System_IO_Stream_EndRead_System_IAsyncResult_">EndRead</a></td>
<td>(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.io.stream.endwrite#System_IO_Stream_EndWrite_System_IAsyncResult_">EndWrite</a></td>
<td>(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Igual a</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizar</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn334193(v=exchg.10).md">Liberar</a></td>
<td>Libere o fluxo. (Substitui <a href="/dotnet/api/system.io.stream.flush#System_IO_Stream_Flush">Stream. Flush ()</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.marshalbyrefobject.getlifetimeservice#System_MarshalByRefObject_GetLifetimeService">GetLifetimeService</a></td>
<td>(Herdado de <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.marshalbyrefobject.initializelifetimeservice#System_MarshalByRefObject_InitializeLifetimeService">InitializeLifetimeService</a></td>
<td>(Herdado de <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone()</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.marshalbyrefobject.memberwiseclone#System_MarshalByRefObject_MemberwiseClone_System_Boolean_">MemberwiseClone (booliano)</a></td>
<td>(Herdado de <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn334198(v=exchg.10).md">Ler</a></td>
<td>Lê uma sequência de bytes do fluxo atual e avança a posição no fluxo até o número de bytes lidos. (Substitui <a href="/dotnet/api/system.io.stream.read#System_IO_Stream_Read_System_Byte___System_Int32_System_Int32_">Stream. Read ([], Int32, Int32)</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.io.stream.readbyte#System_IO_Stream_ReadByte">ReadByte</a></td>
<td>(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn334154(v=exchg.10).md">Seek</a></td>
<td>Define a posição no fluxo atual. (Substitui <a href="/dotnet/api/system.io.stream.seek#System_IO_Stream_Seek_System_Int64_System_IO_SeekOrigin_">Stream. Seek (Int64, SeekOrigin)</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn334196(v=exchg.10).md">SetLength</a></td>
<td>Define o comprimento do fluxo. (Substitui <a href="/dotnet/api/system.io.stream.setlength#System_IO_Stream_SetLength_System_Int64_">Stream. SetLength (Int64)</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn334149(v=exchg.10).md">ToString</a></td>
<td>Retorna uma <a href="/dotnet/api/system.string">cadeia de caracteres</a> que representa o <a href="dn334143(v=exchg.10).md">ColumnStream</a>atual. (Substitui <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn334197(v=exchg.10).md">Gravar</a></td>
<td>Grava uma sequência de bytes no fluxo atual e avança a posição atual dentro desse fluxo pelo número de bytes gravados. (Substitui <a href="/dotnet/api/system.io.stream.write#System_IO_Stream_Write_System_Byte___System_Int32_System_Int32_">Stream. Write ([], Int32, Int32)</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.io.stream.writebyte#System_IO_Stream_WriteByte_System_Byte_">WriteByte</a></td>
<td>(Herdado do <a href="/dotnet/api/system.io.stream">fluxo</a>.)</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe ColumnStream](./columnstream-class.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
