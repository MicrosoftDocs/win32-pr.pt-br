---
description: 'Saiba mais sobre: Propriedades de JET_RECSIZE'
title: Propriedades de JET_RECSIZE (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: JET_RECSIZE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize_properties(v=EXCHG.10)
ms:contentKeyID: 39513545
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4733e1d666bdf3f938c91f437c1764811fb10f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837352"
---
# <a name="jet_recsize-properties"></a>Propriedades de JET_RECSIZE

Incluir membros protegidos  
Incluir membros herdados  

O tipo de [JET_RECSIZE](./jet-recsize-structure2.md) expõe os membros a seguir.

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
<td><a href="hh557581(v=exchg.10).md">cbData</a></td>
<td>Obtém o conjunto de dados do usuário no registro.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></td>
<td>Obtém o tamanho compactado dos dados do usuário no registro. Isso é o mesmo que <a href="hh557581(v=exchg.10).md">cbData</a> se nenhum valor longo intrínseco for compactado).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="hh557913(v=exchg.10).md">cbLongValueData</a></td>
<td>Obtém o conjunto de dados do usuário no registro, mas armazenado na árvore de valor longo.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></td>
<td>Obtém o tamanho compactado dos dados do usuário na árvore de valor longo. Isso é o mesmo que <a href="hh557913(v=exchg.10).md">cbLongValueData</a> se nenhum valor longo separado for compactado.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></td>
<td>Obtém a sobrecarga dos dados de valor longo.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="hh565836(v=exchg.10).md">cbOverhead</a></td>
<td>Obtém a sobrecarga da estrutura de registro ESENT para este registro. Isso inclui o tamanho da chave do registro.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></td>
<td>Obtém o número total de colunas no registro que estão compactadas.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="hh596288(v=exchg.10).md">cLongValues</a></td>
<td>Obtém o número total de valores longos armazenados na árvore de valor longo para esse registro. Isso não inclui valores longos intrínsecos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="hh577486(v=exchg.10).md">cMultiValues</a></td>
<td>Obtém a acumulação do número total de valores além do primeiro para todas as colunas no registro.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></td>
<td>Obtém o número total de colunas fixas e variáveis definidas neste registro.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></td>
<td>Obtém o número total de colunas marcadas definidas neste registro.</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Estrutura de JET_RECSIZE](./jet-recsize-structure2.md)

[Namespace Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
