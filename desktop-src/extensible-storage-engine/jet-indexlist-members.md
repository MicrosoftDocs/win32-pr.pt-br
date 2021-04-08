---
description: 'Saiba mais sobre: membros do JET_INDEXLIST'
title: Membros do JET_INDEXLIST
TOCTitle: JET_INDEXLIST members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INDEXLIST
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist_members(v=EXCHG.10)
ms:contentKeyID: 55103660
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d7800ef911366bad40b2d02ee60e23b5d138d30c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011576"
---
# <a name="jet_indexlist-members"></a>Membros do JET_INDEXLIST

Incluir membros protegidos  
Incluir membros herdados  

Informações sobre uma tabela temporária que contém informações sobre todos os índices de uma determinada tabela.

O tipo de [JET_INDEXLIST](./jet-indexlist-class.md) expõe os membros a seguir.

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
<td><a href="dn335166(v=exchg.10).md">JET_INDEXLIST</a></td>
<td></td>
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
<td><a href="dn335125(v=exchg.10).md">columnidcColumn</a></td>
<td>Obtém o columnid da coluna na tabela temporária que armazena o número de colunas na chave de índice. A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335126(v=exchg.10).md">columnidcEntry</a></td>
<td>Obtém o columnid da coluna na tabela temporária que armazena o número de entradas no índice. Esse valor não é atual e só é atualizado por &quot; API. JetComputeStats &quot; . A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335127(v=exchg.10).md">columnidcKey</a></td>
<td>Obtém o columnid da coluna na tabela temporária que armazena o número de chaves exclusivas no índice. Esse valor não é atual e só é atualizado por &quot; API. JetComputeStats &quot; . A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></td>
<td>Obtém o columnid da coluna na tabela temporária que armazena o tipo de coluna da coluna que está sendo indexada. A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></td>
<td>Obtém o columnid da coluna na tabela temporária que armazena o columnid da coluna que está sendo indexada. A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></td>
<td>Obtém o columnid da coluna na tabela temporária que armazena o grbit que se aplica à coluna indexada. Consulte <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>. A coluna é do tipo <a href="hh577895(v=exchg.10).md">texto</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335168(v=exchg.10).md">columnidCp</a></td>
<td>Obtém o columnid da coluna na tabela temporária que armazena a página de código da coluna indexada. A coluna é do tipo <a href="hh577895(v=exchg.10).md">Short</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335136(v=exchg.10).md">columnidcPage</a></td>
<td>Obtém o columnid da coluna na tabela temporária que armazena o número de páginas no índice. Esse valor não é atual e só é atualizado por &quot; API. JetComputeStats &quot; . A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></td>
<td>Obtém o columnid da coluna na tabela temporária que armazena o grbit que se aplica à coluna indexada. Consulte <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>. A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></td>
<td>Obtém o columnid da coluna na tabela temporária que armazena o grbits usado no índice. Consulte <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>. A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335170(v=exchg.10).md">columnidiColumn</a></td>
<td>Obtém o columnid da coluna na tabela temporária que armazena o índice dessa coluna na chave de índice. A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335138(v=exchg.10).md">columnidindexname</a></td>
<td>Obtém o columnid da coluna na tabela temporária que armazena o nome do índice. A coluna é do tipo <a href="hh577895(v=exchg.10).md">texto</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335171(v=exchg.10).md">columnidLangid</a></td>
<td>Obtém o columnid da coluna na tabela temporária que armazena a ID de idioma (LCID) do índice. A coluna é do tipo <a href="hh577895(v=exchg.10).md">Short</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></td>
<td>Obtém o columnid da coluna na tabela temporária que armazena os sinalizadores de normalização Unicode para o índice. A coluna é do tipo <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335173(v=exchg.10).md">cRecord</a></td>
<td>Obtém o número de registros na tabela temporária.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335174(v=exchg.10).md">TableID</a></td>
<td>Obtém TableName da tabela temporária. Isso deve ser fechado quando a tabela não for mais necessária.</td>
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
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Igual a</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizar</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn335165(v=exchg.10).md">ToString</a></td>
<td>Retorna uma <a href="/dotnet/api/system.string">cadeia de caracteres</a> que representa a <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a>atual. (Substitui <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe JET_INDEXLIST](./jet-indexlist-class.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
