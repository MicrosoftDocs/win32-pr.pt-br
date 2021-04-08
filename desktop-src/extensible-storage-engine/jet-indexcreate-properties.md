---
description: 'Saiba mais sobre: Propriedades de JET_INDEXCREATE'
title: Propriedades de JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_properties(v=EXCHG.10)
ms:contentKeyID: 55103645
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 66b6ada105e6f6d12cb754f288478e85d75a07e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922576"
---
# <a name="jet_indexcreate-properties"></a>Propriedades de JET_INDEXCREATE

Incluir membros protegidos  
Incluir membros herdados  

O tipo de [JET_INDEXCREATE](./jet-indexcreate-class.md) expõe os membros a seguir.

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
<td><a href="dn335122(v=exchg.10).md">cbKey</a></td>
<td>Obtém ou define o comprimento, em caracteres, de szKey, incluindo os dois nulos de terminação.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335156(v=exchg.10).md">cbKeyMost</a></td>
<td>Obtém ou define o tamanho máximo permitido, em bytes, para as chaves no índice. O tamanho mínimo de chave máximo suportado é JET_cbKeyMostMin (255), que é o tamanho de chave máximo herdado. O tamanho máximo da chave depende do tamanho da página do banco de dados <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>. O tamanho máximo da chave pode ser recuperado com o <a href="dn351156(v=exchg.10).md">máximo</a>. Esse parâmetro é ignorado no Windows XP e no Windows Server 2003. Diferentemente da API não gerenciada, <strong>IndexKeyMost ()</strong> (JET_bitIndexKeyMost) não é necessária, ela será adicionada automaticamente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></td>
<td>Obtém ou define o comprimento máximo, em bytes, de cada coluna a ser armazenada no índice.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></td>
<td>Obtém ou define o número de colunas condicionais.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335157(v=exchg.10).md">erra</a></td>
<td>Obtém ou define o código de erro da criação deste índice.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335119(v=exchg.10).md">grbit</a></td>
<td>Obtém ou define as opções de criação de índice.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335159(v=exchg.10).md">pidxUnicode</a></td>
<td>Obtém ou define as opções de comparação Unicode opcionais.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335120(v=exchg.10).md">pSpaceHints</a></td>
<td>Obtém ou define as dicas de alocação, manutenção e uso de espaço.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></td>
<td>Obtém ou define as colunas condicionais opcionais.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335121(v=exchg.10).md">szIndexName</a></td>
<td>Obtém ou define o nome do índice a ser criado.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335161(v=exchg.10).md">szKey</a></td>
<td>Obtém ou define a descrição da chave de índice. Essa é uma cadeia de caracteres dupla com terminação nula de tokens delimitados por nulo. Cada token tem o formato [Direction-especificador] [nome-da-coluna], onde a especificação de direção é &quot; + &quot; ou &quot; - &quot; . por exemplo, um szKey de &quot; + abc\0-def\0 + ghi\0 &quot; será indexado nas três colunas &quot; ABC &quot; (em ordem crescente), &quot; Def &quot; (em ordem decrescente) e &quot; GHI &quot; (em ordem crescente).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335162(v=exchg.10).md">ulDensity</a></td>
<td>Obtém ou define a densidade do índice.</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe JET_INDEXCREATE](./jet-indexcreate-class.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
