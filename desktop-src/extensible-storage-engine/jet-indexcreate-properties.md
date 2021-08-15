---
description: 'Saiba mais sobre: JET_INDEXCREATE propriedades'
title: JET_INDEXCREATE propriedades
TOCTitle: JET_INDEXCREATE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_properties(v=EXCHG.10)
ms:contentKeyID: 55103645
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 0669d00b9c28e5299c5b9f55f0931ec7d22921eddad5e2b6b4876199057d111d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118254246"
---
# <a name="jet_indexcreate-properties"></a>JET_INDEXCREATE propriedades

Incluir membros protegidos  
Incluir membros herdados  

O [JET_INDEXCREATE](./jet-indexcreate-class.md) de dados expõe os membros a seguir.

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
<td>Obtém ou define o tamanho máximo permitida, em bytes, para chaves no índice. O tamanho máximo mínimo da chave com suporte é JET_cbKeyMostMin (255), que é o tamanho máximo da chave herdado. O tamanho máximo da chave depende do tamanho da página do banco de <a href="hh596135(v=exchg.10).md">dados DatabasePageSize</a>. O tamanho máximo da chave pode ser recuperado com <a href="dn351156(v=exchg.10).md">KeyMost.</a> Esse parâmetro é ignorado no Windows XP e Windows Server 2003. Ao contrário da API não gerenciamento, <strong>IndexKeyMost()</strong> (JET_bitIndexKeyMost) não é necessário, ela será adicionada automaticamente.</td>
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
<td><a href="dn335157(v=exchg.10).md">Err</a></td>
<td>Obtém ou define o código de erro da criação desse índice.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335119(v=exchg.10).md">grbit</a></td>
<td>Obtém ou define opções de criação de índice.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335159(v=exchg.10).md">pidxUnicode</a></td>
<td>Obtém ou define as opções opcionais de comparação unicode.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn335120(v=exchg.10).md">pSpaceHints</a></td>
<td>Obtém ou define dicas de alocação, manutenção e uso de espaço.</td>
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
<td>Obtém ou define a descrição da chave de índice. Essa é uma cadeia de caracteres terminada em nulo dupla de tokens delimitados por nulo. Cada token é do formato [direction-specifier][column-name], em que direction-specification é &quot; + &quot; ou &quot; - &quot; . por exemplo, uma szKey de &quot; +abc\0-def\0+gee\0 será indexada sobre as três &quot; colunas abc (em ordem &quot; &quot; crescente), def (em ordem decrescente) e &quot; &quot; &quot; gee (em ordem &quot; crescente).</td>
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

[JET_INDEXCREATE classe](./jet-indexcreate-class.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
