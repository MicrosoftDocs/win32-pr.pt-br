---
description: Após qualquer tipo de falha que interrompe o processamento de transação normal, o KTM e cada gerenciador de recursos devem executar operações de recuperação. A recuperação é o processo pelo qual os participantes da transação chegam a uma exibição consistente de cada estado de transações.
ms.assetid: 5bc9a155-6ba4-41f8-8e12-e87f48d83940
title: Processamento de recuperação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec99ad63d18c95da3ebb3ad5db6c204301d75336cc1842dd21e1edf79f5f9a38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146489"
---
# <a name="recovery-processing"></a>Processamento de recuperação

Após qualquer tipo de falha que interrompe o processamento de transação normal, o KTM e cada gerenciador de recursos devem executar operações *de recuperação.* A recuperação é o processo pelo qual os participantes da transação chegam a uma exibição consistente do estado de cada transação.

Os gerenciadores  de recursos podem estar em dúvida sobre o resultado de uma transação, o que significa que, no momento da falha, eles tinham recebido uma notificação TRANSACTION NOTIFY PREPARE, tinham se preparado para o armazenamento durável, mas não tinham recebido (ou recebido, mas não registrados) um resultado final para \_ a \_ transação. Da mesma forma, o KTM pode estar em dúvida sobre uma transação se ela tiver sido preparada, mas não tiver recebido (ou recebido, mas não registrado) um resultado. No momento da recuperação, todos os resultados que foram enviados, mas não confirmados, devem ser enviados de volta. Por exemplo, se um gerenciador de recursos recebeu uma notificação TRANSACTION NOTIFY COMMIT e chamou a função \_ \_ [**CommitComplete,**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) o RM ainda poderá receber uma notificação TRANSACTION NOTIFY COMMIT duplicada no momento \_ \_ da recuperação.

Para que uma transação seja recuperada corretamente após uma falha do gerenciador de recursos ou do sistema, cada gerenciador de recursos deve fazer o seguinte sempre que for iniciada:

1.  Chame a [**função OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager) para rea abrir seu lidar do gerenciador de recursos usando seu nome exclusivo e persistente. Isso informa à KTM que o gerenciador de recursos está em execução novamente e está disponível para executar a recuperação. Se nenhuma inserção existir para ser recuperada, a chamada para **OpenResourceManager** poderá falhar. Chame [**CreateResourceManager para**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) criar o objeto RM.
2.  Chame [**RecoverResourceManager.**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverresourcemanager) O gerenciador de recursos receberá um evento de notificação [**TRANSACTION \_ NOTIFY \_ RECOVER**](notification-mask.md) para cada inscrever-se para o qual precisa executar operações de recuperação, seguida por uma TRANSACTION \_ NOTIFY LAST \_ \_ RECOVER. O evento de notificação inclui um identificador global exclusivo para a transação e a inscrições.
3.  Chame a [**função OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) para abrir novamente cada alça de inserção para a qual o gerenciador de recursos recebeu uma notificação TRANSACTION \_ NOTIFY \_ RECOVER.
4.  Para cada inserção aberta [**por OpenEnlistment,**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)chame [**RecoverEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverenlistment). Isso faz com que a notificação TRANSACTION \_ NOTIFY COMMIT ou TRANSACTION NOTIFY \_ \_ \_ INDOUBT seja entregue.
5.  Se o RM recebeu TRANSACTION NOTIFY COMMIT, o RM pode concluir a \_ transação chamando \_ [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete).

    Se o RM recebeu TRANSACTION \_ NOTIFY \_ INDOUBT, o RM deve aguardar a notificação de resultado chegar.

6.  Para todas as transações para as que o RM não recebe uma notificação TRANSACTION NOTIFY RECOVER, mas recebeu anteriormente uma notificação TRANSACTION NOTIFY PREPARE, o RM deve processar a transação como se tivesse sido \_ \_ re \_ \_ roll-back.

> [!Note]
>
> Os gerenciadores de recursos têm permissão para se inscrever ou criar novas transações durante o processo de execução da recuperação.

 

O KTM usa um *modelo de transação de anulação* presumido. O cenário a seguir ilustra esse comportamento. Suponha que o KTM e um gerenciador de recursos existam no mesmo computador. Suponha que o KTM emite uma notificação de preparação para uma transação, mas o sistema falha antes que o KTM registra a notificação de preparação. Suponha ainda que o gerenciador de recursos receba e registra a notificação de preparação logo antes de o sistema falhar. Depois que o sistema é restaurado, o KTM não tem conhecimento da transação, pois nunca registrou a fase de preparação. O gerenciador de recursos tem conhecimento da transação porque recebeu, processou e registrou a notificação de preparação. Quando o KTM emite suas notificações de recuperação, o gerenciador de recursos não inclui uma notificação de recuperação para a transação em questão. Com o modelo de anulação presumido, o gerenciador de recursos, nesse caso, tratará a transação preparada como anulada quando não receber notificações para executar a recuperação nessa transação.

 

 



