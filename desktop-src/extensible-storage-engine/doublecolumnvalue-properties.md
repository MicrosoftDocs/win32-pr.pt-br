---
description: 'Saiba mais sobre: propriedades DoubleColumnValue'
title: Propriedades DoubleColumnValue
TOCTitle: DoubleColumnValue properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.DoubleColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.doublecolumnvalue_properties(v=EXCHG.10)
ms:contentKeyID: 55101031
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c2fd318f9cf20e7ee54eb0a2fe9f241afa6dcec8407cdc90f7d8fd8b2779acda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670026"
---
# <a name="doublecolumnvalue-properties"></a>Propriedades DoubleColumnValue

Incluir membros protegidos  
Incluir membros herdados  

O [tipo DoubleColumnValue](./doublecolumnvalue-class.md) expõe os membros a seguir.

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
<td><a href="dn334225(v=exchg.10).md">Comprimento</a></td>
<td>Obtém o comprimento de byte de um valor de coluna, que é zero se a coluna for nula; caso contrário, corresponde ao Tamanho dessa coluna de tamanho fixo. (Herdado <a href="dn334171(v=exchg.10).md">de ColumnValueOfStruct &lt; T &gt; </a>.)</td>
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
<td><a href="dn273977(v=exchg.10).md">Tamanho</a></td>
<td>Obtém o tamanho do valor na coluna. Isso retorna 0 para colunas de tamanho variável (ou seja, binário e cadeia de caracteres). (Substitui <a href="dn334172(v=exchg.10).md">ColumnValue.Size</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334180(v=exchg.10).md">Valor</a></td>
<td>Obtém ou define o valor no struct. (Herdado <a href="dn334171(v=exchg.10).md">de ColumnValueOfStruct &lt; T &gt; </a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334226(v=exchg.10).md">ValueAsObject</a></td>
<td>Obtém o último valor definido ou recuperado da coluna. O valor é retornado como um objeto genérico. (Herdado <a href="dn334171(v=exchg.10).md">de ColumnValueOfStruct &lt; T &gt; </a>.)</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe DoubleColumnValue](./doublecolumnvalue-class.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
