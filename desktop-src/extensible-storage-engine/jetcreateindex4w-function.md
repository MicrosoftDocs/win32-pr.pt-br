---
description: 'Saiba mais sobre: função JetCreateIndex4W'
title: Função JetCreateIndex4W
TOCTitle: JetCreateIndex4W Function
ms:assetid: 968745a2-66ce-4c7f-ab5b-43282adc5313
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835044(v=EXCHG.10)
ms:contentKeyID: 49894666
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c79f1638645f0dcd7e4306f543a9ee15b9668843
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987439"
---
# <a name="jetcreateindex4w-function"></a>Função JetCreateIndex4W


_**Aplica-se a:** Windows | Windows Servidor_

a função **JetCreateIndex4W** cria índices em um banco de dados ESE (Extensible Armazenamento Engine), que pode ser usado para localizar dados específicos rapidamente.

a função **JetCreateIndex4W** foi introduzida no sistema operacional Windows 8.

``` c++
JET_ERR JET_API JetCreateIndex4W(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_INDEXCREATE2* pindexcreate,
  __in          unsigned long cIndexCreate
);
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*TableID*

A tabela na qual o índice será criado.

*pindexcreate*

Uma matriz de estruturas [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , cada uma delas define um índice a ser criado.

*cIndexCreate*

O número de elementos na matriz *pindexcreate* .

### <a name="return-value"></a>Valor retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno listados na tabela a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errCannotIndex</p> | <p>Foi feita uma tentativa de indexar uma coluna de atualização de caução ou SLV (Observe que as colunas SLV foram preteridas).</p> | 
| <p>JET_errColumnNotFound</p> | <p>Foi feita uma tentativa de indexar uma coluna inexistente. Uma tentativa de indexar condicionalmente uma coluna inexistente também pode produzir esse erro.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Esse erro será retornado se o membro <strong>ulDensity</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for definido como um número inferior a 20 ou maior que 100.</p> | 
| <p>JET_errIndexDuplicate</p> | <p>Foi feita uma tentativa de definir dois índices idênticos.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Foi feita uma tentativa de especificar mais de um índice primário para uma tabela. Uma tabela deve ter exatamente um índice primário. Se nenhum índice primário for especificado, o mecanismo de banco de dados criará de forma transparente um.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Uma definição de índice inválida foi especificada. Estes são alguns motivos possíveis para esse erro:</p><ul><li><p>Um índice primário é condicional (<strong>grbit</strong> membro de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem <strong>JET_bitIndexPrimary</strong> definido e o membro <strong>cConditionalColumn</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é maior que zero).</p></li><li><p>aplica-se às versões do Windows a partir do Windows Server 2003. Foi feita uma tentativa de criar um índice de tupla com limites de tupla, mas sem passar informações no membro <strong>ptuplelimits</strong> em <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (ou seja, <em>grbit</em> tem <strong>JET_bitIndexTupleLimits</strong> definido, mas o ponteiro <strong>ptuplelimits</strong> é nulo).</p></li><li><p>Passando uma definição de chave inválida no membro <strong>szKey</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> . Para obter informações sobre definições válidas, consulte <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</p></li><li><p>Definir o membro <strong>cbVarSegMac</strong> em <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ser maior que <strong>JET_cbPrimaryKeyMost</strong> (para um índice primário) ou maior que <strong>JET_cbSecondaryKeyMost</strong> (para um índice secundário).</p></li><li><p>Passando uma combinação inválida para um índice Unicode definido pelo usuário (um que tem o conjunto de bits <strong>JET_bitIndexUnicode</strong> no membro <strong>grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>). Algumas causas comuns podem ser que o campo pidxunicode da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é nulo ou o LCID especificado na estrutura pidxunicode é inválido.</p></li><li><p>Especificando uma coluna com valores de um índice primário.</p></li><li><p>Tentando indexar muitas colunas condicionais. O membro <strong>cConditionalColumn</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não deve ser maior que <strong>JET_ccolKeyMost</strong>.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>aplica-se às versões do Windows a partir do Windows XP. Uma estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> foi especificada e não há suporte para seus limites. Para obter mais informações, consulte a seção comentários da estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>aplica-se às versões do Windows a partir do Windows XP. Um índice de tupla não pode ser exclusivo (<em>grbit</em> não deve ter <strong>JET_bitIndexTuples</strong> e <strong>JET_bitIndexUnique</strong> definido).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>aplica-se às versões do Windows a partir do Windows XP. Um índice de tupla só pode ser em uma única coluna (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem <strong>JET_bitIndexTuples</strong> definido, e o membro <strong>szKey</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> especifica mais de uma coluna).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>aplica-se às versões do Windows a partir do Windows XP. Um índice de tupla não pode ser um índice primário (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não deve ter <strong>JET_bitIndexPrimary</strong> e <strong>JET_bitIndexTuples</strong> definido).</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>aplica-se às versões do Windows a partir do Windows XP. Um índice de tupla só pode estar em uma coluna de texto ou Unicode. Uma tentativa de indexar outras colunas (por exemplo, colunas binárias) resultará em <strong>JET_errIndexTuplesTextColumnsOnly</strong>.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>aplica-se às versões do Windows a partir do Windows XP. Um índice de tupla não permite que o membro <strong>cbVarSegMac</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> seja definida.</p> | 
| <p>JET_errInTransaction</p> | <p>Foi feita uma tentativa de criar um índice sem informações de versão em uma transação.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>A definição de índice é inválida porque o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contém valores inconsistentes. Estes são alguns motivos possíveis:</p><ul><li><p>Um índice primário tinha um bit de ignorar especificado (JET_bitIndexPrimary foi passado com um dos <strong>JET_bitIndexIgnoreNull</strong>, <strong>JET_bitIndexIgnoreAnyNull</strong>ou <strong>JET_bitIndexIgnoreFirstNull</strong>).</p></li><li><p>Um índice vazio não ignora nenhum campo nulo (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem <strong>JET_bitIndexEmpty</strong> definido, mas não tem <strong>JET_bitIndexIgnoreAnyNull</strong> definido).</p></li><li><p>Passando uma estrutura de <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> com um membro <strong>grbit</strong> inválido. Consulte <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</p></li></ul><p>Ao criar vários índices de uma vez (ou seja, se o parâmetro <em>cIndexCreate</em> for maior que um), nenhum dos índices poderá conter qualquer um dos seguintes bits:</p><ul><li><p><strong>JET_bitIndexPrimary</strong></p></li><li><p><strong>JET_bitIndexUnversioned</strong></p></li><li><p><strong>JET_bitIndexEmpty</strong></p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>Uma LCID (identificação de localidade) inválida foi passada (por meio do membro <strong>LCID</strong> na estrutura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , que o membro <strong>pidxunicode</strong> na estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contém um ponteiro para, ou por meio do membro <strong>LCID</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</p> | 
| <p>JET_errInvalidName</p> | <p>Um nome de índice inválido foi especificado. Consulte <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> para obter mais detalhes.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um parâmetro inválido foi passado para a API. A seguir estão alguns motivos pelos quais esse erro pode ser retornado:</p><ul><li><p>O campo <strong>cbKey</strong> de uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é definido como zero.</p></li><li><p>O membro <strong>cbStruct</strong> de uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não está definido como sizeof (JET_INDEXCREATE2).</p></li></ul> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Ocorreu um erro ao tentar normalizar uma coluna Unicode. Isso pode ser causado pela execução de recursos do sistema.</p> | 
| <p>JET_errSpaceHintsInvalid</p> | <p>Um elemento da estrutura de dicas de espaço JET não estava correto ou é acionável.</p> | 



#### <a name="remarks"></a>Comentários

A função **JetCreateIndex4W** itera através dos índices fornecidos no parâmetro *pindexcreate* e, às vezes, é anulada na primeira falha. Todos os índices após o primeiro índice com um erro podem não ter sido tentados, mesmo que o membro **Err** da estrutura de [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) contenha JET_errSuccess.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows 8.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2012.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte também

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
