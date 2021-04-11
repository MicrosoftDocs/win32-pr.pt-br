---
description: 'Saiba mais sobre: Propriedades de StringColumnValue'
title: Propriedades de StringColumnValue
TOCTitle: StringColumnValue properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.StringColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.stringcolumnvalue_properties(v=EXCHG.10)
ms:contentKeyID: 55104024
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 822e469fae8de69137cbbe7a8e085137c290850a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170123"
---
# <a name="stringcolumnvalue-properties"></a>Propriedades de StringColumnValue

Incluir membros protegidos  
Incluir membros herdados  

O tipo [StringColumnValue](./stringcolumnvalue-class.md) expõe os membros a seguir.

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
<td><a href="dn351195(v=exchg.10).md">Comprimento</a></td>
<td>Obtém o comprimento de bytes de um valor de coluna, que será zero se a coluna for nula, caso contrário, ela corresponderá ao comprimento de byte do valor da cadeia de caracteres. O comprimento do byte é determinado na suposição de dois bytes por caractere. (Substitui <a href="dn334213(v=exchg.10).md">columnvalue. Length</a>.)</td>
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
<td><a href="dn351137(v=exchg.10).md">Tamanho</a></td>
<td>Obtém o tamanho do valor na coluna. Isso retorna 0 para colunas de tamanho variável (ou seja, binary e String). (Substitui <a href="dn334172(v=exchg.10).md">columnvalue. Size</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn351204(v=exchg.10).md">Valor</a></td>
<td>Obtém ou define o valor da coluna. Use <a href="dn334138(v=exchg.10).md">SetColumns (JET_SESID, JET_TABLEID, [])</a> para atualizar um registro com o valor da coluna.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn351202(v=exchg.10).md">ValueAsObject</a></td>
<td>Obtém o último conjunto ou o valor recuperado da coluna. O valor é retornado como um objeto genérico. (Substitui <a href="dn334214(v=exchg.10).md">columnvalue. ValueAsObject</a>.)</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe StringColumnValue](./stringcolumnvalue-class.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
