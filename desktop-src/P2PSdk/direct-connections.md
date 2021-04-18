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
# <a name="direct-connections"></a><span data-ttu-id="baf02-104">Conexões diretas</span><span class="sxs-lookup"><span data-stu-id="baf02-104">Direct Connections</span></span>

<span data-ttu-id="baf02-105">O grafo de pares e as infraestruturas de agrupamento de pares permitem que os aplicativos se conectem diretamente a um nó (gráfico) ou membro (agrupamento) e, em seguida, troquem dados diretamente com o nó.</span><span class="sxs-lookup"><span data-stu-id="baf02-105">The Peer Graphing and Peer Grouping Infrastructures allow applications to connect directly to one node (Graphing) or member (Grouping), and then exchange data directly with the node.</span></span> <span data-ttu-id="baf02-106">Essa conexão é chamada de **conexão direta**.</span><span class="sxs-lookup"><span data-stu-id="baf02-106">This connection is called a **direct connection**.</span></span>

## <a name="direct-connections-using-the-peer-graphing-infrastructure"></a><span data-ttu-id="baf02-107">Conexões diretas usando a infraestrutura de grafo de pares</span><span class="sxs-lookup"><span data-stu-id="baf02-107">Direct Connections using the Peer Graphing Infrastructure</span></span>

<span data-ttu-id="baf02-108">Antes que uma conexão direta possa ser estabelecida entre dois nós em um grafo, ambos os nós devem ser registrados para o evento de **\_ \_ \_ \_ conexão direta de evento de grafo de pares** .</span><span class="sxs-lookup"><span data-stu-id="baf02-108">Before a direct connection can be established between two nodes in a graph, both nodes must be registered for the **PEER\_GRAPH\_EVENT\_DIRECT\_CONNECTION** event.</span></span> <span data-ttu-id="baf02-109">Para receber dados em uma conexão direta, os nós também devem ser registrados para o evento de **dados de entrada de evento de grafo de pares \_ \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="baf02-109">To receive data over a direct connection, the nodes must also be registered for the **PEER\_GRAPH\_EVENT\_INCOMING\_DATA** event.</span></span>

<span data-ttu-id="baf02-110">**Par \_ A \_ \_ \_ conexão direta de evento de grafo** é um evento que notifica um aplicativo se uma tentativa de conexão direta é ou não bem-sucedida ou falha.</span><span class="sxs-lookup"><span data-stu-id="baf02-110">**PEER\_GRAPH\_EVENT\_DIRECT\_CONNECTION** is an event that notifies an application whether or not a direct connection attempt succeeds or fails.</span></span> <span data-ttu-id="baf02-111">O status real de êxito ou falha de uma chamada para [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection) é retornado na estrutura de dados de evento de grafo de [**pares \_ \_ \_**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) .</span><span class="sxs-lookup"><span data-stu-id="baf02-111">The actual success or failure status of a call to [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection) is returned in the [**PEER\_GRAPH\_EVENT\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) structure.</span></span>

<span data-ttu-id="baf02-112">Para criar uma conexão direta, um aplicativo chama [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection)e, em seguida, passa um identificador para o grafo, um ponteiro para a identidade do outro nó que está participando da conexão e um ponteiro para uma estrutura de endereço IPv6 para o nó participante.</span><span class="sxs-lookup"><span data-stu-id="baf02-112">To create a direct connection, an application calls [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection), and then passes a handle to the graph, a pointer to the identity of the other node that is participating in the connection, and a pointer to an IPv6 address structure for the participating node.</span></span> <span data-ttu-id="baf02-113">A identidade do nó e o endereço IPv6 que são especificados na chamada para **PeerGraphOpenDirectConnection** devem ser registrados para o evento de dados de entrada de evento de grafo de pares ou não podem receber dados enviados por um ponto de chamada. **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="baf02-113">The node identity and IPv6 address that are specified in the call to **PeerGraphOpenDirectConnection** must be registered for the **PEER\_GRAPH\_EVENT\_INCOMING\_DATA** event, or it cannot receive data sent by a calling peer.</span></span> <span data-ttu-id="baf02-114">Quando bem-sucedido, **PeerGraphOpenDirectConnection** retorna uma ID de conexão de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="baf02-114">When successful, **PeerGraphOpenDirectConnection** returns a 64-bit connection ID.</span></span> <span data-ttu-id="baf02-115">No entanto, o par deve aguardar o evento de **\_ \_ \_ \_ conexão direta do evento de grupo par** antes que a ID de conexão direta possa ser identificada como válida.</span><span class="sxs-lookup"><span data-stu-id="baf02-115">However, the peer must wait for the **PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION** event before the direct connection ID can be identified as valid.</span></span>

