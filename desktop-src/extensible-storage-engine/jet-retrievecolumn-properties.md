---
description: 'Saiba mais sobre: Propriedades de JET_RETRIEVECOLUMN'
title: Propriedades de JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103808
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c1e902b7e79111f3e9d9bf0160880d95c3957804de981fd56bbc36db5a9c3fc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107340"
---
# <a name="jet_retrievecolumn-properties"></a>Propriedades de JET_RETRIEVECOLUMN

Incluir membros protegidos  
Incluir membros herdados  

O tipo de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) expõe os membros a seguir.

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
<td><a href="dn335226(v=exchg.10).md">cbActual</a></td>
<td>Obtém o tamanho, em bytes, dos dados recuperados por uma operação de recuperação de coluna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335228(v=exchg.10).md">cbData</a></td>
<td>Obtém ou define o tamanho do buffer <a href="dn351040(v=exchg.10).md">pvData</a> , em bytes. A operação de recuperação de coluna não armazenará mais dados em pvData do que cbData.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335230(v=exchg.10).md">columnid</a></td>
<td>Obtém ou define o identificador de coluna da coluna a ser recuperada.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></td>
<td>Obtém o columnid da coluna marcada, com vários valores ou esparsos quando todas as colunas marcadas são recuperadas passando 0 como columnid.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335231(v=exchg.10).md">erra</a></td>
<td>Obtém o aviso retornado da recuperação da coluna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335232(v=exchg.10).md">grbit</a></td>
<td>Obtém ou define as opções de recuperação de coluna.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335233(v=exchg.10).md">ibData</a></td>
<td>Obtém ou define o deslocamento no buffer no qual os dados serão armazenados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335234(v=exchg.10).md">ibLongValue</a></td>
<td>Obtém ou define o deslocamento para o primeiro byte a ser recuperado de uma coluna do tipo <a href="hh577895(v=exchg.10).md">LongBinary</a> ou <a href="hh577895(v=exchg.10).md">LONGTEXT</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn351039(v=exchg.10).md">itagSequence</a></td>
<td>Obtém ou define o número de sequência dos valores contidos em uma coluna com vários valores. Se itagSequence for 0, o número de instâncias de uma coluna com vários valores será retornado em vez de quaisquer dados de coluna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn351040(v=exchg.10).md">pvData</a></td>
<td>Obtém ou define o buffer que armazenará os dados que serão recuperados da coluna.</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
