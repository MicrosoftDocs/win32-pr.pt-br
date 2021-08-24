---
description: A infraestrutura de mesmo nível usa eventos para notificar aplicativos de alterações que ocorreram em uma rede de mesmo nível, por exemplo, um nó que é adicionado ou removido de um grafo.
ms.assetid: a056da1c-b8f9-4dad-8df9-df24c6b359b7
title: Infraestrutura de eventos de pares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a889f59e4429e64258c047dfbf0249bb4dca125bfc3f9d659e6042dd40be9443
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119775946"
---
# <a name="peer-events-infrastructure"></a>Infraestrutura de eventos de pares

A infraestrutura de mesmo nível usa eventos para notificar aplicativos de alterações que ocorreram em uma rede de mesmo nível, por exemplo, um nó que é adicionado ou removido de um grafo. O grafo de pares e as infraestruturas de agrupamento de pares usam a infraestrutura de eventos de pares.

## <a name="receiving-peer-event-notification"></a>Recebendo notificação de eventos de pares

Um par pode se registrar para receber notificações quando um atributo de um grafo ou grupo for alterado ou ocorrer um evento de mesmo nível específico. Um aplicativo de mesmo nível chama a função [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent) ou [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent) e passa um identificador de evento para a infraestrutura de mesmo nível, que é criada anteriormente por uma chamada para [**CreateEvent**](graphing-reference-links.md). A infraestrutura de mesmo nível usa o identificador para sinalizar um aplicativo que ocorreu um evento de mesmo nível.

O aplicativo também passa uma série de estruturas de [**\_ \_ \_ registro**](/windows/desktop/api/P2P/ns-p2p-peer_group_event_registration) de eventos de [**\_ grafo \_ \_**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_registration) de pares ou de grupo de pares que indicam à infraestrutura de pares os eventos de pares específicos para os quais o aplicativo está solicitando a notificação. O aplicativo também deve especificar exatamente quantas estruturas estão sendo passadas.

## <a name="peer-graphing-events"></a>Eventos de grafo de pares

Um aplicativo de grafo de pares pode se registrar para receber notificações para 9 eventos de grafo de pares. Cada nome de evento é precedido com o **\_ \_ evento \_ de grafo par**, por exemplo, o **status do grafo de pares \_ \_ \_ foi alterado**. Salvo indicação em contrário, as informações sobre uma alteração são recuperadas usando [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata).

-   **Par \_ O \_ status do evento de grafo \_ \_ alterado** indica que o status de um grafo foi alterado, por exemplo, um nó foi sincronizado com um grafo.
-   **Par \_ A \_ propriedade de evento do grafo \_ \_ alterada** indica que uma propriedade de um grafo ou grupo foi alterada, por exemplo, o nome amigável de um grafo foi alterado.
    > [!Note]  
    > O aplicativo deve chamar [**PeerGraphGetProperties**](/windows/desktop/api/P2P/nf-p2p-peergraphgetproperties) para obter as informações alteradas.

     

-   **Par \_ O \_ registro de evento de grafo \_ \_ alterado** indica que um registro foi alterado, por exemplo, um registro é excluído.
-   **Par \_ \_ \_ \_ Conexão direta de evento de grafo** indica que uma conexão direta foi alterada, por exemplo, um nó conectado.
-   **Par \_ \_Conexão de \_ vizinho \_ de evento de grafo** indica que uma conexão com um nó vizinho é alterada, por exemplo, um nó se conectou.
-   **Par \_ \_Dados de \_ entrada \_ de evento de grafo** indicam que os dados foram recebidos de uma conexão direta ou de vizinho.
-   **Par \_ Conexão de evento de grafo \_ \_ \_ necessária** indica que a infraestrutura de gráfico requer uma nova conexão.
    > [!Note]  
    > Uma chamada para [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) se conecta a um novo nó. Uma chamada para [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata) não retorna dados.

     

-   **Par \_ Nó de evento de grafo \_ \_ \_ alterado** indica que as informações de presença de nó foram alteradas, por exemplo, um endereço IP foi alterado.
-   **Par \_ O \_ evento \_ sincronizado do Graph** indica que um tipo de registro específico está sincronizado.

