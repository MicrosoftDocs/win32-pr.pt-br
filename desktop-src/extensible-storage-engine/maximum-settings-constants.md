---
description: 'Saiba mais sobre: as constantes de configurações máximas'
title: Constantes de configurações máximas
TOCTitle: Maximum Settings Constants
ms:assetid: 1111051f-55af-4c33-be38-6a3973c2c815
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269189(v=EXCHG.10)
ms:contentKeyID: 32765492
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3754732e59c9a90c74366558d9904fc13376db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827275"
---
# <a name="maximum-settings-constants"></a>Constantes de configurações máximas


_**Aplica-se a:** Windows | Windows Server_

## <a name="maximum-settings-constants"></a>Constantes de configurações máximas

Essas constantes fornecem as configurações máximas que são permitidas em itens em um banco de dados ESE.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante/valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_BASE_NAME_LENGTH<br />
3</p></td>
<td><p>Define o comprimento do prefixo usado para nomear arquivos que são usados pelo mecanismo de banco de dados. Esse comprimento é aplicável ao nome definido para o parâmetro do sistema <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_MAX_COMPUTERNAME_LENGTH<br />
15</p></td>
<td><p>Define o comprimento máximo para <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbBookmarkMost<br />
256</p></td>
<td><p>O tamanho máximo padrão de um indicador. Isso é válido quando o tamanho da chave é deixado com seu valor padrão.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbBookmarkMostMost<br />
2000</p></td>
<td><p>O tamanho máximo de um indicador quando o ESENT é configurado para ter as maiores chaves possíveis.</p>
<p><strong>Windows 7:</strong> JET_cbBookmarkMostMost é introduzido no Windows 7.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbNameMost<br />
64</p></td>
<td><p>O comprimento máximo de um objeto, coluna, índice ou nome de propriedade.</p>
<p><strong>Observação</strong>  Se for Unicode, o valor será 128.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbFullNameMost<br />
255</p></td>
<td><p>O comprimento máximo de uma &quot; construção Name.Name.Name.. &quot; .</p>
<p><strong>Observação</strong>  Se for Unicode, o valor será 510.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbColumnLVPageOverhead<br />
82</p></td>
<td><p>Esse número pode ser usado para calcular a quantidade máxima de um BLOB que pode ser armazenado pelo mecanismo de banco de dados em uma única página de banco de dados. A fórmula tem tamanho máximo = JET_paramDatabasePageSize – JET_cbColumnLVPageOverhead.</p>
<p>Esse valor agora é obsoleto. O tamanho da parte de valor longo deve ser recuperado com o parâmetro JET_paramLVChunkSizeMost.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbColumnMost<br />
255</p></td>
<td><p>O tamanho máximo de dados de coluna de valor não longo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbLVDefaultValueMost<br />
255</p></td>
<td><p>O tamanho máximo de um valor padrão de coluna de valor longo (LongBinary ou LongText).</p></td>
</tr>
<tr class="even">
<td><p>JET_cbKeyMost<br />
255</p></td>
<td><p>O tamanho máximo padrão de uma chave de classificação ou de índice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbKeyMostMost<br />
2000</p></td>
<td><p>O tamanho máximo configurável de uma chave de classificação ou de índice para qualquer tamanho de página. (Consulte JET_INDEXCREATE2. cbKeyMost)</p>
<p><strong>Windows 7:</strong> JET_cbKeyMostMost é introduzido no sistema operacional Windows 7.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbKeyMost2KBytePage<br />
500</p></td>
<td><p>O tamanho máximo de configurável permitido para uma chave de índice em um banco de dados usando páginas de 2048 bytes. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter mais informações.</p>
<p><strong>Windows Vista:</strong> O JET_cbKeyMost2KBytePage é introduzido no sistema operacional Windows Vista.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbKeyMost4KBytePage<br />
1000</p></td>
<td><p>O tamanho máximo de configurável permitido para uma chave de índice em um banco de dados usando páginas de 4096 bytes. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter mais informações.</p>
<p><strong>Windows Vista:</strong> O JET_cbKeyMost4KBytePage é introduzido no Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbKeyMost8KBytePage<br />
2000</p></td>
<td><p>O tamanho máximo de configurável permitido para uma chave de índice em um banco de dados usando páginas de 8192 bytes. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter mais informações.</p>
<p><strong>Windows Vista:  </strong> JET_cbKeyMost8KBytePage é introduzido no Windows Vista</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbKeyMostMin<br />
255</p></td>
<td><p>O tamanho máximo permitido mínimo para uma chave de índice. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter mais informações.</p>
<p><strong>Windows Vista:  </strong> O JET_cbKeyMostMin é introduzido no Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbLimitKeyMost<br />
256</p></td>
<td><p>O tamanho máximo da chave quando a chave é formada usando um limite <em>grbit</em>, como JET_bitStrLimit, que é usado na função <a href="gg269329(v=exchg.10).md">JetMakeKey</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbPrimaryKeyMost<br />
255</p></td>
<td><p>O tamanho máximo do índice primário. Isso agora é obsoleto.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbSecondaryKeyMost<br />
255</p></td>
<td><p>O tamanho máximo do índice secundário. Isso agora é obsoleto.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ccolKeyMost<br />
12</p></td>
<td><p>O número máximo de componentes em uma chave de classificação ou de índice.</p>
<p><strong>Windows Vista:  </strong> No Windows Vista e versões posteriores do Windows, o valor é 16.</p></td>
</tr>
<tr class="even">
<td><p>JET_ccolMost<br />
0x0000fee0</p></td>
<td><p>O número máximo de colunas permitidas em uma tabela.</p>
<p><strong>Windows XP:  </strong> O valor 0x0000fee0 é usado no Windows XP e versões posteriores e posteriores do Windows</p>
<p><strong>Windows 2000:  </strong> O valor 0x00007ffe é usado no Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ccolFixedMost<br />
interrupção</p></td>
<td><p>O número máximo de colunas fixas permitidas em uma tabela, atualmente 127.</p></td>
</tr>
<tr class="even">
<td><p>JET_ccolVarMost<br />
0x00000080</p></td>
<td><p>O número máximo de colunas de comprimento variável que podem estar contidas em uma tabela, no momento, 128.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ccolTaggedMost<br />
(JET_ccolMost-0x000000FF)</p></td>
<td><p>O número máximo de colunas marcadas que podem estar contidas em uma tabela, no momento, 64993.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
</tbody>
</table>

