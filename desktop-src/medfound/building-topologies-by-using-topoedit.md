---
description: Criando topologias usando TopoEdit
ms.assetid: 04173f3d-3722-48ee-a6fb-9cdb2a897a33
title: Criando topologias usando TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92758911113c7500cb13fa814d07321435fafeb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089796"
---
# <a name="building-topologies-by-using-topoedit"></a><span data-ttu-id="f5dc9-103">Criando topologias usando TopoEdit</span><span class="sxs-lookup"><span data-stu-id="f5dc9-103">Building Topologies by Using TopoEdit</span></span>

<span data-ttu-id="f5dc9-104">Uma topologia deve ter os três nós a seguir:</span><span class="sxs-lookup"><span data-stu-id="f5dc9-104">A topology must have the following three nodes:</span></span>

-   <span data-ttu-id="f5dc9-105">Nó de origem: os fluxos de um arquivo de mídia, que são usados como uma fonte para a topologia.</span><span class="sxs-lookup"><span data-stu-id="f5dc9-105">Source node: The streams from a media file, which are used as a source for the topology.</span></span>
-   <span data-ttu-id="f5dc9-106">Nó de transformação: uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="f5dc9-106">Transform node: A Media Foundation transform (MFT).</span></span> <span data-ttu-id="f5dc9-107">Esses nós geralmente são codificadores, decodificadores e efeitos para a topologia.</span><span class="sxs-lookup"><span data-stu-id="f5dc9-107">These nodes are usually encoders, decoders, and effects for the topology.</span></span>
-   <span data-ttu-id="f5dc9-108">Nó de saída: o coletor de fluxo que passa os dados de mídia, quadros de vídeo ou fluxos de áudio para a sessão de mídia para reprodução.</span><span class="sxs-lookup"><span data-stu-id="f5dc9-108">Output node: The stream sink that passes the media data, video frames, or audio streams to the Media Session for playback.</span></span>

