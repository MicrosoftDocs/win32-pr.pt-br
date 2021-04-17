---
description: Criação de topologia avançada
ms.assetid: 66aa07d8-6756-4d5b-9f0a-24b902da6fa2
title: Criação de topologia avançada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4cc061d4e557dda4ccbb81eabc55e8e1b3e33b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296316"
---
# <a name="advanced-topology-building"></a><span data-ttu-id="413fe-103">Criação de topologia avançada</span><span class="sxs-lookup"><span data-stu-id="413fe-103">Advanced Topology Building</span></span>

<span data-ttu-id="413fe-104">Esta seção descreve algumas técnicas avançadas para a criação de topologias.</span><span class="sxs-lookup"><span data-stu-id="413fe-104">This section describes some advanced techniques for building topologies.</span></span> <span data-ttu-id="413fe-105">Você pode usar essas técnicas se quiser mais controle sobre as topologias que você envia para a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="413fe-105">You can use these techniques if you want more control over the topologies that you send to the Media Session.</span></span>

<span data-ttu-id="413fe-106">Como essas técnicas se destinam a cenários que vão além da funcionalidade fornecida pelo carregador de topologia padrão, muitos dos detalhes dependerão dos requisitos específicos do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="413fe-106">Because these techniques are intended for scenarios that go beyond the functionality provided by the standard topology loader, many of the details will depend on the particular requirements of your application.</span></span> <span data-ttu-id="413fe-107">Portanto, esta seção está organizada de forma flexível em relação a subtarefas menores, em vez de cenários completos de ponta a ponta.</span><span class="sxs-lookup"><span data-stu-id="413fe-107">Therefore, this section is organized loosely around smaller subtasks, rather than complete, end-to-end scenarios.</span></span>

<span data-ttu-id="413fe-108">O aplicativo de reprodução típico segue estas etapas:</span><span class="sxs-lookup"><span data-stu-id="413fe-108">The typical playback application follows these steps:</span></span>

1.  <span data-ttu-id="413fe-109">O aplicativo cria uma topologia parcial e a enfileira na sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="413fe-109">The application builds a partial topology and queues it on the Media Session.</span></span>
2.  <span data-ttu-id="413fe-110">A sessão de mídia invoca o carregador de topologia para resolver a topologia.</span><span class="sxs-lookup"><span data-stu-id="413fe-110">The Media Session invokes the topology loader to resolve the topology.</span></span>

<span data-ttu-id="413fe-111">Se você quiser ir além dos recursos do carregador de topologia, há três abordagens gerais:</span><span class="sxs-lookup"><span data-stu-id="413fe-111">If you want to go beyond the capabilities of the topology loader, there are three general approaches:</span></span>

-   <span data-ttu-id="413fe-112">Crie uma topologia completa.</span><span class="sxs-lookup"><span data-stu-id="413fe-112">Build a complete topology.</span></span> <span data-ttu-id="413fe-113">Ao enfileirar a topologia na sessão de mídia, chame [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) com o \_ sinalizador resolution do settopologia do MFSESSION \_ .</span><span class="sxs-lookup"><span data-stu-id="413fe-113">When you queue the topology on the Media Session, call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) with the MFSESSION\_SETTOPOLOGY\_NORESOLUTION flag.</span></span> <span data-ttu-id="413fe-114">Esse sinalizador impede que a sessão de mídia tente resolver a topologia.</span><span class="sxs-lookup"><span data-stu-id="413fe-114">This flag prevents the Media Session from attempting to resolve the topology.</span></span>

-   <span data-ttu-id="413fe-115">Invoque diretamente o carregador de topologia para resolver a topologia.</span><span class="sxs-lookup"><span data-stu-id="413fe-115">Directly invoke the topology loader to resolve the topology.</span></span> <span data-ttu-id="413fe-116">Em seguida, você pode modificar a topologia completa antes de enfileirar a fila na sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="413fe-116">You can then modify the full topology before queuing it on the Media Session.</span></span>

-   <span data-ttu-id="413fe-117">Implemente um carregador de topologia personalizado.</span><span class="sxs-lookup"><span data-stu-id="413fe-117">Implement a custom topology loader.</span></span> <span data-ttu-id="413fe-118">Com essa abordagem, você coloca em fila uma topologia parcial, mas a sessão de mídia chama seu carregador personalizado em vez da implementação de Media Foundation padrão.</span><span class="sxs-lookup"><span data-stu-id="413fe-118">With this approach, you queue a partial topology, but the Media Session invokes your custom loader instead of the standard Media Foundation implementation.</span></span> <span data-ttu-id="413fe-119">Uma vantagem dessa abordagem é que você pode executar a criação de topologia personalizada dentro do ambiente protegido.</span><span class="sxs-lookup"><span data-stu-id="413fe-119">One advantage of this approach is that you can perform custom topology building inside the protected environment.</span></span> <span data-ttu-id="413fe-120">(Nesse caso, no entanto, o carregador de topologia deve ser um componente confiável.</span><span class="sxs-lookup"><span data-stu-id="413fe-120">(In that case, however, the topology loader must be a trusted component.</span></span> <span data-ttu-id="413fe-121">Para obter mais informações, consulte [proteção de caminho de mídia](protected-media-path.md).)</span><span class="sxs-lookup"><span data-stu-id="413fe-121">For more information, see [Protected Media Path](protected-media-path.md).)</span></span>

<span data-ttu-id="413fe-122">Esta seção contém os seguintes tópicos.</span><span class="sxs-lookup"><span data-stu-id="413fe-122">This section contains the following topics.</span></span>



| <span data-ttu-id="413fe-123">Tópico</span><span class="sxs-lookup"><span data-stu-id="413fe-123">Topic</span></span>                                                                          | <span data-ttu-id="413fe-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="413fe-124">Description</span></span>                                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="413fe-125">Carregadores de topologia personalizados</span><span class="sxs-lookup"><span data-stu-id="413fe-125">Custom Topology Loaders</span></span>](custom-topology-loaders.md)                         | <span data-ttu-id="413fe-126">Como fornecer uma implementação personalizada do [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) para a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="413fe-126">How to provide a custom implementation of [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) for the Media Session.</span></span>          |
| [<span data-ttu-id="413fe-127">Associando nós de saída a coletores de mídia</span><span class="sxs-lookup"><span data-stu-id="413fe-127">Binding Output Nodes to Media Sinks</span></span>](binding-output-nodes-to-media-sinks.md) | <span data-ttu-id="413fe-128">Como preparar os nós de saída em uma topologia se você estiver usando o carregador de topologia fora da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="413fe-128">How to prepare the output nodes in a topology if you are using the topology loader outside of the Media Session.</span></span> |
| [<span data-ttu-id="413fe-129">Adicionando um decodificador a uma topologia</span><span class="sxs-lookup"><span data-stu-id="413fe-129">Adding a Decoder to a Topology</span></span>](adding-a-decoder-to-a-topology.md)           | <span data-ttu-id="413fe-130">Como selecionar um decodificador manualmente e adicioná-lo a uma topologia.</span><span class="sxs-lookup"><span data-stu-id="413fe-130">How to select a decoder manually and add it to a topology.</span></span>                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="413fe-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="413fe-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="413fe-132">Topologias</span><span class="sxs-lookup"><span data-stu-id="413fe-132">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



