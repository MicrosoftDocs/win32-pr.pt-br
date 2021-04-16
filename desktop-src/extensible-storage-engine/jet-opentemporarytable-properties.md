---
description: 'Saiba mais sobre: Propriedades de JET_OPENTEMPORARYTABLE'
title: Propriedades de JET_OPENTEMPORARYTABLE (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: JET_OPENTEMPORARYTABLE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable_properties(v=EXCHG.10)
ms:contentKeyID: 55104127
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: e9c55afddd1128a517c27f6a86466b488e6924a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104570342"
---
# <a name="jet_opentemporarytable-properties"></a>Propriedades de JET_OPENTEMPORARYTABLE

Incluir membros protegidos  
Incluir membros herdados  

O tipo de [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) expõe os membros a seguir.

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
<td><a href="dn335290(v=exchg.10).md">cbKeyMost</a></td>
<td>Obtém ou define o tamanho máximo de uma chave que representa uma determinada linha. O tamanho máximo da chave pode ser definido para controlar como as chaves são truncadas. O truncamento de chave é importante porque pode afetar quando as linhas são consideradas distintas. Se esse parâmetro for definido como 0 ou 255, o tamanho máximo da chave e sua semântica permanecerão idênticos ao tamanho máximo da chave com suporte do Windows Server 2003. Esse parâmetro também pode ser definido como um valor maior como uma função do tamanho da página do banco de dados para a instância <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>. Confira o <a href="dn335292(v=exchg.10).md">melhor</a> para obter mais informações.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></td>
<td>Obtém ou define a quantidade máxima de dados que serão usados de qualquer variável lengthcolumn para construir uma chave para uma determinada linha. Esse parâmetro pode ser usado para controlar a quantidade de espaço de chave consumida por qualquer coluna de chave fornecida. Esse limite está em bytes. Se esse parâmetro for zero ou for o mesmo que a propriedade <a href="dn335290(v=exchg.10).md">cbKeyMost</a> , nenhum limite estará em vigor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335287(v=exchg.10).md">ccolumn</a></td>
<td>Obtém ou define o número de colunas em <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn351232(v=exchg.10).md">grbit</a></td>
<td>Obtém ou define as opções para a tabela temporária.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335288(v=exchg.10).md">pidxunicode</a></td>
<td>Obtém ou define os sinalizadores de ID de localidade e normalização a serem usados para comparar quaisquer dados de coluna de chave Unicode na tabela temporária. Quando esse parâmetro for NULL, o LCID padrão será usado para comparar todas as colunas de chave Unicode na tabela temporária. O LCID padrão é a localidade inglês dos EUA. Quando esse parâmetro é nulo, os sinalizadores de normalização padrão serão usados para comparar quaisquer dados de coluna de chave Unicode na tabela temporária. Os sinalizadores de normalização padrão são: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn351228(v=exchg.10).md">prgcolumndef</a></td>
<td>Obtém ou define as definições de coluna para as colunas criadas na tabela temporária.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn351233(v=exchg.10).md">prgcolumnid</a></td>
<td>Obtém ou define o buffer de saída que recebe a matriz de IDs de coluna geradas durante a criação da tabela temporária. As IDs de coluna nessa matriz correspondem exatamente à matriz de entrada de definições de coluna. Como resultado, o tamanho desse buffer deve corresponder ao tamanho de <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335293(v=exchg.10).md">TableID</a></td>
<td>Obtém o identificador de tabela para a tabela temporária criada como resultado de uma chamada bem-sucedida para JetOpenTemporaryTable.</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)

[Namespace Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
