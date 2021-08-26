---
description: Ao trabalhar com grafos de pares, as funções devem ser chamadas em uma ordem específica. O fluxo de chamadas depende se você está criando ou abrindo um grafo par. Este tópico identifica o fluxo de chamadas de função em um aplicativo de grafo par simples.
ms.assetid: cb4f48d0-d1e2-4a4b-bd5a-6e8f66d03806
title: Trabalhando com grafos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcdb4a40f1c086ada772239798990c3dfb24326b3e70bd768a95eacc35ee384b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034026"
---
# <a name="working-with-graphs"></a>Trabalhando com grafos

Ao trabalhar com grafos de pares, as funções devem ser chamadas em uma ordem específica. O fluxo de chamadas depende se você está criando ou abrindo um grafo par. Este tópico identifica o fluxo de chamadas de função em um aplicativo de grafo par simples.

## <a name="starting-up-a-graph"></a>Iniciando um Graph

Antes que um aplicativo chama uma função na API de Grafo de Pares, [**PeerGraphStartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup) deve ser chamado para inicializar a API de Grafo de Pares para um aplicativo e, em seguida, definir a versão com suporte.

## <a name="creating-a-peer-graph"></a>Criando um par Graph

O procedimento a seguir identifica o fluxo de chamadas para criar um grafo par.

> [!IMPORTANT]
> Apenas um par deve chamar [**PeerGraphCriar**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate). Todos os outros pares devem chamar [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen). Várias chamadas para **PeerGraphCriar** invalidar um grafo.

 

-   Criar um grafo par. Chame [**PeerGraphCriar**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate).
-   Registre-se para eventos de par. Chame [**PeerGraphRegisterEvent.**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)
    > [!Note]  
    > Para obter mais informações sobre o registro de eventos de pares, consulte [Infraestrutura de eventos](peer-events-infrastructure.md).

     

-   Escutar conexões com um grafo par. Chame [**PeerGraphListen.**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)
-   Execute funções dependentes do aplicativo pelo restante do tempo de execução, por exemplo, processar eventos de pares e trabalhar com conexões.
-   Feche a conexão com um grafo par. Chame [**PeerGraphClose.**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)

## <a name="opening-a-peer-graph"></a>Abrindo um par Graph

O fluxo de chamadas de função para abrir um grafo par depende do valor de retorno da chamada para [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen). Os valores mais importantes são **S \_ OK** e **PEER S DATA \_ \_ \_ CREATED,** que são explicados nas seções a seguir deste tópico.

> [!Note]  
> Se uma chamada para [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) não retornar **S \_ OK** ou **PEER S DATA \_ \_ \_ CREATED**, tratará o erro.

 

## <a name="when-peergraphopen-returns-s_ok"></a>Quando PeerGraphOpen retorna S \_ OK

Quando uma chamada para [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) retorna **S \_ OK**, um grafo par e um banco de dados existente foram abertos. O procedimento a seguir identifica o que você pode fazer para abrir um grafo de pares quando uma chamada para **PeerGraphOpen** retorna **S \_ OK**

-   Registre-se para eventos de par. Chame [**PeerGraphRegisterEvent.**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)
    > [!Note]  
    > Para obter mais informações sobre o registro de eventos, consulte [Infraestrutura de eventos](peer-events-infrastructure.md).

     

-   Localize um nó. Esse é um processo executado fora da infraestrutura de grafo de pares, usando um método ou aplicativo que você identifica. A API de Grafo de Pares não fornece um mecanismo específico para encontrar um nó de grafo inicial ao que se conectar. Um aplicativo deve usar outro mecanismo, como a API [PNRP (Protocolo](pnrp-namespace-provider-api.md) de Resolução de Nomes Pares), para localizar o nó inicial.
-   Se um nó for encontrado, conecte-se a ele. Chame [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)e, em seguida, [**chame PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) para escutar conexões com o grafo par.
    > [!Note]  
    > Se um nó não for encontrado, não chame [**PeerGraphConnect e**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) [**PeerGraphListen.**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)

     

-   Execute funções dependentes do aplicativo pelo restante do tempo de execução, por exemplo, processe eventos de pares e trabalhe com conexões, dependendo se o nó está conectado ao grafo par ou não. Por exemplo, o aplicativo pode optar por tempo acima ou executar periodicamente a descoberta de um nó ativo no grafo.
-   Feche a conexão com o grafo par. Chame [**PeerGraphClose.**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)

## <a name="when-peergraphopen-returns-peer_s_data_created"></a>Quando PeerGraphOpen retorna DADOS \_ PARES \_ CRIADOS \_

Quando [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) retorna **PEER S DATA \_ \_ \_ CREATED**, isso significa que um banco de dados existente para um grafo par não é encontrado, um novo banco de dados é criado e esta é a primeira vez que ele é aberto. Para usar ou escutar em um grafo par, um par deve ser conectado e sincronizado com um grafo par.

O procedimento a seguir identifica o que você pode fazer para abrir um grafo de pares quando uma chamada para [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) retorna **PEER S DATA \_ \_ \_ CREATED**.

-   Abra um grafo par. Chame [**PeerGraphOpen.**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)
-   Registre-se para eventos de par. Chame [**PeerGraphRegisterEvent.**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)
    > [!Note]  
    > Para obter mais informações sobre o registro de eventos de pares, consulte [Infraestrutura de eventos](peer-events-infrastructure.md).

     

-   Localize um nó. Esse é um processo executado fora da infraestrutura de grafo de pares, usando um método ou aplicativo que você identifica. A API de Grafo de Pares não fornece um mecanismo específico para encontrar um nó de grafo inicial ao que se conectar. Um aplicativo deve usar outro mecanismo, como a API [PNRP (Protocolo](pnrp-namespace-provider-api.md) de Resolução de Nomes Pares), para localizar o nó inicial.
-   Se um nó for encontrado, conecte-se a ele. Chame [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)e, em seguida, [**chame PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) para escutar conexões com o grafo par.
    > [!Note]  
    > Se um nó não for encontrado, não chame [**PeerGraphConnect e**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) [**PeerGraphListen.**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)

     

-   Execute funções dependentes do aplicativo pelo restante do tempo de execução, por exemplo, processe eventos de pares e trabalhe com conexões, dependendo se o nó está conectado ao grafo par ou não. Por exemplo, o aplicativo pode optar por tempo acima ou executar periodicamente a descoberta de um nó ativo no grafo.
-   Feche a conexão com o grafo par. Chame [**PeerGraphClose.**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)

 

 



