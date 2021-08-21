---
description: As funções a seguir são usadas com transações.
ms.assetid: e9704ea8-e67d-4278-b77e-1d4787224d52
title: Funções do Gerenciador de Transações do Kernel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce98208b6ac78795be95b7255e9f263971ad6f08237e75ac0ef661c38a0878a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535276"
---
# <a name="kernel-transaction-manager-functions"></a>Funções do Gerenciador de Transações do Kernel

As funções a seguir são usadas com transações.



| Função                                                            | Descrição                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**Committransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | Solicita que a transação especificada seja comprometida.                                           |
| [**CommitTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | Solicita que a transação especificada seja comprometida.                                           |
| [**Createtransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | Cria um novo objeto de transação.                                                               |
| [**GetTransactionId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionid)                        | Obtém a ID da transação especificada.                                                   |
| [**GetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | Retorna as informações solicitadas sobre a transação especificada.                              |
| [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | Abre uma transação existente.                                                                  |
| [**RollbackComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)                        | Indica que o RM (gerenciador de recursos) concluiu com êxito a replicação de uma transação. |
| [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | Solicita que a transação especificada seja relembolsada.                                         |
| [**RollbackTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | Solicita que a transação especificada seja relembolsada. Essa função retorna de forma assíncrona.   |
| [**SetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | Define as informações de transação para a transação especificada.                                 |



 

As funções a seguir são usadas com inscrições.



| Função                                                                          | Descrição                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)                                          | Indica que um RM concluiu a confirmação de uma transação solicitada pelo TM (gerenciador de transações).                                                                                                                                                                                                                                                                        |
| [**CommitEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-commitenlistment)                                      | Confirma a transação para a insrução especificada.                                                                                                                                                                                                                                                                                                                                |
| [**GetEnlistmentId**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentid)                                        | Obtém a ID para a insrução especificada.                                                                                                                                                                                                                                                                                                                                         |
| [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)                                      | Cria uma instalação, define seu estado inicial e abre um alçamento para a instalação com o acesso especificado.                                                                                                                                                                                                                                                                       |
| [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) | Recupera uma estrutura opaca de dados de recuperação de KTM. As informações de recuperação são armazenadas em um log em nome de um RM chamando a [**função SetEnlistmentRecoveryInformation.**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation) Após uma falha, o RM pode usar a [**função GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) para recuperar as informações. |
| [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)                                          | Abre um objeto de inscrever-se existente e retorna um identificador para a inscrever-se.                                                                                                                                                                                                                                                                                                         |
| [**PrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-prepareenlistment)                                    | Chamado pelo TM superior para indicar que seu trabalho de pré-preparação foi concluído.                                                                                                                                                                                                                                                                                                   |
| [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment)                              | Chamado pelo TM superior para indicar que seu trabalho de pré-preparação foi concluído.                                                                                                                                                                                                                                                                                                   |
| [**RecoverEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverenlistment)                                    | Recupera o estado de uma instalação.                                                                                                                                                                                                                                                                                                                                                      |
| [**ReadOnlyEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)                                  | Solicita que a insrução especificada seja convertida em uma inscrições somente leitura. Uma inscrições somente leitura não pode participar do resultado da transação e não é registrada de forma durável para recuperação.                                                                                                                                                                                 |
| [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)                                  | Acumula a transação especificada associada a uma insrução. Essa função não pode ser chamada para inscrições somente leitura.                                                                                                                                                                                                                                                |
| [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)      | Define uma estrutura opaca definida pelo usuário de dados de recuperação da KTM. As informações de recuperação são armazenadas em um log em nome de um RM chamando [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation). Após uma falha, o RM pode usar [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) para recuperar as informações.                  |
| [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)                                    | Indica que o RM está recusando uma solicitação de fase única. Quando um TM recebe essa chamada, ele inicia uma commit em duas fases e envia uma solicitação de preparação para todas as RMs ins inscritos.                                                                                                                                                                                                             |



 

As funções a seguir são usadas com gerenciadores de recursos.



| Função                                                                           | Descrição                                                                                                                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager)                             | Cria um novo objeto RM e associa o RM a um TM (gerenciador de transações).                                                                                  |
| [**GetNotificationResourceManager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)           | Solicita e recebe uma notificação para RM. Essa função é usada pelo registro RM para receber notificações quando uma transação altera o estado.                 |
| [**GetNotificationResourceManagerAsync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync) | Solicita e recebe notificação assíncrona para um RM. Essa função é usada pelo RM para se registrar para receber notificações quando uma transação muda de estado. |
| [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager)                                 | Abre um RM existente.                                                                                                                                            |
| [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)                                         | Indica que o RM concluiu todo o processamento necessário para garantir que uma operação de confirmação ou anulação seja bem-sucedida para a transação especificada.           |
| [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)                                   | Sinaliza que esse RM concluiu seu trabalho de pré-preparação, para que outras RMs agora possam iniciar suas operações de preparação.                                                |
| [**RecoverResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverresourcemanager)                           | Recupera o estado de um RM de seu arquivo de log.                                                                                                                         |
| [**SetResourceManagerCompletionPort**](/windows/desktop/api/Ktmw32/nf-ktmw32-setresourcemanagercompletionport)       | Associa a porta de conclusão de E/S especificada ao RM especificado. Essa porta recebe todas as notificações para o RM.                                             |



 

As funções a seguir são usadas com gerenciadores de transações.



| Função                                                                            | Descrição                                                                 |
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager)                        | Cria um novo objeto TM e retorna um identificador com o acesso especificado.     |
| [**GetCurrentClockTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-getcurrentclocktransactionmanager) | Obtém um valor de relógio virtual de um TM.                                    |
| [**GetTransactionManagerId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionmanagerid)                          | Obtém um identificador para o TM especificado.                                 |
| [**OpenTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager)                            | Abre um TM existente.                                                       |
| [**OpenTransactionManagerById**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanagerbyid)                    | Abre um TM existente.                                                       |
| [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)                      | Recupera o estado de um TM de seu arquivo de log.                                    |
| [**RenameTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-renametransactionmanager)                        | Renomeia um TM.                                                               |
| [**RollforwardTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-rollforwardtransactionmanager)              | Recupera o estado do TM de seu arquivo de log para o valor do relógio virtual especificado. |



 

 

 



