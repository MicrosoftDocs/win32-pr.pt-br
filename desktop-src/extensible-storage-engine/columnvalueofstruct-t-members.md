---
description: 'Saiba mais sobre: membros do ColumnValueOfStruct <T>'
title: Membros de ColumnValueOfStruct (T)
TOCTitle: ColumnValueOfStruct(T) members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
ms:mtpsurl: https://msdn.microsoft.com/library/Dn334217(v=EXCHG.10)
ms:contentKeyID: 55101002
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: e96cbcc8210206b4f9dff01600a30ee22188d7a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570348"
---
# <a name="columnvalueofstructt-members"></a>Membros do ColumnValueOfStruct \<T\>

Incluir membros protegidos  
Incluir membros herdados  

Defina uma coluna de um tipo de struct (por exemplo, Int32/GUID).

O [tipo \<T\> ColumnValueOfStruct](./columnvalueofstruct-t-class.md) expõe os membros a seguir.

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
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn334175(v=exchg.10).md">ColumnValueOfStruct &lt; T&gt;</a></td>
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
<td><a href="dn334166(v=exchg.10).md">Columnid</a></td>
<td>Obtém ou define o columnid a ser definido ou recuperado. (Herdado de <a href="dn334206(v=exchg.10).md">columnvalue</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334212(v=exchg.10).md">Erro</a></td>
<td>Obtém o aviso gerado pela recuperação ou definição desta coluna. (Herdado de <a href="dn334206(v=exchg.10).md">columnvalue</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334165(v=exchg.10).md">ItagSequence</a></td>
<td>Obtém ou define a sequência de iTag da coluna. (Herdado de <a href="dn334206(v=exchg.10).md">columnvalue</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334225(v=exchg.10).md">Comprimento</a></td>
<td>Obtém o comprimento de bytes de um valor de coluna, que será zero se a coluna for nula, caso contrário, ela corresponderá ao tamanho dessa coluna de tamanho fixo. (Substitui <a href="dn334213(v=exchg.10).md">columnvalue. Length</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334169(v=exchg.10).md">RetrieveGrbit</a></td>
<td>Obtém ou define opções de recuperação de coluna. (Herdado de <a href="dn334206(v=exchg.10).md">columnvalue</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334215(v=exchg.10).md">SetGrbit</a></td>
<td>Obtém ou define opções de atualização de coluna. (Herdado de <a href="dn334206(v=exchg.10).md">columnvalue</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Propriedade protegida" alt="Protected property" /></td>
<td><a href="dn334172(v=exchg.10).md">Tamanho</a></td>
<td>Obtém o tamanho do valor na coluna. Isso retorna 0 para colunas de tamanho variável (ou seja, binary e String). (Herdado de <a href="dn334206(v=exchg.10).md">columnvalue</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334180(v=exchg.10).md">Valor</a></td>
<td>Obtém ou define o valor na estrutura.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334226(v=exchg.10).md">ValueAsObject</a></td>
<td>Obtém o último conjunto ou o valor recuperado da coluna. O valor é retornado como um objeto genérico. (Substitui <a href="dn334214(v=exchg.10).md">columnvalue. ValueAsObject</a>.)</td>
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
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn334178(v=exchg.10).md">CheckDataCount</a></td>
<td>Verifique se os dados recuperados são exatamente o tamanho necessário para a estrutura. Uma exceção será lançada se houver uma incompatibilidade.</td>
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
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn334208(v=exchg.10).md">GetValueFromBytes</a></td>
<td>Dados obtidos recuperados do ESENT, decodifique os dados e defina o valor no objeto Columnvalue. (Herdado de <a href="dn334206(v=exchg.10).md">columnvalue</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn334223(v=exchg.10).md">ToString</a></td>
<td>Obtém uma representação de cadeia de caracteres deste objeto. (Substitui <a href="dn334163(v=exchg.10).md">columnvalue. ToString ()</a>.)</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[\<T\>Classe ColumnValueOfStruct](./columnvalueofstruct-t-class.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
