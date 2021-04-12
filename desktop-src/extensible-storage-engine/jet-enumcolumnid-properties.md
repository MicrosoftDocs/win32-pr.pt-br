---
description: 'Saiba mais sobre: Propriedades de JET_ENUMCOLUMNID'
title: Propriedades de JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_properties(v=EXCHG.10)
ms:contentKeyID: 55103627
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 1e45574d7cabd937d6b2d7351a917ac62340f355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501314"
---
# <a name="jet_enumcolumnid-properties"></a>Propriedades de JET_ENUMCOLUMNID

Incluir membros protegidos  
Incluir membros herdados  

O tipo de [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) expõe os membros a seguir.

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
<td><a href="dn335141(v=exchg.10).md">columnid</a></td>
<td>Obtém ou define a ID de columnid a ser enumerada.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335092(v=exchg.10).md">ctagSequence</a></td>
<td>Obtém ou define a contagem de valores de coluna (por índice baseado em um) para enumerar para a ID de coluna especificada. Se ctagSequence for 0 (zero), rgtagSequence será ignorado e todos os valores de coluna para a ID de coluna especificada serão enumerados.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335093(v=exchg.10).md">rgtagSequence</a></td>
<td>Obtém ou define a matriz de índices com base em um na matriz de valores de coluna para uma determinada coluna. Um único elemento é um itagSequence que é definido em JET_RETRIEVECOLUMN. Um itagSequence de 0 (zero) significa &quot; ignorar &quot; . Um itagSequence de 1 significa retornar o primeiro valor de coluna da coluna, 2 significa o segundo e assim por diante.</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