Depois que um aplicativo recebe uma notificação de que ocorreu um evento de par, o aplicativo chama [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata)e passa o identificador de evento de par retornado por [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent). A infraestrutura de pares retorna um ponteiro para uma estrutura de [**\_ dados de \_ evento \_ de grafo par**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) que contém os dados solicitados. Essa função deve ser chamada até **que \_ pares \_ nenhum \_ \_ dado de evento** seja retornado.

Depois que um aplicativo não requer uma notificação de evento de mesmo nível, o aplicativo chama [**PeerGraphUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphunregisterevent)e passa o identificador de evento de par retornado pelo [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent) quando o aplicativo é registrado.

## <a name="handling-graph-connection-referrals"></a>manipulando referências de conexão Graph

Quando [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) é chamado, o ponto de conexão é notificado sobre êxito ou falha por meio do evento de **conexão de vizinho de evento de grafo de pares \_ \_ \_ \_** assíncrono. Se a conexão falhou devido a problemas de rede específicos (como um firewall configurado incorretamente), o evento **de \_ \_ conexão de \_ vizinho \_ do evento de grafo par** é gerado, com o status da conexão definido como **par \_ conexão \_ falhou**.

No entanto, quando um par recebe uma referência quando tenta se conectar a um nó ocupado, **a \_ \_ conexão de \_ vizinho \_ do evento de grafo par** é gerada no ponto de conexão, com o status da conexão definido como **par \_ conexão \_ falha**. O ponto de conexão pode ser referenciado em outro nó que está ocupado e pode enviar uma referência, e o mesmo evento e status são gerados no ponto de conexão. Essa cadeia de referências que resultam em status de evento de **\_ \_ falha na conexão de pares** pode continuar até que o número máximo de tentativas de conexão seja esgotado. O par não tem um mecanismo para determinar a diferença entre uma tentativa de conexão completa e a referência de conexão.

Para resolver esse problema, os desenvolvedores devem considerar o uso de eventos de alteração de status do grafo de pares para determinar se a tentativa de conexão bem-sucedido. Se o evento não for recebido dentro de um período de tempo específico, o aplicativo poderá assumir que o ponto de conexão está sendo referenciado e que o aplicativo par deve considerar a tentativa de conexão com uma falha.

## <a name="peer-grouping-events"></a>Eventos de agrupamento de pares

Um aplicativo de agrupamento de pares pode se registrar para receber notificações de 8 eventos de mesmo nível. Cada nome de evento é precedido com o **\_ \_ evento \_ de grupo de pares**; por exemplo, o status do evento de grupo de **pares \_ \_ \_ \_ foi alterado**. Salvo indicação em contrário, as informações sobre uma alteração são recuperadas usando [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata).

-   **Par \_ O \_ status do evento de grupo \_ \_ alterado** indica que o status do grupo foi alterado. Há dois valores de status possíveis: **\_ escuta de \_ status \_ do grupo de pares**, que indica que o grupo não tem conexões e está aguardando novos membros; e o status do grupo de **pares \_ \_ \_ tem conexões**, o que indica que o grupo tem pelo menos uma conexão. Esse valor de status pode ser obtido chamando [**PeerGroupGetStatus**](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus) depois que esse evento é gerado.
-   **Par \_ A \_ propriedade de evento de grupo \_ \_ alterada** indica que as propriedades do grupo foram alteradas ou atualizadas pelo criador do grupo.
-   **Par \_ Registro de evento de grupo \_ \_ \_ alterado** indica que uma operação de registro foi executada. Esse evento é gerado quando um par que participa do grupo publica, atualiza ou exclui um registro. Por exemplo, esse evento é gerado quando um aplicativo de chat envia uma mensagem de chat.
-   **Par \_ O \_ membro de evento de grupo \_ \_ alterado** indica que o status de um membro dentro do grupo foi alterado. As alterações de status incluem:
    -   **Par \_ MEMBRO \_ conectado**. Um par se conectou ao grupo.
    -   **Par \_ MEMBRO \_ desconectado**. Um par foi desconectado do grupo.
    -   **Par \_ MEMBRO \_ associado**. Novas informações de associação foram publicadas para um par.
    -   **Par \_ MEMBRO \_ atualizado**. Um par foi atualizado com novas informações, como um novo endereço IP.
