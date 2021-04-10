---
description: 'Saiba mais sobre: membros do JET_INDEXCREATE'
title: Membros do JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_members(v=EXCHG.10)
ms:contentKeyID: 55103641
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: cbe9ce962221db30c8cdae90461fa55fc0baea19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171349"
---
# <a name="jet_indexcreate-members"></a>Membros do JET_INDEXCREATE

Incluir membros protegidos  
Incluir membros herdados  

Contém as informações necessárias para criar um índice sobre os dados em um banco de dado ESE. Contém as informações necessárias para criar um índice sobre os dados em um banco de dado ESE.

O tipo de [JET_INDEXCREATE](./jet-indexcreate-class.md) expõe os membros a seguir.

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
<td><a href="dn335115(v=exchg.10).md">JET_INDEXCREATE</a></td>
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
<td><a href="dn335122(v=exchg.10).md">cbKey</a></td>
<td>Obtém ou define o comprimento, em caracteres, de szKey, incluindo os dois nulos de terminação.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335156(v=exchg.10).md">cbKeyMost</a></td>
<td>Obtém ou define o tamanho máximo permitido, em bytes, para as chaves no índice. O tamanho mínimo de chave máximo suportado é JET_cbKeyMostMin (255), que é o tamanho de chave máximo herdado. O tamanho máximo da chave depende do tamanho da página do banco de dados <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>. O tamanho máximo da chave pode ser recuperado com o <a href="dn351156(v=exchg.10).md">máximo</a>. Esse parâmetro é ignorado no Windows XP e no Windows Server 2003. Diferentemente da API não gerenciada, <strong>IndexKeyMost ()</strong> (JET_bitIndexKeyMost) não é necessária, ela será adicionada automaticamente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></td>
<td>Obtém ou define o comprimento máximo, em bytes, de cada coluna a ser armazenada no índice.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></td>
<td>Obtém ou define o número de colunas condicionais.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335157(v=exchg.10).md">erra</a></td>
<td>Obtém ou define o código de erro da criação deste índice.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335119(v=exchg.10).md">grbit</a></td>
<td>Obtém ou define as opções de criação de índice.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335159(v=exchg.10).md">pidxUnicode</a></td>
<td>Obtém ou define as opções de comparação Unicode opcionais.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335120(v=exchg.10).md">pSpaceHints</a></td>
<td>Obtém ou define as dicas de alocação, manutenção e uso de espaço.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></td>
<td>Obtém ou define as colunas condicionais opcionais.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335121(v=exchg.10).md">szIndexName</a></td>
<td>Obtém ou define o nome do índice a ser criado.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335161(v=exchg.10).md">szKey</a></td>
<td>Obtém ou define a descrição da chave de índice. Essa é uma cadeia de caracteres dupla com terminação nula de tokens delimitados por nulo. Cada token tem o formato [Direction-especificador] [nome-da-coluna], onde a especificação de direção é &quot; + &quot; ou &quot; - &quot; . por exemplo, um szKey de &quot; + abc\0-def\0 + ghi\0 &quot; será indexado nas três colunas &quot; ABC &quot; (em ordem crescente), &quot; Def &quot; (em ordem decrescente) e &quot; GHI &quot; (em ordem crescente).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335162(v=exchg.10).md">ulDensity</a></td>
<td>Obtém ou define a densidade do índice.</td>
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
<td><a href="dn335116(v=exchg.10).md">ContentEquals</a></td>
<td>Retorna um valor que indica se essa instância é igual a outra instância.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn335153(v=exchg.10).md">DeepClone</a></td>
<td>Retorna uma cópia profunda do objeto.</td>
</tr>
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
<td><a href="dn335154(v=exchg.10).md">ToString</a></td>
<td>Gere uma representação de cadeia de caracteres da instância. (Substitui <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe JET_INDEXCREATE](./jet-indexcreate-class.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
