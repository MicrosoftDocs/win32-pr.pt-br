---
description: Um Gerenciador de transações (TM) é uma instância de um log. No KTM, os objetos TM especificam o log e algumas das funcionalidades do TM. Normalmente, há muitos objetos TM em um nó específico. Os gerenciadores de recursos (RMs) devem ser associados a um TM específico.
ms.assetid: 8d43977a-84cf-4109-b7db-f9c94a226c5d
title: Gerenciadores de transações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313215816642201c75ae5f0facae3bf98799c8d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759489"
---
# <a name="transaction-managers"></a>Gerenciadores de transações

Um Gerenciador de transações (TM) é uma instância de um log. No KTM, os objetos TM especificam o log e algumas das funcionalidades do TM. Normalmente, há muitos objetos TM em um nó específico. Os gerenciadores de recursos (RMs) devem ser associados a um TM específico. Há três tipos de TMs:

-   Um volátil TM, que não tem nenhum log.
-   Um TM normal, que tem um log e é usado para coordenar as transações de um ou mais RMs.
-   Um Gerenciador de transações superior.

## <a name="volatile-transaction-managers"></a>Gerenciadores de transações voláteis

Um volátil TM é um TM para somente leitura ou volátil do RMs. Ele não tem um log e não mantém o estado das transações entre as reinicializações do sistema.

## <a name="transaction-managers"></a>Gerenciadores de transações

TMs têm um log, um ou mais RMs durável ou volátil, ou ambos. O TM persistirá o estado de uma transação entre reinicializações do sistema até que as transações sejam concluídas. Um modelo de anulação presumido é usado, de modo que as transações que estavam ativas, mas não preparadas quando o objeto TM é desligado, são revertidas. Ao abrir um TM pela primeira vez, você deve recuperar o TM chamando a função [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager) .

## <a name="superior-transaction-managers"></a>Gerenciadores de transações superiores

Uma TM superior é uma TM para outros TMs. Ele coordena transações. Ele também emite notificações de **\_ \_ preparação de notificação de transação** para o KTM (kernel Transaction Manager). Um exemplo de TM superior é o Microsoft Coordenador de Transações Distribuídas (DTC). Essa capacidade vem com uma responsabilidade de tempo de recuperação adicional. Durante a recuperação, o RM deve primeiro chamar a função [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) para reabrir a inscrição. Ele também deve entregar (ou entregar novamente) o resultado da transação se a transação foi confirmada; é gratuito fornecer um resultado chamando a função [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) ou a função [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction) . Essa obrigação não termina até que tenha recebido um evento de notificação de **confirmação de transação associada \_ \_ \_ concluída** ou de **\_ \_ reversão \_** da reinício de notificação de transação. Se uma TM superior falhar em executar essas operações no momento da recuperação, o KTM limpará todas as transações que não receberam resultados no final da fase de recuperação. No entanto, isso pode resultar em resultados de transação inconsistentes.

## <a name="transaction-manager-functions"></a>Funções do Gerenciador de transações

As funções a seguir são usadas com gerenciadores de transações.



| Função                                                                            | Descrição                                                                                    |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**Createtransactionmanager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager)                        | Cria um novo objeto do Gerenciador de transações (TM) e retorna um identificador com o acesso especificado.  |
| [**GetCurrentClockTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-getcurrentclocktransactionmanager) | Obtém um valor de relógio virtual de um Gerenciador de transações.                                      |
| [**GetTransactionManagerId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionmanagerid)                          | Obtém um identificador para o Gerenciador de transações especificado.                                   |
| [**OpenTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager)                            | Abre um Gerenciador de transações existente.                                                         |
| [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)                      | Recupera o estado de um Gerenciador de transações de seu arquivo de log.                                      |
| [**RollforwardTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-rollforwardtransactionmanager)              | Recupera o estado de um Gerenciador de transações de seu arquivo de log para o valor de relógio virtual especificado. |



 

 

 



