---
description: 'Saiba mais sobre: função JetCreateTable'
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
ms.openlocfilehash: 6f385cfd668af934bfde2669277db7ed048a1fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105808253"
---
# <a name="jetcreatetable-function"></a>Função JetCreateTable


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetcreatetable-function"></a>Função JetCreateTable

A função **JetCreateTable** cria uma tabela vazia em um banco de dados ESE.

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

O contexto da sessão de banco de dados a ser usado.

*DBID*

O identificador de banco de dados a ser usado.

*szTableName*

O nome do índice a ser criado.

O nome deve ser formatado de acordo com as seguintes regras:

  - Ser menor que JET_cbNameMost, não incluindo o nulo de terminação.

  - Ser feita do seguinte conjunto de caracteres: 0 a 9, A a Z, a a z e todas as outras pontuações, exceto para " \! " (ponto de exclamação), "," (vírgula), " \[ " (colchete de abertura) e " \] " (colchete de fechamento) — ou seja, caracteres ASCII 0x20, 0x22 a 0x2d, 0x2F a 0x5A, 0x5c, 0x5d até 0x7F.

  - Não comece com um espaço.

  - Ser feita de pelo menos um caractere que não seja de espaço.

*lPages*

O número inicial de páginas de banco de dados a serem alocadas para a tabela. A especificação de um número maior que um pode reduzir a fragmentação se várias linhas forem inseridas nessa tabela.

*lDensity*

A densidade da tabela, em pontos percentuais. O número deve ser 0 ou estar no intervalo de 20 a 100. Passar 0 significa que o valor padrão deve ser usado. O padrão é 80.

*ptableid*

Em caso de sucesso, o identificador de tabela é retornado nesse campo. O valor será indefinido se a API não retornar JET_errSuccess.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

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
<td><p>Se ptablecreate- &gt; grbit especificar JET_bitTableCreateTemplateTable, mas ptablecreate- &gt; szTemplateTableName será definido como NULL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnDuplicate</p></td>
<td><p>Já existe uma coluna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Foi feita uma tentativa de indexar uma coluna não existente. A tentativa de indexar condicionalmente uma coluna não existente também pode produzir esse erro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnRedundant</p></td>
<td><p>Foi feita uma tentativa de adicionar uma coluna redundante. Não deve haver mais de uma coluna de incremento automático e não há mais de uma coluna de versão por tabela.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid</p></td>
<td><p>Uma densidade inválida foi passada no membro <em>ulDensity</em> na estrutura <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDDLNotInheritable</p></td>
<td><p>Significa que a tabela nomeada no membro <strong>szTemplateTableName</strong> da estrutura de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> não foi marcada como uma tabela de modelo (ou seja, essa tabela não tinha JET_bitTableCreateTemplateTable definido).</p></td>
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
<td><p>Uma definição de índice inválida foi especificada. Alguns dos motivos possíveis para receber esse erro são:</p>
<ul>
<li><p>Um índice primário é condicional (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tem JET_bitIndexPrimary definido e o membro <strong>cConditionalColumn</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> é maior que zero).</p></li>
<li><p>Windows Server 2003 e posterior. Tentativa de criar um índice de tupla com limites de tupla, mas sem passar o membro <strong>ptuplelimits</strong> na estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tem JET_BITINDEXTUPLELIMITS definido, mas o ponteiro <strong>ptuplelimits</strong> é nulo).</p></li>
<li><p>Passando uma definição de chave inválida no membro <strong>szKey</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> . Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter uma discussão sobre definições válidas.</p></li>
<li><p>Definir o membro <strong>cbVarSegMac</strong> em <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ser maior que JET_cbPrimaryKeyMost (para um índice primário) ou maior que JET_cbSecondaryKeyMost (para um índice secundário).</p></li>
<li><p>Passando uma combinação inválida para um índice Unicode definido pelo usuário (um que tem o conjunto de bits JET_bitIndexUnicode no membro <strong>grbit</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>). Algumas causas comuns incluem o membro <strong>pidxunicode</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> é NULL ou o LCID especificado na estrutura <strong>pidxunicode</strong> é inválido.</p></li>
<li><p>Especificando uma coluna com valores múltiplos para um índice primário.</p></li>
<li><p>Tentando indexar muitas colunas condicionais. O membro <strong>cConditionalColumn</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> não deve ser maior que JET_ccolKeyMost.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Windows XP e posterior. Uma estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> foi especificada e não há suporte para seus limites. Consulte a seção comentários da estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesNonUniqueOnly</p></td>
<td><p>Windows XP e posterior. Um índice de tupla não pode ser exclusivo (ou seja, o membro <em>grbit</em> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> não deve ter JET_bitIndexPrimary e JET_bitIndexUnique definido).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesOneColumnOnly</p></td>
<td><p>Windows XP e posterior. Um índice de tupla só pode ser sobre uma única coluna (ou seja, se o membro <strong>grbit</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tiver JET_bitIndexTuples definido e o membro <strong>szKey</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> especificar mais de uma coluna).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesSecondaryIndexOnly</p></td>
<td><p>Windows XP e posterior. Um índice de tupla não pode ser um índice primário (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> não deve ter JET_bitIndexPrimary e JET_bitIndexTuples definido).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed</p></td>
<td><p>Windows XP e posterior. Um índice de tupla não permite que o membro <strong>cbVarSegMac</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> seja definida.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesTextColumnsOnly</p></td>
<td><p>Windows XP e posterior. Um índice de tupla só pode estar em uma coluna de texto ou Unicode. Uma tentativa de indexar outras colunas (como colunas binárias) resultará em JET_errIndexTuplesTextColumnsOnly.</p></td>
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
