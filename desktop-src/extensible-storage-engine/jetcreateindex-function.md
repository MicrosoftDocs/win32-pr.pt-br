---
description: 'Saiba mais sobre: Função JetCreateIndex'
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
ms.openlocfilehash: 698f9a050415568c06c8e10819cfed12a4a17181
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478392"
---
# <a name="jetcreateindex-function"></a>Função JetCreateIndex


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetcreateindex-function"></a>Função JetCreateIndex

A **função JetCreateIndex** permite que você crie um índice de dados em um banco de dados ESE (Extensible Armazenamento Engine), que você pode usar para localizar dados específicos rapidamente.

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

O contexto de sessão do banco de dados a ser usado para uma chamada à API específica.

*Tableid*

A tabela para a que um índice será criado.

*szIndexName*

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do índice a ser criado.

O nome do índice deve estar em conformidade com as seguintes diretrizes:

  - Ele deve conter menos caracteres do que JET_cbNameMost, não incluindo o caractere nulo de terminação.

  - Ele deve conter apenas caracteres das seguintes categorias: 0 a 9, A a Z, a a z e todos os caracteres de pontuação, exceto " \! " (ponto de exclamação), "," (vírgula), " " (colchete de abertura) e " " (colchete de fechamento) — ou seja, os caracteres ASCII 0x20, 0x22 por meio de 0x2d, 0x2f por meio de \[ \] 0x5a, 0x5c e 0x5d por 0x7f.

  - Ele não deve começar com um espaço.

  - Ele deve conter pelo menos um caractere sem espaço.

*grbit*

Um grupo de bits que contém as opções a serem usadas para uma chamada específica. Esse parâmetro pode incluir zero ou mais das opções encontradas na [estrutura JET_INDEXCREATE](./jet-indexcreate-structure.md) dados.

*szKey*

Um ponteiro para uma cadeia de caracteres terminada em nulo dupla de tokens delimitados por nulo.

Para obter mais informações sobre esse parâmetro, consulte a [estrutura JET_INDEXCREATE](./jet-indexcreate-structure.md) dados.

*cbKey*

O comprimento, em bytes, do *parâmetro szKey,* incluindo os dois caracteres nulos de terminação.

*lDensity*

A densidade percentual da árvore de índice B+ inicial.

Para obter mais informações sobre esse parâmetro, consulte a [estrutura JET_INDEXCREATE](./jet-indexcreate-structure.md) dados.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno listados na tabela a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Significado</p> | 
|--------------------|----------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 



Para obter uma lista de erros adicionais que podem ser retornados pela **função JetCreateIndex,** consulte [JetCreateIndex2](./jetcreateindex2-function.md).

#### <a name="remarks"></a>Comentários

Chamar a **função JetCreateIndex** é idêntico a chamar a função [JetCreateIndex2](./jetcreateindex2-function.md) com uma estrutura JET_INDEXCREATE que contém as mesmas configurações que os parâmetros de **JetCreateIndex** e um parâmetro *cIndexCreate* igual [a](./jet-indexcreate-structure.md) 1. Para os campos da estrutura [JET_INDEXCREATE](./jet-indexcreate-structure.md) que não têm parâmetros correspondentes em **JetCreateIndex,** um valor de 0 é assumido.

Observe que **JetCreateIndex** foi superado por [JetCreateIndex2](./jetcreateindex2-function.md).

#### <a name="requirements"></a>Requisitos


| | | <p>Cliente</p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p>Servidor</p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p>Cabeçalho</p> | <p>É declarado em Esent.h.</p> | | <p>Biblioteca</p> | <p>Usa ESENT.lib.</p> | | <p>DLL</p> | <p>Requer ESENT.dll.</p> | | <p>Unicode</p> | <p>É implementado como <strong>JetCreateIndexW</strong> (Unicode) e <strong>JetCreateIndexA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
