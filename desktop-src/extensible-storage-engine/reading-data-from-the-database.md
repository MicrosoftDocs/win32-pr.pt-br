---
description: 'Saiba mais sobre: Lendo dados do banco de dados'
title: Lendo dados do banco de dados
TOCTitle: Reading Data from the Database
ms:assetid: c3c48918-ccd6-4c34-849c-93bd7533ce92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294080(v=EXCHG.10)
ms:contentKeyID: 32765695
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 7d33aa2640c07018186a5516d985fd4e46194d39cd4b12b7254f430f889e2484
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780256"
---
# <a name="reading-data-from-the-database"></a>Lendo dados do banco de dados


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="reading-data-from-the-database"></a>Lendo dados do banco de dados

A leitura de dados do banco de dados deve ser executada dentro de uma transação.

O procedimento a seguir mostra como executar uma operação de leitura simples no banco de dados.

### <a name="to-read-data-from-a-database"></a>Para ler dados de um banco de dados

1.  Chame [JetBeginTransaction ou](./jetbegintransaction-function.md) [JetBeginTransaction2](./jetbegintransaction2-function.md) com a ID da sessão para iniciar a transação.

2.  Mova o cursor para o registro desejado chamando [JetMove](./jetmove-function.md) com JET_MoveFirst no *parâmetro cRow.* Para obter mais informações sobre como mover o cursor, consulte [o tópico Indexação na](./indexing-in-the-table.md) tabela.

3.  Chame [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) no registro atual com JET_ColInfo especificado no parâmetro *InfoLevel* para recuperar a ID da coluna. A ID da coluna é retornada na [estrutura JET_COLUMNDEF](./jet-columndef-structure.md) dados.

4.  Leia os dados da coluna chamando [JetRetrieveColumn](./jetretrievecolumn-function.md) com a ID da coluna recuperada na etapa 3 no parâmetro columnid. O *parâmetro pvData* contém o tipo de dados especificado na [estrutura JET_COLUMNDEF](./jet-columndef-structure.md) recuperada na etapa 3.

5.  Chame [JetCommitTransaction para](./jetcommittransaction-function.md) fazer commit da transação no banco de dados.
