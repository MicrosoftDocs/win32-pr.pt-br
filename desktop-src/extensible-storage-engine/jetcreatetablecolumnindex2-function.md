---
description: 'Saiba mais sobre: Função JetCreateTableColumnIndex2'
title: Função JetCreateTableColumnIndex2
TOCTitle: JetCreateTableColumnIndex2 Function
ms:assetid: ad9caaf3-8cd2-453f-894d-8ac438c50b73
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294057(v=EXCHG.10)
ms:contentKeyID: 32765672
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndex2W
- JetCreateTableColumnIndex2
- JetCreateTableColumnIndex2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cb6e0583c0efa2dbfc52af14f6d1ba0c4200d4f3a3421d1953084daca467358e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119728526"
---
# <a name="jetcreatetablecolumnindex2-function"></a>Função JetCreateTableColumnIndex2


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetcreatetablecolumnindex2-function"></a>Função JetCreateTableColumnIndex2

A **função JetCreateTableColumnIndex2** cria uma tabela em um banco de dados ESE com um conjunto inicial de índices e um conjunto inicial de colunas de uma matriz de JET_TABLECREATE2 [estruturas.](./jet-tablecreate2-structure.md) A [JET_TABLECREATE2](./jet-tablecreate2-structure.md) estrutura permite que uma função de retorno de chamada seja especificada.

