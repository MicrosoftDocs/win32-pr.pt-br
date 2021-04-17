---
description: Criando uma topologia de reprodução com TopoEdit
ms.assetid: 4d4c4ff9-dad1-4c79-a44a-2ad20f1bbca0
title: Criando uma topologia de reprodução com TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f942984b3ba56ef1288566cee80e7d30026de155
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "105813431"
---
# <a name="building-a-playback-topology-with-topoedit"></a><span data-ttu-id="9f5c2-103">Criando uma topologia de reprodução com TopoEdit</span><span class="sxs-lookup"><span data-stu-id="9f5c2-103">Building a Playback Topology with TopoEdit</span></span>

<span data-ttu-id="9f5c2-104">O TopoEdit pode criar uma topologia de reprodução para um arquivo de mídia local adicionando e conectando automaticamente os nós de origem, transformação e saída.</span><span class="sxs-lookup"><span data-stu-id="9f5c2-104">TopoEdit can build a playback topology for a local media file by automatically adding and connecting the source, transform, and output nodes.</span></span> <span data-ttu-id="9f5c2-105">TopoEdit não resolve automaticamente a topologia.</span><span class="sxs-lookup"><span data-stu-id="9f5c2-105">TopoEdit does not automatically resolve the topology.</span></span> <span data-ttu-id="9f5c2-106">Para reproduzir a topologia, resolva-a e, em seguida, use os controles de transporte.</span><span class="sxs-lookup"><span data-stu-id="9f5c2-106">To play the topology, resolve it and then use the transport controls.</span></span>

## <a name="to-build-and-play-a-topology-for-a-media-file"></a><span data-ttu-id="9f5c2-107">Para compilar e reproduzir uma topologia para um arquivo de mídia</span><span class="sxs-lookup"><span data-stu-id="9f5c2-107">To build and play a topology for a media file</span></span>

1.  <span data-ttu-id="9f5c2-108">No menu **arquivo** , clique em **processar arquivo**.</span><span class="sxs-lookup"><span data-stu-id="9f5c2-108">On the **File** menu, click **Render File**.</span></span>

    <span data-ttu-id="9f5c2-109">Isso abre a caixa de diálogo **selecionar origem da mídia** .</span><span class="sxs-lookup"><span data-stu-id="9f5c2-109">This opens the **Select Media Source** dialog box.</span></span>

2.  <span data-ttu-id="9f5c2-110">Navegue até a pasta onde o arquivo de mídia está localizado.</span><span class="sxs-lookup"><span data-stu-id="9f5c2-110">Navigate to the folder where the media file is located.</span></span>
3.  <span data-ttu-id="9f5c2-111">No campo **nome do arquivo:** , insira o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="9f5c2-111">In the **File name:** field, enter the name of the file.</span></span>
4.  <span data-ttu-id="9f5c2-112">Clique em **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="9f5c2-112">Click **Open**.</span></span>

    <span data-ttu-id="9f5c2-113">O **painel topologia** mostra a topologia conectada.</span><span class="sxs-lookup"><span data-stu-id="9f5c2-113">The **Topology Pane** shows the connected topology.</span></span> <span data-ttu-id="9f5c2-114">Internamente, o TopoEdit executa as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="9f5c2-114">Internally, TopoEdit performs the following tasks:</span></span>

    -   <span data-ttu-id="9f5c2-115">Enumera os fluxos no arquivo de mídia e cria os nós de origem.</span><span class="sxs-lookup"><span data-stu-id="9f5c2-115">Enumerates the streams in the media file and creates the source nodes.</span></span>
    -   <span data-ttu-id="9f5c2-116">Dependendo do tipo de mídia dos nós de origem, o adiciona nós de transformação, como decodificadores.</span><span class="sxs-lookup"><span data-stu-id="9f5c2-116">Depending on the media type of the source nodes, adds transform nodes, such as decoders.</span></span>
    -   <span data-ttu-id="9f5c2-117">Adiciona o coletor de processamento de áudio de streaming (SAR) para fluxo de áudio e o coletor de processador de vídeo avançado (EVR) para o fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9f5c2-117">Adds the Streaming Audio Renderer (SAR) sink for audio stream and the enhanced video renderer (EVR) sink for the video stream.</span></span>
    -   <span data-ttu-id="9f5c2-118">Conecta as entradas de nó e as saídas de nó.</span><span class="sxs-lookup"><span data-stu-id="9f5c2-118">Connects the node inputs and the node outputs.</span></span>

5.  <span data-ttu-id="9f5c2-119">No menu **topologia** , clique em **resolver topologia**.</span><span class="sxs-lookup"><span data-stu-id="9f5c2-119">On the **Topology** menu, click **Resolve Topology**.</span></span>
6.  <span data-ttu-id="9f5c2-120">Clique no botão **reproduzir** na barra de ferramentas para reproduzir a topologia.</span><span class="sxs-lookup"><span data-stu-id="9f5c2-120">Click the **Play** button on the toolbar to play the topology.</span></span> A imagem a seguir mostra o botão **reproduzir** :::image type="icon" source="images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg"::: .

## <a name="related-topics"></a><span data-ttu-id="9f5c2-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9f5c2-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f5c2-123">Controles de reprodução no TopoEdit</span><span class="sxs-lookup"><span data-stu-id="9f5c2-123">Playback Controls in TopoEdit</span></span>](playback-controls-in-topoedit.md)
</dt> <dt>

[<span data-ttu-id="9f5c2-124">Resolvendo uma topologia com TopoEdit</span><span class="sxs-lookup"><span data-stu-id="9f5c2-124">Resolving a Topology with TopoEdit</span></span>](resolving-a-topology-with-topoedit.md)
</dt> <dt>

[<span data-ttu-id="9f5c2-125">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="9f5c2-125">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