<span data-ttu-id="baf02-116">Depois que uma conexão é feita e uma ID de conexão válida é confirmada, um aplicativo pode chamar [**PeerGraphSendData**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata) para enviar os dados pela conexão especificada pela ID de conexão válida para o par participante — se o par participante estiver registrado para o evento de **entrada de evento de grafo de pares \_ \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="baf02-116">After a connection is made and a valid connection ID is confirmed, an application can call [**PeerGraphSendData**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata) to send the data across the connection specified by the valid connection ID to the participating peer—if the participating peer is registered for the **PEER\_GRAPH\_EVENT\_INCOMING\_DATA** event.</span></span> <span data-ttu-id="baf02-117">Os dados opacos estão disponíveis como uma estrutura de [**\_ dados de mesmo nível**](/windows/desktop/api/P2P/ns-p2p-peer_data) nos [**dados de entrada do evento de mesmo nível \_ \_ \_**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) retornados pelo evento de **dados de entrada de evento de grafo de pares \_ \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="baf02-117">The opaque data is available as a [**PEER\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_data) structure in the [**PEER\_EVENT\_INCOMING\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) returned by the **PEER\_GRAPH\_EVENT\_INCOMING\_DATA** event.</span></span>

<span data-ttu-id="baf02-118">Quando uma conexão não é necessária, um aplicativo chama [**PeerGraphCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) com o identificador do grafo e a ID da conexão.</span><span class="sxs-lookup"><span data-stu-id="baf02-118">When a connection is not needed, an application calls [**PeerGraphCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) with the graph handle and the connection ID.</span></span>

## <a name="direct-connections-using-the-peer-grouping-infrastructure"></a><span data-ttu-id="baf02-119">Conexões diretas usando a infraestrutura de agrupamento de pares</span><span class="sxs-lookup"><span data-stu-id="baf02-119">Direct Connections using the Peer Grouping Infrastructure</span></span>

<span data-ttu-id="baf02-120">As conexões diretas dentro da infraestrutura de agrupamento de pares são tratadas de forma semelhante à infraestrutura de gráfico de pares.</span><span class="sxs-lookup"><span data-stu-id="baf02-120">Direct connections within the Peer Grouping Infrastructure are handled similar to the Peer Graphing Infrastructure.</span></span>

<span data-ttu-id="baf02-121">Antes que uma conexão direta possa ser estabelecida entre dois membros em um grupo, ambos os membros devem se registrar para o evento de **\_ \_ \_ \_ conexão direta de evento de grupo de pares** .</span><span class="sxs-lookup"><span data-stu-id="baf02-121">Before a direct connection can be established between two members in a group, both members must register for the **PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION** event.</span></span> <span data-ttu-id="baf02-122">Se um membro do grupo quiser receber dados em uma conexão direta, o membro do grupo também deverá se registrar para o evento de **\_ entrada de evento de \_ \_ \_ dados do grupo de pares** .</span><span class="sxs-lookup"><span data-stu-id="baf02-122">If a group member wants to receive data over a direct connection, the group member must also register for the **PEER\_GROUP\_EVENT\_INCOMING\_DATA** event.</span></span>

