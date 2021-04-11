---
description: 'Saiba mais sobre: função JetCreateIndex3'
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
ms.openlocfilehash: c4f3331a903d4885499ff6c2cd2cad0d8b8534a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297042"
---
# <a name="jetcreateindex3-function"></a>Função JetCreateIndex3


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetcreateindex3-function"></a>Função JetCreateIndex3

A função **JetCreateIndex3** cria índices em um banco de dados ESE, que pode ser usado para localizar dados específicos rapidamente.

**Windows 7: o JetCreateIndex3** é introduzido no sistema operacional Windows 7.

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

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*TableID*

A tabela na qual o índice será criado.

*pindexcreate*

Uma matriz de estruturas [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , cada uma delas define um índice a ser criado.

*cIndexCreate*

O número de elementos na matriz *pindexcreate* .

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
<td><p>JET_errCannotIndex</p></td>
<td><p>Foi feita uma tentativa de indexar uma coluna de atualização de caução ou SLV (Observe que as colunas SLV foram preteridas).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Foi feita uma tentativa de indexar uma coluna não existente. A tentativa de indexar condicionalmente uma coluna não existente também pode produzir esse erro.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid</p></td>
<td><p>Esse erro será retornado se o membro <strong>ulDensity</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for definido como um número inferior a 20 ou maior que 100.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexDuplicate</p></td>
<td><p>Foi feita uma tentativa de definir dois índices idênticos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexHasPrimary</p></td>
<td><p>Foi feita uma tentativa de especificar mais de um índice primário para uma tabela. Uma tabela deve ter exatamente um índice primário. Se nenhum índice primário for especificado, o mecanismo de banco de dados criará de forma transparente um.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>Uma definição de índice inválida foi especificada. Estes são alguns motivos possíveis para receber esse erro:</p>
<ul>
<li><p>Um índice primário é condicional (<strong>grbit</strong> membro de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem JET_bitIndexPrimary definido e o membro <strong>cConditionalColumn</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é maior que zero).</p></li>
<li><p>Windows Server 2003 e versões posteriores do Windows. Tentativa de criar um índice de tupla com limites de tupla, mas sem passar informações no membro <strong>ptuplelimits</strong> em <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (ou seja, <em>grbit</em> tem JET_bitIndexTupleLimits definido, mas o ponteiro <strong>ptuplelimits</strong> é nulo).</p></li>
<li><p>Passando uma definição de chave inválida no membro <strong>szKey</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> . Consulte <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> para obter uma discussão sobre definições válidas.</p></li>
<li><p>Definir o membro <strong>cbVarSegMac</strong> em <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ser maior que JET_cbPrimaryKeyMost (para um índice primário) ou maior que JET_cbSecondaryKeyMost (para um índice secundário).</p></li>
<li><p>Passando uma combinação inválida para um índice Unicode definido pelo usuário (um que tem o conjunto de bits JET_bitIndexUnicode no membro <strong>grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>). Algumas causas comuns podem ser que o campo pidxunicode da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é nulo ou o LCID especificado na estrutura pidxunicode é inválido.</p></li>
<li><p>Especificando uma coluna com valores múltiplos para um índice primário.</p></li>
<li><p>Tentando indexar muitas colunas condicionais. O membro <strong>cConditionalColumn</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não deve ser maior que JET_ccolKeyMost.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Windows XP e versões posteriores do Windows. Uma estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> foi especificada e não há suporte para seus limites. Consulte a seção comentários da estrutura de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesNonUniqueOnly</p></td>
<td><p>Windows XP e versões posteriores do Windows. Um índice de tupla não pode ser exclusivo (<em>grbit</em> não deve ter JET_bitIndexTuples e JET_bitIndexUnique definido).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesOneColumnOnly</p></td>
<td><p>Windows XP e versões posteriores do Windows. Um índice de tupla só pode ser em uma única coluna (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem JET_bitIndexTuples definido, e o membro <strong>szKey</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> especifica mais de uma coluna).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesSecondaryIndexOnly</p></td>
<td><p>Windows XP e versões posteriores do Windows. Um índice de tupla não pode ser um índice primário (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não deve ter JET_bitIndexPrimary e JET_bitIndexTuples definido).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesTextColumnsOnly</p></td>
<td><p>Windows XP e versões posteriores do Windows. Um índice de tupla só pode estar em uma coluna de texto ou Unicode. Uma tentativa de indexar outras colunas (por exemplo, colunas binárias) resultará em JET_errIndexTuplesTextColumnsOnly.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed</p></td>
<td><p>Windows XP e versões posteriores do Windows. Um índice de tupla não permite que o membro <strong>cbVarSegMac</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> seja definida.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInTransaction</p></td>
<td><p>Foi feita uma tentativa de criar um índice sem informações de versão em uma transação.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>A definição de índice é inválida porque o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contém valores inconsistentes. Estes são alguns motivos possíveis:</p>
<ul>
<li><p>Um índice primário tinha um bit de ignorar especificado (JET_bitIndexPrimary foi passado com um dos JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull ou JET_bitIndexIgnoreFirstNull).</p></li>
<li><p>Um índice vazio não ignora nenhum campo nulo (ou seja, o membro <strong>grbit</strong> da estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> tem JET_bitIndexEmpty definido, mas não tem JET_bitIndexIgnoreAnyNull definido).</p></li>
<li><p>Passando uma estrutura de <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> com um membro <strong>grbit</strong> inválido. Consulte <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</p></li>
</ul>
<p>Ao criar vários índices de uma vez (ou seja, se o parâmetro <em>cIndexCreate</em> for maior que um), nenhum dos índices poderá conter qualquer um dos seguintes bits:</p>
<ul>
<li><p>JET_bitIndexPrimary</p></li>
<li><p>JET_bitIndexUnversioned</p></li>
<li><p>JET_bitIndexEmpty</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Uma LCID (identificação de localidade) inválida foi passada (por meio do membro <strong>LCID</strong> na estrutura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , que o membro <strong>pidxunicode</strong> na estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contém um ponteiro para, ou por meio do membro <strong>LCID</strong> da estrutura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidName</p></td>
<td><p>Um nome de índice inválido foi especificado. Consulte <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> para obter mais detalhes.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um parâmetro inválido foi passado para a API. A seguir estão alguns motivos pelos quais esse erro pode ser retornado:</p>
<ul>
<li><p>O campo <strong>cbKey</strong> de uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> é definido como zero.</p></li>
<li><p>O membro <strong>cbStruct</strong> de uma estrutura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> não está definido como sizeof ( <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeTranslationFail</p></td>
<td><p>Ocorreu um erro ao tentar normalizar uma coluna Unicode. Isso pode ser causado pela execução de recursos do sistema.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSpaceHintsInvalid</p></td>
<td><p>Um elemento da estrutura de dicas de espaço JET não estava correto ou é acionável.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Comentários

O valor de retorno é JET_errSuccess na conclusão bem-sucedida de todos os índices especificados.

**JetCreateIndex3** faz a iteração pelos índices fornecidos em **pindexcreate** e, às vezes, anulará na primeira falha. Todos os índices após o primeiro índice com um erro podem não ter sido tentados, mesmo que o membro **Err** da estrutura de [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) contenha JET_errSuccess.

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
<td><p>Implementado como <strong>JetCreateIndex3W</strong> (Unicode) e <strong>JetCreateIndex3A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


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
