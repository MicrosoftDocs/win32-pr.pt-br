---
description: Uma transação é um objeto que define uma unidade lógica de trabalho.
ms.assetid: 29661a58-ada9-4b7c-8d85-ab65b824c7cd
title: Transações (Gerenciador de Transações do Kernel)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 471d2ece52d510c1a77baa59ee3af980c4e4630a17d0911fdcbe590bad78903f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913876"
---
# <a name="transactions"></a>Transactions

Uma transação é um objeto que define uma unidade lógica de trabalho. A transação está ativa, desde que haja um alçamento que referencie a transação e ela seja considerada ativa se a transação ainda não tiver sido comprometida ou retida. Se uma transação for criada e todos os lidares com ela foram fechados antes que ocorra uma confirmação ou re reação, a transação será relembolsada.

Considere o caso de um cliente transacional no modo de usuário que cria uma transação para escopo de suas operações e, em seguida, executa atualizações em um ou mais gerenciadores de recursos. Ocorre o seguinte:

1.  O cliente chama a [**função CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction) para criar a transação e recebe um handle para essa transação como o valor de retorno.

    A transação pode ser aberta ou herdada por qualquer número de processos; cada processo está, portanto, envolvido na transação. A falha de qualquer um desses processos fará com que a transação seja anulada.

    Essa transação pode ainda não ser persistente. Somente as transações que atingiram o estado preparado deverão ser recuperadas em falhas do sistema se a transação usar o registro em log de anulação presumida.

2.  O cliente deve passar uma transação para o gerenciador de recursos explicitamente.
3.  O cliente executa todas as operações transacionais com uma ou mais RMs, como sistemas de arquivos transacionados.
4.  O cliente chama a [**função CommitTransaction.**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)
5.  O gerenciador de recursos recebe notificações da KTM para preparar e fazer commit de seus dados.

## <a name="transactions-and-threads"></a>Transações e threads

As transações não são iguais aos threads. Vários threads ou processos podem fazer parte de uma única transação. Por outro lado, um thread pode fazer parte de várias transações diferentes em momentos diferentes.

## <a name="transaction-functions"></a>Funções de transação

As funções a seguir são usadas com transações.



| Função                                                            | Descrição                                                                                   |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**Committransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | Solicita que a transação especificada seja comprometida.                                         |
| [**CommitTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | Solicita que a transação especificada seja comprometida.                                         |
| [**Createtransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | Cria um novo objeto de transação.                                                             |
| [**GetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | Retorna as informações solicitadas sobre a transação especificada.                            |
| [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | Abre uma transação existente.                                                                |
| [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | Solicita que a transação especificada seja relembolsada.                                       |
| [**RollbackTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | Solicita que a transação especificada seja relembolsada. Essa função retorna de forma assíncrona. |
| [**SetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | Define as informações de transação para a transação especificada.                               |



 

 

 



