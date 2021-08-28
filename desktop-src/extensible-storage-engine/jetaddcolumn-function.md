---
description: 'Saiba mais sobre: Função JetAddColumn'
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
ms.openlocfilehash: a1f59d4bb49145dd897994bebb776249a55e14d8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466373"
---
# <a name="jetaddcolumn-function"></a>Função JetAddColumn


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetaddcolumn-function"></a>Função JetAddColumn

A **função JetAddColumn** adiciona uma nova coluna a uma tabela existente em um banco de dados ESE.

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

O contexto de sessão do banco de dados a ser usado para a chamada à API.

*Tableid*

A tabela à qual adicionar a coluna.

*szColumnName*

O nome da coluna a ser acrescentada. O nome deve atender aos seguintes critérios:

  - Ele deve ter menos de JET_cbNameMost caracteres de comprimento, não incluindo o NULL de **terminação.**

  - Ele deve conter caracteres somente dos seguintes conjuntos: 0 a 9, A a Z, a a z e todas as outras pontuações, exceto ponto de exclamação ( ), vírgula (,), colchete de abertura ( ) e colchete de fechamento ( ) — ou seja, caracteres \! \[ ASCII 0x20, 0x22 por meio de 0x2d, 0x2f por meio de 0x5a, 0x5c e 0x5d por meio \] 0x7f.

  - Ele não pode começar com um espaço.

  - Ele deve conter pelo menos um caractere sem espaço.

*pcolumndef*

Um ponteiro para uma [JET_COLUMNDEF,](./jet-columndef-structure.md) que define os dados que podem ser armazenados em uma coluna.

*pvDefault*

Um ponteiro para um buffer que contém o valor padrão da coluna. O comprimento do buffer é **cbDefault.** Se não houver nenhum padrão, de acordo **com pvDefault** como **NULL** e **cbDefault** como zero. Os valores padrão não podem ser maiores que JET_cbColumnMost bytes para colunas fixas ou JET_cbLVDefaultValueMost bytes para valores longos. Se um valor padrão for maior que esse, ele será silenciosamente truncado.

Se *grbit* tiver JET_bitColumnUserDefinedDefault definido, **pvDefault** será interpretado como um ponteiro para uma [estrutura JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) dados.

*cbDefault*

O tamanho, em bytes, do buffer especificado em **pvDefault.**

*pcolumnid*

