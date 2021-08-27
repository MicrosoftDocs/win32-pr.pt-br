---
description: 'Saiba mais sobre: função JetCreateTableColumnIndex'
title: Função JetCreateTableColumnIndex
TOCTitle: JetCreateTableColumnIndex Function
ms:assetid: 9192614b-20a6-40fb-906a-51fc057e7483
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269343(v=EXCHG.10)
ms:contentKeyID: 32765632
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndexA
- JetCreateTableColumnIndexW
- JetCreateTableColumnIndex
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b17fea6bc4ee4856c3cae653eb8f138156ce9927
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986009"
---
# <a name="jetcreatetablecolumnindex-function"></a>Função JetCreateTableColumnIndex


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetcreatetablecolumnindex-function"></a>Função JetCreateTableColumnIndex

A função **JetCreateTableColumnIndex** cria uma tabela em um banco de dados ESE com um conjunto inicial de índices e um conjunto inicial de colunas de uma matriz de estruturas de [JET_TABLECREATE](./jet-tablecreate-structure.md) . O nome **JetCreateTableColumnIndex** vem da ordem de criação dos objetos. Primeiro, ele cria uma tabela, colunas e, finalmente, índices.

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE* ptablecreate
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*DBID*

O identificador de banco de dados a ser usado para a chamada à API.

*ptablecreate*

