---
description: 'Saiba mais sobre: função JetCreateIndex2'
title: Função JetCreateIndex2
TOCTitle: JetCreateIndex2 Function
ms:assetid: 8810eaed-40cb-4561-aafc-9a9bbdb0d05b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269324(v=EXCHG.10)
ms:contentKeyID: 32765614
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndex2W
- JetCreateIndex2A
- JetCreateIndex2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fc11fe1e5d2b4d6f14ad77cb98434b0daf6b81f1
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987449"
---
# <a name="jetcreateindex2-function"></a>Função JetCreateIndex2


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetcreateindex2-function"></a>Função JetCreateIndex2

A função **JetCreateIndex2** cria índices em um banco de dados ESE, que pode ser usado para localizar dados específicos rapidamente.

```cpp
    JET_ERR JET_API JetCreateIndex2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_INDEXCREATE* pindexcreate,
      __in          unsigned long cIndexCreate
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*TableID*

A tabela na qual o índice será criado.

*pindexcreate*

Uma matriz de estruturas [JET_INDEXCREATE](./jet-indexcreate-structure.md) , cada uma delas define um índice a ser criado.

*cIndexCreate*

O número de elementos na matriz *pindexcreate* .

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errCannotIndex</p> | <p>Foi feita uma tentativa de indexar uma coluna de atualização de caução ou SLV (Observe que as colunas SLV foram preteridas).</p> | 
| <p>JET_errColumnNotFound</p> | <p>Foi feita uma tentativa de indexar uma coluna não existente. A tentativa de indexar condicionalmente uma coluna não existente também pode produzir esse erro.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Esse erro será retornado se o membro <strong>ulDensity</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for definido como um número inferior a 20 ou maior que 100.</p> | 
| <p>JET_errIndexDuplicate</p> | <p>Foi feita uma tentativa de definir dois índices idênticos.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Foi feita uma tentativa de especificar mais de um índice primário para uma tabela. Uma tabela deve ter exatamente um índice primário. Se nenhum índice primário for especificado, o mecanismo de banco de dados criará de forma transparente um.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Uma definição de índice inválida foi especificada. Alguns dos motivos possíveis para receber esse erro são:</p><ul><li><p>Um índice primário é condicional (<strong>grbit</strong> membro de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tem JET_bitIndexPrimary definido e o membro <strong>cConditionalColumn</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> é maior que zero).</p></li><li><p>Windows Server 2003 e posterior. Tentativa de criar um índice de tupla com limites de tupla, mas sem passar informações no membro <strong>ptuplelimits</strong> em <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (ou seja, <em>grbit</em> tem JET_bitIndexTupleLimits definido, mas o ponteiro <strong>ptuplelimits</strong> é nulo).</p></li><li><p>Passando uma definição de chave inválida no membro <strong>szKey</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> . Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter uma discussão sobre definições válidas.</p></li><li><p>Definir o membro <strong>cbVarSegMac</strong> em <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ser maior que JET_cbPrimaryKeyMost (para um índice primário) ou maior que JET_cbSecondaryKeyMost (para um índice secundário).</p></li><li><p>Passando uma combinação inválida para um índice Unicode definido pelo usuário (um que tem o conjunto de bits JET_bitIndexUnicode no membro <strong>grbit</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>). Algumas causas comuns podem ser que o campo pidxunicode da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> é nulo ou o LCID especificado na estrutura pidxunicode é inválido.</p></li><li><p>Especificando uma coluna com valores múltiplos para um índice primário.</p></li><li><p>Tentando indexar muitas colunas condicionais. O membro <strong>cConditionalColumn</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> não deve ser maior que JET_ccolKeyMost.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Windows XP e posterior. Uma estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> foi especificada e não há suporte para seus limites. Consulte a seção comentários da estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Windows XP e posterior. Um índice de tupla não pode ser exclusivo (<em>grbit</em> não deve ter JET_bitIndexTuples e JET_bitIndexUnique definido).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Windows XP e posterior. Um índice de tupla só pode ser em uma única coluna (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tem JET_bitIndexTuples definido, e o membro <strong>szKey</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> especifica mais de uma coluna).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Windows XP e posterior. Um índice de tupla não pode ser um índice primário (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> não deve ter JET_bitIndexPrimary e JET_bitIndexTuples definido).</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Windows XP e posterior. Um índice de tupla só pode estar em uma coluna de texto ou Unicode. Uma tentativa de indexar outras colunas (por exemplo, colunas binárias) resultará em JET_errIndexTuplesTextColumnsOnly.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Windows XP e posterior. Um índice de tupla não permite que o membro <strong>cbVarSegMac</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> seja definida.</p> | 
| <p>JET_errInTransaction</p> | <p>Foi feita uma tentativa de criar um índice sem informações de versão em uma transação.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>A definição de índice é inválida porque o membro <strong>grbit</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> contém valores inconsistentes. Alguns motivos possíveis são:</p><ul><li><p>Um índice primário tinha um bit de ignorar especificado (JET_bitIndexPrimary foi passado com um dos JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull ou JET_bitIndexIgnoreFirstNull).</p></li><li><p>Um índice vazio não ignora nenhum campo nulo (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> tem JET_bitIndexEmpty definido, mas não tem JET_bitIndexIgnoreAnyNull definido).</p></li><li><p>Passando uma estrutura de <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> com um membro <strong>grbit</strong> inválido. Consulte <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</p></li></ul><p>Ao criar vários índices de uma vez (ou seja, se o parâmetro <em>cIndexCreate</em> for maior que um), nenhum dos índices poderá conter qualquer um dos seguintes bits:</p><ul><li><p>JET_bitIndexPrimary</p></li><li><p>JET_bitIndexUnversioned</p></li><li><p>JET_bitIndexEmpty</p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>Uma LCID (identificação de localidade) inválida foi passada (por meio do membro <strong>LCID</strong> na estrutura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , que o membro <strong>pidxunicode</strong> na estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> contém um ponteiro para, ou por meio do membro <strong>LCID</strong> da estrutura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</p> | 
| <p>JET_errInvalidName</p> | <p>Um nome de índice inválido foi especificado. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obter mais detalhes.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um parâmetro inválido foi passado para a API. Alguns dos motivos pelos quais esse erro pode ser retornado são:</p><ul><li><p>O campo <strong>cbKey</strong> de uma estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> é definido como zero.</p></li><li><p>O membro <strong>cbStruct</strong> de uma estrutura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> não está definido como sizeof (<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</p></li></ul> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Ocorreu um erro ao tentar normalizar uma coluna Unicode. Isso pode ser causado pela execução de recursos do sistema.</p> | 



#### <a name="remarks"></a>Comentários

O valor de retorno é JET_errSuccess na conclusão bem-sucedida de todos os índices especificados.

**JetCreateIndex2** faz a iteração pelos índices fornecidos em **pindexcreate** e, às vezes, anulará na primeira falha. Todos os índices após o primeiro índice com um erro podem não ter sido tentados, mesmo que o membro **Err** da estrutura de [JET_INDEXCREATE](./jet-indexcreate-structure.md) contenha JET_errSuccess.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetCreateIndex2W</strong> (Unicode) e <strong>JetCreateIndex2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
