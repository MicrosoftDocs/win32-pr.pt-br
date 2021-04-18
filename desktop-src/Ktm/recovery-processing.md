---
description: Após qualquer tipo de falha que interrompa o processamento normal de transações, o KTM e cada Gerenciador de recursos devem executar operações de recuperação. A recuperação é o processo pelo qual os participantes da transação chegam em uma exibição consistente de cada Estado de transações.
ms.assetid: 5bc9a155-6ba4-41f8-8e12-e87f48d83940
title: Processamento de recuperação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8e74d4f8bff3e56af03b017522212e7a02e232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796342"
---
# <a name="recovery-processing"></a>Processamento de recuperação

Após qualquer tipo de falha que interrompa o processamento normal de transações, o KTM e cada Gerenciador de recursos devem executar operações de *recuperação* . A recuperação é o processo pelo qual os participantes da transação chegam em uma exibição consistente do estado de cada transação.

Os gerenciadores de *recursos podem ser* inoportunos sobre o resultado de uma transação, ou seja, no momento da falha, receberam uma notificação de preparação de notificação de transação \_ , se \_ preparou com o armazenamento durável, mas não havia recebido (ou recebido, mas não registrado) um resultado final para a transação. Da mesma forma, o KTM pode ser incerto sobre uma transação, caso tenha sido preparada, mas não tenha recebido (ou recebido, mas não registrado) um resultado. No momento da recuperação, todos os resultados enviados, mas não confirmados, devem ser enviados novamente. Por exemplo, se um Gerenciador de recursos tiver recebido uma notificação de confirmação de notificação de transação \_ \_ e tiver chamado a função [**COMMITCOMPLETE**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) , o RM ainda poderá receber uma notificação de confirmação de transação duplicada \_ \_ no momento da recuperação.

Para que uma transação seja recuperada corretamente após uma falha do sistema ou do Gerenciador de recursos, cada Gerenciador de recursos deve fazer o seguinte sempre que for iniciado:

1.  Chame a função [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager) para reabrir seu identificador do Gerenciador de recursos usando seu nome exclusivo e persistente. Isso informa ao KTM que o Gerenciador de recursos está em execução novamente e está disponível para executar a recuperação. Se não existirem inlistagens a serem recuperadas, a chamada para **OpenResourceManager** poderá falhar. Chame [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) para recriar o objeto RM.
2.  Chame [**RecoverResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverresourcemanager). O Gerenciador de recursos receberá um evento Notification [**\_ Notification \_**](notification-mask.md) de notificação de recuperação para cada inscrição para a qual precisa realizar operações de recuperação, seguida de uma transação \_ notificar a \_ última \_ recuperação. O evento de notificação inclui um identificador global exclusivo para a transação e a inscrição.
3.  Chame a função [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) para abrir novamente cada identificador de inscrição para o qual o Gerenciador de recursos recebeu uma notificação de recuperação de notificação de transação \_ \_ .
4.  Para cada Inscrição aberta pelo [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment), chame [**RecoverEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverenlistment). Isso faz com que a notificação de notificação de confirmação de transação \_ \_ ou de incerteza de transação \_ \_ seja entregue novamente.
5.  Se o RM recebeu a \_ confirmação de notificação de transação \_ , o RM poderá concluir a transação chamando [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete).

    Se o RM recebeu uma \_ notificação de \_ incerteza de transação, o RM deve aguardar a chegada da notificação de resultado.

6.  Para todas as transações que o RM não recebe uma notificação de recuperação de notificação de transação \_ \_ , mas anteriormente recebeu uma \_ \_ notificação de preparação de notificação de transação para, o RM deve processar a transação como se fosse revertida.

> [!Note]
>
> Os gerenciadores de recursos têm permissão para inscrever-se ou criar novas transações durante o processo de execução da recuperação.

 

O KTM usa um modelo de transação de *anulação presumido* . O cenário a seguir ilustra esse comportamento. Suponha que o KTM e um Gerenciador de recursos existam no mesmo computador. Suponha que o KTM emita uma notificação de preparação para uma transação, mas o sistema falha antes de o KTM registrar a notificação de preparação. Suponha ainda que o Gerenciador de recursos receba e registre a notificação de preparação imediatamente antes do sistema falhar. Depois que o sistema é restaurado, o KTM não tem conhecimento da transação, porque ele nunca registrou a fase de preparação. O Gerenciador de recursos tem conhecimento da transação, pois recebeu, processou e registrou a notificação de preparação. Quando o KTM emite suas notificações de recuperação, o Gerenciador de recursos não inclui uma notificação de recuperação para a transação em questão. Com o modelo de anulação presumido, o Gerenciador de recursos, nesse caso, tratará a transação preparada como anulada quando não receber notificações para executar a recuperação nessa transação.

 

 



