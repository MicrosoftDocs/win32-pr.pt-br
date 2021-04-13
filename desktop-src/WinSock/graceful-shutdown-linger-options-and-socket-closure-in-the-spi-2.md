---
description: É importante distinguir entre desligar uma conexão de soquete e fechar um soquete.
ms.assetid: f076b1ec-6b96-4386-8519-4728e0a2b1ff
title: Desligamento normal, opções persistentes e fechamento de soquete no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743cae48977421c08611c79053520799420e9e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501693"
---
# <a name="graceful-shutdown-linger-options-and-socket-closure-in-the-spi"></a>Desligamento normal, opções persistentes e fechamento de soquete no SPI

É importante distinguir entre desligar uma conexão de soquete e fechar um soquete. Desligar uma conexão de soquete envolve uma troca de mensagens de protocolo entre os dois pontos de extremidade, que daqui em diante é chamado de sequência de desligamento. Duas classes gerais de sequências de desligamento são definidas: normal e de anulação. Em uma sequência de desligamento normal, todos os dados que foram enfileirados, mas ainda não transmitidos, podem ser enviados antes que a conexão seja fechada. Em um desligamento anulado, todos os dados não enviados são perdidos. A ocorrência de uma sequência de desligamento (normal ou de anulação) também pode ser usada para fornecer uma \_ indicação FD Close para os aplicativos associados, indicando que um desligamento está em andamento. Fechar um soquete, por outro lado, faz com que o identificador de soquete se torne desalocado para que o aplicativo não possa mais fazer referência ou usar o soquete de forma alguma.

No Windows Sockets, a função [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) e a função [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) podem ser usadas para iniciar uma sequência de desligamento, enquanto a função [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) é usada para desalocar identificadores de soquete e liberar todos os recursos associados. Uma certa confusão surge, no entanto, do fato de que a função **WSPCloseSocket** resultará implicitamente na ocorrência de uma sequência de desligamento, caso ainda não tenha ocorrido. Na verdade, ele se tornou uma prática de programação bastante comum para contar com esse recurso e usar **WSPCloseSocket** para iniciar a sequência de desligamento e desalocar o identificador de soquete.

Para facilitar esse uso, a interface de soquetes fornece controles por meio do mecanismo de opção de soquete que permite que o programador indique se a sequência de desligamento implícita deve ser normal ou anulada, e também se a função deve permanecer ou não concluída imediatamente) para dar tempo para que uma sequência de desligamento normal seja concluída.

Ao estabelecer os valores apropriados para as opções de soquete, de modo \_ remanescente e, portanto \_ , DONTLINGER, os seguintes tipos de comportamento podem ser obtidos com a função [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) .

-   Sequência de desligamento abortada, retorno imediato de [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)).
-   Desligamento normal, atraso de retorno até que a sequência de desligamento seja concluída ou um intervalo de tempo especificado decorra. Se o intervalo de tempo expirar antes da conclusão da sequência de desligamento normal, ocorrerá uma sequência de desligamento anulada e [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) retornará.
-   Desligamento normal, retornar imediatamente e permitir que a sequência de desligamento seja concluída em segundo plano. Esse é o comportamento padrão. No entanto, observe que o aplicativo não tem como saber quando (ou se) a sequência de desligamento normal é concluída.

Uma técnica que pode ser usada para minimizar a chance de problemas ocorrendo durante a desmontagem da conexão não depende de um desligamento implícito ser iniciado pelo [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)). Em vez disso, uma das duas funções explícitas de desligamento ([**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) ou [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85))) são usadas. Isso, por sua vez, fará com \_ que uma indicação de fechamento FD seja recebida pelo aplicativo de mesmo nível indicando que todos os dados pendentes foram recebidos. Para ilustrar isso, a tabela a seguir mostra as funções que seriam invocadas pelos componentes do cliente e do servidor de um aplicativo, em que o cliente é responsável por iniciar um desligamento normal.

| Lado do cliente                                                                                                                         | Lado do Servidor                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| (1) invoca [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) (*s*, SD \_ Send) para sinalizar o fim da sessão e esse cliente não tem mais dados a serem enviados. |                                                                                                              |
|                                                                                                                                     | (2) recebe FD \_ Close, indicando que o desligamento normal está em andamento e que todos os dados foram recebidos.        |
|                                                                                                                                     | (3) envia todos os dados de resposta restantes.                                                                       |
| (5 ') obtém FD \_ Read e Invoke recv para obter os dados de resposta enviados pelo servidor.                                                         | (4) invoca [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85))(*s*, SD \_ Send) para indicar que o servidor não tem mais dados para enviar. |
| (5) recebe a \_ indicação de fechamento FD.                                                                                                  | (4 ') invoca [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                      |
| (6) invoca [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                              |                                                                                                              |



 

A sequência de tempo é mantida da etapa (1) para a etapa (6) entre o cliente e o servidor, exceto para as etapas (4 ') e (5 ') que têm apenas a diferença de tempo local no sentido em que a etapa (5) segue a etapa (5 ') no lado do cliente enquanto a etapa (4 ') segue a etapa (4) no lado do servidor, sem nenhuma relação de tempo com a parte remota.

 

 