<span data-ttu-id="f5dc9-109">Para obter informações sobre a estrutura de topologia, consulte [sobre topologias](about-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="f5dc9-109">For information about topology structure, see [About Topologies](about-topologies.md).</span></span>

<span data-ttu-id="f5dc9-110">Para criar uma topologia, você deve adicionar os nós, conectar os nós e resolver a topologia para que ela possa ser reproduzida.</span><span class="sxs-lookup"><span data-stu-id="f5dc9-110">To build a topology, you must add the nodes, connect the nodes, and resolve the topology so that it can be played.</span></span>

<span data-ttu-id="f5dc9-111">Os nós de topologia são exibidos como caixas, com texto mostrando o nome do nó.</span><span class="sxs-lookup"><span data-stu-id="f5dc9-111">Topology nodes are displayed as boxes, with text showing the name of the node.</span></span> <span data-ttu-id="f5dc9-112">As caixas verdes representam os nós que são adicionados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="f5dc9-112">Green boxes represent the nodes that are added by the user.</span></span> <span data-ttu-id="f5dc9-113">Quando uma topologia é resolvida, o TopoEdit pode adicionar nós de transformação automaticamente à topologia.</span><span class="sxs-lookup"><span data-stu-id="f5dc9-113">When a topology is resolved, TopoEdit can add transform nodes to the topology automatically.</span></span> <span data-ttu-id="f5dc9-114">Eles aparecem como caixas azuis no **painel topologia**.</span><span class="sxs-lookup"><span data-stu-id="f5dc9-114">These appear as blue boxes on the **Topology Pane**.</span></span>

<span data-ttu-id="f5dc9-115">As entradas e saídas de topologia são representadas por como quadrados pretos ao longo da borda do nó.</span><span class="sxs-lookup"><span data-stu-id="f5dc9-115">Topology inputs and outputs are represented by as black squares along the edge of the node.</span></span> <span data-ttu-id="f5dc9-116">A *entrada de nó* é mostrada no lado esquerdo do nó e a *saída do nó* está no lado direito do nó.</span><span class="sxs-lookup"><span data-stu-id="f5dc9-116">The *node input* is shown on the left side of the node, and the *node output* is on the right side of the node.</span></span>

<span data-ttu-id="f5dc9-117">Os nós de topologia são conectados por meio de uma *conexão de nó* que aparece como uma linha preta conectando a entrada de nó de um nó à saída do nó de outro nó.</span><span class="sxs-lookup"><span data-stu-id="f5dc9-117">The topology nodes are connected through a *node connection* that appears as a black line connecting the node input of one node to the node output of another node.</span></span>

<span data-ttu-id="f5dc9-118">A ilustração a seguir mostra uma topologia conectada para uma fonte de áudio.</span><span class="sxs-lookup"><span data-stu-id="f5dc9-118">The following illustration shows a connected topology for an audio source.</span></span>

![ilustração mostrando conexões do nó de origem, para dois nós de transformação e, em seguida, para o nó de saída](images/e94b4cce-aa8a-497f-94c2-cc9dace17291.gif)

<span data-ttu-id="f5dc9-120">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="f5dc9-120">This section contains the following topics:</span></span>



| <span data-ttu-id="f5dc9-121">Tópico</span><span class="sxs-lookup"><span data-stu-id="f5dc9-121">Topic</span></span>                                                                                          | <span data-ttu-id="f5dc9-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5dc9-122">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="f5dc9-123">Adicionando nós de origem com TopoEdit</span><span class="sxs-lookup"><span data-stu-id="f5dc9-123">Adding Source Nodes with TopoEdit</span></span>](adding-source-nodes-with-topoedit.md)                     | <span data-ttu-id="f5dc9-124">Descreve o processo de adicionar nós de origem a uma topologia.</span><span class="sxs-lookup"><span data-stu-id="f5dc9-124">Describes the process of adding source nodes to a topology.</span></span>    |
| [<span data-ttu-id="f5dc9-125">Adicionando nós de transformação com TopoEdit</span><span class="sxs-lookup"><span data-stu-id="f5dc9-125">Adding Transform Nodes with TopoEdit</span></span>](adding-transform-nodes-with-topoedit.md)               | <span data-ttu-id="f5dc9-126">Descreve o processo de adicionar nós de transformação a uma topologia.</span><span class="sxs-lookup"><span data-stu-id="f5dc9-126">Describes the process of adding transform nodes to a topology.</span></span> |
| [<span data-ttu-id="f5dc9-127">Adicionando nós de saída com TopoEdit</span><span class="sxs-lookup"><span data-stu-id="f5dc9-127">Adding Output Nodes with TopoEdit</span></span>](adding-output-nodes-with-topoedit.md)                     | <span data-ttu-id="f5dc9-128">Descreve o processo de adicionar nós de saída a uma topologia.</span><span class="sxs-lookup"><span data-stu-id="f5dc9-128">Describes the process of adding output nodes to a topology.</span></span>    |
| [<span data-ttu-id="f5dc9-129">Conectando e desconectando nós de topologia</span><span class="sxs-lookup"><span data-stu-id="f5dc9-129">Connecting and Disconnecting Topology Nodes</span></span>](connecting-and-disconnecting-topology-nodes.md) | <span data-ttu-id="f5dc9-130">Descreve o processo de conexão de dois nós.</span><span class="sxs-lookup"><span data-stu-id="f5dc9-130">Describes the process of connecting two nodes.</span></span>                 |
| [<span data-ttu-id="f5dc9-131">Resolvendo uma topologia com TopoEdit</span><span class="sxs-lookup"><span data-stu-id="f5dc9-131">Resolving a Topology with TopoEdit</span></span>](resolving-a-topology-with-topoedit.md)                   | <span data-ttu-id="f5dc9-132">Descreve o processo de resolução de topologia.</span><span class="sxs-lookup"><span data-stu-id="f5dc9-132">Describes the process of topology resolution.</span></span>                  |



 

## <a name="related-topics"></a><span data-ttu-id="f5dc9-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5dc9-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5dc9-134">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="f5dc9-134">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



