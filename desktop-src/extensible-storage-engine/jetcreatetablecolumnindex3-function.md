---
description: 'Saiba mais sobre: Função JetCreateTableColumnIndex3'
title: Função JetCreateTableColumnIndex3
TOCTitle: JetCreateTableColumnIndex3 Function
ms:assetid: c1a1b091-b4a6-4cdc-a0ea-af21c1462449
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294079(v=EXCHG.10)
ms:contentKeyID: 32765694
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndex3
- JetCreateTableColumnIndex3W
- JetCreateTableColumnIndex3A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b1e22b8816f3083fdf3cf623107197bc8a06883
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985939"
---
# <a name="jetcreatetablecolumnindex3-function"></a>Função JetCreateTableColumnIndex3


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetcreatetablecolumnindex3-function"></a>Função JetCreateTableColumnIndex3

A **função JetCreateTableColumnIndex3** cria uma tabela em um banco de dados ESE com um conjunto inicial de índices e um conjunto inicial de colunas de uma matriz de JET_TABLECREATE3 [estruturas.](./jet-tablecreate3-structure.md) A [JET_TABLECREATE3](./jet-tablecreate3-structure.md) estrutura permite que uma função de retorno de chamada seja especificada.

**Windows 7:** **JetCreateTableColumnIndex3** é introduzido no sistema operacional Windows 7.

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex3(
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

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errCallbackNotResolved</p> | <p>Não foi possível resolver a função de retorno de chamada. A DLL pode não ter sido encontrada ou a função na DLL pode não ter sido encontrada. Com o log suficiente habilitado, o log de eventos fornecerá mais detalhes.</p> | 
| <p>JET_errCannotIndex</p> | <p>Foi feita uma tentativa de indexar em uma coluna Escrow-update ou SLV (observe que as colunas SLV foram preterida).</p> | 
| <p>JET_errCannotNestDDL</p> | <p>Se ptablecreate- grbit especificar JET_bitTableCreateTemplateTable, mas &gt; ptablecreate- &gt; szTemplateTableName for definido como NULL.</p> | 
| <p>JET_errColumnDuplicate</p> | <p>Já existe uma coluna.</p> | 
| <p>JET_errColumnNotFound</p> | <p>Foi feita uma tentativa de indexar em uma coluna inexistente. Tentar indexar condicionalmente em uma coluna inexistente também pode produzir esse erro.</p> | 
| <p>JET_errColumnRedundant</p> | <p>Foi feita uma tentativa de adicionar uma coluna redundante. Não deve haver mais de uma coluna de decremento automático e não mais de uma coluna de versão por tabela.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Esse erro será retornado se o <strong>membro ulDensity</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for definido como um número menor que 20 ou mais de 100.</p> | 
| <p>JET_errDDLNotInheritable</p> | <p>Significa que a tabela nomeada no membro <strong>szTemplateTableName</strong> da estrutura <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> não foi marcada como uma tabela de modelo (ou seja, essa tabela não tinha JET_bitTableCreateTemplateTable definida).</p> | 
| <p>JET_errIndexDuplicate</p> | <p>Foi feita uma tentativa de definir dois índices idênticos.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Foi feita uma tentativa de especificar mais de um índice primário para uma tabela. Uma tabela deve ter exatamente um índice primário. Se nenhum índice primário for especificado, o mecanismo de banco de dados criará um de forma transparente.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Uma definição de índice inválida foi especificada. A seguir estão alguns dos possíveis motivos para receber esse erro:</p><ul><li><p>Um índice primário é condicional (ou seja, o <strong>membro grbit</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem JET_bitIndexPrimary definido e o membro <strong>cConditionalColumn</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é maior que zero).</p></li><li><p>Windows Server 2003 e versões posteriores do Windows. Tentar criar um índice de tupla com limites de tupla, mas sem passar o membro <strong>ptuplelimits</strong> na estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (ou seja, o <strong>membro grbit</strong> da estrutura JET_INDEXCREATE2 tem JET_bitIndexTupleLimits definido, mas o ponteiro <strong>ptuplelimits</strong> é NULL).</p></li><li><p>Passando uma definição de chave inválida no <strong>membro szKey</strong> da <a href="gg294082(v=exchg.10).md">estrutura JET_INDEXCREATE2</a> dados. Consulte <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> para uma discussão sobre definições válidas.</p></li><li><p>Definir o <strong>membro cbVarSegMac</strong> <a href="gg294082(v=exchg.10).md">no JET_INDEXCREATE2</a> ser maior que JET_cbPrimaryKeyMost (para um índice primário) ou maior que JET_cbSecondaryKeyMost (para um índice secundário).</p></li><li><p>Passando uma combinação inválida para um índice Unicode definido pelo usuário (um que tem o bit JET_bitIndexUnicode definido no <strong>membro grbit</strong> do <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>). Algumas causas comuns incluem o <strong>membro pidxunicode</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é NULL ou o LCID especificado na estrutura <strong>pidxunicode</strong> é inválido.</p></li><li><p>Especificando uma coluna com vários valores para um índice primário.</p></li><li><p>Tentando indexar muitas colunas condicionais. O <strong>membro cConditionalColumn</strong> da <a href="gg294082(v=exchg.10).md">estrutura JET_INDEXCREATE2</a> não deve ser maior que JET_ccolKeyMost.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Windows XP e versões posteriores Windows. Uma <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> estrutura foi especificada e seus limites não são suportados. Consulte a seção de comentários da estrutura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> dados.</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Windows XP e versões posteriores Windows. Um índice de tupla não pode ser exclusivo (ou seja, o <em>membro grbit</em> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não deve ter JET_bitIndexPrimary e JET_bitIndexUnique definidos).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Windows XP e versões posteriores Windows. Um índice de tupla só pode estar sobre uma única coluna (ou seja, se o membro <strong>grbit</strong> <a href="gg294082(v=exchg.10).md">da</a> estrutura JET_INDEXCREATE2 tiver JET_bitIndexTuples definido e o membro <strong>szKey</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> especificar mais de uma coluna).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Windows XP e versões posteriores Windows. Um índice de tupla não pode ser um índice primário (ou seja, o <strong>membro grbit</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não deve ter JET_bitIndexPrimary e JET_bitIndexTuples definidos).</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Windows XP e versões posteriores Windows. Um índice de tupla só pode estar em um texto ou coluna Unicode. Uma tentativa de indexar outras colunas (como colunas binárias) resultará em JET_errIndexTuplesTextColumnsOnly.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Windows XP e versões posteriores Windows. Um índice de tupla não permite que <strong>o membro cbVarSegMac</strong> <a href="gg294082(v=exchg.10).md">da estrutura JET_INDEXCREATE2</a> seja definido.</p> | 
| <p>JET_errInTransaction</p> | <p>Foi feita uma tentativa de criar um índice sem informações de versão durante uma transação.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>O <strong>membro cp</strong> da estrutura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> não foi definido como uma página de código válida. Os únicos valores válidos para colunas de texto são inglês (1252) e Unicode (1200). Um valor de 0 significa que o padrão será usado (inglês, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>O <strong>membro coltyp</strong> da <a href="gg269252(v=exchg.10).md">estrutura JET_COLUMNCREATE</a> não foi definido como um tipo de coluna válido.</p> | 
| <p>JET_errInvalidCreateIndex</p> | <p>Veja a seguir alguns motivos pelos quais esse erro pode ocorrer:</p><ul><li><p>O <strong>membro rgindexcreate</strong> da <a href="gg269203(v=exchg.10).md">estrutura JET_TABLECREATE2</a> foi definido como NULL.</p></li><li><p>O <strong>membro rgcolumncreate</strong> da estrutura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> foi definido como NULL.</p></li><li><p>O <strong>membro cbStruct</strong> de uma <a href="gg294082(v=exchg.10).md">estrutura JET_INDEXCREATE2</a> não foi definido como um valor válido.</p></li></ul> | 
| <p>JET_errInvalidgrbit</p> | <p>Uma combinação inválida de <strong>membros grbit</strong> foi especificada no <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a>.</p><p>A definição de índice é inválida porque o <strong>membro grbit</strong> contém valores inconsistentes. Veja a seguir alguns motivos possíveis:</p><ul><li><p>Um índice primário tinha um bit de ignorar especificado (ou seja, JET_bitIndexPrimary foi passado com JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull ou JET_bitIndexIgnoreFirstNull).</p></li><li><p>Um índice vazio não ignora quaisquer membros nulos (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem JET_bitIndexEmpty definido, mas não tem JET_bitIndexIgnoreAnyNull definido).</p></li><li><p>Passando uma estrutura de <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> com um membro <strong>grbit</strong> inválido.</p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>Uma LCID (identificação de localidade) inválida foi passada (por meio do membro <strong>LCID</strong> da estrutura de <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> que é apontada pelo membro <strong>pidxunicode</strong> na estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ou pelo campo <strong>LCID</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um parâmetro inválido foi fornecido. Estes são alguns motivos possíveis:</p><ul><li><p>O membro <strong>rgcolumncreate</strong> da estrutura de <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> é nulo.</p></li><li><p>O membro <strong>cbStruct</strong> de uma das estruturas de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> dadas no membro <strong>rgcolumncreate</strong> da estrutura de <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> não foi definido como sizeof (JET_COLUMNCREATE).</p></li><li><p>O membro <strong>cbKey</strong> de uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é definido como zero.</p></li><li><p>O membro <strong>cbStruct</strong> de uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não está definido como sizeof (JET_INDEXCREATE2).</p></li></ul> | 
| <p>JET_errRecordTooBig</p> | <p>O registro é muito grande. A soma do membro <strong>cbMax</strong> da estrutura de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> para todas as colunas fixas não deve exceder um determinado valor.</p> | 
| <p>JET_errTableDuplicate</p> | <p>A tabela já existe.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Foi feita uma tentativa de adicionar muitas colunas à tabela. Uma tabela não pode ter mais de JET_ccolFixedMost colunas fixas, não mais do que JET_ccolVarMost colunas de comprimento variável e não mais do que JET_ccolTaggedMost colunas marcadas.</p> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Ocorreu um erro ao tentar normalizar uma coluna Unicode. Isso pode ser causado pela execução de recursos do sistema.</p> | 
| <p>JET_errSpaceHintsInvalid</p> | <p>Um elemento da estrutura de dicas de espaço JET não estava correto ou é acionável.</p> | 



#### <a name="remarks"></a>Comentários

O nome **JetCreateTableColumnIndex3** vem da ordem de criação dos objetos: ele primeiro cria uma tabela, colunas e, finalmente, índices. **JetCreateTableColumnIndex3** cria uma tabela com um conjunto inicial de colunas e índices. Colunas e índices adicionais podem ser adicionados e removidos dinamicamente com [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md)e [JetDeleteIndex](./jetdeleteindex-function.md).

Assim como o [JetOpenTable](./jetopentable-function.md), quando o aplicativo é feito usando a *tabelaid* retornada, ele normalmente deve ser fechado com [JetCloseTable](./jetclosetable-function.md).

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista ou Windows XP.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008 ou Windows server 2003.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetCreateTableColumnIndex3W</strong> (Unicode) e <strong>JetCreateTableColumnIndex3A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

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
