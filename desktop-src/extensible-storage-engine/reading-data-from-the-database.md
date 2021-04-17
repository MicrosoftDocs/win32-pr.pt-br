---
description: 'Saiba mais sobre: lendo dados do banco'
title: Lendo dados do banco de dados
TOCTitle: Reading Data from the Database
ms:assetid: c3c48918-ccd6-4c34-849c-93bd7533ce92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294080(v=EXCHG.10)
ms:contentKeyID: 32765695
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 176cd3189dd1c2701331eff0ef5387827da19b94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780147"
---
# <a name="reading-data-from-the-database"></a>Lendo dados do banco de dados


_**Aplica-se a:** Windows | Windows Server_

## <a name="reading-data-from-the-database"></a>Lendo dados do banco de dados

A leitura de dados do Database deve ser executada em uma transação.

O procedimento a seguir mostra como executar uma operação de leitura simples no banco de dados.

### <a name="to-read-data-from-a-database"></a>Para ler dados de um banco de dado

1.  Chame [JetBeginTransaction](./jetbegintransaction-function.md) ou [JETBEGINTRANSACTION2](./jetbegintransaction2-function.md) com a ID de sessão para iniciar a transação.

2.  Mova o cursor para o registro desejado chamando [JetMove](./jetmove-function.md) com JET_MoveFirst no parâmetro de *galinha* . Para obter mais informações sobre como mover o cursor, consulte o tópico [indexação na tabela](./indexing-in-the-table.md) .

3.  Chame [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) no registro atual com JET_ColInfo especificado no parâmetro *InfoLevel* para recuperar a ID de coluna para a coluna. A ID da coluna é retornada na estrutura de [JET_COLUMNDEF](./jet-columndef-structure.md) .

4.  Leia os dados da coluna chamando [JetRetrieveColumn](./jetretrievecolumn-function.md) com a ID de coluna recuperada na etapa 3 no parâmetro columnid. O parâmetro *pvData* contém o tipo de dados especificado na estrutura de [JET_COLUMNDEF](./jet-columndef-structure.md) recuperada na etapa 3.

5.  Chame [JetCommitTransaction](./jetcommittransaction-function.md) para confirmar a transação para o banco de dados.
