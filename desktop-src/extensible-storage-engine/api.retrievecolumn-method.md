---
description: 'Saiba mais sobre: Método Api.RetrieveColumn'
title: Método Api.RetrieveColumn
TOCTitle: 'RetrieveColumn method '
ms:assetid: Overload:Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100835
ms.date: 07/30/2014
ms.topic: article
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
dev_langs:
- CSharp
- JScript
- VB
- other
ms.openlocfilehash: 392fb670cbe9f64025cd2270c52dc7bc317507821d25b3cf842d323db6ddccc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840396"
---
# <a name="apiretrievecolumn-method"></a>Método Api.RetrieveColumn

Incluir membros protegidos  
Incluir membros herdados  

## <a name="overload-list"></a>Lista de sobrecargas

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334041(v=exchg.10).md">RetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera um único valor de coluna do registro atual. O registro é o registro associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334060(v=exchg.10).md">RetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</a></td>
<td>Recupera um único valor de coluna do registro atual. O registro é o registro associado à entrada de índice na posição atual do cursor. Como alternativa, essa função pode recuperar uma coluna de um registro que está sendo criado no buffer de cópia do cursor. Essa função também pode recuperar dados de coluna de uma entrada de índice que faz referência ao registro atual. Além de recuperar o valor real da coluna, JetRetrieveColumn também pode ser usado para recuperar o tamanho de uma coluna, antes de recuperar os dados da coluna em si para que os buffers de aplicativo possam ser dimensionados adequadamente.</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
