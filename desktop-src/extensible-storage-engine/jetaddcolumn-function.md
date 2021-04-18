---
description: 'Saiba mais sobre: função JetAddColumn'
title: Função JetAddColumn
TOCTitle: JetAddColumn Function
ms:assetid: e146f784-2cbd-42c0-bf64-b37dc6f9ee43
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294122(v=EXCHG.10)
ms:contentKeyID: 32765736
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAddColumnW
- JetAddColumnA
- JetAddColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b8c3eac113daeae43ec4a8e62b7fcda9ddbf9f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791090"
---
# <a name="jetaddcolumn-function"></a>Função JetAddColumn


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetaddcolumn-function"></a>Função JetAddColumn

A função **JetAddColumn** adiciona uma nova coluna a uma tabela existente em um banco de dados ESE.

```cpp
    JET_ERR JET_API JetAddColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szColumnName,
      __in          const JET_COLUMNDEF* pcolumndef,
      __in_opt      const void* pvDefault,
      __in          unsigned long cbDefault,
      __out_opt     JET_COLUMNID* pcolumnid
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*TableID*

A tabela à qual adicionar a coluna.

*szColumnName*

O nome da coluna a ser adicionada. O nome deve atender aos seguintes critérios:

  - Ele deve ter menos de JET_cbNameMost caracteres de comprimento, não incluindo o **nulo** de terminação.

  - Ele deve conter caracteres somente dos seguintes conjuntos: 0 a 9, A a Z, a a z e todas as outras pontuações, exceto para ponto de exclamação ( \! ), vírgula (,), colchete de abertura ( \[ ) e colchete de fechamento ( \] ) — ou seja, caracteres ASCII 0x20, 0x22 a 0x2d, 0x2F a 0x5A, 0x5c e 0x5d até 0x7F.

  - Ele não pode começar com um espaço.

  - Ele deve conter pelo menos um caractere que não seja de espaço.

*pcolumndef*

Um ponteiro para uma estrutura de [JET_COLUMNDEF](./jet-columndef-structure.md) , que define os dados que podem ser armazenados em uma coluna.

*pvDefault*

Um ponteiro para um buffer que contém o valor padrão para a coluna. O comprimento do buffer é **cbDefault**. Se não houver nenhum padrão, defina **pvDefault** como **nulo** e **cbDefault** como zero. Os valores padrão não podem ser maiores que JET_cbColumnMost bytes para colunas fixas ou JET_cbLVDefaultValueMost bytes para valores longos. Se um valor padrão for maior que isso, ele será silenciosamente truncado.

Se *grbit* tiver JET_bitColumnUserDefinedDefault definido, **pvDefault** será interpretado como um ponteiro para uma estrutura de [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) .

*cbDefault*

O tamanho, em bytes, do buffer especificado em **pvDefault**.

*pcolumnid*

Um ponteiro para uma estrutura de [JET_COLUMNID](./jet-columnid.md) , que, em caso de êxito, receberá o identificador da coluna recém-criada. Em caso de falha, o valor é indefinido.

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
<td><p>A operação foi bem-sucedida.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFixedDDL</p></td>
<td><p>Foi feita uma tentativa de modificar a definição de dados de uma tabela DDL fixa. Um exemplo de uma tabela com DDL fixo é uma tabela de modelo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um parâmetro inválido foi passado para a API. Alguns exemplos de parâmetros inválidos são:</p>
<ul>
<li><p>Passando o tamanho errado da estrutura de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> em seu membro <em>cbStruct</em> .</p></li>
<li><p>Passando JET_bitColumnUserDefinedDefault, mas não definindo <strong>cbDefault</strong> como sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInTransaction</p></td>
<td><p>Foi feita uma tentativa de adicionar uma coluna com o conjunto de bits JET_bitColumnUnversioned, mas a sessão está em uma transação no momento.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnDuplicate</p></td>
<td><p>Já existe uma coluna. Foi feita uma tentativa de adicionar uma coluna sem informações de versão e essa coluna já existe.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableNotEmpty</p></td>
<td><p>A tabela contém dados. Uma coluna de atualização de caução só pode ser adicionada a uma tabela vazia.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBig</p></td>
<td><p>O registro é muito grande. A soma do parâmetro <strong>cbMax</strong> para as colunas fixas não deve exceder um determinado valor.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyColumns</p></td>
<td><p>Foi feita uma tentativa de adicionar muitas colunas à tabela. Uma tabela não pode ter mais de JET_ccolFixedMost colunas fixas, não mais do que JET_ccolVarMost colunas de comprimento variável e não mais do que JET_ccolTaggedMost colunas marcadas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnRedundant</p></td>
<td><p>Foi feita uma tentativa de adicionar uma coluna redundante. Não deve haver mais de uma coluna de incremento automático e não há mais de uma coluna de versão por tabela.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCallbackNotResolved</p></td>
<td><p>A função de retorno de chamada não pôde ser resolvida. A DLL pode não ter sido encontrada ou a função na DLL pode não ter sido encontrada. O log de eventos fornecerá mais detalhes se o registro em log suficiente estiver habilitado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>Um aviso que indica que o comprimento máximo (<strong>cbMax</strong>) de uma coluna fixa ou variável foi maior que JET_cbColumnMost. Esse limite não se aplica a valores longos ( <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> e <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Um nome inválido foi passado como <strong>szColumnName</strong>. Para obter mais informações sobre as restrições, consulte os critérios para <strong>szColumnName</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>O campo <strong>coltyp</strong> não foi definido como um tipo de coluna válido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>O parâmetro <strong>CP</strong> da estrutura de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> não foi definido como uma página de código válida. Os únicos valores válidos para colunas de texto são Inglês (1252) e Unicode (1200). Um valor de 0 significa que o padrão será usado (Inglês, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTaggedNotNULL</p></td>
<td><p>JET_bitColumnNotNULL não pode ser usada com colunas marcadas, de valor longo ou SLV.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Foi especificada uma combinação inválida de <em>grbits</em> . Alguns dos motivos para esse erro são:</p>
<ul>
<li><p>JET_bitColumnFixed foi usado em uma coluna marcada, de valor longo ou SLV.</p></li>
<li><p>JET_bitColumnEscrowUpdate foi usado em uma coluna que não era do tipo <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</p></li>
<li><p>JET_bitColumnEscrowUpdate foi usado em uma coluna de versão (JET_bitColumnVersion).</p></li>
<li><p>JET_bitColumnEscrowUpdate foi usado em uma coluna AutoIncrememnt (JET_bitColumnAutoincrement).</p></li>
<li><p>JET_bitColumnEscrowUpdate foi usado em uma coluna que não tinha um valor padrão (<strong>cbDefault</strong> era igual a zero).</p></li>
<li><p>JET_bitColumnFinalize foi usada em uma coluna que não era uma coluna de atualização de caução (JET_bitColumnEscrowUpdate não foi definida).</p></li>
<li><p>JET_bitColumnDeleteOnZero foi usada em uma coluna que não era uma coluna de atualização de caução (JET_bitColumnEscrowUpdate não foi definida).</p></li>
<li><p>JET_bitColumnAutoincrement foi usado em uma coluna que não foi <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</p>
<p><strong>Windows 2000:  </strong> Esse motivo para o código de erro é usado somente no Windows 2000.</p>
<p>JET_bitColumnAutoincrement foi usado em uma coluna que não foi <a href="gg269213(v=exchg.10).md">JET_coltypLong</a> nem <a href="gg269213(v=exchg.10).md">JET_coltypCurrency</a>.</p>
<p><strong>Windows XP:  </strong> Esse motivo para o código de erro é usado no Windows XP e em sistemas operacionais posteriores.</p></li>
<li><p>JET_bitColumnVersion foi usado em uma coluna que não foi <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</p></li>
<li><p>JET_bitColumnVersion foi usado em uma coluna de incremento automático.</p></li>
<li><p>JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnFixed.</p></li>
<li><p>JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnNotNULL.</p></li>
<li><p>JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnVersion.</p></li>
<li><p>JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnAutoincrement.</p></li>
<li><p>JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnUpdatable.</p></li>
<li><p>JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnEscrowUpdate.</p></li>
<li><p>JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnFinalize.</p></li>
<li><p>JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnDeleteOnZero.</p></li>
<li><p>JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnMaybeNull.</p></li>
<li><p>JET_bitColumnUserDefinedDefault foi usado em uma coluna não marcada (que é fixed ou Variable).</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errMultiValuedColumnMustBeTagged</p></td>
<td><p>Uma coluna com valores múltiplos (JET_bitColumnMultiValued) só pode ser usada em uma coluna marcada ou de valor longo (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotBeTagged</p></td>
<td><p>Foi feita uma tentativa de usar uma coluna marcada quando a coluna não pode ser marcada. Algumas das restrições para desautorizar colunas marcadas são:</p>
<ul>
<li><p>Uma coluna de atualização de caução (JET_bitColumnEscrowUpdate) não pode ser usada em uma coluna de valor marcado ou longo (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p></li>
<li><p>Uma coluna AutoIncrement não pode ser marcada.</p></li>
<li><p>Uma coluna de versão não pode ser marcada.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errExclusiveTableLockRequired</p></td>
<td><p>Um bloqueio exclusivo na tabela era necessário para esta operação.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>Um aviso que indica que o comprimento máximo (<em>cbMax</em>) de uma coluna fixa ou variável foi maior que JET_cbColumnMost. Esse limite não se aplica a valores longos ( <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> e <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p></td>
</tr>
</tbody>
</table>


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
<td><p>Implementado como <strong>JetAddColumnW</strong> (Unicode) e <strong>JetAddColumnA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
