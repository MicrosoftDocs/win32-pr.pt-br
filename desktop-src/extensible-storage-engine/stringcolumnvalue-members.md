---
description: 'Saiba mais sobre: Membros StringColumnValue'
title: Membros StringColumnValue
TOCTitle: StringColumnValue members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.StringColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.stringcolumnvalue_members(v=EXCHG.10)
ms:contentKeyID: 55104040
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 68f0050acea5c838fba3b23b4dc3f4df65177bf72012932fe8f07e568ebedd15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118071246"
---
# <a name="stringcolumnvalue-members"></a>Membros StringColumnValue

Incluir membros protegidos  
Incluir membros herdados  

Um valor de coluna de cadeia de caracteres Unicode.

O [tipo StringColumnValue](./stringcolumnvalue-class.md) expõe os membros a seguir.

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
<td><a href="dn351187(v=exchg.10).md">StringColumnValue</a></td>
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
<td>Obtém ou define a columnid a ser definida ou recuperada. (Herdado de <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334212(v=exchg.10).md">Erro</a></td>
<td>Obtém o aviso gerado recuperando ou configurando essa coluna. (Herdado de <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334165(v=exchg.10).md">ItagSequence</a></td>
<td>Obtém ou define a sequência de itag da coluna. (Herdado de <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn351195(v=exchg.10).md">Comprimento</a></td>
<td>Obtém o comprimento de byte de um valor de coluna, que é zero se a coluna for nula; caso contrário, corresponde ao comprimento de byte do valor da cadeia de caracteres. O comprimento do byte é determinado na suposição de dois bytes por caractere. (Substitui <a href="dn334213(v=exchg.10).md">ColumnValue.Length</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334169(v=exchg.10).md">RetrieveGrbit</a></td>
<td>Obtém ou define opções de recuperação de coluna. (Herdado de <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334215(v=exchg.10).md">SetGrbit</a></td>
<td>Obtém ou define opções de atualização de coluna. (Herdado de <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Propriedade protegida" alt="Protected property" /></td>
<td><a href="dn351137(v=exchg.10).md">Tamanho</a></td>
<td>Obtém o tamanho do valor na coluna. Isso retorna 0 para colunas de tamanho variável (ou seja, binário e cadeia de caracteres). (Substitui <a href="dn334172(v=exchg.10).md">ColumnValue.Size</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn351204(v=exchg.10).md">Valor</a></td>
<td>Obtém ou define o valor da coluna. Use <a href="dn334138(v=exchg.10).md">SetColumns(JET_SESID, JET_TABLEID, [])</a> para atualizar um registro com o valor da coluna.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn351202(v=exchg.10).md">ValueAsObject</a></td>
<td>Obtém o último valor definido ou recuperado da coluna. O valor é retornado como um objeto genérico. (Substitui <a href="dn334214(v=exchg.10).md">ColumnValue.ValueAsObject</a>.)</td>
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
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">Gettype</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn351134(v=exchg.10).md">GetValueFromBytes</a></td>
<td>Dados recuperados do ESENT, decodificar os dados e definir o valor no objeto ColumnValue. (Substitui <a href="dn334208(v=exchg.10).md">ColumnValue.GetValueFromBytes([], Int32, Int32, Int32)</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Memberwiseclone</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn351194(v=exchg.10).md">ToString</a></td>
<td>Obtém uma representação de cadeia de caracteres desse objeto. (Substitui <a href="dn334163(v=exchg.10).md">ColumnValue.ToString()</a>.)</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe StringColumnValue](./stringcolumnvalue-class.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
