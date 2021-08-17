---
description: 'Saiba mais sobre: Usando colunas em uma tabela'
title: Usando colunas em uma tabela
TOCTitle: Using Columns in a Table
ms:assetid: 064ac59e-d306-4335-a623-754a003f5ebc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269178(v=EXCHG.10)
ms:contentKeyID: 32765481
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 332cca1c64c851ded44951fc9bb7f68ebd9f6818030cefeb8406f965a1bd5d6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471296"
---
# <a name="using-columns-in-a-table"></a>Usando colunas em uma tabela


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="using-columns-in-a-table"></a>Usando colunas em uma tabela

Uma tabela pode ser criada com um conjunto inicial de colunas chamando [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) ou sem colunas chamando [JetCreateTable](./jetcreatetable-function.md). Quando a tabela é criada com um conjunto inicial de colunas na chamada para [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) ou [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), ela contém uma estrutura [JET_TABLECREATE](./jet-tablecreate-structure.md) [(ou JET_TABLECREATE2](./jet-tablecreate2-structure.md)). Essas estruturas contêm uma matriz [JET_COLUMNCREATE](./jet-columncreate-structure.md) estruturas que definem o conjunto de colunas na tabela. O **membro grbit** define as opções na coluna e o membro **coltyp** define o tipo de dados que podem ser definidos na coluna.

Quando a tabela é criada sem colunas, elas devem ser adicionadas chamando [JetAddColumn](./jetaddcolumn-function.md) com a [estrutura JET_COLUMNDEF](./jet-columndef-structure.md) dados. O **membro grbit** da [estrutura JET_COLUMNDEF](./jet-columndef-structure.md) define as opções na coluna e o membro **coltyp** define o tipo de dados que podem ser definidos na coluna. Os valores de coluna padrão são definidos na chamada para [JetAddColumn](./jetaddcolumn-function.md) especificando um valor no parâmetro *pvDefault* e o tamanho no parâmetro *cbDefault.* Uma coluna sem um valor padrão efetivamente tem um valor padrão null.

Os valores na tabela só podem ser definidos dentro do contexto de uma transação. A transação começa na chamada para [JetBeginTransaction](./jetbegintransaction-function.md) e termina na chamada para [JetCommitTransaction.](./jetcommittransaction-function.md) Dentro da transação, um único valor de coluna pode ser definido chamando [JetSetColumn](./jetsetcolumn-function.md)ou valores de várias colunas podem ser definidos chamando [JetSetColumns](./jetsetcolumns-function.md). [JetSetColumns](./jetsetcolumns-function.md) usa uma matriz de [JET_SETCOLUMN](./jet-setcolumn-structure.md) estruturas para definir várias colunas na tabela. Os dados estão contidos no *parâmetro pvData* [de JetSetColumn](./jetsetcolumn-function.md)ou no membro **pvData** na [estrutura JET_SETCOLUMN.](./jet-setcolumn-structure.md)

As [estruturas JET_COLUMNBASE](./jet-columnbase-structure.md), [JET_COLUMNLIST](./jet-columnlist-structure.md)e [JET_COLUMNDEF](./jet-columndef-structure.md) são retornadas nas chamadas para [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)e [JetGetColumnInfo,](./jetgetcolumninfo-function.md) dependendo do tipo de coluna recuperado. A [estrutura JET_COLUMNBASE](./jet-columnbase-structure.md) descreve os parâmetros da coluna base e o JET_COLUMNLIST contém as informações necessárias para percorrer [a](./jet-columnlist-structure.md) tabela temporária criada pelas funções [JetGetColumnInfo](./jetgetcolumninfo-function.md) e [JetGetTableColumnInfo.](./jetgettablecolumninfo-function.md)