**Windows XP: JetCreateTableColumnIndex2** é introduzido no Windows XP.

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex2(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE2* ptablecreate
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto de sessão do banco de dados a ser usado para a chamada à API.

*Dbid*

O identificador de banco de dados a ser usado para a chamada à API.

*ptablecreate*

Um ponteiro para uma [JET_TABLECREATE2](./jet-tablecreate2-structure.md) que define a tabela a ser criada. Consulte [JET_TABLECREATE2](./jet-tablecreate2-structure.md) para obter mais detalhes.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) tipo de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>Não foi possível resolver a função de retorno de chamada. A DLL pode não ter sido encontrada ou a função na DLL pode não ter sido encontrada. Com o log suficiente habilitado, o log de eventos fornecerá mais detalhes.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotIndex</p></td>
<td><p>Foi feita uma tentativa de indexar em uma coluna Escrow-update ou SLV (observe que as colunas SLV foram preterida).</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotNestDDL</p></td>
<td><p>Se ptablecreate- grbit especificar JET_bitTableCreateTemplateTable, mas &gt; ptablecreate- &gt; szTemplateTableName for definido como NULL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnDuplicate</p></td>
<td><p>Já existe uma coluna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Foi feita uma tentativa de indexar em uma coluna inexistente. Tentar indexar condicionalmente em uma coluna inexistente também pode produzir esse erro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnRedundant</p></td>
<td><p>Foi feita uma tentativa de adicionar uma coluna redundante. Não deve haver mais de uma coluna de decremento automático e não mais de uma coluna de versão por tabela.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid</p></td>
<td><p>Esse erro será retornado se o <strong>membro ulDensity</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for definido como um número menor que 20 ou mais de 100.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDDLNotInheritable</p></td>
<td><p>Significa que a tabela nomeada no membro <strong>szTemplateTableName</strong> da estrutura <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> não era marcada como uma tabela de modelo (ou seja, essa tabela não tinha JET_bitTableCreateTemplateTable definida).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexDuplicate</p></td>
<td><p>Foi feita uma tentativa de definir dois índices idênticos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexHasPrimary</p></td>
<td><p>Foi feita uma tentativa de especificar mais de um índice primário para uma tabela. Uma tabela deve ter exatamente um índice primário. Se nenhum índice primário for especificado, o mecanismo de banco de dados criará um de forma transparente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>Uma definição de índice inválida foi especificada. Alguns dos possíveis motivos para receber esse erro são:</p>
<ul>
<li><p>Um índice primário é condicional (ou seja, o <strong>membro grbit</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tem um conjunto JET_bitIndexPrimary e o membro <strong>cConditionalColumn</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> é maior que zero).</p></li>
<li><p>Windows Server 2003 e posterior. Tentar criar um índice de tupla com limites de tupla, mas sem passar o membro <strong>ptuplelimits</strong> na estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (ou seja, o <strong>membro grbit</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tem JET_bitIndexTupleLimits definido, mas o ponteiro <strong>ptuplelimits</strong> é NULL).</p></li>
<li><p>Passando uma definição de chave inválida no <strong>membro szKey</strong> da <a href="gg269186(v=exchg.10).md">estrutura JET_INDEXCREATE</a> dados. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para uma discussão sobre definições válidas.</p></li>
<li><p>Definir o <strong>membro cbVarSegMac</strong> <a href="gg269186(v=exchg.10).md">no JET_INDEXCREATE</a> ser maior que JET_cbPrimaryKeyMost (para um índice primário) ou maior que JET_cbSecondaryKeyMost (para um índice secundário).</p></li>
<li><p>Passando uma combinação inválida para um índice Unicode definido pelo usuário (um que tem o bit JET_bitIndexUnicode definido no <strong>membro grbit</strong> do <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>). Algumas causas comuns incluem <strong>o membro pidxunicode</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> é NULL ou o LCID especificado na estrutura <strong>pidxunicode</strong> é inválido.</p></li>
<li><p>Especificando uma coluna com vários valores para um índice primário.</p></li>
<li><p>Tentando indexar muitas colunas condicionais. O <strong>membro cConditionalColumn</strong> da <a href="gg269186(v=exchg.10).md">estrutura JET_INDEXCREATE</a> não deve ser maior que JET_ccolKeyMost.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Windows XP e posterior. Uma <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> estrutura de dados foi especificada e seus limites não são suportados. Consulte a seção de comentários da estrutura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> dados.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesNonUniqueOnly</p></td>
<td><p>Windows XP e posterior. Um índice de tupla não pode ser exclusivo (ou seja, o <em>membro grbit</em> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> não deve ter JET_bitIndexPrimary e JET_bitIndexUnique definidos).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesOneColumnOnly</p></td>
<td><p>Windows XP e posterior. Um índice de tupla só poderá ser sobre uma única coluna (ou seja, se o membro <strong>grbit</strong> <a href="gg269186(v=exchg.10).md">da</a> estrutura JET_INDEXCREATE tiver JET_bitIndexTuples definido e o membro <strong>szKey</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> especificar mais de uma coluna).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesSecondaryIndexOnly</p></td>
<td><p>Windows XP e posterior. Um índice de tupla não pode ser um índice primário (ou seja, o <strong>membro grbit</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> não deve ter JET_bitIndexPrimary e JET_bitIndexTuples definidos).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesTextColumnsOnly</p></td>
<td><p>Windows XP e posterior. Um índice de tupla só pode estar em um texto ou coluna Unicode. Uma tentativa de indexar outras colunas (como colunas binárias) resultará em JET_errIndexTuplesTextColumnsOnly.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed</p></td>
<td><p>Windows XP e posterior. Um índice de tupla não permite que <strong>o membro cbVarSegMac</strong> <a href="gg269186(v=exchg.10).md">da estrutura JET_INDEXCREATE</a> seja definido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>Foi feita uma tentativa de criar um índice sem informações de versão durante uma transação.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>O <strong>membro cp</strong> da estrutura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> não foi definido como uma página de código válida. Os únicos valores válidos para colunas de texto são inglês (1252) e Unicode (1200). Um valor de 0 significa que o padrão será usado (inglês, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>O <strong>membro coltyp</strong> da <a href="gg269252(v=exchg.10).md">estrutura JET_COLUMNCREATE</a> não foi definido como um tipo de coluna válido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCreateIndex</p></td>
<td><p>Alguns dos motivos pelos quais esse erro pode ocorrer:</p>
<ul>
<li><p>O <strong>membro rgindexcreate</strong> da <a href="gg269203(v=exchg.10).md">estrutura JET_TABLECREATE2</a> foi definido como NULL.</p></li>
<li><p>O <strong>membro rgcolumncreate</strong> da estrutura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> foi definido como NULL.</p></li>
<li><p>O <strong>membro cbStruct</strong> de uma <a href="gg269186(v=exchg.10).md">estrutura JET_INDEXCREATE</a> não foi definido como um valor válido.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Uma combinação inválida de <strong>membros grbit</strong> foi especificada <a href="gg294146(v=exchg.10).md">em JET_TABLECREATE</a> ou <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</p>
<p>A definição de índice é inválida porque o <strong>membro grbit</strong> contém valores inconsistentes. Alguns motivos possíveis são:</p>
<ul>
<li><p>Um índice primário tinha um bit de ignorar especificado (ou seja, JET_bitIndexPrimary foi passado com JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull ou JET_bitIndexIgnoreFirstNull).</p></li>
<li><p>Um índice vazio não ignora nenhum membro NULL (ou seja, o <strong>membro grbit</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tem JET_bitIndexEmpty definido, mas não tem JET_bitIndexIgnoreAnyNull definido).</p></li>
<li><p>Passando uma estrutura <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> com um membro <strong>grbit</strong> inválido.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Uma LCID (ID de localidade) inválida foi passada (por meio do membro <strong>lcid</strong> da estrutura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> que é apontada pelo membro <strong>pidxunicode</strong> na estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ou por meio do campo <strong>lcid</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE).</a></p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um parâmetro inválido foi dado. Alguns motivos possíveis são:</p>
<ul>
<li><p>O <strong>membro rgcolumncreate</strong> da estrutura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> é NULL.</p></li>
<li><p>O <strong>membro cbStruct</strong> de uma das estruturas <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> fornecidas no <strong>membro rgcolumncreate</strong> da estrutura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> não foi definido como sizeof( JET_COLUMNCREATE ).</p></li>
<li><p>O <strong>membro cbKey</strong> de uma <a href="gg269186(v=exchg.10).md">estrutura JET_INDEXCREATE</a> é definido como zero.</p></li>
<li><p>O <strong>membro cbStruct</strong> de uma <a href="gg269186(v=exchg.10).md">estrutura JET_INDEXCREATE</a> não está definido como sizeof( JET_INDEXCREATE ).</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errRecordTooBig</p></td>
<td><p>O registro é muito grande. A soma do membro <strong>cbMax</strong> da estrutura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> para todas as colunas fixas não deve exceder um determinado valor.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableDuplicate</p></td>
<td><p>A tabela já existe.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyColumns</p></td>
<td><p>Foi feita uma tentativa de adicionar muitas colunas à tabela. Uma tabela não pode ter mais de JET_ccolFixedMost colunas fixas, não mais do que JET_ccolVarMost colunas de comprimento variável e não mais do que JET_ccolTaggedMost colunas marcadas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeTranslationFail</p></td>
<td><p>Ocorreu um erro ao tentar normalizar uma coluna Unicode. Isso pode ser causado pela falta de recursos do sistema.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Comentários

O nome **JetCreateTableColumnIndex2** vem da ordem de criação dos objetos: primeiro, ele cria uma tabela, colunas e, por fim, índices. **JetCreateTableColumnIndex2** cria uma tabela com um conjunto inicial de colunas e índices. Colunas e índices adicionais podem ser adicionados e removidos dinamicamente com [JetAddColumn,](./jetaddcolumn-function.md) [JetDeleteColumn,](./jetdeletecolumn-function.md) [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md)e [JetDeleteIndex](./jetdeleteindex-function.md).

Como [JetOpenTable](./jetopentable-function.md), quando o aplicativo é feito usando *a tableid retornada*, ele geralmente deve ser fechado com [JetCloseTable](./jetclosetable-function.md).

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer Windows Vista ou Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer Windows Server 2008 ou Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Biblioteca</strong></p></td>
<td><p>Use ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementado como <strong>JetCreateTableColumnIndex2W</strong> (Unicode) e <strong>JetCreateTableColumnIndex2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_CBTYP](./jet-cbtyp.md)  
[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetCreateTable](./jetcreatetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetDeleteColumn](./jetdeletecolumn-function.md)  
[JetDeleteColumn2](./jetdeletecolumn2-function.md)
