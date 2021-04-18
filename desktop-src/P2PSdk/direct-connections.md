---
description: O grafo de pares e as infraestruturas de agrupamento de pares permitem que os aplicativos se conectem diretamente a um nó (gráfico) ou membro (agrupamento) e, em seguida, troquem dados diretamente com o nó. Essa conexão é chamada de conexão direta.
ms.assetid: 65f3d3a5-c015-4724-b9ed-45af7fde7a45
title: Conexões diretas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e357b3a4ebc765a013de05234bc8fc9be20943d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756708"
---
# <a name="direct-connections"></a>Conexões diretas

O grafo de pares e as infraestruturas de agrupamento de pares permitem que os aplicativos se conectem diretamente a um nó (gráfico) ou membro (agrupamento) e, em seguida, troquem dados diretamente com o nó. Essa conexão é chamada de **conexão direta**.

## <a name="direct-connections-using-the-peer-graphing-infrastructure"></a>Conexões diretas usando a infraestrutura de grafo de pares

Antes que uma conexão direta possa ser estabelecida entre dois nós em um grafo, ambos os nós devem ser registrados para o evento de **\_ \_ \_ \_ conexão direta de evento de grafo de pares** . Para receber dados em uma conexão direta, os nós também devem ser registrados para o evento de **dados de entrada de evento de grafo de pares \_ \_ \_ \_** .

**Par \_ A \_ \_ \_ conexão direta de evento de grafo** é um evento que notifica um aplicativo se uma tentativa de conexão direta é ou não bem-sucedida ou falha. O status real de êxito ou falha de uma chamada para [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection) é retornado na estrutura de dados de evento de grafo de [**pares \_ \_ \_**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) .

Para criar uma conexão direta, um aplicativo chama [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection)e, em seguida, passa um identificador para o grafo, um ponteiro para a identidade do outro nó que está participando da conexão e um ponteiro para uma estrutura de endereço IPv6 para o nó participante. A identidade do nó e o endereço IPv6 que são especificados na chamada para **PeerGraphOpenDirectConnection** devem ser registrados para o evento de dados de entrada de evento de grafo de pares ou não podem receber dados enviados por um ponto de chamada. **\_ \_ \_ \_** Quando bem-sucedido, **PeerGraphOpenDirectConnection** retorna uma ID de conexão de 64 bits. No entanto, o par deve aguardar o evento de **\_ \_ \_ \_ conexão direta do evento de grupo par** antes que a ID de conexão direta possa ser identificada como válida.

Depois que uma conexão é feita e uma ID de conexão válida é confirmada, um aplicativo pode chamar [**PeerGraphSendData**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata) para enviar os dados pela conexão especificada pela ID de conexão válida para o par participante — se o par participante estiver registrado para o evento de **entrada de evento de grafo de pares \_ \_ \_ \_** . Os dados opacos estão disponíveis como uma estrutura de [**\_ dados de mesmo nível**](/windows/desktop/api/P2P/ns-p2p-peer_data) nos [**dados de entrada do evento de mesmo nível \_ \_ \_**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) retornados pelo evento de **dados de entrada de evento de grafo de pares \_ \_ \_ \_** .

Quando uma conexão não é necessária, um aplicativo chama [**PeerGraphCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) com o identificador do grafo e a ID da conexão.

## <a name="direct-connections-using-the-peer-grouping-infrastructure"></a>Conexões diretas usando a infraestrutura de agrupamento de pares

As conexões diretas dentro da infraestrutura de agrupamento de pares são tratadas de forma semelhante à infraestrutura de gráfico de pares.

Antes que uma conexão direta possa ser estabelecida entre dois membros em um grupo, ambos os membros devem se registrar para o evento de **\_ \_ \_ \_ conexão direta de evento de grupo de pares** . Se um membro do grupo quiser receber dados em uma conexão direta, o membro do grupo também deverá se registrar para o evento de **\_ entrada de evento de \_ \_ \_ dados do grupo de pares** .

**Par \_ A \_ \_ \_ conexão direta de evento de grupo** é um evento que é um evento que notifica um aplicativo se uma tentativa de conexão direta é ou não bem-sucedida ou falha. O status real de êxito ou falha de uma chamada para [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) é retornado na estrutura de [**PEER_GROUP_EVENT_DATA**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) .

Para criar uma conexão direta, um aplicativo chama [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)e, em seguida, passa um identificador para o grupo, um ponteiro para a identidade do outro membro que participará dessa conexão e um ponteiro para uma estrutura de endereço IPv6 para o membro participante. O membro cuja identidade e endereço IPv6 são especificados na chamada para **PeerGroupOpenDirectConnection** deve ser registrado para o evento **de \_ \_ entrada de evento de grupo \_ \_ de pares** ou o membro não pode receber dados enviados por um ponto de chamada. **PeerGroupOpenDirectConnection** retorna uma ID de conexão de 64 bits quando bem-sucedida. No entanto, um par deve aguardar até que o evento de **\_ \_ \_ \_ conexão direta do evento de grafo de pares** seja gerado antes que a ID de conexão direta possa ser identificada como válida.

Depois que uma conexão é feita e uma ID de conexão válida é confirmada, um aplicativo pode chamar [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) para enviar dados através de uma conexão especificada pela ID de conexão válida para o par participante — se o par participante estiver registrado para o evento de **entrada de evento do grupo de pares \_ \_ \_ \_** . Os dados opacos estão disponíveis como uma estrutura de [**\_ dados de pares**](/windows/desktop/api/P2P/ns-p2p-peer_data) nos [**dados de entrada do evento de mesmo nível \_ \_ \_**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) retornados pelo evento de **entrada de evento do grupo de pares \_ \_ \_ \_** .

Quando a conexão não é necessária, o aplicativo chama [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) com o identificador de grupo e a ID de conexão.

## <a name="example-of-a-direct-connection-for-graphing"></a>Exemplo de uma conexão direta para o gráfico


```C++
#include <p2p.h>

#pragma comment(lib, "p2pgraph.lib")

//-----------------------------------------------------------------------------
// Function: CreateDirectConnection
//
// Purpose:  Demonstrate how to create a direct connection.
//
// Arguments:
//           hGraph - the graph in which to create the connection
//           pwzId  - the peer identification string
//
// Returns:  ULONGLONG - the connection id or 0
//

ULONGLONG CreateDirectConnection(HGRAPH hGraph, PCWSTR pwzId)
{
    HRESULT   hr = S_OK;

    ULONGLONG ullConnection = 0; // the connection id to return

    HPEERENUM hPeerEnum = NULL;
 
    hr = PeerGraphEnumNodes(hGraph, pwzId, &hPeerEnum);

    if (SUCCEEDED(hr))
    {
        ULONG cItem = 1; // want only one matching result

        PEER_NODE_INFO ** ppNodeInfo = NULL;

        hr = PeerGraphGetNextItem(hPeerEnum, &cItem, (PVOID**) &ppNodeInfo);

        if (SUCCEEDED(hr))
        {
            if ((cItem > 0) && (NULL != ppNodeInfo))
            {
                if ((*ppNodeInfo)->cAddresses > 0)
                {
                    hr = PeerGraphOpenDirectConnection(hGraph, pwzId,
                            &(*ppNodeInfo)->pAddresses[0], &ullConnection);
                }
                PeerGraphFreeData(ppNodeInfo);
            }
        }
        PeerGraphEndEnumeration(hPeerEnum);
    }
    return ullConnection;
}

```



 

 