Um ponteiro para uma [JET_COLUMNID,](./jet-columnid.md) que, em caso de êxito, receberá o identificador da coluna recém-criada. Em caso de falha, o valor é indefinido.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi bem-sucedida.</p> | 
| <p>JET_errFixedDDL</p> | <p>Foi feita uma tentativa de modificar a definição de dados de uma tabela DDL fixa. Um exemplo de uma tabela com DDL fixa é uma Tabela de Modelo.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um parâmetro inválido foi passado para a API. Alguns exemplos de parâmetros inválidos são:</p><ul><li><p>Passando o tamanho errado da estrutura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> em seu <em>membro cbStruct.</em></p></li><li><p>Passando JET_bitColumnUserDefinedDefault, mas não definindo <strong>cbDefault</strong> como sizeof(<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</p></li></ul> | 
| <p>JET_errInTransaction</p> | <p>Foi feita uma tentativa de adicionar uma coluna com o JET_bitColumnUnversioned bit definido, mas a sessão está atualmente em uma transação.</p> | 
| <p>JET_errColumnDuplicate</p> | <p>Já existe uma coluna. Foi feita uma tentativa de adicionar uma coluna sem informações de versão e essa coluna já existe.</p> | 
| <p>JET_errTableNotEmpty</p> | <p>A tabela contém dados. Uma coluna Escrow Update só pode ser adicionada a uma tabela vazia.</p> | 
| <p>JET_errRecordTooBig</p> | <p>O registro é muito grande. A soma do parâmetro <strong>cbMax</strong> para as colunas fixas não deve exceder um determinado valor.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Foi feita uma tentativa de adicionar muitas colunas à tabela. Uma tabela não pode ter mais de JET_ccolFixedMost colunas fixas, não mais do que JET_ccolVarMost colunas de comprimento variável e não mais do que JET_ccolTaggedMost colunas marcadas.</p> | 
| <p>JET_errColumnRedundant</p> | <p>Foi feita uma tentativa de adicionar uma coluna redundante. Não deve haver mais de uma coluna de decremento automático e não mais de uma coluna de versão por tabela.</p> | 
| <p>JET_errCallbackNotResolved</p> | <p>Não foi possível resolver a função de retorno de chamada. A DLL pode não ter sido encontrada ou a função na DLL pode não ter sido encontrada. O log de eventos fornecerá mais detalhes se o log suficiente estiver habilitado.</p> | 
| <p>JET_wrnColumnMaxTruncated</p> | <p>Um aviso que indica que o comprimento máximo (<strong>cbMax</strong>) de uma coluna fixa ou variável era maior que JET_cbColumnMost. Esse limite não se aplica a Valores Longos (que é <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> e <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p> | 
| <p>JET_errInvalidName</p> | <p>Um nome inválido foi passado <strong>como szColumnName.</strong> Para obter mais informações sobre as restrições, consulte os critérios <strong>de szColumnName</strong>.</p> | 
| <p>JET_errInvalidColumnType</p> | <p>O <strong>campo coltyp</strong> não foi definido como um tipo de coluna válido.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>O <strong>parâmetro cp</strong> da estrutura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> não foi definido como uma página de código válida. Os únicos valores válidos para colunas de texto são inglês (1252) e Unicode (1200). Um valor de 0 significa que o padrão será usado (inglês, 1252).</p> | 
| <p>JET_errTaggedNotNULL</p> | <p>JET_bitColumnNotNULL pode ser usado com colunas marcadas, Valor Longo ou SLV.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Uma combinação inválida de <em>grbits</em> foi especificada. Alguns dos motivos para esse erro são:</p><ul><li><p>JET_bitColumnFixed foi usado em uma coluna marcada, Valor Longo ou SLV.</p></li><li><p>JET_bitColumnEscrowUpdate foi usado em uma coluna que não era do tipo <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</p></li><li><p>JET_bitColumnEscrowUpdate foi usado em uma coluna Version (JET_bitColumnVersion).</p></li><li><p>JET_bitColumnEscrowUpdate foi usado em uma coluna AutoIncrememnt (JET_bitColumnAutoincrement).</p></li><li><p>JET_bitColumnEscrowUpdate foi usado em uma coluna que não tinha um valor padrão (<strong>cbDefault</strong> era igual a zero).</p></li><li><p>JET_bitColumnFinalize foi usado em uma coluna que não era uma coluna Escrow Update (JET_bitColumnEscrowUpdate não foi definida).</p></li><li><p>JET_bitColumnDeleteOnZero foi usado em uma coluna que não era uma coluna Escrow Update (JET_bitColumnEscrowUpdate não foi definido).</p></li><li><p>JET_bitColumnAutoincrement foi usado em uma coluna que não <a href="gg269213(v=exchg.10).md">foi JET_coltypLong</a>.</p><p><strong>Windows 2000:</strong> Esse motivo para o código de erro é usado somente Windows 2000.</p><p>JET_bitColumnAutoincrement foi usado em uma coluna que não era <a href="gg269213(v=exchg.10).md">JET_coltypLong</a> nem <a href="gg269213(v=exchg.10).md">JET_coltypCurrency</a>.</p><p><strong>Windows XP:</strong> Esse motivo para o código de erro é usado no Windows XP e sistemas operacionais posteriores.</p></li><li><p>JET_bitColumnVersion foi usado em uma coluna que não foi <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</p></li><li><p>JET_bitColumnVersion foi usado em uma coluna de decremento automático.</p></li><li><p>JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnFixed.</p></li><li><p>JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnNotNULL.</p></li><li><p>JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnVersion.</p></li><li><p>JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnAutoincrement.</p></li><li><p>JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnUpdatable.</p></li><li><p>JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnEscrowUpdate.</p></li><li><p>JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnFinalize.</p></li><li><p>JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnDeleteOnZero.</p></li><li><p>JET_bitColumnUserDefinedDefault foi usado em conjunto com JET_bitColumnMaybeNull.</p></li><li><p>JET_bitColumnUserDefinedDefault foi usado em uma coluna não marcada (que é fixed ou Variable).</p></li></ul> | 
| <p>JET_errMultiValuedColumnMustBeTagged</p> | <p>Uma coluna com valores múltiplos (JET_bitColumnMultiValued) só pode ser usada em uma coluna marcada ou de valor longo (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p> | 
| <p>JET_errCannotBeTagged</p> | <p>Foi feita uma tentativa de usar uma coluna marcada quando a coluna não pode ser marcada. Algumas das restrições para desautorizar colunas marcadas são:</p><ul><li><p>Uma coluna de atualização de caução (JET_bitColumnEscrowUpdate) não pode ser usada em uma coluna de valor marcado ou longo (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p></li><li><p>Uma coluna AutoIncrement não pode ser marcada.</p></li><li><p>Uma coluna de versão não pode ser marcada.</p></li></ul> | 
| <p>JET_errExclusiveTableLockRequired</p> | <p>Um bloqueio exclusivo na tabela era necessário para esta operação.</p> | 
| <p>JET_wrnColumnMaxTruncated</p> | <p>Um aviso que indica que o comprimento máximo (<em>cbMax</em>) de uma coluna fixa ou variável foi maior que JET_cbColumnMost. Esse limite não se aplica a valores longos ( <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> e <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p> | 



#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetAddColumnW</strong> (Unicode) e <strong>JetAddColumnA</strong> (ANSI).</p> | 



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