<span data-ttu-id="baf02-123">**Par \_ A \_ \_ \_ conexão direta de evento de grupo** é um evento que é um evento que notifica um aplicativo se uma tentativa de conexão direta é ou não bem-sucedida ou falha.</span><span class="sxs-lookup"><span data-stu-id="baf02-123">**PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION** is an event that is an event that notifies an application whether or not a direct connection attempt succeeds or fails.</span></span> <span data-ttu-id="baf02-124">O status real de êxito ou falha de uma chamada para [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) é retornado na estrutura de [**PEER_GROUP_EVENT_DATA**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) .</span><span class="sxs-lookup"><span data-stu-id="baf02-124">The actual success or failure status of a call to [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) is returned in the [**PEER_GROUP_EVENT_DATA**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) structure.</span></span>

<span data-ttu-id="baf02-125">Para criar uma conexão direta, um aplicativo chama [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)e, em seguida, passa um identificador para o grupo, um ponteiro para a identidade do outro membro que participará dessa conexão e um ponteiro para uma estrutura de endereço IPv6 para o membro participante.</span><span class="sxs-lookup"><span data-stu-id="baf02-125">To create a direct connection, an application calls [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection), and then passes a handle to the group, a pointer to the identity of the other member that will participate in this connection, and a pointer to an IPv6 address structure for the participating member.</span></span> <span data-ttu-id="baf02-126">O membro cuja identidade e endereço IPv6 são especificados na chamada para **PeerGroupOpenDirectConnection** deve ser registrado para o evento **de \_ \_ entrada de evento de grupo \_ \_ de pares** ou o membro não pode receber dados enviados por um ponto de chamada.</span><span class="sxs-lookup"><span data-stu-id="baf02-126">The member whose identity and IPv6 address are specified in the call to **PeerGroupOpenDirectConnection** must be registered for the **PEER\_GROUP\_EVENT\_INCOMING\_DATA** event, or the member cannot receive data sent by a calling peer.</span></span> <span data-ttu-id="baf02-127">**PeerGroupOpenDirectConnection** retorna uma ID de conexão de 64 bits quando bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="baf02-127">**PeerGroupOpenDirectConnection** returns a 64-bit connection ID when successful.</span></span> <span data-ttu-id="baf02-128">No entanto, um par deve aguardar até que o evento de **\_ \_ \_ \_ conexão direta do evento de grafo de pares** seja gerado antes que a ID de conexão direta possa ser identificada como válida.</span><span class="sxs-lookup"><span data-stu-id="baf02-128">However, a peer must wait for the **PEER\_GRAPH\_EVENT\_DIRECT\_CONNECTION** event to be raised before the direct connection ID can be identified as valid.</span></span>

<span data-ttu-id="baf02-129">Depois que uma conexão é feita e uma ID de conexão válida é confirmada, um aplicativo pode chamar [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) para enviar dados através de uma conexão especificada pela ID de conexão válida para o par participante — se o par participante estiver registrado para o evento de **entrada de evento do grupo de pares \_ \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="baf02-129">After a connection is made and a valid connection ID is confirmed, then an application can call [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) to send data across a connection specified by the valid connection ID to the participating peer—if the participating peer is registered for the **PEER\_GROUP\_EVENT\_INCOMING\_DATA** event.</span></span> <span data-ttu-id="baf02-130">Os dados opacos estão disponíveis como uma estrutura de [**\_ dados de pares**](/windows/desktop/api/P2P/ns-p2p-peer_data) nos [**dados de entrada do evento de mesmo nível \_ \_ \_**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) retornados pelo evento de **entrada de evento do grupo de pares \_ \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="baf02-130">The opaque data is available as a [**PEER\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_data) structure in the [**PEER\_EVENT\_INCOMING\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) returned by the **PEER\_GROUP\_EVENT\_INCOMING\_DATA** event.</span></span>

<span data-ttu-id="baf02-131">Quando a conexão não é necessária, o aplicativo chama [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) com o identificador de grupo e a ID de conexão.</span><span class="sxs-lookup"><span data-stu-id="baf02-131">When the connection is not needed, the application calls [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) with the group handle and the connection ID.</span></span>

## <a name="example-of-a-direct-connection-for-graphing"></a><span data-ttu-id="baf02-132">Exemplo de uma conexão direta para o gráfico</span><span class="sxs-lookup"><span data-stu-id="baf02-132">Example of a Direct Connection for Graphing</span></span>


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



 

 



