---
description: É importante distinguir entre desligar uma conexão de soquete e fechar um soquete.
ms.assetid: f076b1ec-6b96-4386-8519-4728e0a2b1ff
title: Desligamento normalmente, opções de persistente e fechamento de soquete na SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5791732404948fe59d3f5c15c2ac46cdbba8d8327fb3dc5f794be1f070a9eeff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132129"
---
# <a name="graceful-shutdown-linger-options-and-socket-closure-in-the-spi"></a>Desligamento normalmente, opções de persistente e fechamento de soquete na SPI

É importante distinguir entre desligar uma conexão de soquete e fechar um soquete. Desligar uma conexão de soquete envolve uma troca de mensagens de protocolo entre os dois pontos de extremidade, que é conhecido como uma sequência de desligamento. Duas classes gerais de sequências de desligamento são definidas: normalmente e anulativa. Em uma sequência de desligamento normalmente, todos os dados que foram en fila, mas que ainda não foram transmitidos, podem ser enviados antes que a conexão seja fechada. Em um desligamento anulativo, todos os dados não importantes são perdidos. A ocorrência de uma sequência de desligamento (normalmente ou anulativa) também pode ser usada para fornecer uma indicação FD CLOSE para os aplicativos associados, indicando que \_ um desligamento está em andamento. Fechar um soquete, por outro lado, faz com que o alça de soquete se torne desaloqueado para que o aplicativo não possa mais referenciar ou usar o soquete de nenhuma maneira.

No Windows Sockets, a função [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) e a função [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) podem ser usadas para iniciar uma sequência de desligamento, enquanto a [**função WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) é usada para desalocar os alças de soquete e liberar todos os recursos associados. No entanto, surge alguma confusão do fato de que a função **WSPCloseSocket** causará implicitamente uma sequência de desligamento se ela ainda não tiver ocorrido. Na verdade, tornou-se uma prática de programação bastante comum contar com esse recurso e usar **WSPCloseSocket** para iniciar a sequência de desligamento e desalocar o alça de soquete.

Para facilitar esse uso, a interface de soquetes fornece controles por meio do mecanismo de opção de soquete que permite que o programador indique se a sequência de desligamento implícita deve ser normal ou anulativa e também se a função deve permanecer ou não concluída imediatamente) para permitir que uma sequência de desligamento normal seja concluída.

Ao estabelecer valores apropriados para as opções de soquete SO LINGER e SO DONTLINGER, os seguintes tipos de comportamento podem ser obtidos com a \_ \_ função [**WSPCloseSocket.**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))

-   Sequência de desligamento anulativo, retorno imediato de [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)).
-   Desligamento normalmente, retorno de atraso até que uma sequência de desligamento seja concluída ou um intervalo de tempo especificado. Se o intervalo de tempo expirar antes da conclusão da sequência de desligamento normalmente, ocorrerá uma sequência de desligamento anulativo e [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) retornará.
-   Desligamento normalmente, retorne imediatamente e permita que a sequência de desligamento seja concluída em segundo plano. Esse é o comportamento padrão. Observe, no entanto, que o aplicativo não tem como saber quando (ou se) a sequência de desligamento normalmente é concluída.

Uma técnica que pode ser usada para minimizar a chance de problemas que ocorrem durante a rebaixamento de conexão é não depender de um desligamento implícito que está sendo iniciado pelo [**WSPCloseSocket.**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) Em vez disso, uma das duas funções de desligamento explícitas ([**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) ou [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85))) é usada. Isso, por sua vez, fará com que uma indicação FD CLOSE seja recebida pelo aplicativo par, indicando que todos os dados pendentes \_ foram recebidos. Para ilustrar isso, a tabela a seguir mostra as funções que seriam invocadas pelos componentes de cliente e servidor de um aplicativo, em que o cliente é responsável por iniciar um desligamento normalmente.

| Lado do cliente                                                                                                                         | Lado do Servidor                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| (1) Invoca [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) (*s*, SD SEND) para sinalizar o fim da sessão e que o cliente não tem \_ mais dados a enviar. |                                                                                                              |
|                                                                                                                                     | (2) Recebe FD CLOSE, indicando o desligamento normalmente em \_ andamento e que todos os dados foram recebidos.        |
|                                                                                                                                     | (3) Envia todos os dados de resposta restantes.                                                                       |
| (5') Obtém FD READ e invoca recv para obter todos os dados \_ de resposta enviados pelo servidor.                                                         | (4) Invoca [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85))(*s*, SD SEND) para indicar que o servidor não \_ tem mais dados a enviar. |
| (5) Recebe a indicação FD \_ CLOSE.                                                                                                  | (4') Invoca [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                      |
| (6) Invoca [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                              |                                                                                                              |



 

A sequência de tempo é mantida da etapa (1) para a etapa (6) entre o cliente e o servidor, exceto pelas etapas (4') e (5'), que só têm significância de tempo local no sentido de que a etapa (5) segue a etapa (5') no lado do cliente, enquanto a etapa (4') segue a etapa (4) no lado do servidor, sem relação de tempo com a parte remota.

 

 
