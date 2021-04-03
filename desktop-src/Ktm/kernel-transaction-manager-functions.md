---
description: As funções a seguir são usadas com transações.
ms.assetid: e9704ea8-e67d-4278-b77e-1d4787224d52
title: Funções do Gerenciador de transações do kernel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221bcc13bb1cfb1f8cc67eb4d16f40a27799b921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837118"
---
# <a name="kernel-transaction-manager-functions"></a>Funções do Gerenciador de transações do kernel

As funções a seguir são usadas com transações.



| Função                                                            | Descrição                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | Solicita que a transação especificada seja confirmada.                                           |
| [**CommitTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | Solicita que a transação especificada seja confirmada.                                           |
| [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | Cria um novo objeto de transação.                                                               |
| [**Gettransactionid**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionid)                        | Obtém a ID da transação especificada.                                                   |
| [**GetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | Retorna as informações solicitadas sobre a transação especificada.                              |
| [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | Abre uma transação existente.                                                                  |
| [**RollbackComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)                        | Indica que o Gerenciador de recursos (RM) concluiu com êxito a reversão de uma transação. |
| [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | Solicita que a transação especificada seja revertida.                                         |
| [**RollbackTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | Solicita que a transação especificada seja revertida. Essa função retorna de forma assíncrona.   |
| [**SetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | Define as informações da transação para a transação especificada.                                 |



 

As funções a seguir são usadas com inlistagens.



| Função                                                                          | Descrição                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)                                          | Indica que um RM concluiu a confirmação de uma transação que foi solicitada pelo Gerenciador de transações (TM).                                                                                                                                                                                                                                                                        |
| [**CommitEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-commitenlistment)                                      | Confirma a transação para a inscrição especificada.                                                                                                                                                                                                                                                                                                                                |
| [**Getalistaid**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentid)                                        | Obtém a ID da inscrição especificada.                                                                                                                                                                                                                                                                                                                                         |
| [**Subinscrição**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)                                      | Cria uma inscrição, define seu estado inicial e abre um identificador para a inscrição com o acesso especificado.                                                                                                                                                                                                                                                                       |
| [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) | Recupera uma estrutura opaca de dados de recuperação do KTM. As informações de recuperação são armazenadas em um log em nome de um RM chamando a função [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation) . Após uma falha, o RM pode usar a função [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) para recuperar as informações. |
| [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)                                          | Abre um objeto de inscrição existente e retorna um identificador para a inscrição.                                                                                                                                                                                                                                                                                                         |
| [**PrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-prepareenlistment)                                    | Chamado por TM superior para indicar que seu trabalho de pré-preparação foi concluído.                                                                                                                                                                                                                                                                                                   |
| [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment)                              | Chamado por TM superior para indicar que seu trabalho de pré-preparação foi concluído.                                                                                                                                                                                                                                                                                                   |
| [**RecoverEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverenlistment)                                    | Recupera o estado de uma inscrição.                                                                                                                                                                                                                                                                                                                                                      |
| [**ReadOnlyEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)                                  | Solicita que a inscrição especificada seja convertida em uma inscrição somente leitura. Uma inscrição somente leitura não pode participar do resultado da transação e não é permanentemente registrada para recuperação.                                                                                                                                                                                 |
| [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)                                  | Reverte a transação especificada que está associada a uma inscrição. Esta função não pode ser chamada para inlistagens somente leitura.                                                                                                                                                                                                                                                |
| [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)      | Define uma estrutura opaca e definida pelo usuário de dados de recuperação do KTM. As informações de recuperação são armazenadas em um log em nome de um RM chamando [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation). Após uma falha, o RM pode usar [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) para recuperar as informações.                  |
| [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)                                    | Indica que o RM está recusando uma solicitação de fase única. Quando um TM recebe essa chamada, ele inicia uma confirmação de duas fases e envia uma solicitação de preparação para todos os RMs inscritos.                                                                                                                                                                                                             |



 

As funções a seguir são usadas com gerenciadores de recursos.



| Função                                                                           | Descrição                                                                                                                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager)                             | Cria um novo objeto RM e associa o RM a um Gerenciador de transações (TM).                                                                                  |
| [**GetNotificationResourceManager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)           | Solicita e recebe uma notificação para o RM. Essa função é usada pelo registro do RM para receber notificações quando um estado de transação é alterado.                 |
| [**GetNotificationResourceManagerAsync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync) | Solicita e recebe notificação assíncrona para um RM. Essa função é usada pelo RM para se registrar para receber notificações quando um estado de transação for alterado. |
| [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager)                                 | Abre um RM existente.                                                                                                                                            |
| [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)                                         | Indica que o RM concluiu todo o processamento necessário para garantir que uma operação de confirmação ou anulação terá sucesso para a transação especificada.           |
| [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)                                   | Sinaliza que este RM concluiu seu trabalho de preprepare, para que outro RMs agora possa iniciar suas operações de preparação.                                                |
| [**RecoverResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverresourcemanager)                           | Recupera o estado de um RM de seu arquivo de log.                                                                                                                         |
| [**SetResourceManagerCompletionPort**](/windows/desktop/api/Ktmw32/nf-ktmw32-setresourcemanagercompletionport)       | Associa a porta de conclusão de e/s especificada ao RM especificado. Esta porta recebe todas as notificações para o RM.                                             |



 

As funções a seguir são usadas com gerenciadores de transações.



| Função                                                                            | Descrição                                                                 |
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**Createtransactionmanager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager)                        | Cria um novo objeto TM e retorna um identificador com o acesso especificado.     |
| [**GetCurrentClockTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-getcurrentclocktransactionmanager) | Obtém um valor de relógio virtual de um TM.                                    |
| [**GetTransactionManagerId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionmanagerid)                          | Obtém um identificador para o TM especificado.                                 |
| [**OpenTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager)                            | Abre um TM existente.                                                       |
| [**OpenTransactionManagerById**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanagerbyid)                    | Abre um TM existente.                                                       |
| [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)                      | Recupera o estado de TM de seu arquivo de log.                                    |
| [**RenameTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-renametransactionmanager)                        | Renomeia um TM.                                                               |
| [**RollforwardTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-rollforwardtransactionmanager)              | Recupera o estado de TM de seu arquivo de log para o valor de relógio virtual especificado. |



 

 

 