Um ponteiro para uma estrutura de [JET_TABLECREATE](./jet-tablecreate-structure.md) que define a tabela a ser criada. Consulte [JET_TABLECREATE](./jet-tablecreate-structure.md) para obter mais detalhes.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errCallbackNotResolved</p> | <p>A função de retorno de chamada não pôde ser resolvida. A DLL pode não ter sido encontrada ou a função na DLL pode não ter sido encontrada. Com o registro em log suficiente habilitado, o log de eventos fornecerá mais detalhes.</p> | 
| <p>JET_errCannotIndex</p> | <p>Foi feita uma tentativa de indexar uma coluna de atualização de caução ou SLV (Observe que as colunas SLV foram preteridas).</p> | 
| <p>JET_errCannotNestDDL</p> | <p>Se ptablecreate- &gt; grbit especificar JET_bitTableCreateTemplateTable, mas ptablecreate- &gt; szTemplateTableName será definido como NULL.</p> | 
| <p>JET_errColumnDuplicate</p> | <p>Já existe uma coluna.</p> | 
| <p>JET_errColumnNotFound</p> | <p>Foi feita uma tentativa de indexar uma coluna não existente. A tentativa de indexar condicionalmente uma coluna não existente também pode produzir esse erro.</p> | 
| <p>JET_errColumnRedundant</p> | <p>Foi feita uma tentativa de adicionar uma coluna redundante. Não deve haver mais de uma coluna de incremento automático e não há mais de uma coluna de versão por tabela.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Esse erro será retornado se o membro <strong>ulDensity</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for definido como um número inferior a 20 ou maior que 100.</p> | 
| <p>JET_errDDLNotInheritable</p> | <p>Significa que a tabela nomeada no membro <strong>szTemplateTableName</strong> da estrutura de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> não foi marcada como uma tabela de modelo (ou seja, essa tabela não tinha JET_bitTableCreateTemplateTable definido).</p> | 
| <p>JET_errIndexDuplicate</p> | <p>Foi feita uma tentativa de definir dois índices idênticos.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Foi feita uma tentativa de especificar mais de um índice primário para uma tabela. Uma tabela deve ter exatamente um índice primário. Se nenhum índice primário for especificado, o mecanismo de banco de dados criará de forma transparente um.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Uma definição de índice inválida foi especificada. Alguns dos motivos possíveis para receber esse erro são:</p><ul><li><p>Um índice primário é condicional (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tem JET_bitIndexPrimary definido e o membro <strong>cConditionalColumn</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> é maior que zero).</p></li><li><p>Windows Server 2003 e posterior. Tentativa de criar um índice de tupla com limites de tupla, mas sem passar o membro <strong>ptuplelimits</strong> na estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tem JET_BITINDEXTUPLELIMITS definido, mas o ponteiro <strong>ptuplelimits</strong> é nulo).</p></li><li><p>Passando uma definição de chave inválida no membro <strong>szKey</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> . Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter uma discussão sobre definições válidas.</p></li><li><p>Definir o membro <strong>cbVarSegMac</strong> em <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ser maior que JET_cbPrimaryKeyMost (para um índice primário) ou maior que JET_cbSecondaryKeyMost (para um índice secundário).</p></li><li><p>Passando uma combinação inválida para um índice Unicode definido pelo usuário (um que tem o conjunto de bits JET_bitIndexUnicode no membro <strong>grbit</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>). Algumas causas comuns incluem o membro <strong>pidxunicode</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> é NULL ou o LCID especificado na estrutura <strong>pidxunicode</strong> é inválido.</p></li><li><p>Especificando uma coluna com valores múltiplos para um índice primário.</p></li><li><p>Tentando indexar muitas colunas condicionais. O membro <strong>cConditionalColumn</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> não deve ser maior que JET_ccolKeyMost.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Windows XP e posterior. Uma estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> foi especificada e não há suporte para seus limites. Consulte a seção comentários da estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Windows XP e posterior. Um índice de tupla não pode ser exclusivo (ou seja, o membro <em>grbit</em> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> não deve ter JET_bitIndexPrimary e JET_bitIndexUnique definido).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Windows XP e posterior. Um índice de tupla só pode ser sobre uma única coluna (ou seja, se o membro <strong>grbit</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiver JET_bitIndexTuples definido e o membro <strong>szKey</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> especificar mais de uma coluna).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Windows XP e posterior. Um índice de tupla não pode ser um índice primário (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> não deve ter JET_bitIndexPrimary e JET_bitIndexTuples definido).</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Windows XP e posterior. Um índice de tupla só pode estar em uma coluna de texto ou Unicode. Uma tentativa de indexar outras colunas (como colunas binárias) resultará em JET_errIndexTuplesTextColumnsOnly.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Windows XP e posterior. Um índice de tupla não permite que o membro <strong>cbVarSegMac</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> seja definida.</p> | 
| <p>JET_errInTransaction</p> | <p>Foi feita uma tentativa de criar um índice sem informações de versão em uma transação.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>O membro <strong>CP</strong> da estrutura de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> não foi definido como uma página de código válida. Os únicos valores válidos para colunas de texto são Inglês (1252) e Unicode (1200). Um valor de 0 significa que o padrão será usado (Inglês, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>O membro <strong>coltyp</strong> da estrutura de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> não foi definido como um tipo de coluna válido.</p> | 
| <p>JET_errInvalidCreateIndex</p> | <p>Alguns dos motivos pelos quais esse erro pode ocorrer:</p><ul><li><p>O membro <strong>rgindexcreate</strong> da estrutura de <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> foi definido como nulo.</p></li><li><p>O membro <strong>rgcolumncreate</strong> da estrutura de <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> foi definido como nulo.</p></li><li><p>O membro <strong>cbStruct</strong> de uma estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> não foi definido como um valor válido.</p></li></ul> | 
| <p>JET_errInvalidgrbit</p> | <p>Uma combinação inválida de membros <strong>grbit</strong> foi especificada em <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</p><p>A definição do índice é inválida porque o membro <strong>grbit</strong> contém valores inconsistentes. Alguns motivos possíveis são:</p><ul><li><p>Um índice primário tinha um bit de ignorar especificado (ou seja, JET_bitIndexPrimary foi passado com JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull ou JET_bitIndexIgnoreFirstNull).</p></li><li><p>Um índice vazio não ignora nenhum membro NULL (ou seja, o <strong>membro grbit</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tem JET_bitIndexEmpty definido, mas não tem JET_bitIndexIgnoreAnyNull definido).</p></li><li><p>Passando uma <a href="gg269214(v=exchg.10).md">estrutura JET_CONDITIONALCOLUMN</a> com um membro <strong>grbit</strong> inválido.</p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>Uma LCID (ID de localidade) inválida foi passada (por meio do membro <strong>lcid</strong> da estrutura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> que é apontada pelo membro <strong>pidxunicode</strong> na estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ou por meio do campo <strong>lcid</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE).</a></p> | 
| <p>JET_errInvalidParameter</p> | <p>Um parâmetro inválido foi dado. Alguns motivos possíveis são:</p><ul><li><p>O <strong>membro rgcolumncreate</strong> da estrutura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> é NULL.</p></li><li><p>O <strong>membro cbStruct</strong> de uma das estruturas <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> fornecidas no <strong>membro rgcolumncreate</strong> da estrutura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> não foi definido como sizeof( JET_COLUMNCREATE).</p></li><li><p>O <strong>membro cbKey</strong> de uma <a href="gg269186(v=exchg.10).md">estrutura JET_INDEXCREATE</a> é definido como zero.</p></li><li><p>O <strong>membro cbStruct</strong> de uma <a href="gg269186(v=exchg.10).md">estrutura JET_INDEXCREATE</a> não está definido como sizeof( JET_INDEXCREATE).</p></li></ul> | 
| <p>JET_errRecordTooBig</p> | <p>O registro é muito grande. A soma do membro <strong>cbMax</strong> da estrutura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> para todas as colunas fixas não deve exceder um determinado valor.</p> | 
| <p>JET_errTableDuplicate</p> | <p>A tabela já existe.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Foi feita uma tentativa de adicionar muitas colunas à tabela. Uma tabela não pode ter mais de JET_ccolFixedMost colunas fixas, não mais do que JET_ccolVarMost colunas de comprimento variável e não mais do que JET_ccolTaggedMost colunas marcadas.</p> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Ocorreu um erro ao tentar normalizar uma coluna Unicode. Isso pode ser causado pela falta de recursos do sistema.</p> | 



#### <a name="remarks"></a>Comentários

Chamar **JetCreateTableColumnIndex** é idêntico a chamar [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), com cada campo na estrutura [JET_TABLECREATE2](./jet-tablecreate2-structure.md) que contém o valor do campo correspondente [de JET_TABLECREATE](./jet-tablecreate-structure.md), com as seguintes exceções:

  - JET_TABLECREATE2.cbStruct definido como sizeof( JET_TABLECREATE2)

  - JET_TABLECREATE2.szCallback definido como NULL

  - JET_TABLECREATE2.cbtyp definido como 0

Consulte [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) para obter mais detalhes.

Como [JetOpenTable](./jetopentable-function.md), quando o aplicativo é feito usando *a tableid retornada*, ele geralmente deve ser fechado com [JetCloseTable](./jetclosetable-function.md).

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetCreateTableColumnIndexW</strong> (Unicode) e <strong>JetCreateTableColumnIndexA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex]()  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
