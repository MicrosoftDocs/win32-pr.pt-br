---
description: 'Saiba mais sobre: propriedades BytesColumnValue'
title: Propriedades BytesColumnValue
TOCTitle: BytesColumnValue properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.BytesColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytescolumnvalue_properties(v=EXCHG.10)
ms:contentKeyID: 55100964
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d7973f35a59af3cda2e8bb3bd400d2ef10e43e4f18fe9431f61ed50b62b343f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117902102"
---
# <a name="bytescolumnvalue-properties"></a>Propriedades BytesColumnValue

Incluir membros protegidos  
Incluir membros herdados  

O [tipo BytesColumnValue](./bytescolumnvalue-class.md) expõe os membros a seguir.

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
<td><a href="dn334126(v=exchg.10).md">Comprimento</a></td>
<td>Obtém o comprimento de byte de um valor de coluna, que é zero se a coluna for nula; caso contrário, corresponde ao comprimento real da matriz de byte. (Substitui <a href="dn334213(v=exchg.10).md">ColumnValue.Length</a>.)</td>
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
<td><a href="dn334176(v=exchg.10).md">Tamanho</a></td>
<td>Obtém o tamanho do valor na coluna. Isso retorna 0 para colunas de tamanho variável (ou seja, binário e cadeia de caracteres). (Substitui <a href="dn334172(v=exchg.10).md">ColumnValue.Size</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334129(v=exchg.10).md">Valor</a></td>
<td>Obtém ou define o valor da coluna. Use <a href="dn334138(v=exchg.10).md">SetColumns(JET_SESID, JET_TABLEID, [])</a> para atualizar um registro com o valor da coluna.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334177(v=exchg.10).md">ValueAsObject</a></td>
<td>Obtém o último valor definido ou recuperado da coluna. O valor é retornado como um objeto genérico. (Substitui <a href="dn334214(v=exchg.10).md">ColumnValue.ValueAsObject</a>.)</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe BytesColumnValue](./bytescolumnvalue-class.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
