---
description: 'Saiba mais sobre: Função JetCreateTableColumnIndex4W'
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
ms.openlocfilehash: 2e0ecb22fe9936c9843c603211b0594599de7fcd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479182"
---
# <a name="jetcreatetablecolumnindex4w-function"></a>Função JetCreateTableColumnIndex4W


_**Aplica-se a:** Windows | Windows Servidor_

A **função JetCreateTableColumnIndex4W** cria uma tabela em um banco de dados ESE (Extensible Armazenamento Engine com um conjunto inicial de índices e um conjunto inicial de colunas de uma matriz [de](./jet-tablecreate3-structure.md) JET_TABLECREATE3 estruturas). A [JET_TABLECREATE3](./jet-tablecreate3-structure.md) estrutura permite que uma função de retorno de chamada seja especificada.

A **função JetCreateTableColumnIndex4W** foi introduzida no Windows 8 operacional.

``` c++
JET_ERR JET_API JetCreateTableColumnIndex4W(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in_out      JET_TABLECREATE3* ptablecreate
);
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto de sessão do banco de dados a ser usado para a chamada à API.

*Dbid*

O identificador de banco de dados a ser usado para a chamada à API.

*ptablecreate*

Um ponteiro para uma [JET_TABLECREATE3](./jet-tablecreate3-structure.md) que define a tabela a ser criada. Consulte [JET_TABLECREATE3](./jet-tablecreate3-structure.md) para obter mais detalhes.

### <a name="return-value"></a>Valor retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno listados na tabela a seguir. Para obter mais informações sobre os possíveis erros de ESE (Extensible Armazenamento Enginge), consulte [Extensible Armazenamento Engine Error](./extensible-storage-engine-errors.md) [Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errCallbackNotResolved</p> | <p>Não foi possível resolver a função de retorno de chamada. A DLL pode não ter sido encontrada ou a função na DLL pode não ter sido encontrada. Com o log suficiente habilitado, o log de eventos fornecerá mais detalhes.</p> | 
| <p>JET_errCannotIndex</p> | <p>Foi feita uma tentativa de indexar em uma coluna Escrow-update ou SLV (observe que as colunas SLV foram preterida).</p> | 
| <p>JET_errCannotNestDDL</p> | <p>Retornado se o <em>parâmetro ptablecreate-grbit &gt; </em> especificar o valor JET_bitTableCreateTemplateTable, mas o parâmetro <em>ptablecreate-szTemplateTableName &gt; </em> for definido como nulo.</p> | 
| <p>JET_errColumnDuplicate</p> | <p>Já existe uma coluna.</p> | 
| <p>JET_errColumnNotFound</p> | <p>Foi feita uma tentativa de indexar em uma coluna inexistente. Uma tentativa de indexar condicionalmente em uma coluna inexistente também pode produzir esse erro.</p> | 
| <p>JET_errColumnRedundant</p> | <p>Foi feita uma tentativa de adicionar uma coluna redundante. Não deve existir mais de uma coluna de autoincremento e não deve existir mais de uma coluna de versão por tabela.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Esse erro será retornado se o <strong>membro ulDensity</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for definido como um número menor que 20 ou mais de 100.</p> | 
| <p>JET_errDDLNotInheritable</p> | <p>Significa que a tabela nomeada no membro <strong>szTemplateTableName</strong> da estrutura JET_TABLECREATE3 não foi marcada como uma tabela de modelo (ou seja, essa tabela não tinha o valor do parâmetro <a href="gg269264(v=exchg.10).md">JET_bitTableCreateTemplateTable</a> definido).</p> | 
| <p>JET_errIndexDuplicate</p> | <p>Foi feita uma tentativa de definir dois índices idênticos.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Foi feita uma tentativa de especificar mais de um índice primário para uma tabela. Uma tabela deve ter exatamente um índice primário. Se nenhum índice primário for especificado, o mecanismo de banco de dados criará um de forma transparente.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Uma definição de índice inválida foi especificada. Veja a seguir alguns dos possíveis motivos para esse erro:</p><ul><li><p>Um índice primário é condicional (ou seja, o membro <strong>grbit</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem o valor JET_bitIndexPrimary definido e o membro <strong>cConditionalColumn</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é maior que zero).</p></li><li><p>Aplica-se a versões do sistema operacional Windows Server a partir do Windows Server 2003. Uma tentativa de criar um índice de tupla com limites de tupla, mas sem passar o membro <strong>ptuplelimits</strong> na estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (ou seja, o <strong>membro grbit</strong> da estrutura <strong>JET_INDEXCREATE2</strong> tem um valor JET_bitIndexTupleLimits definido, mas o ponteiro <strong>ptuplelimits</strong> é nulo).</p></li><li><p>Passando uma definição de chave inválida no <strong>membro szKey</strong> da <a href="gg294082(v=exchg.10).md">estrutura JET_INDEXCREATE2</a> dados. Para obter informações sobre definições válidas, <a href="gg294082(v=exchg.10).md">consulte JET_INDEXCREATE2</a>.</p></li><li><p>Definir o <strong>membro cbVarSegMac</strong> <a href="gg294082(v=exchg.10).md">no JET_INDEXCREATE2</a> como maior que o valor JET_cbPrimaryKeyMost (para um índice primário) ou maior que o valor JET_cbSecondaryKeyMost (para um índice secundário).</p></li><li><p>Passando uma combinação inválida para um índice Unicode definido pelo usuário (um que tem o bit de valor JET_bitIndexUnicode definido no <strong>membro grbit</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2).</a> Algumas causas comuns incluem <strong>o membro pidxunicode</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é nulo ou o LCID especificado na estrutura <strong>pidxunicode</strong> é inválido.</p></li><li><p>Especificando uma coluna com vários valores para um índice primário.</p></li><li><p>Tentando indexar muitas colunas condicionais. O <strong>membro cConditionalColumn</strong> da <a href="gg294082(v=exchg.10).md">estrutura JET_INDEXCREATE2</a> não deve ser maior que <strong>JET_ccolKeyMost</strong>.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Aplica-se a versões do Windows começando com Windows XP. Uma <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> estrutura foi especificada e seus limites não são suportados. Para obter mais informações, consulte a seção de comentários da <a href="gg269207(v=exchg.10).md">estrutura JET_TUPLELIMITS</a> dados.</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Aplica-se a versões do Windows começando com Windows XP. Um índice de tupla não pode ser exclusivo (ou seja, o <em>membro grbit</em> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não deve ter os valores JET_bitIndexPrimary e JET_bitIndexUnique definidos).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Aplica-se a versões do Windows começando com Windows XP. Um índice de tupla só poderá ser sobre uma única coluna (ou seja, se o membro <strong>grbit</strong> <a href="gg294082(v=exchg.10).md">da</a> estrutura JET_INDEXCREATE2 tiver um valor definido JET_bitIndexTuples e o membro <strong>szKey</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> especificar mais de uma coluna).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Aplica-se a versões do Windows começando com Windows XP. Um índice de tupla não pode ser um índice primário (ou seja, o <strong>membro grbit</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não deve ter JET_bitIndexPrimary e JET_bitIndexTuples definidos).</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Aplica-se a versões do Windows começando com Windows XP. Um índice de tupla só pode estar em um texto ou coluna Unicode. Uma tentativa de indexar outras colunas (como colunas binárias) resultará em um JET_errIndexTuplesTextColumnsOnly de resposta.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Aplica-se a versões do Windows começando com Windows XP. Um índice de tupla não permite que <strong>o membro cbVarSegMac</strong> <a href="gg294082(v=exchg.10).md">da estrutura JET_INDEXCREATE2</a> seja definido.</p> | 
| <p>JET_errInTransaction</p> | <p>Foi feita uma tentativa de criar um índice sem informações de versão durante uma transação.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>O <strong>membro cp</strong> da estrutura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> não foi definido como uma página de código válida. Os únicos valores válidos para colunas de texto são inglês (1252) e Unicode (1200). Um valor de 0 significa que o padrão será usado (inglês, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>O <strong>membro coltyp</strong> da <a href="gg269252(v=exchg.10).md">estrutura JET_COLUMNCREATE</a> não foi definido como um tipo de coluna válido.</p> | 
| <p>JET_errInvalidCreateIndex</p> | <p>Veja a seguir alguns motivos pelos quais esse erro pode ocorrer:</p><ul><li><p>O <strong>membro rgindexcreate</strong> da estrutura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> foi definido como nulo.</p></li><li><p>O <strong>membro rgcolumncreate</strong> da estrutura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> foi definido como nulo.</p></li><li><p>O <strong>membro cbStruct</strong> de uma <a href="gg294082(v=exchg.10).md">estrutura JET_INDEXCREATE2</a> não foi definido como um valor válido.</p></li></ul> | 
| <p>JET_errInvalidgrbit</p> | <p>Uma combinação inválida de <strong>membros grbit</strong> foi especificada na <a href="gg269264(v=exchg.10).md">estrutura JET_TABLECREATE3</a> dados.</p><p>A definição de índice é inválida porque o <strong>membro grbit</strong> contém valores inconsistentes. Veja a seguir alguns motivos possíveis:</p><ul><li><p>Um índice primário tinha um bit de ignorar especificado (ou seja, JET_bitIndexPrimary valor foi passado com os valores JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull ou JET_bitIndexIgnoreFirstNull).</p></li><li><p>Um índice vazio não ignora quaisquer membros nulos (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem o valor de JET_bitIndexEmpty definido, mas não tem JET_bitIndexIgnoreAnyNull valor definido).</p></li><li><p>Passando uma estrutura de <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> com um membro <strong>grbit</strong> inválido.</p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>Uma LCID (identificação de localidade) inválida foi passada (por meio do membro <strong>LCID</strong> da estrutura de <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> que o membro <strong>pidxunicode</strong> na estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> aponta para ou por meio do campo <strong>LCID</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um parâmetro inválido foi fornecido. Estes são alguns motivos possíveis:</p><ul><li><p>O membro <strong>rgcolumncreate</strong> da estrutura de <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> é nulo.</p></li><li><p>O membro <strong>cbStruct</strong> de uma das estruturas de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> dadas no membro <strong>rgcolumncreate</strong> da estrutura de <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> não foi definido como sizeof (JET_COLUMNCREATE).</p></li><li><p>O membro <strong>cbKey</strong> de uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é definido como zero.</p></li><li><p>O membro <strong>cbStruct</strong> de uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não está definido como sizeof (JET_INDEXCREATE2).</p></li></ul> | 
| <p>JET_errRecordTooBig</p> | <p>O registro é muito grande. A soma do membro <strong>cbMax</strong> da estrutura de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> para todas as colunas fixas não deve exceder um determinado valor.</p> | 
| <p>JET_errTableDuplicate</p> | <p>A tabela já existe.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Foi feita uma tentativa de adicionar muitas colunas à tabela. Uma tabela não pode ter mais de <strong>JET_ccolFixedMost</strong> colunas fixas, não mais do que <strong>JET_ccolVarMost</strong> colunas de comprimento variável e não mais do que <strong>JET_ccolTaggedMost</strong> colunas marcadas.</p> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Ocorreu um erro quando foi feita uma tentativa de normalizar uma coluna Unicode. Isso pode ser causado pela execução de recursos do sistema.</p> | 
| <p>JET_errSpaceHintsInvalid</p> | <p>Um elemento da estrutura de dicas de espaço JET não estava correto ou é acionável.</p> | 



#### <a name="remarks"></a>Comentários

A função **JetCreateTableColumnIndex4W** cria uma tabela com um conjunto inicial de colunas e índices. Colunas e índices adicionais podem ser adicionados e removidos dinamicamente por meio das funções [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), [JetCreateIndex4W](./jetcreateindex4w-function.md)e [JetDeleteIndex](./jetdeleteindex-function.md) .

Assim como acontece com a função [JetOpenTable](./jetopentable-function.md) , quando o aplicativo é feito usando o *TableID* retornado, a função [JetCloseTable](./jetclosetable-function.md) deve fechar o aplicativo.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows 8.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2012.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



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
