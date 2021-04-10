---
description: Resolvendo uma topologia com TopoEdit
ms.assetid: da3e2bbc-7c9f-4a15-8842-c1bb00662cd2
title: Resolvendo uma topologia com TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8397e380b19a6f45736c06e859d2a80456aad079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164890"
---
# <a name="resolving-a-topology-with-topoedit"></a><span data-ttu-id="a88bf-103">Resolvendo uma topologia com TopoEdit</span><span class="sxs-lookup"><span data-stu-id="a88bf-103">Resolving a Topology with TopoEdit</span></span>

<span data-ttu-id="a88bf-104">Há dois tipos de topologias:</span><span class="sxs-lookup"><span data-stu-id="a88bf-104">There are two types of topologies:</span></span>

-   <span data-ttu-id="a88bf-105">Topologia parcial.</span><span class="sxs-lookup"><span data-stu-id="a88bf-105">Partial Topology.</span></span> <span data-ttu-id="a88bf-106">O nó de origem está conectado diretamente ao nó de saída.</span><span class="sxs-lookup"><span data-stu-id="a88bf-106">The source node is connected directly to the output node.</span></span> <span data-ttu-id="a88bf-107">Em alguns casos, uma topologia parcial pode ter alguns nós de transformação intermediários, como efeitos, mas não todos.</span><span class="sxs-lookup"><span data-stu-id="a88bf-107">In some cases, a partial topology can have some intermediate transform nodes, such as effects, but not all.</span></span> <span data-ttu-id="a88bf-108">Os nós de transformação que são omitidos normalmente são decodificadores ou MFTs de conversão de formato, como conversores de cor e reamostragens de áudio.</span><span class="sxs-lookup"><span data-stu-id="a88bf-108">The transform nodes that are omitted are typically decoders or format conversion MFTs, such as color converters and audio resamplers.</span></span>

-   <span data-ttu-id="a88bf-109">Topologia completa.</span><span class="sxs-lookup"><span data-stu-id="a88bf-109">Full Topology.</span></span> <span data-ttu-id="a88bf-110">O nó de origem está conectado ao nó de saída por meio de um nó de transformação.</span><span class="sxs-lookup"><span data-stu-id="a88bf-110">The source node is connected to the output node through a transform node.</span></span> <span data-ttu-id="a88bf-111">Esse tipo de topologia deve ter cada nó para processar dados.</span><span class="sxs-lookup"><span data-stu-id="a88bf-111">This type of topology must have every node to process data.</span></span>

<span data-ttu-id="a88bf-112">TopoEdit só pode reproduzir topologias completas.</span><span class="sxs-lookup"><span data-stu-id="a88bf-112">TopoEdit can only play full topologies.</span></span> <span data-ttu-id="a88bf-113">O TopoEdit usa o objeto de carregador de topologia, fornecido pelo Media Foundation, para converter uma topologia parcial em uma topologia completa, inserindo as transformações necessárias.</span><span class="sxs-lookup"><span data-stu-id="a88bf-113">TopoEdit uses the topology loader object, provided by Media Foundation, to convert a partial topology into a full topology by inserting the required transforms.</span></span> <span data-ttu-id="a88bf-114">O processo de criação de uma topologia completa é chamado de resolução de uma topologia.</span><span class="sxs-lookup"><span data-stu-id="a88bf-114">The process of creating a full topology is called resolving a topology.</span></span>

<span data-ttu-id="a88bf-115">Para obter informações sobre tipos de topologia, consulte a seção topologias parciais em [sobre topologias](about-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="a88bf-115">For information about topology types, see the Partial Topologies section in [About Topologies](about-topologies.md).</span></span>

<span data-ttu-id="a88bf-116">Antes de resolver uma topologia, verifique se:</span><span class="sxs-lookup"><span data-stu-id="a88bf-116">Before you resolve a topology ensure that:</span></span>

-   <span data-ttu-id="a88bf-117">A topologia contém um nó de origem e um nó de saída.</span><span class="sxs-lookup"><span data-stu-id="a88bf-117">The topology contains a source node and an output node.</span></span>

-   <span data-ttu-id="a88bf-118">Os nós de origem e saída estão conectados por uma conexão de nó válida.</span><span class="sxs-lookup"><span data-stu-id="a88bf-118">The source and the output nodes are connected by a valid node connection.</span></span> <span data-ttu-id="a88bf-119">Durante a resolução da topologia, o carregador de topologia verifica o tipo de mídia dos nós quanto à compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="a88bf-119">During topology resolution, the topology loader checks the media type of the nodes for compatibility.</span></span> <span data-ttu-id="a88bf-120">Se houver uma conexão de nó inválida, o processo falhará e uma mensagem de erro será exibida.</span><span class="sxs-lookup"><span data-stu-id="a88bf-120">If an invalid node connection exists, then the process fails and an error message is displayed.</span></span>

<span data-ttu-id="a88bf-121">Para resolver uma topologia, no menu **topologia** , clique em **resolver topologia**.</span><span class="sxs-lookup"><span data-stu-id="a88bf-121">To resolve a topology, from the **Topology** menu, click **Resolve Topology**.</span></span>

<span data-ttu-id="a88bf-122">A barra de ferramentas indica o status da topologia: **\[ resolvido \]** ou **\[ não resolvido \]**.</span><span class="sxs-lookup"><span data-stu-id="a88bf-122">The toolbar indicates the topology status: **\[Resolved\]** or **\[Not Resolved\]**.</span></span>

<span data-ttu-id="a88bf-123">Se TopoEdit resolver uma topologia com êxito, o **status da topologia** será definido como **\[ resolvido \]** e os controles de reprodução serão habilitados.</span><span class="sxs-lookup"><span data-stu-id="a88bf-123">If TopoEdit resolves a topology successfully, **Topology Status** is set to **\[Resolved\]** and the playback controls are enabled.</span></span>

<span data-ttu-id="a88bf-124">Cada vez que você faz alterações na topologia, o **status da topologia** é definido como **\[ não resolvido \]** , o que indica que ela deve ser resolvida novamente.</span><span class="sxs-lookup"><span data-stu-id="a88bf-124">Each time you make changes to the topology, **Topology Status** is set to **\[Not Resolved\]** which indicates that it must be resolved again.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a88bf-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a88bf-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a88bf-126">Criando topologias usando TopoEdit</span><span class="sxs-lookup"><span data-stu-id="a88bf-126">Building Topologies by Using TopoEdit</span></span>](building-topologies-by-using-topoedit.md)
</dt> <dt>

[<span data-ttu-id="a88bf-127">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="a88bf-127">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



