---
description: 'Saiba mais sobre: usando colunas em uma tabela'
title: Usando colunas em uma tabela
TOCTitle: Using Columns in a Table
ms:assetid: 064ac59e-d306-4335-a623-754a003f5ebc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269178(v=EXCHG.10)
ms:contentKeyID: 32765481
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: cd715b171162f63aaf0772ff6ec2e4a6d057a0d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791333"
---
# <a name="using-columns-in-a-table"></a>Usando colunas em uma tabela


_**Aplica-se a:** Windows | Windows Server_

## <a name="using-columns-in-a-table"></a>Usando colunas em uma tabela

Uma tabela pode ser criada com um conjunto inicial de colunas chamando [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) ou sem colunas chamando [JetCreateTable](./jetcreatetable-function.md). Quando a tabela é criada com um conjunto inicial de colunas na chamada para [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) ou [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), ela contém uma estrutura [JET_TABLECREATE](./jet-tablecreate-structure.md) (ou [JET_TABLECREATE2](./jet-tablecreate2-structure.md)). Essas estruturas contêm uma matriz de estruturas [JET_COLUMNCREATE](./jet-columncreate-structure.md) que definem o conjunto de colunas na tabela. O membro **grbit** define as opções na coluna e o membro **coltyp** define o tipo de dados que podem ser definidos na coluna.

Quando a tabela é criada sem colunas, elas devem ser adicionadas chamando [JetAddColumn](./jetaddcolumn-function.md) com a estrutura de [JET_COLUMNDEF](./jet-columndef-structure.md) . O membro **grbit** da estrutura [JET_COLUMNDEF](./jet-columndef-structure.md) define as opções na coluna e o membro **coltyp** define o tipo de dados que podem ser definidos na coluna. Os valores de coluna padrão são definidos na chamada para [JetAddColumn](./jetaddcolumn-function.md) especificando um valor no parâmetro *pvDefault* e o tamanho no parâmetro *cbDefault* . Uma coluna sem um valor padrão efetivamente tem um valor padrão de NULL.

Os valores na tabela só podem ser definidos dentro do contexto de uma transação. A transação começa na chamada para [JetBeginTransaction](./jetbegintransaction-function.md) e termina na chamada para [JetCommitTransaction](./jetcommittransaction-function.md). Dentro da transação, um único valor de coluna pode ser definido chamando [JetSetColumn](./jetsetcolumn-function.md)ou vários valores de colunas podem ser definidos chamando [JetSetColumns](./jetsetcolumns-function.md). [JetSetColumns](./jetsetcolumns-function.md) usa uma matriz de estruturas [JET_SETCOLUMN](./jet-setcolumn-structure.md) para definir várias colunas na tabela. Os dados estão contidos no parâmetro *pvData* de [JetSetColumn](./jetsetcolumn-function.md)ou no membro **pvData** na estrutura [JET_SETCOLUMN](./jet-setcolumn-structure.md) .

As estruturas [JET_COLUMNBASE](./jet-columnbase-structure.md), [JET_COLUMNLIST](./jet-columnlist-structure.md)e [JET_COLUMNDEF](./jet-columndef-structure.md) são retornadas nas chamadas para [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)e [JetGetColumnInfo](./jetgetcolumninfo-function.md) dependendo do tipo de coluna que é recuperado. A estrutura de [JET_COLUMNBASE](./jet-columnbase-structure.md) descreve os parâmetros da coluna base e a [JET_COLUMNLIST](./jet-columnlist-structure.md) contém as informações necessárias para percorrer a tabela temporária que é criada pelas funções [JetGetColumnInfo](./jetgetcolumninfo-function.md) e [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) .
