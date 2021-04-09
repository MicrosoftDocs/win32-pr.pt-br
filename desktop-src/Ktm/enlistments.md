---
description: Um Gerenciador de recursos se relaciona em uma transação quando começa a participar dessa transação específica.
ms.assetid: 9c201699-c00b-4efe-9f30-8d4e182de785
title: Inscrições
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52820af2a7b280bc4740d0309fb627725e648685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171696"
---
# <a name="enlistments"></a>Inscrições

Um Gerenciador de recursos se relaciona em uma transação quando começa a participar dessa transação específica. A inscrição define quais notificações o Gerenciador de recursos aceita. Um Gerenciador de recursos cria um objeto de inscrição quando ele se alista em uma transação. Esse objeto sinaliza para KTM que o Gerenciador de recursos (RM) está solicitando notificações sobre a transação especificada.

O RM fornece uma estrutura de [**\_ máscara de notificação**](notification-mask.md) que detalha quais notificações ele está solicitando.

## <a name="enlistment-functions"></a>Funções de inscrição

As funções a seguir são usadas com inlistagens.



| Função                                                                          | Descrição                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)                                          | Indica que um Gerenciador de recursos (RM) concluiu a confirmação de uma transação que foi solicitada pelo Gerenciador de transações (TM).                                                                                                                                                                                                                                                                        |
| [**Subinscrição**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)                                      | Cria uma inscrição, define seu estado inicial e abre um identificador para a inscrição com o acesso especificado.                                                                                                                                                                                                                                                                                          |
| [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) | Recupera uma estrutura opaca de dados de recuperação do KTM. As informações de recuperação são armazenadas em um log em nome de um Gerenciador de recursos (RM) chamando a função [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation) . Após uma falha, o RM pode usar a função [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) para recuperar as informações. |
| [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)                                          | Abre um objeto de inscrição existente e retorna um identificador para a inscrição.                                                                                                                                                                                                                                                                                                                            |
| [**ReadOnlyEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)                                  | Solicita que a inscrição especificada seja convertida em uma inscrição somente leitura. Uma inscrição somente leitura não pode participar do resultado da transação e não é permanentemente registrada para recuperação.                                                                                                                                                                                                    |
| [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)                                  | Reverte a transação especificada que está associada a uma inscrição. Esta função não pode ser chamada para inlistagens somente leitura.                                                                                                                                                                                                                                                                   |
| [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)      | Define uma estrutura opaca e definida pelo usuário de dados de recuperação do KTM. As informações de recuperação são armazenadas em um log em nome de um RM (Gerenciador de recursos) chamando [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation). Após uma falha, o RM pode usar [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) para recuperar as informações.                  |
| [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)                                    | Indica que o Gerenciador de recursos (RM) está recusando uma solicitação de fase única. Quando um Gerenciador de transação (TM) recebe essa chamada, ele inicia uma confirmação de duas fases e envia uma solicitação de preparação para todos os RMs inscritos.                                                                                                                                                                                       |



 

 

 



