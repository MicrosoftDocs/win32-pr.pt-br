---
description: 'Saiba mais sobre: Propriedades de JET_SETCOLUMN'
title: Propriedades de JET_SETCOLUMN
TOCTitle: JET_SETCOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_SETCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setcolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103854
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 43f005ce4edb909e842566e43b9b74ed80471c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461000"
---
# <a name="jet_setcolumn-properties"></a>Propriedades de JET_SETCOLUMN

Incluir membros protegidos  
Incluir membros herdados  

O tipo de [JET_SETCOLUMN](./jet-setcolumn-class.md) expõe os membros a seguir.

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
<td><a href="dn335266(v=exchg.10).md">cbData</a></td>
<td>Obtém ou define o tamanho dos dados a serem definidos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335268(v=exchg.10).md">columnid</a></td>
<td>Obtém ou define o identificador de coluna de uma coluna a ser definida.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335269(v=exchg.10).md">erra</a></td>
<td>Obtém o código de erro ou o aviso retornado da operação de definição de coluna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335270(v=exchg.10).md">grbit</a></td>
<td>Obtém ou define as opções para a operação definir coluna.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335271(v=exchg.10).md">ibData</a></td>
<td>Obtém ou define o deslocamento dos dados a serem definidos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335272(v=exchg.10).md">ibLongValue</a></td>
<td>Obtém ou define o deslocamento para o primeiro byte a ser definido em uma coluna do tipo <a href="hh577895(v=exchg.10).md">LongBinary</a> ou <a href="hh577895(v=exchg.10).md">LONGTEXT</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335273(v=exchg.10).md">itagSequence</a></td>
<td>Obtém ou define o número de sequência do valor em uma coluna de valores múltiplos a ser definida. A matriz de valores é baseada em um. O primeiro valor é Sequence 1, não 0 (zero). Se a coluna de registro tiver apenas um valor, 1 deverá ser passado como itagSequence se esse valor estiver sendo substituído. Um valor de 0 (zero) significa adicionar uma nova instância de valor de coluna ao final da sequência de valores de coluna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn351058(v=exchg.10).md">pvData</a></td>
<td>Obtém ou define um ponteiro para os dados a serem definidos.</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe JET_SETCOLUMN](./jet-setcolumn-class.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
