---
description: Um gerenciador de recursos se inslista em uma transação quando inicia a participação nessa transação específica.
ms.assetid: 9c201699-c00b-4efe-9f30-8d4e182de785
title: Inscrições
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c19fea9c19da9bb16f81bd417e22c943876997ac224e3823020e5660218dfa5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146579"
---
# <a name="enlistments"></a>Inscrições

Um gerenciador de recursos se inslista em uma transação quando inicia a participação nessa transação específica. A inscrever-se define quais notificações o gerenciador de recursos aceita. Um gerenciador de recursos cria um objeto de inscrever-se quando ele se ins inscrito em uma transação. Esse objeto sinaliza ao KTM que o RM (gerenciador de recursos) está solicitando notificações sobre a transação especificada.

O RM fornece uma estrutura [**NOTIFICATION \_ MASK**](notification-mask.md) que detalha quais notificações ele está solicitando.

## <a name="enlistment-functions"></a>Funções de inscrever-se

As funções a seguir são usadas com inscrições.



| Função                                                                          | Descrição                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)                                          | Indica que um RM (Gerenciador de Recursos) concluiu a confirmação de uma transação solicitada pelo TM (gerenciador de transações).                                                                                                                                                                                                                                                                        |
| [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)                                      | Cria uma instalação, define seu estado inicial e abre um alçamento para a instalação com o acesso especificado.                                                                                                                                                                                                                                                                                          |
| [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) | Recupera uma estrutura opaca de dados de recuperação de KTM. As informações de recuperação são armazenadas em um log em nome de um RM (gerenciador de recursos) chamando a [**função SetEnlistmentRecoveryInformation.**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation) Após uma falha, o RM pode usar a [**função GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) para recuperar as informações. |
| [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)                                          | Abre um objeto de inscrever-se existente e retorna um identificador para a inscrever-se.                                                                                                                                                                                                                                                                                                                            |
| [**ReadOnlyEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)                                  | Solicita que a insrução especificada seja convertida em uma inscrições somente leitura. Uma inscrições somente leitura não pode participar do resultado da transação e não é registrada de forma durável para recuperação.                                                                                                                                                                                                    |
| [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)                                  | Acumula a transação especificada associada a uma insrução. Essa função não pode ser chamada para inscrições somente leitura.                                                                                                                                                                                                                                                                   |
| [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)      | Define uma estrutura opaca definida pelo usuário de dados de recuperação da KTM. As informações de recuperação são armazenadas em um log em nome de um RM (gerenciador de recursos) chamando [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation). Após uma falha, o RM pode usar [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) para recuperar as informações.                  |
| [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)                                    | Indica que o RM (gerenciador de recursos) está recusando uma solicitação de fase única. Quando um TM (gerenciador de transações) recebe essa chamada, ele inicia uma commit em duas fases e envia uma solicitação de preparação para todas as RMs ins inscritos.                                                                                                                                                                                       |



 

 

 



