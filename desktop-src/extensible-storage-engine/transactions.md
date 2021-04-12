---
description: 'Saiba mais sobre: transações (eventos do Windows)'
title: Transações (Eventos do Windows)
TOCTitle: Transactions
ms:assetid: 1ceb362c-1efe-439b-b10a-016c8a54f27b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269197(v=EXCHG.10)
ms:contentKeyID: 32765500
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 90b5b566f5ff961ce7b0ae3725f580e1f39c041d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297040"
---
# <a name="transactions-windows-events"></a>Transações (Eventos do Windows)


_**Aplica-se a:** Windows | Windows Server_

## <a name="transactions"></a>Transactions

Transações ESE são unidades lógicas de processamento que controlam como um aplicativo vê e manipula linhas no banco de dados. Seu aplicativo pode usar pontos de salvamento de transação para determinar se deve manter ou descartar um determinado conjunto de alterações no banco de dados. Todas as transações no ESE são atômicas, consistentes, isoladas e duráveis (ACID), conforme descrito abaixo:

  - **Atômico:** Todas as atualizações na transação aparecem no banco de dados ou são descartadas.

<!-- end list -->

  - **Consistente:** O banco de dados sempre será iniciado em um estado legal e sempre terminará em outro estado legal. Para aplicativos ESE, o mecanismo de banco de dados controlará algumas restrições simples, por exemplo, exclusividade de um índice exclusivo, mas o aplicativo em si definirá quase todos os outros aspectos do que significa que o banco de dados está em um estado legal.

<!-- end list -->

  - **Isolamento:** As transações são isoladas de atualizações por outras sessões. Uma transação nunca verá um conjunto parcial de alterações feitas por outra transação.

<!-- end list -->

  - **Durável:** Depois que o mecanismo de banco de dados reconhece que uma transação foi confirmada, suas alterações são persistentes no banco de dados. A durabilidade de uma transação pode ser opcionalmente cancelada por motivos de desempenho.

As transações são executadas dentro dos limites das chamadas para [JetBeginTransaction](./jetbegintransaction-function.md) e [JetCommitTransaction](./jetcommittransaction-function.md) ou [JetRollback](./jetrollback-function.md). Quando o aplicativo entra na transação, o banco de dados aparece congelado na instância no momento em que a transação é iniciada. Isso é chamado de isolamento de instantâneo. Se a transação for encerrada chamando [JetRollback](./jetrollback-function.md), nenhuma das operações executadas na transação será confirmada no banco de dados. Se o processo ou a máquina falhar antes de [JetCommitTransaction](./jetcommittransaction-function.md) ser chamado, ele será o mesmo que chamar [JetRollback](./jetrollback-function.md).

Este procedimento mostra como iniciar e confirmar uma transação que lê e atualiza dados em um banco de dado.

### <a name="to-start-and-commit-a-transaction"></a>Para iniciar e confirmar uma transação

1.  Chame [JetBeginTransaction](./jetbegintransaction-function.md) ou [JETBEGINTRANSACTION2](./jetbegintransaction2-function.md) com a ID de sessão para iniciar a transação.

2.  Mova o cursor para o registro desejado chamando [JetMove](./jetmove-function.md) com JET_MoveFirst especificado no parâmetro de *galinha* . Para obter mais informações sobre como mover o cursor, consulte o tópico [indexação na tabela](./indexing-in-the-table.md) .

3.  Chame [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) no registro atual com JET_ColInfo especificado no parâmetro *InfoLevel* para recuperar a ID de coluna para a coluna. A ID da coluna é retornada na estrutura de [JET_COLUMNDEF](./jet-columndef-structure.md) .

4.  Chame [JetSetColumn](./jetsetcolumn-function.md) com a ID de sessão, ID de tabela e ID de coluna da coluna que é atualizada. Os dados da coluna estão contidos no parâmetro *pvData* .

5.  Chame [JetCommitTransaction](./jetcommittransaction-function.md) para confirmar a transação para o banco de dados.

A maneira como um mecanismo de banco de dados ESE implementa o isolamento de instantâneo tem algumas diferenças importantes de modelos de bloqueio e isolamento de banco de dados relacional tradicionais. Quando uma transação lê uma linha, ela sempre pode acessar a linha sem falhar ou aguardar que outras sessões liberem um bloqueio. Quando uma transação tenta atualizar uma linha, ela terá sucesso se for a primeira sessão a atualizar essa linha, que é o primeiro gravador vence. Se a sessão não for o primeiro gravador, ela falhará imediatamente com um erro de conflito de gravação. A sessão deve abortar sua transação, aguardar (geralmente por um atraso aleatório), para que a outra transação confirme suas alterações e, em seguida, repita a transação. O mecanismo de banco de dados não fará com que a sessão aguarde automaticamente até que a outra transação tenha concluído sua atualização. Normalmente, uma transação será testada se puder atualizar uma linha dentro da chamada [JetUpdate](./jetupdate-function.md) . Se não for possível bloquear a linha para atualização, o [JetUpdate](./jetupdate-function.md) falhará com JET_errWriteConflict.

As sessões são limitadas a um thread desde o momento em que a transação começa até o final da transação. É recomendável que todas as operações de atualização e recuperação sejam executadas em uma transação. O ESE também dá suporte a modificações de esquema, como a criação de tabelas e a adição de colunas dentro da transação. Tanto as modificações de atualização quanto de esquema podem ser executadas na mesma transação. Depois que a transação for concluída com [JetCommitTransaction](./jetcommittransaction-function.md), a atualização será registrada no arquivo de log de transações. Esses arquivos podem ser usados para manter um estado logicamente consistente no caso de um encerramento de processo inesperado ou de um desligamento do sistema.

As transações podem ser aninhadas até 7 níveis com chamadas correspondentes para [JetBeginTransaction](./jetbegintransaction-function.md) e [JetCommitTransaction](./jetcommittransaction-function.md) ou [JetRollback](./jetrollback-function.md) aninhadas entre si. Isso permite que o aplicativo Reverta uma parte da transação sem precisar refazer a transação inteira. A chamada aninhada para [JetCommitTransaction](./jetcommittransaction-function.md) significa que esse nível de processamento está concluído; no entanto, a transação não é confirmada no banco de dados até a chamada mais externa para confirmar a transação com [JetCommitTransaction](./jetcommittransaction-function.md).

Colunas de atualização de caução podem ser atualizadas simultaneamente por várias sessões sem falha com Jet_errWriteConflict. A função [JetEscrowUpdate](./jetescrowupdate-function.md) só pode ser chamada em colunas de caução, colunas que foram criadas com Jet_bitColumnEscrowUpdate.