-   **Par \_ \_conexão de \_ vizinho \_ do evento de grupo**. Os pares que participarão de conexões vizinhas dentro do grupo devem ser registrados para esse evento. Observe que o registro para esse evento não permite que o par receba dados; o registro para esse evento garante apenas a notificação quando uma solicitação de uma conexão vizinha é recebida.
-   **Par \_ \_ \_ \_ conexão direta de evento de grupo**. Os colegas que participarão de conexões diretas dentro do grupo deverão se registrar nesse evento. Observe que o registro para esse evento não permite que o par receba dados; o registro para esse evento garante apenas a notificação quando uma solicitação de conexão direta é recebida.
-   **Par \_ AGRUPAR \_ \_ \_ dados de entrada de evento**. Os pares que receberão dados sobre um vizinho ou conexão direta deverão se registrar para esse evento. Quando esse evento é gerado, os dados opacos transmitidos pelo outro par participante podem ser obtidos chamando [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata). Observe que para receber esse evento, o par deve ter sido registrado anteriormente **para \_ \_ \_ \_ conexão direta de evento de grupo de pares** ou **\_ \_ \_ \_ conexão de vizinho de evento de grupo de pares**.
-   **Par \_ \_ \_ \_ falha na conexão de evento de grupo**. Uma conexão falhou por algum motivo. Nenhum dado é fornecido quando esse evento é gerado e [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) não deve ser chamado.

Depois que um aplicativo recebe uma notificação de que um evento de mesmo nível ocorreu (excluindo **\_ \_ \_ \_ falha na conexão de evento de grupo de pares**), o aplicativo chama [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)e passa o identificador de evento de par retornado por [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent). A infraestrutura de pares retorna um ponteiro para uma estrutura de dados de evento de grupo de pares que contém os dados solicitados. [**\_ \_ \_**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) Essa função deve ser chamada até **que \_ pares \_ nenhum \_ \_ dado de evento** seja retornado. Quando um aplicativo não requer mais uma notificação para um evento de mesmo nível, uma chamada deve ser feita ao [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent), passando o identificador de evento de par retornado por **PeerGroupRegisterEvent** quando o aplicativo é registrado para o evento específico.

## <a name="example-of-registering-for-peer-graphing-events"></a>Exemplo de registro para eventos de grafo de pares

O exemplo de código a seguir mostra como registrar-se com os eventos de grafo de pares.


```C++
//-----------------------------------------------------------------------------
// Function: RegisterForEvents
//
// Purpose:  Registers the EventCallback function so it can be called for only
//           the events that are specified.
//
// Returns:  HRESULT
//
HRESULT RegisterForEvents()
{
    HPEEREVENT  g_hPeerEvent = NULL;        // The one PeerEvent handle
    HANDLE      g_hEvent = NULL;            // Handle signaled by Graphing when we have an event
    HRESULT hr = S_OK;
    PEER_GRAPH_EVENT_REGISTRATION regs[] = {
        { PEER_GRAPH_EVENT_RECORD_CHANGED, 0 },
        { PEER_GRAPH_EVENT_NODE_CHANGED,   0 },
        { PEER_GRAPH_EVENT_STATUS_CHANGED, 0 },
        { PEER_GRAPH_EVENT_DIRECT_CONNECTION, 0 },
        { PEER_GRAPH_EVENT_INCOMING_DATA, 0 },
    };

    g_hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (g_hEvent == NULL)
    {
        wprintf(L"CreateEvent call failed.\n");
        hr = E_OUTOFMEMORY;
    }
    else
    {
        hr = PeerGraphRegisterEvent(g_hGraph, g_hEvent, celems(regs), regs,  &g_hPeerEvent);
        if (FAILED(hr))
        {
           wprintf(L"PeerGraphRegisterEvent call failed.\n");
            CloseHandle(g_hEvent);
            g_hEvent = NULL;
        }
    }

    if (SUCCEEDED(hr))
    {
        if (!RegisterWaitForSingleObject(&g_hWait, g_hEvent, EventCallback, NULL, INFINITE, WT_EXECUTEDEFAULT))
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            wprintf(L"Could not set up event callback.\n");
            CloseHandle(g_hEvent);
            g_hEvent = NULL;
        }
    }

    return hr;
}
```



 

 



