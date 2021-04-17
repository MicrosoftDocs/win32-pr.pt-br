---
description: 'Saiba mais sobre: função JetCreateTableColumnIndex4W'
title: Função JetCreateTableColumnIndex4W
TOCTitle: JetCreateTableColumnIndex4W Function
ms:assetid: 5a74b397-dfb4-4a1d-807b-284329239bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835042(v=EXCHG.10)
ms:contentKeyID: 49894664
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateTableColumnIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 26ebdb8cf62123febe2d44b5a638c285c180062c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766445"
---
# <a name="jetcreatetablecolumnindex4w-function"></a>Função JetCreateTableColumnIndex4W


_**Aplica-se a:** Windows | Windows Server_

A função **JetCreateTableColumnIndex4W** cria uma tabela em um ESE (mecanismo de armazenamento extensível) (banco de dados com um conjunto inicial de índices e um conjunto inicial de colunas de uma matriz de estruturas de [JET_TABLECREATE3](./jet-tablecreate3-structure.md) . A estrutura de [JET_TABLECREATE3](./jet-tablecreate3-structure.md) permite que uma função de retorno de chamada seja especificada.

A função **JetCreateTableColumnIndex4W** foi introduzida no sistema operacional Windows 8.

``` c++
JET_ERR JET_API JetCreateTableColumnIndex4W(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in_out      JET_TABLECREATE3* ptablecreate
);
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*DBID*

O identificador de banco de dados a ser usado para a chamada à API.

*ptablecreate*

Um ponteiro para uma estrutura de [JET_TABLECREATE3](./jet-tablecreate3-structure.md) que define a tabela a ser criada. Consulte [JET_TABLECREATE3](./jet-tablecreate3-structure.md) para obter mais detalhes.

### <a name="return-value"></a>Retornar valor

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno listados na tabela a seguir. Para obter mais informações sobre os possíveis erros de ESE (Extensible Storage enginge), consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código de retorno</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>A operação foi concluída com sucesso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCallbackNotResolved</p></td>
<td><p>A função de retorno de chamada não pôde ser resolvida. A DLL pode não ter sido encontrada ou a função na DLL pode não ter sido encontrada. Com o registro em log suficiente habilitado, o log de eventos fornecerá mais detalhes.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotIndex</p></td>
<td><p>Foi feita uma tentativa de indexar uma coluna de atualização de caução ou SLV (Observe que as colunas SLV foram preteridas).</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotNestDDL</p></td>
<td><p>Retornado se o parâmetro <em>ptablecreate- &gt; grbit</em> especifica o valor JET_bitTableCreateTemplateTable, mas o parâmetro <em>ptablecreate- &gt; szTemplateTableName</em> está definido como NULL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnDuplicate</p></td>
<td><p>Já existe uma coluna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Foi feita uma tentativa de indexar uma coluna inexistente. Uma tentativa de indexar condicionalmente uma coluna inexistente também pode produzir esse erro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnRedundant</p></td>
<td><p>Foi feita uma tentativa de adicionar uma coluna redundante. Não deve existir mais de uma coluna de incremento automático e não existe mais de uma coluna de versão por tabela.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid</p></td>
<td><p>Esse erro será retornado se o membro <strong>ulDensity</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for definido como um número inferior a 20 ou maior que 100.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDDLNotInheritable</p></td>
<td><p>Significa que a tabela nomeada no membro <strong>szTemplateTableName</strong> da estrutura de <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> não foi marcada como uma tabela de modelo (ou seja, essa tabela não tinha o valor de parâmetro JET_bitTableCreateTemplateTable definido).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexDuplicate</p></td>
<td><p>Foi feita uma tentativa de definir dois índices idênticos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexHasPrimary</p></td>
<td><p>Foi feita uma tentativa de especificar mais de um índice primário para uma tabela. Uma tabela deve ter exatamente um índice primário. Se nenhum índice primário for especificado, o mecanismo de banco de dados criará de forma transparente um.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>Uma definição de índice inválida foi especificada. Estes são alguns dos motivos possíveis para esse erro:</p>
<ul>
<li><p>Um índice primário é condicional (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem o valor JET_bitIndexPrimary definido e o membro <strong>cConditionalColumn</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é maior que zero).</p></li>
<li><p>Aplica-se às versões do sistema operacional Windows Server a partir do Windows Server 2003. Uma tentativa de criar um índice de tupla com limites de tupla, mas sem passar o membro <strong>ptuplelimits</strong> na estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (ou seja, o membro <strong>grbit</strong> da estrutura de <strong>JET_INDEXCREATE2</strong> tem JET_bitIndexTupleLimits valor definido, mas o ponteiro <strong>ptuplelimits</strong> é nulo).</p></li>
<li><p>Passando uma definição de chave inválida no membro <strong>szKey</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> . Para obter informações sobre definições válidas, consulte <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</p></li>
<li><p>Definir o membro <strong>cbVarSegMac</strong> em <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ser maior que o valor de JET_cbPrimaryKeyMost (para um índice primário) ou maior que o valor de JET_cbSecondaryKeyMost (para um índice secundário).</p></li>
<li><p>Passando uma combinação inválida para um índice Unicode definido pelo usuário (um que tenha o bit de valor JET_bitIndexUnicode definido no membro <strong>grbit</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ). Algumas causas comuns incluem o membro <strong>pidxunicode</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é NULL ou o LCID especificado na estrutura <strong>pidxunicode</strong> é inválido.</p></li>
<li><p>Especificando uma coluna com valores de um índice primário.</p></li>
<li><p>Tentando indexar muitas colunas condicionais. O membro <strong>cConditionalColumn</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não deve ser maior que <strong>JET_ccolKeyMost</strong>.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Aplica-se às versões do Windows a partir do Windows XP. Uma estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> foi especificada e não há suporte para seus limites. Para obter mais informações, consulte a seção comentários da estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesNonUniqueOnly</p></td>
<td><p>Aplica-se às versões do Windows a partir do Windows XP. Um índice de tupla não pode ser exclusivo (ou seja, o membro <em>grbit</em> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não deve ter os valores JET_bitIndexPrimary e JET_bitIndexUnique definidos).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesOneColumnOnly</p></td>
<td><p>Aplica-se às versões do Windows a partir do Windows XP. Um índice de tupla só pode ser sobre uma única coluna (ou seja, se o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tiver JET_bitIndexTuples valor definido e o membro <strong>szKey</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> especificar mais de uma coluna).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesSecondaryIndexOnly</p></td>
<td><p>Aplica-se às versões do Windows a partir do Windows XP. Um índice de tupla não pode ser um índice primário (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não deve ter JET_bitIndexPrimary e JET_bitIndexTuples definido).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesTextColumnsOnly</p></td>
<td><p>Aplica-se às versões do Windows a partir do Windows XP. Um índice de tupla só pode estar em uma coluna de texto ou Unicode. Uma tentativa de indexar outras colunas (como colunas binárias) resultará em um código de resposta JET_errIndexTuplesTextColumnsOnly.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed</p></td>
<td><p>Aplica-se às versões do Windows a partir do Windows XP. Um índice de tupla não permite que o membro <strong>cbVarSegMac</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> seja definida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>Foi feita uma tentativa de criar um índice sem informações de versão em uma transação.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>O membro <strong>CP</strong> da estrutura de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> não foi definido como uma página de código válida. Os únicos valores válidos para colunas de texto são Inglês (1252) e Unicode (1200). Um valor de 0 significa que o padrão será usado (Inglês, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>O membro <strong>coltyp</strong> da estrutura de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> não foi definido como um tipo de coluna válido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCreateIndex</p></td>
<td><p>A seguir estão alguns motivos pelos quais esse erro pode ocorrer:</p>
<ul>
<li><p>O membro <strong>rgindexcreate</strong> da estrutura de <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> foi definido como nulo.</p></li>
<li><p>O membro <strong>rgcolumncreate</strong> da estrutura de <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> foi definido como nulo.</p></li>
<li><p>O membro <strong>cbStruct</strong> de uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não foi definido como um valor válido.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Uma combinação inválida de membros <strong>grbit</strong> foi especificada na estrutura de <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> .</p>
<p>A definição do índice é inválida porque o membro <strong>grbit</strong> contém valores inconsistentes. Estes são alguns motivos possíveis:</p>
<ul>
<li><p>Um índice primário tinha um bit de ignorar especificado (ou seja, JET_bitIndexPrimary valor foi passado com os valores de JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull ou JET_bitIndexIgnoreFirstNull).</p></li>
<li><p>Um índice vazio não ignora quaisquer membros nulos (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem o valor de JET_bitIndexEmpty definido, mas não tem JET_bitIndexIgnoreAnyNull valor definido).</p></li>
<li><p>Passando uma estrutura de <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> com um membro <strong>grbit</strong> inválido.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Uma LCID (identificação de localidade) inválida foi passada (por meio do membro <strong>LCID</strong> da estrutura de <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> que o membro <strong>pidxunicode</strong> na estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> aponta para ou por meio do campo <strong>LCID</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um parâmetro inválido foi fornecido. Estes são alguns motivos possíveis:</p>
<ul>
<li><p>O membro <strong>rgcolumncreate</strong> da estrutura de <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> é nulo.</p></li>
<li><p>O membro <strong>cbStruct</strong> de uma das estruturas de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> dadas no membro <strong>rgcolumncreate</strong> da estrutura de <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> não foi definido como sizeof (JET_COLUMNCREATE).</p></li>
<li><p>O membro <strong>cbKey</strong> de uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é definido como zero.</p></li>
<li><p>O membro <strong>cbStruct</strong> de uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não está definido como sizeof (JET_INDEXCREATE2).</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errRecordTooBig</p></td>
<td><p>O registro é muito grande. A soma do membro <strong>cbMax</strong> da estrutura de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> para todas as colunas fixas não deve exceder um determinado valor.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableDuplicate</p></td>
<td><p>A tabela já existe.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyColumns</p></td>
<td><p>Foi feita uma tentativa de adicionar muitas colunas à tabela. Uma tabela não pode ter mais de <strong>JET_ccolFixedMost</strong> colunas fixas, não mais do que <strong>JET_ccolVarMost</strong> colunas de comprimento variável e não mais do que <strong>JET_ccolTaggedMost</strong> colunas marcadas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeTranslationFail</p></td>
<td><p>Ocorreu um erro quando foi feita uma tentativa de normalizar uma coluna Unicode. Isso pode ser causado pela execução de recursos do sistema.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSpaceHintsInvalid</p></td>
<td><p>Um elemento da estrutura de dicas de espaço JET não estava correto ou é acionável.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Comentários

A função **JetCreateTableColumnIndex4W** cria uma tabela com um conjunto inicial de colunas e índices. Colunas e índices adicionais podem ser adicionados e removidos dinamicamente por meio das funções [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), [JetCreateIndex4W](./jetcreateindex4w-function.md)e [JetDeleteIndex](./jetdeleteindex-function.md) .

Assim como acontece com a função [JetOpenTable](./jetopentable-function.md) , quando o aplicativo é feito usando o *TableID* retornado, a função [JetCloseTable](./jetclosetable-function.md) deve fechar o aplicativo.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2012.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Biblioteca</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Confira também

[JET_CBTYP](./jet-cbtyp.md)  
[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_INDEXCREATE2](./jet-indexcreate2-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TABLECREATE3](./jet-tablecreate3-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetCreateIndex3](./jetcreateindex3-function.md)  
[JetCreateTable](./jetcreatetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetDeleteColumn](./jetdeletecolumn-function.md)  
[JetDeleteColumn2](./jetdeletecolumn2-function.md)
