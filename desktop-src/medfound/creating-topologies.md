---
description: Criando topologias
ms.assetid: afd1e646-9bb6-4265-a225-6aaaf1a7bb2a
title: Criando topologias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a9ec738c82ea2b85bcae7d4c05627b81ad939db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370538"
---
# <a name="creating-topologies"></a><span data-ttu-id="1ee75-103">Criando topologias</span><span class="sxs-lookup"><span data-stu-id="1ee75-103">Creating Topologies</span></span>

<span data-ttu-id="1ee75-104">Esta seção descreve alguns dos procedimentos gerais para a criação de uma topologia.</span><span class="sxs-lookup"><span data-stu-id="1ee75-104">This section describes some of the general procedures for creating a topology.</span></span>

<span data-ttu-id="1ee75-105">As etapas gerais para criar uma topologia são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="1ee75-105">The general steps for creating a topology are as follows:</span></span>

1.  <span data-ttu-id="1ee75-106">Crie um novo objeto de topologia chamando [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span><span class="sxs-lookup"><span data-stu-id="1ee75-106">Create a new topology object by calling [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span></span> <span data-ttu-id="1ee75-107">Essa função retorna um ponteiro para a interface [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) da topologia.</span><span class="sxs-lookup"><span data-stu-id="1ee75-107">This function returns a pointer to the topology's [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface.</span></span>

2.  <span data-ttu-id="1ee75-108">Inicialmente, a topologia não contém nenhum nó.</span><span class="sxs-lookup"><span data-stu-id="1ee75-108">Initially, the topology does not contain any nodes.</span></span> <span data-ttu-id="1ee75-109">Para criar nós para a topologia, chame [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode).</span><span class="sxs-lookup"><span data-stu-id="1ee75-109">To create nodes for the topology, call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode).</span></span> <span data-ttu-id="1ee75-110">Essa função retorna um ponteiro para a interface [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) do nó.</span><span class="sxs-lookup"><span data-stu-id="1ee75-110">This function returns a pointer to the node's [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) interface.</span></span> <span data-ttu-id="1ee75-111">Você deve especificar o tipo de nó ao criar o nó:</span><span class="sxs-lookup"><span data-stu-id="1ee75-111">You must specify the node type when you create the node:</span></span>

    -   <span data-ttu-id="1ee75-112">Nó de origem.</span><span class="sxs-lookup"><span data-stu-id="1ee75-112">Source node.</span></span>

    -   <span data-ttu-id="1ee75-113">Nó de transformação.</span><span class="sxs-lookup"><span data-stu-id="1ee75-113">Transform node.</span></span>

    -   <span data-ttu-id="1ee75-114">Nó de saída.</span><span class="sxs-lookup"><span data-stu-id="1ee75-114">Output node.</span></span>

    -   <span data-ttu-id="1ee75-115">Nó de t.</span><span class="sxs-lookup"><span data-stu-id="1ee75-115">Tee node.</span></span>

3.  <span data-ttu-id="1ee75-116">Inicialize cada nó.</span><span class="sxs-lookup"><span data-stu-id="1ee75-116">Initialize each node.</span></span> <span data-ttu-id="1ee75-117">O processo de inicialização depende do tipo de nó, conforme descrito nos tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="1ee75-117">The initialization process depends on the node type, as described in the topics that follow.</span></span>

4.  <span data-ttu-id="1ee75-118">Adicione cada nó à topologia chamando [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode).</span><span class="sxs-lookup"><span data-stu-id="1ee75-118">Add each node to the topology by calling [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode).</span></span>

5.  <span data-ttu-id="1ee75-119">Conecte os nós.</span><span class="sxs-lookup"><span data-stu-id="1ee75-119">Connect the nodes.</span></span> <span data-ttu-id="1ee75-120">Para conectar um nó, chame [**IMFTopologyNode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) no nó upstream e passe um ponteiro para o nó downstream.</span><span class="sxs-lookup"><span data-stu-id="1ee75-120">To connect a node, call [**IMFTopologyNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) on the upstream node, and pass in a pointer to the downstream node.</span></span>

<span data-ttu-id="1ee75-121">Os tópicos a seguir fornecem as etapas específicas para cada tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="1ee75-121">The following topics give the specific steps for each node type.</span></span>



| <span data-ttu-id="1ee75-122">Tópico</span><span class="sxs-lookup"><span data-stu-id="1ee75-122">Topic</span></span>                                                    | <span data-ttu-id="1ee75-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ee75-123">Description</span></span>                     |
|----------------------------------------------------------|---------------------------------|
| [<span data-ttu-id="1ee75-124">Criando nós de origem</span><span class="sxs-lookup"><span data-stu-id="1ee75-124">Creating Source Nodes</span></span>](creating-source-nodes.md)       | <span data-ttu-id="1ee75-125">Como criar um nó de origem.</span><span class="sxs-lookup"><span data-stu-id="1ee75-125">How to create a source node.</span></span>    |
| [<span data-ttu-id="1ee75-126">Criando nós de transformação</span><span class="sxs-lookup"><span data-stu-id="1ee75-126">Creating Transform Nodes</span></span>](creating-transform-nodes.md) | <span data-ttu-id="1ee75-127">Como criar um nó de transformação.</span><span class="sxs-lookup"><span data-stu-id="1ee75-127">How to create a transform node.</span></span> |
| [<span data-ttu-id="1ee75-128">Criando nós de saída</span><span class="sxs-lookup"><span data-stu-id="1ee75-128">Creating Output Nodes</span></span>](creating-output-nodes.md)       | <span data-ttu-id="1ee75-129">Como criar um nó de saída.</span><span class="sxs-lookup"><span data-stu-id="1ee75-129">How to create an output node.</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="1ee75-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1ee75-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ee75-131">Topologias</span><span class="sxs-lookup"><span data-stu-id="1ee75-131">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



