---
description: Conectando e desconectando nós de topologia
ms.assetid: b2f70989-f0a8-4a11-baeb-18f026afaeab
title: Conectando e desconectando nós de topologia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08057eba74314ae6b87da418b743a089506a3b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772958"
---
# <a name="connecting-and-disconnecting-topology-nodes"></a><span data-ttu-id="9424f-103">Conectando e desconectando nós de topologia</span><span class="sxs-lookup"><span data-stu-id="9424f-103">Connecting and Disconnecting Topology Nodes</span></span>

<span data-ttu-id="9424f-104">Para que uma topologia seja funcional, o nó de origem e o nó de saída devem estar conectados.</span><span class="sxs-lookup"><span data-stu-id="9424f-104">For a topology to be functional, the source node and the output node must be connected.</span></span> <span data-ttu-id="9424f-105">Para conectar dois nós de topologia, arraste a saída do nó de um nó para a entrada de nó do outro nó.</span><span class="sxs-lookup"><span data-stu-id="9424f-105">To connect two topology nodes, drag the node output of one node to the node input of the other node.</span></span> <span data-ttu-id="9424f-106">TopoEdit exibe a conexão do nó como uma linha preta.</span><span class="sxs-lookup"><span data-stu-id="9424f-106">TopoEdit displays the node connection as a black line.</span></span> <span data-ttu-id="9424f-107">Isso é equivalente a conectar nós de topologia chamando o método [**IMFTopologyNode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) .</span><span class="sxs-lookup"><span data-stu-id="9424f-107">This is equivalent to connecting topology nodes by calling the [**IMFTopologyNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) method.</span></span>

<span data-ttu-id="9424f-108">A topologia só poderá ser resolvida se a conexão do nó for válida; ou seja, se os tipos de mídia dos dois nós forem compatíveis.</span><span class="sxs-lookup"><span data-stu-id="9424f-108">The topology can be resolved only if the node connection is valid; that is, if the media types of the two nodes are compatible.</span></span> <span data-ttu-id="9424f-109">Para obter informações sobre como resolver topologias, consulte [resolvendo uma topologia com TopoEdit](resolving-a-topology-with-topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="9424f-109">For information about resolving topologies, see [Resolving a Topology with TopoEdit](resolving-a-topology-with-topoedit.md).</span></span>

<span data-ttu-id="9424f-110">Se você tentar fazer uma conexão de um nó que já está conectado, a nova conexão de nó substituirá a conexão de nó antiga.</span><span class="sxs-lookup"><span data-stu-id="9424f-110">If you attempt to make a connection from a node that is already connected, the new node connection replaces the old node connection.</span></span>

<span data-ttu-id="9424f-111">Para excluir uma conexão, selecione a conexão do nó e pressione a tecla DELETE ou selecione **excluir** no menu **topologia** .</span><span class="sxs-lookup"><span data-stu-id="9424f-111">To delete a connection, select the node connection and press the DELETE key or select **Delete** from the **Topology** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9424f-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9424f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9424f-113">Criando topologias usando TopoEdit</span><span class="sxs-lookup"><span data-stu-id="9424f-113">Building Topologies by Using TopoEdit</span></span>](building-topologies-by-using-topoedit.md)
</dt> <dt>

[<span data-ttu-id="9424f-114">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="9424f-114">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



