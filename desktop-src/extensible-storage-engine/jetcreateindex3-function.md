---
description: 'Saiba mais sobre: Função JetCreateIndex3'
title: Função JetCreateIndex3
TOCTitle: JetCreateIndex3 Function
ms:assetid: bc9b940e-65c6-49d6-ad32-74434527d29f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294075(v=EXCHG.10)
ms:contentKeyID: 32765690
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndex3A
- JetCreateIndex3
- JetCreateIndex3W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bb8e2eec2fe0b60245884b654f99353480833f27
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465413"
---
# <a name="jetcreateindex3-function"></a>Função JetCreateIndex3


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetcreateindex3-function"></a>Função JetCreateIndex3

A **função JetCreateIndex3** cria índices sobre dados em um banco de dados ESE, que podem ser usados para localizar dados específicos rapidamente.

**Windows 7: JetCreateIndex3** é introduzido no sistema operacional Windows 7.

```cpp
    JET_ERR JET_API JetCreateIndex3(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_INDEXCREATE2* pindexcreate,
      __in          unsigned long cIndexCreate
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto de sessão do banco de dados a ser usado para a chamada à API.

*Tableid*

A tabela na qual o índice será criado.

*pindexcreate*

Uma matriz de [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) estruturas, cada uma das quais define um índice a ser criado.

*cIndexCreate*

O número de elementos na matriz *pindexcreate.*

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errCannotIndex</p> | <p>Foi feita uma tentativa de indexar em uma coluna Escrow-update ou SLV (observe que as colunas SLV foram preterida).</p> | 
| <p>JET_errColumnNotFound</p> | <p>Foi feita uma tentativa de indexar em uma coluna inexistente. Tentar indexar condicionalmente em uma coluna inexistente também pode produzir esse erro.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Esse erro será retornado se o <strong>membro ulDensity</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for definido como um número menor que 20 ou maior que 100.</p> | 
| <p>JET_errIndexDuplicate</p> | <p>Foi feita uma tentativa de definir dois índices idênticos.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Foi feita uma tentativa de especificar mais de um índice primário para uma tabela. Uma tabela deve ter exatamente um índice primário. Se nenhum índice primário for especificado, o mecanismo de banco de dados criará um de forma transparente.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Uma definição de índice inválida foi especificada. A seguir estão alguns possíveis motivos para receber esse erro:</p><ul><li><p>Um índice primário é condicional (<strong>o membro grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem JET_bitIndexPrimary definido e o membro <strong>cConditionalColumn</strong> do <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é maior que zero).</p></li><li><p>Windows Server 2003 e versões posteriores do Windows. Tentar criar um índice de tupla com limites de tupla, mas sem passar informações no membro <strong>ptuplelimits</strong> no <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (ou seja, <em>grbit</em> tem JET_bitIndexTupleLimits definido, mas o ponteiro <strong>ptuplelimits</strong> é NULL).</p></li><li><p>Passando uma definição de chave inválida no <strong>membro szKey</strong> da <a href="gg294082(v=exchg.10).md">estrutura JET_INDEXCREATE2</a> dados. Consulte <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> para uma discussão sobre definições válidas.</p></li><li><p>Definir o <strong>membro cbVarSegMac</strong> <a href="gg294082(v=exchg.10).md">no JET_INDEXCREATE2</a> ser maior que JET_cbPrimaryKeyMost (para um índice primário) ou maior que JET_cbSecondaryKeyMost (para um índice secundário).</p></li><li><p>Passando uma combinação inválida para um índice Unicode definido pelo usuário (um que tem o bit JET_bitIndexUnicode definido no <strong>membro grbit</strong> do <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>). Algumas causas comuns podem ser que o campo pidxunicode da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é NULL ou o LCID especificado na estrutura pidxunicode é inválido.</p></li><li><p>Especificando uma coluna com vários valores para um índice primário.</p></li><li><p>Tentando indexar muitas colunas condicionais. O <strong>membro cConditionalColumn</strong> da <a href="gg294082(v=exchg.10).md">estrutura JET_INDEXCREATE2</a> não deve ser maior que JET_ccolKeyMost.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Windows XP e versões posteriores Windows. Uma <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> estrutura de dados foi especificada e seus limites não têm suporte. Consulte a seção de comentários da estrutura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> dados.</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Windows XP e versões posteriores Windows. Um índice de tupla não pode ser exclusivo (<em>grbit</em> não deve ter JET_bitIndexTuples e JET_bitIndexUnique definidos).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Windows XP e versões posteriores Windows. Um índice de tupla só pode ser sobre uma única coluna (ou seja, o membro <strong>grbit</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem JET_bitIndexTuples definido e o membro <strong>szKey</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> especifica mais de uma coluna).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Windows XP e versões posteriores Windows. Um índice de tupla não pode ser um índice primário (ou seja, o <strong>membro grbit</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não deve ter JET_bitIndexPrimary e JET_bitIndexTuples definidos).</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Windows XP e versões posteriores Windows. Um índice de tupla só pode estar em um texto ou coluna Unicode. Uma tentativa de indexar outras colunas (por exemplo, colunas binárias) resultará em JET_errIndexTuplesTextColumnsOnly.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Windows XP e versões posteriores Windows. Um índice de tupla não permite que <strong>o membro cbVarSegMac</strong> <a href="gg294082(v=exchg.10).md">da estrutura JET_INDEXCREATE2</a> seja definido.</p> | 
| <p>JET_errInTransaction</p> | <p>Foi feita uma tentativa de criar um índice sem informações de versão durante uma transação.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>A definição de índice é inválida porque o <strong>membro grbit</strong> da <a href="gg294082(v=exchg.10).md">estrutura JET_INDEXCREATE2</a> contém valores inconsistentes. Veja a seguir alguns motivos possíveis:</p><ul><li><p>Um índice primário tinha um bit de ignorar especificado (JET_bitIndexPrimary foi passado com um dos JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull ou JET_bitIndexIgnoreFirstNull).</p></li><li><p>Um índice vazio não ignora nenhum campo NULL (ou seja, o <strong>membro grbit</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem JET_bitIndexEmpty definido, mas não tem JET_bitIndexIgnoreAnyNull definido).</p></li><li><p>Passando uma <a href="gg269214(v=exchg.10).md">estrutura JET_CONDITIONALCOLUMN</a> com um membro <strong>grbit</strong> inválido. Consulte <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</p></li></ul><p>Ao criar vários índices ao mesmo tempo (ou seja, se o parâmetro <em>cIndexCreate</em> for maior que um), nenhum dos índices poderá conter nenhum dos seguintes bits:</p><ul><li><p>JET_bitIndexPrimary</p></li><li><p>JET_bitIndexUnversioned</p></li><li><p>JET_bitIndexEmpty</p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>Uma LCID (ID de localidade) inválida foi passada (por meio do membro <strong>lcid</strong> na estrutura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX,</a> para a qual o membro <strong>pidxunicode</strong> na estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contém um ponteiro ou por meio do membro <strong>lcid</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2).</a></p> | 
| <p>JET_errInvalidName</p> | <p>Um nome de índice inválido foi especificado. Consulte <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> para obter mais detalhes.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um parâmetro inválido foi passado para a API. Veja a seguir alguns motivos pelos quais esse erro pode ser retornado:</p><ul><li><p>O <strong>campo cbKey</strong> de uma <a href="gg294082(v=exchg.10).md">estrutura JET_INDEXCREATE2</a> é definido como zero.</p></li><li><p>O <strong>membro cbStruct</strong> de uma <a href="gg294082(v=exchg.10).md">estrutura JET_INDEXCREATE2</a> não está definido como sizeof( <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</p></li></ul> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Ocorreu um erro ao tentar normalizar uma coluna Unicode. Isso pode ser causado pela falta de recursos do sistema.</p> | 
| <p>JET_errSpaceHintsInvalid</p> | <p>Um elemento da estrutura de dicas de espaço JET não estava correto ou a ação.</p> | 



#### <a name="remarks"></a>Comentários

O valor de retorno é JET_errSuccess a conclusão bem-sucedida de todos os índices especificados.

**JetCreateIndex3** itera pelos índices determinados em **pindexcriar** e, às vezes, anulará na primeira falha. Os índices após o primeiro índice com um erro podem não ter sido tentados, mesmo que o membro **err** da estrutura JET_INDEXCREATE2 [contenha](./jet-indexcreate2-structure.md) JET_errSuccess.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetCreateIndex3W</strong> (Unicode) e <strong>JetCreateIndex3A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE2](./jet-indexcreate2-structure.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JET_SPACEHINTS](./jet-spacehints-structure.md)
