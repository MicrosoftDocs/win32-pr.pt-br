---
description: O material a seguir é fornecido como esclarecimento para o assunto de desligar conexões de soquete que fecham os soquetes. É importante distinguir a diferença entre desligar uma conexão de soquete e fechar um soquete.
ms.assetid: 383747c3-dd3d-4a18-b4e8-2815d5e5c0c7
title: Desligamento normal, opções persistentes e fechamento de soquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59f6791eaa803da561fc9f3c175b5270950cbec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164473"
---
# <a name="graceful-shutdown-linger-options-and-socket-closure"></a>Desligamento normal, opções persistentes e fechamento de soquete

O material a seguir é fornecido como esclarecimento para o assunto de desligar conexões de soquete que fecham os soquetes. É importante distinguir a diferença entre desligar uma conexão de soquete e fechar um soquete.

Desligar uma conexão de soquete envolve uma troca de mensagens de protocolo entre os dois pontos de extremidade, daqui em diante, chamado de sequência de desligamento. Duas classes gerais de sequências de desligamento são definidas: normal e de anulação (também chamada de difícil). Em uma sequência de desligamento normal, todos os dados que foram enfileirados, mas ainda não transmitidos, podem ser enviados antes que a conexão seja fechada. Em um desligamento anulado, todos os dados não enviados são perdidos. A ocorrência de uma sequência de desligamento (normal ou de anulação) também pode ser usada para fornecer uma \_ indicação FD Close para os aplicativos associados, indicando que um desligamento está em andamento.

Fechar um soquete, por outro lado, faz com que o identificador de soquete se torne desalocado para que o aplicativo não possa mais fazer referência ou usar o soquete de forma alguma.

No Windows Sockets, a função de [**desligamento**](/windows/desktop/api/winsock/nf-winsock-shutdown) e a função [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) podem ser usadas para iniciar uma sequência de desligamento, enquanto a função [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) é usada para desalocar identificadores de soquete e liberar todos os recursos associados. Uma certa confusão surge, no entanto, do fato de que a função **fechamento** implicitamente faz com que uma sequência de desligamento ocorra caso ainda não tenha ocorrido. Na verdade, ele se tornou uma prática de programação bastante comum para contar com esse recurso e usar o **fechamento** para iniciar a sequência de desligamento e desalocar o identificador de soquete.

Para facilitar esse uso, a interface de soquetes fornece controles por meio do mecanismo de opção de soquete que permite que o programador indique se a sequência de desligamento implícita deve ser normal ou anulada, e também se a função [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) deve permanecer (não concluída imediatamente) para dar tempo para a conclusão de uma sequência de desligamento normal. Essas distinções importantes e as ramificações de usar **fechamento** dessa maneira ainda não são amplamente compreendidas.

Ao estabelecer os valores apropriados para as opções de soquete, de modo \_ remanescente e, portanto \_ , DONTLINGER, os seguintes tipos de comportamento podem ser obtidos com a função [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) :

-   Sequência de desligamento abortada, retorno imediato de [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket).
-   Desligamento normal, atrasando o retorno até que a sequência de desligamento seja concluída ou um intervalo de tempo especificado decorre. Se o intervalo de tempo expirar antes da conclusão da sequência de desligamento normal, ocorrerá uma sequência de desligamento abortada e [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) retornará.
-   Desligamento normal, retorno imediato — permitindo que a sequência de desligamento seja concluída em segundo plano. Embora esse seja o comportamento padrão, o aplicativo não tem como saber quando (ou se) a sequência de desligamento normal é realmente concluída.

O uso das opções de \_ soquete de so persistentes e \_ de DONTLINGER e a estrutura [**persistente**](/windows/desktop/api/winsock/ns-winsock-linger) associada é discutida mais detalhadamente nas seções de referência nas opções de [**soquete de \_ soquete de sol**](sol-socket-socket-options.md) e na estrutura **persistente** .

Uma técnica que pode ser usada para minimizar a chance de problemas ocorrendo durante a desmontagem da conexão é evitar depender de um desligamento implícito que está sendo iniciado pelo [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket). Em vez disso, use uma das duas funções de desligamento explícitas, [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) ou [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect). Isso, por sua vez, faz com \_ que uma indicação de fechamento FD seja recebida pelo aplicativo par, indicando que todos os dados pendentes foram recebidos. Para ilustrar isso, a tabela a seguir mostra as funções que seriam invocadas pelos componentes do cliente e do servidor de um aplicativo, em que o cliente é responsável por iniciar um desligamento normal.

| Lado do cliente                                                                                                                | Lado do Servidor                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| (1) invoca o [**desligamento**](/windows/desktop/api/winsock/nf-winsock-shutdown)(s, SD \_ Send) para sinalizar o fim da sessão e esse cliente não tem mais dados a serem enviados. |                                                                                                       |
|                                                                                                                            | (2) recebe FD \_ Close, indicando que o desligamento normal está em andamento e que todos os dados foram recebidos. |
|                                                                                                                            | (3) envia todos os dados de resposta restantes.                                                                |
| (somente significância de tempo local) Obtém o FD \_ Read e chama [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) para obter os dados de resposta enviados pelo servidor.  | (4) invoca o [**desligamento**](/windows/desktop/api/winsock/nf-winsock-shutdown)(s, SD \_ Send) para indicar que o servidor não tem mais dados a serem enviados.  |
| (5) recebe a \_ indicação de fechamento FD.                                                                                         | (somente significância de tempo local) Invoca [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) .                       |
| (6) invoca [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket).                                                                          |                                                                                                       |



 

 

 



