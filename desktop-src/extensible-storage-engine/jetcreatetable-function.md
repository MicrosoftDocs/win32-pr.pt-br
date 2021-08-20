---
description: 'Saiba mais sobre: Função JetCreateTable'
title: Função JetCreateTable
TOCTitle: JetCreateTable Function
ms:assetid: 28455b8b-0000-4bd5-a3ca-e1ef0446ee07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269210(v=EXCHG.10)
ms:contentKeyID: 32765513
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableW
- JetCreateTable
- JetCreateTableA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a915f8a66a931a1ddb976249e3d4fd991ff740b3f1cd154ed059046c5a8bc703
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944876"
---
# <a name="jetcreatetable-function"></a>Função JetCreateTable


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetcreatetable-function"></a>Função JetCreateTable

A **função JetCreateTable** cria uma tabela vazia em um banco de dados ESE.

```cpp
    JET_ERR JET_API JetCreateTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          unsigned long lPages,
      __in          unsigned long lDensity,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto de sessão do banco de dados a ser usado.

*Dbid*

O identificador de banco de dados a ser usado.

*szTableName*

O nome do índice a ser criado.

O nome deve ser formatado de acordo com as seguintes regras:

  - Seja menor que JET_cbNameMost, sem incluir o NULL de terminação.

  - Seja feita do seguinte conjunto de caracteres: 0 a 9, A a Z, a a z e todas as outras pontuações, exceto " \! " (ponto de exclamação), "," (vírgula), " " (colchete de abertura) e " " (colchete de fechamento) — ou seja, caracteres ASCII 0x20, 0x22 por meio de 0x2d, 0x2f por meio de \[ \] 0x5a, 0x5c, 0x5d 0x7f.

  - Não comece com um espaço.

  - Ser feita de pelo menos um caractere não espaço.

*lPages*

O número inicial de páginas de banco de dados a ser alocada para a tabela. Especificar um número maior que um pode reduzir a fragmentação se muitas linhas são inseridas nesta tabela.

*lDensity*

A densidade da tabela, em pontos percentuais. O número deve ser 0 ou no intervalo de 20 a 100. Passar 0 significa que o valor padrão deve ser usado. O padrão é 80.

*Ptableid*

Em caso de êxito, o identificador de tabela é retornado nesse campo. O valor será indefinido se a API não retornar JET_errSuccess.

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
<td><p>Uma densidade inválida foi passada no membro <em>ulDensity</em> na estrutura <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> dados.</p></td>
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
<td><p>JET_errIndexTuplesVarSegMacNotAllowed</p></td>
<td><p>Windows XP e posterior. Um índice de tupla não permite que <strong>o membro cbVarSegMac</strong> <a href="gg269186(v=exchg.10).md">da estrutura JET_INDEXCREATE</a> seja definido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesTextColumnsOnly</p></td>
<td><p>Windows XP e posterior. Um índice de tupla só pode estar em um texto ou coluna Unicode. Uma tentativa de indexar outras colunas (como colunas binárias) resultará em JET_errIndexTuplesTextColumnsOnly.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>Foi feita uma tentativa de criar um índice sem informações de versão durante uma transação.</p></td>
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
<td><p>Alguns dos motivos pelos quais esse erro pode ocorrer:</p>
<ul>
<li><p>O membro <strong>rgindexcreate</strong> da estrutura de <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> foi definido como nulo.</p></li>
<li><p>O membro <strong>rgcolumncreate</strong> da estrutura de <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> foi definido como nulo.</p></li>
<li><p>O membro <strong>cbStruct</strong> de uma estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> não foi definido como um valor válido.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Uma combinação inválida de membros <strong>grbit</strong> foi especificada em <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</p>
<p>A definição do índice é inválida porque o membro <strong>grbit</strong> contém valores inconsistentes. Alguns motivos possíveis são:</p>
<ul>
<li><p>Um índice primário tinha um bit de ignorar especificado (ou seja, JET_bitIndexPrimary foi passado com JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull ou JET_bitIndexIgnoreFirstNull).</p></li>
<li><p>Um índice vazio não ignora quaisquer membros nulos (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tem JET_bitIndexEmpty definido, mas não tem JET_bitIndexIgnoreAnyNull definido).</p></li>
<li><p>Passando uma estrutura de <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> com um membro <strong>grbit</strong> inválido.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Uma LCID (identificação de localidade) inválida foi passada (por meio do membro <strong>LCID</strong> da estrutura de <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> que é apontada pelo membro <strong>pidxunicode</strong> na estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ou pelo campo <strong>LCID</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um parâmetro inválido foi fornecido. Alguns motivos possíveis são:</p>
<ul>
<li><p>O membro <strong>rgcolumncreate</strong> da estrutura de <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> é nulo.</p></li>
<li><p>O membro <strong>cbStruct</strong> de uma das estruturas de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> dadas no membro <strong>rgcolumncreate</strong> da estrutura de <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> não foi definido como sizeof (JET_COLUMNCREATE).</p></li>
<li><p>O membro <strong>cbKey</strong> de uma estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> é definido como zero.</p></li>
<li><p>O membro <strong>cbStruct</strong> de uma estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> não está definido como sizeof (JET_INDEXCREATE).</p></li>
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
<td><p>Foi feita uma tentativa de adicionar muitas colunas à tabela. Uma tabela não pode ter mais de JET_ccolFixedMost colunas fixas, não mais do que JET_ccolVarMost colunas de comprimento variável e não mais do que JET_ccolTaggedMost colunas marcadas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeTranslationFail</p></td>
<td><p>Ocorreu um erro ao tentar normalizar uma coluna Unicode. Isso pode ser causado pela execução de recursos do sistema.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Comentários

**JetCreateTable** cria uma tabela que não contém nenhuma coluna. Para adicionar colunas, consulte [JetAddColumn](./jetaddcolumn-function.md).

Internamente, **JetCreateTable** chama [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), preenchendo uma estrutura [JET_TABLECREATE2](./jet-tablecreate2-structure.md) com:

  - JET_TABLECREATE2. cbStruct = sizeof (JET_TABLECREATE2)

  - JET_TABLECREATE2. szTableName = szTableName

  - JET_TABLECREATE2. ulPages = lPage

  - JET_TABLECREATE2. ulDensity = lDensity

  - JET_TABLECREATE2. TableName = JET_tableidNil

Todos os outros campos da estrutura de [JET_TABLECREATE2](./jet-tablecreate2-structure.md) interna são definidos como zero ou nulos. Na saída, *pTableID* será definido como JET_TABLECREATE2. TableName.

Consulte [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) para obter mais detalhes.

Como o [JetOpenTable](./jetopentable-function.md), quando o aplicativo é feito usando o membro **TableName** retornado da estrutura [JET_TABLECREATE2](./jet-tablecreate2-structure.md) , ele normalmente deve ser fechado com [JetCloseTable](./jetclosetable-function.md).

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p></td>
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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementado como <strong>JetCreateTableW</strong> (Unicode) e <strong>JetCreateTableA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
