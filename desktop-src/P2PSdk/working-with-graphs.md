---
description: Ao trabalhar com grafos de pares, as funções devem ser chamadas em uma ordem específica. O fluxo de chamadas depende se você está criando ou abrindo um grafo de mesmo nível. Este tópico identifica o fluxo de chamadas de função em um aplicativo de grafo de pares simples.
ms.assetid: cb4f48d0-d1e2-4a4b-bd5a-6e8f66d03806
title: Trabalhando com grafos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4328b7a0109139421cf03c72a7228a3dc17e375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771825"
---
# <a name="working-with-graphs"></a>Trabalhando com grafos

Ao trabalhar com grafos de pares, as funções devem ser chamadas em uma ordem específica. O fluxo de chamadas depende se você está criando ou abrindo um grafo de mesmo nível. Este tópico identifica o fluxo de chamadas de função em um aplicativo de grafo de pares simples.

## <a name="starting-up-a-graph"></a>Iniciando um grafo

Antes que um aplicativo chame uma função na API de grafo de pares, [**PeerGraphStartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup) deve ser chamado para inicializar a API de grafo de pares para um aplicativo e, em seguida, definir a versão com suporte.

## <a name="creating-a-peer-graph"></a>Criando um grafo de mesmo nível

O procedimento a seguir identifica o fluxo de chamadas para criar um grafo de mesmo nível.

> [!IMPORTANT]
> Somente um par deve chamar [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate). Todos os outros pares devem chamar [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen). Várias chamadas para **PeerGraphCreate** invalidam um grafo.

 

-   Crie um grafo par. Chame [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate).
-   Registre-se para eventos de pares. Chame [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent).
    > [!Note]  
    > Para obter mais informações sobre como registrar-se para eventos de pares, consulte [infraestrutura de eventos](peer-events-infrastructure.md).

     

-   Ouça as conexões a um grafo par. Chame [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).
-   Executar funções dependentes do aplicativo para o restante do tempo de execução, por exemplo, processar eventos de mesmo nível e trabalhar com conexões.
-   Feche a conexão com um grafo par. Chame [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose).

## <a name="opening-a-peer-graph"></a>Abrindo um grafo par

O fluxo de chamadas de função para abrir um grafo de mesmo nível depende do valor de retorno da chamada para [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen). Os valores mais importantes são os **s \_ OK** e **\_ \_ os dados \_ de pares criados**, que são explicados nas seções a seguir deste tópico.

> [!Note]  
> Se uma chamada para [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) não retornar os dados de pares **\_ OK** ou **iguais \_ \_ \_ criados**, manipule o erro.

 

## <a name="when-peergraphopen-returns-s_ok"></a>Quando PeerGraphOpen retorna S \_ OK

Quando uma chamada para [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) retorna **S \_ OK**, um grafo par e um banco de dados existente foram abertos. O procedimento a seguir identifica o que você pode fazer para abrir um grafo de mesmo nível quando uma chamada para **PeerGraphOpen** retorna **S \_ OK**

-   Registre-se para eventos de pares. Chame [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent).
    > [!Note]  
    > Para obter mais informações sobre como registrar eventos, consulte [infraestrutura de eventos](peer-events-infrastructure.md).

     

-   Localize um nó. Esse é um processo executado fora da infraestrutura de grafo de pares, usando um método ou aplicativo que você identifica. A API de grafo de pares não fornece um mecanismo específico para localizar um nó de grafo inicial ao qual se conectar. Um aplicativo deve usar outro mecanismo, como a API [PNRP (Peer Name Resolution Protocol)](pnrp-namespace-provider-api.md) , para localizar o nó inicial.
-   Se um nó for encontrado, conecte-se a ele. Chame [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)e chame [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) para escutar conexões com o grafo par.
    > [!Note]  
    > Se um nó não for encontrado, não chame [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) e [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).

     

-   Executar funções dependentes do aplicativo para o restante do tempo de execução, por exemplo, processar eventos de mesmo nível e trabalhar com conexões, dependendo se o nó está conectado ao grafo de mesmo nível ou não. Por exemplo, o aplicativo pode escolher o tempo limite ou executar periodicamente a descoberta para um nó ativo no grafo.
-   Feche a conexão com o grafo par. Chame [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose).

## <a name="when-peergraphopen-returns-peer_s_data_created"></a>Quando PeerGraphOpen retorna \_ \_ os dados de pares \_ criados

Quando [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) retorna **\_ \_ os dados de pares \_ criados**, isso significa que um banco de dado existente para um grafo par não é encontrado, um novo banco de dados é criado e esta é a primeira vez que ele é aberto. Para usar ou escutar em um grafo par, um par deve estar conectado e sincronizado com um grafo par.

O procedimento a seguir identifica o que você pode fazer para abrir um grafo de mesmo nível quando uma chamada para [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) retorna **dados de pares \_ \_ \_ criados**.

-   Abra um grafo par. Chame [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen).
-   Registre-se para eventos de pares. Chame [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent).
    > [!Note]  
    > Para obter mais informações sobre como registrar-se para eventos de pares, consulte [infraestrutura de eventos](peer-events-infrastructure.md).

     

-   Localize um nó. Esse é um processo executado fora da infraestrutura de grafo de pares, usando um método ou aplicativo que você identifica. A API de grafo de pares não fornece um mecanismo específico para localizar um nó de grafo inicial ao qual se conectar. Um aplicativo deve usar outro mecanismo, como a API [PNRP (Peer Name Resolution Protocol)](pnrp-namespace-provider-api.md) , para localizar o nó inicial.
-   Se um nó for encontrado, conecte-se a ele. Chame [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)e chame [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) para escutar conexões com o grafo par.
    > [!Note]  
    > Se um nó não for encontrado, não chame [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) e [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).

     

-   Executar funções dependentes do aplicativo para o restante do tempo de execução, por exemplo, processar eventos de mesmo nível e trabalhar com conexões, dependendo se o nó está conectado ao grafo de mesmo nível ou não. Por exemplo, o aplicativo pode escolher o tempo limite ou executar periodicamente a descoberta para um nó ativo no grafo.
-   Feche a conexão com o grafo par. Chame [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose).

 

 



