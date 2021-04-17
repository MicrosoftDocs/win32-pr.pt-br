---
description: 'Saiba mais sobre: colunas esparsas com vários valores'
title: Colunas esparsas com valores múltiplos
TOCTitle: Multi-Valued Sparse Columns
ms:assetid: 36e82a73-aad4-4e0d-a743-a2182c41fe9c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269225(v=EXCHG.10)
ms:contentKeyID: 32765527
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 21448d50e17881517086c1b258dcce02e84286a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780672"
---
# <a name="multi-valued-sparse-columns"></a>Colunas esparsas com valores múltiplos


_**Aplica-se a:** Windows | Windows Server_

## <a name="multi-valued-sparse-columns"></a>Colunas esparsas com valores múltiplos

As colunas esparsas podem ser fixas ou ter comprimento variável, e são exclusivas, pois não ocupam espaço em um registro se forem nulas ou saírem do valor padrão. Colunas esparsas, também chamadas de colunas marcadas, podem conter mais de um valor em um único registro. As colunas marcadas podem ser qualquer um dos tipos de colunas descritos nas constantes [JET_coltyp](./jet-coltyp.md) . Eles são criados quando a coluna é adicionada à tabela, definindo o sinalizador JET_bitColumnTagged na estrutura de [JET_COLUMNDEF](./jet-columndef-structure.md) na chamada para [JetAddColumn](./jetaddcolumn-function.md)ou na estrutura [JET_COLUMNCREATE](./jet-columncreate-structure.md) usada na chamada para [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) ou [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md). As colunas do tipo JET_coltypLongText e JET_coltypLongBinary são criadas automaticamente como colunas marcadas.

Somente colunas marcadas podem conter vários valores em um registro, colunas de comprimento fixo ou variável não podem conter vários valores. Há dois tipos de colunas com valores múltiplos:

  - As colunas marcadas têm valores múltiplos por padrão. Quando um segundo valor é adicionado à coluna, ele se torna automaticamente com valores múltiplos.

  - Colunas marcadas que são criadas com a opção JET_bitColumnMultiValued na estrutura [JET_COLUMNDEF](./jet-columndef-structure.md) na chamada de [JetAddColumn](./jetaddcolumn-function.md).

A opção JET_bitColumnMultiValued altera a maneira como a coluna é indexada. Colunas com valores múltiplos com a opção JET_bitColumnMultiValued são indexadas mais extensivamente do que as colunas com vários valores marcadas. Essas colunas são indexadas sobre todos os valores na coluna de valores múltiplos, enquanto colunas com vários valores marcados são indexadas apenas no primeiro valor da coluna de valores múltiplos. Por exemplo, considere uma coluna com vários valores em que a opção JET_bitColumnMultiValued está definida e ela é a primeira coluna com vários valores em um índice. Esta coluna contém três valores: A, B e C. Um índice nessa coluna contém entradas para todos os três valores, A, B e C. Se a opção JET_bitColumnMultiValued não tiver sido definida, o índice nessa coluna conterá apenas o primeiro valor, A, no índice.
