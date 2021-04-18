---
description: 'Saiba mais sobre: função JetCreateIndex'
title: Função JetCreateIndex
TOCTitle: JetCreateIndex Function
ms:assetid: d164e74a-7719-4587-9059-8fb18b365133
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294099(v=EXCHG.10)
ms:contentKeyID: 32765714
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndexA
- JetCreateIndex
- JetCreateIndexW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c0208a5f0adac4ff5128b506123f3b68589cd0d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785187"
---
# <a name="jetcreateindex-function"></a>Função JetCreateIndex


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetcreateindex-function"></a>Função JetCreateIndex

A função **JetCreateIndex** permite que você crie um índice de dados em um ESE (mecanismo de armazenamento extensível), que pode ser usado para localizar dados específicos rapidamente.

```cpp
    JET_ERR JET_API JetCreateIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit,
      __in          const tchar* szKey,
      __in          unsigned long cbKey,
      __in          unsigned long lDensity
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para uma chamada de API específica.

*TableID*

A tabela para a qual um índice será criado.

*szIndexName*

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do índice a ser criado.

O nome do índice deve estar de acordo com as seguintes diretrizes:

  - Ele deve conter menos caracteres que JET_cbNameMost, não incluindo o caractere nulo de terminação.

  - Ele deve conter somente caracteres das seguintes categorias: 0 a 9, A a Z, a a z e todos os caracteres de pontuação, exceto para " \! " (ponto de exclamação), "," (vírgula), " \[ " (colchete de abertura) e " \] " (colchete de fechamento) — ou seja, os caracteres ASCII 0x20, 0x22 a 0x2d, 0x2F a 0x5A, 0x5c e 0x5d até 0x7F.

  - Ele não deve começar com um espaço.

  - Ele deve conter pelo menos um caractere que não seja de espaço.

*grbit*

Um grupo de bits que contém as opções a serem usadas para uma chamada específica. Esse parâmetro pode incluir zero ou mais das opções encontradas na estrutura de [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

*szKey*

Um ponteiro para uma cadeia de caracteres dupla com terminação nula de tokens delimitados por nulo.

Para obter mais informações sobre esse parâmetro, consulte a estrutura de [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

*cbKey*

O comprimento, em bytes, do parâmetro *szKey* , incluindo os dois caracteres nulos de terminação.

*lDensity*

A densidade percentual da árvore inicial do índice B +.

Para obter mais informações sobre esse parâmetro, consulte a estrutura de [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno listados na tabela a seguir. Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código de retorno</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>A operação foi concluída com sucesso.</p></td>
</tr>
</tbody>
</table>


Para obter uma lista de erros adicionais que podem ser retornados pela função **JetCreateIndex** , consulte [JetCreateIndex2](./jetcreateindex2-function.md).

#### <a name="remarks"></a>Comentários

Chamar a função **JetCreateIndex** é idêntico a chamar a função [JetCreateIndex2](./jetcreateindex2-function.md) com uma estrutura [JET_INDEXCREATE](./jet-indexcreate-structure.md) que contém as mesmas configurações que os parâmetros de **JetCreateIndex** e um parâmetro *cIndexCreate* igual a 1. Para os campos da estrutura de [JET_INDEXCREATE](./jet-indexcreate-structure.md) que não têm parâmetros correspondentes em **JetCreateIndex**, é assumido um valor de 0.

Observe que **JetCreateIndex** foi substituído pelo [JetCreateIndex2](./jetcreateindex2-function.md).

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Cliente</p></td>
<td><p>Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p>Servidor</p></td>
<td><p>Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p>parâmetro</p></td>
<td><p>É declarado em ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p>Biblioteca</p></td>
<td><p>Usa ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p>DLL</p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p>Unicode</p></td>
<td><p>É implementado como <strong>JetCreateIndexW</strong> (Unicode) e <strong>JetCreateIndexA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
