---
description: 'Saiba mais sobre: Colunas esparsas com valor múltiplo'
title: Colunas esparsas com valores múltiplos
TOCTitle: Multi-Valued Sparse Columns
ms:assetid: 36e82a73-aad4-4e0d-a743-a2182c41fe9c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269225(v=EXCHG.10)
ms:contentKeyID: 32765527
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 21dbe18be8be26af9fe32d9b80cbd5744c172793e27701d46438df4d63dcf395
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115576"
---
# <a name="multi-valued-sparse-columns"></a>Colunas esparsas com valores múltiplos


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="multi-valued-sparse-columns"></a>Colunas esparsas com valores múltiplos

Colunas esparsas podem ter comprimento fixo ou variável e são exclusivas porque não assumem espaço em um registro se são NULL ou deixadas com seu valor padrão. Colunas esparsas, também conhecidas como colunas marcadas, podem conter mais de um valor em um único registro. Colunas marcadas podem ser qualquer um dos tipos de colunas descritos nas [constantes JET_coltyp](./jet-coltyp.md) dados. Eles são criados quando a coluna é adicionada à tabela definindo o sinalizador JET_bitColumnTagged na estrutura [do JET_COLUMNDEF](./jet-columndef-structure.md) na chamada para [JetAddColumn](./jetaddcolumn-function.md)ou na estrutura JET_COLUMNCREATE usada [na](./jet-columncreate-structure.md) chamada para [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) ou [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md). Colunas do tipo JET_coltypLongText e JET_coltypLongBinary são criadas automaticamente como colunas marcadas.

Somente colunas marcadas podem conter vários valores em um registro, colunas de comprimento fixa ou variável podem não conter vários valores. Há dois tipos de colunas com valores múltiplos:

  - As colunas marcadas têm valores múltiplos por padrão. Quando um segundo valor é adicionado à coluna, ele se torna automaticamente com vários valores.

  - Colunas marcadas que são criadas com a JET_bitColumnMultiValued na [estrutura JET_COLUMNDEF](./jet-columndef-structure.md) na chamada para [JetAddColumn](./jetaddcolumn-function.md).

A JET_bitColumnMultiValued de dados altera a maneira como a coluna é indexada. Colunas com vários valores com a JET_bitColumnMultiValued são indexadas mais extensivamente do que colunas com vários valores marcadas. Essas colunas são indexadas em todos os valores na coluna com vários valores, enquanto as colunas com valores múltiplos marcadas são indexadas apenas sobre o primeiro valor na coluna com valores múltiplos. Por exemplo, considere uma coluna com vários valores em que a JET_bitColumnMultiValued é definida e é a primeira coluna com valores múltiplos em um índice. Esta coluna contém três valores: A, B e C. Um índice sobre essa coluna contém entradas para todos os três valores, A, B e C. Se a JET_bitColumnMultiValued não tiver sido definida, o índice sobre essa coluna conterá apenas o primeiro valor, A, no índice.
