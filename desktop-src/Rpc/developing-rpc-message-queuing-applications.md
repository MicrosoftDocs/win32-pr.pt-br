---
title: Desenvolvendo aplicativos de enfileiramento RPC-Message
description: É necessário ter muito pouco esforço para aproveitar o transporte MSMQ em seu aplicativo RPC.
ms.assetid: 1ea97df8-cdf5-43b8-88aa-9e8fa6ae845a
keywords:
- Chamada de procedimento remoto RPC, tarefas, desenvolvendo aplicativos de enfileiramento de mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e51707c0a6903200e51dd35e50e998430c8eae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008054"
---
# <a name="developing-rpc-message-queuing-applications"></a>Desenvolvendo aplicativos de enfileiramento RPC-Message

É necessário ter muito pouco esforço para aproveitar o transporte MSMQ em seu aplicativo RPC. Para mensagens síncronas, você só precisa especificar o [**ncadg \_ MQ**](/windows/desktop/Midl/ncadg-mq)(transporte de fila de mensagens) como a sequência de protocolos. O **protocolo \_ MQ ncadg** dá suporte a todos os recursos de datagrama padrão, exceto chamadas de difusão. Além disso, observe que, no momento, o transporte de fila de mensagens não oferece suporte a pontos de extremidade dinâmicos.

Ao aplicar o \[ [](/windows/desktop/Midl/message) \] atributo Message a declarações de procedimento remoto no arquivo IDL, você implementa automaticamente o enfileiramento de mensagens em modo assíncrono para essas chamadas. Isso possibilita que os aplicativos de cliente e de servidor controlem muitas das propriedades associadas a mensagens e filas de mensagens, incluindo:

-   Qualidade do serviço
-   Confirmação de recebimento
-   Registro no diário
-   Prioridade da chamada
-   Persistência da fila de processo do servidor

A qualidade do serviço é o esforço que o transporte fará para fornecer a chamada para o processo do servidor. Uma entrega expressa será enfileirada na memória, portanto, é bem rápida, mas a chamada será perdida se uma conexão de rede ou computador ficar inativa no horário errado. Uma entrega recuperável será postada em um arquivo de disco até ser entregue, portanto, a chamada não será perdida, mesmo diante de uma falha do computador. Isso oferece entrega garantida, mas a um custo no desempenho conforme cada chamada é gravada no disco.

Você também pode instruir o transporte MSMQ a aguardar a confirmação de que a chamada atingiu a fila de destino (servidor) antes de retornar. A escolha dessa opção bloqueia o cliente até que o servidor reconheça a chamada, caso contrário, o controle retorna ao cliente imediatamente após fazer a chamada.

Usando o registro no diário, as chamadas podem ser registradas em disco. Se o registro no diário estiver ativado, cada chamada será registrada em disco conforme transmitida para o próximo salto em seu caminho para o processo do servidor.

A prioridade de chamada pode ser usada em conjunto com o atributo de função de \[ [**mensagem**](/windows/desktop/Midl/message) RPC \] para permitir que chamadas com prioridade mais alta tenham precedência sobre chamadas com prioridade mais baixa, mesmo que as chamadas de alta prioridade cheguem mais tarde. A prioridade de chamada também funcionará de forma limitada com o RPC síncrono, mas as chamadas RPC síncronas não podem ser empilhadas da mesma maneira que as chamadas assíncronas.

O processo de cliente controla todas as propriedades acima chamando [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption). Depois de definido, essas propriedades permanecerão em vigor até que sejam alteradas em outra chamada para **RpcBindingSetOption**.

O processo do servidor RPC pode controlar o tempo de vida de sua fila de recebimento. Por padrão, a fila é excluída quando o processo do servidor é encerrado. No entanto, o processo do servidor pode usar [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) ao configurar seu ponto de extremidade para informar ao transporte para permitir que a fila continue existindo e para aceitar solicitações de chamada mesmo quando o processo do servidor não estiver em execução. Nesse caso, as chamadas são enfileiradas e executadas posteriormente, quando o processo do servidor volta a ficar online.

> [!Note]  
> Se você estiver usando chamadas de mensagens assíncronas \[ [](/windows/desktop/Midl/message) \] em uma interface, deverá registrar a interface chamando [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) ou [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) antes de chamar [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)**(ncadg \_ MQ)**. Depois de ativar a sequência de protocolo, todas as chamadas que já estiverem aguardando na fila para o servidor começarão a ser lidas na fila. Se a interface RPC correspondente não tiver sido registrada, as chamadas falharão. Essa situação pode ocorrer se você tiver uma configuração de um ponto de extremidade permanente para suas chamadas de procedimento remoto, o servidor tiver sido desligado e os clientes continuarem a enviar chamadas para o servidor. Essas chamadas serão empilhadas na fila, aguardando para serem lidas quando o servidor ficar online novamente.

 

Para obter mais informações, consulte [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption), [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)e \[ [**Message**](/windows/desktop/Midl/message) \] , [**ncadg \_ MQ**](/windows/desktop/Midl/ncadg-mq).

 

 