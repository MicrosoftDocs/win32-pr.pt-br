---
description: Uma transação é um objeto que define uma unidade lógica de trabalho.
ms.assetid: 29661a58-ada9-4b7c-8d85-ab65b824c7cd
title: Transações (kernel Transaction Manager)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff77ae0d89f5e334319ea0b7b73c27a4b34b57e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778425"
---
# <a name="transactions"></a>Transactions

Uma transação é um objeto que define uma unidade lógica de trabalho. A transação estará ativa contanto que haja um identificador que referencie a transação e ela será considerada ativa se a transação ainda não tiver sido confirmada ou revertida. Se uma transação for criada e todos os identificadores tiverem sido fechados antes de uma confirmação ou reversão ocorrer, a transação será revertida.

Considere o caso de um cliente transacional de modo de usuário que cria uma transação para o escopo de suas operações e, em seguida, executa atualizações em um ou mais gerenciadores de recursos. Ocorre o seguinte:

1.  O cliente chama a função [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction) para criar a transação e recebe um identificador para essa transação como o valor de retorno.

    A transação pode ser aberta ou herdada por qualquer número de processos; cada processo é, portanto, envolvido na transação. A falha de qualquer um desses processos fará com que a transação seja anulada.

    Esta transação ainda não pode ser persistente. Somente as transações que atingiram o estado preparado devem ser recuperadas entre falhas do sistema se a transação usar o registro em log de anulação presumido.

2.  O cliente deve passar uma transação para o Gerenciador de recursos explicitamente.
3.  O cliente executa todas as suas operações transacionais com um ou mais RMs, como sistemas de arquivos transacionados.
4.  O cliente chama a função [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) .
5.  O Gerenciador de recursos recebe notificações do KTM para preparar e confirmar seus dados.

## <a name="transactions-and-threads"></a>Transações e threads

As transações não são as mesmas que os threads. Vários threads ou processos podem fazer parte de uma única transação. Por outro lado, um thread pode fazer parte de várias transações diferentes em momentos diferentes.

## <a name="transaction-functions"></a>Funções de transação

As funções a seguir são usadas com transações.



| Função                                                            | Descrição                                                                                   |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | Solicita que a transação especificada seja confirmada.                                         |
| [**CommitTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | Solicita que a transação especificada seja confirmada.                                         |
| [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | Cria um novo objeto de transação.                                                             |
| [**GetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | Retorna as informações solicitadas sobre a transação especificada.                            |
| [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | Abre uma transação existente.                                                                |
| [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | Solicita que a transação especificada seja revertida.                                       |
| [**RollbackTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | Solicita que a transação especificada seja revertida. Essa função retorna de forma assíncrona. |
| [**SetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | Define as informações da transação para a transação especificada.                               |



 

 

 



