---
description: 'Saiba mais sobre: Propriedades de GuidColumnValue'
title: Propriedades de GuidColumnValue
TOCTitle: GuidColumnValue properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.GuidColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.guidcolumnvalue_properties(v=EXCHG.10)
ms:contentKeyID: 55103238
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: fc297722e8fe4d6520f019f004ff8d4111616a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565905"
---
# <a name="guidcolumnvalue-properties"></a>Propriedades de GuidColumnValue

Incluir membros protegidos  
Incluir membros herdados  

O tipo [GuidColumnValue](./guidcolumnvalue-class.md) expõe os membros a seguir.

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
<td>Obtém o comprimento de bytes de um valor de coluna, que será zero se a coluna for nula, caso contrário, ela corresponderá ao tamanho dessa coluna de tamanho fixo. (Herdado <a href="dn334171(v=exchg.10).md">de &lt; ColumnValueOfStruct &gt; T</a>.)</td>
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
<td><a href="dn350894(v=exchg.10).md">Tamanho</a></td>
<td>Obtém o tamanho do valor na coluna. Isso retorna 0 para colunas de tamanho variável (ou seja, binary e String). (Substitui <a href="dn334172(v=exchg.10).md">columnvalue. Size</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334180(v=exchg.10).md">Valor</a></td>
<td>Obtém ou define o valor na estrutura. (Herdado <a href="dn334171(v=exchg.10).md">de &lt; ColumnValueOfStruct &gt; T</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334226(v=exchg.10).md">ValueAsObject</a></td>
<td>Obtém o último conjunto ou o valor recuperado da coluna. O valor é retornado como um objeto genérico. (Herdado <a href="dn334171(v=exchg.10).md">de &lt; ColumnValueOfStruct &gt; T</a>.)</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe GuidColumnValue](./guidcolumnvalue-class.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
