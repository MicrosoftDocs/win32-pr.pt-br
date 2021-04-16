---
description: Configuração de grafo de filtro de DVD
ms.assetid: 0c68c456-2240-4090-b45c-bd098cfea645
title: Configuração de grafo de filtro de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec7bb8757e5246fc01309fbef55e654436560b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500638"
---
# <a name="dvd-filter-graph-configuration"></a><span data-ttu-id="be2ec-103">Configuração de grafo de filtro de DVD</span><span class="sxs-lookup"><span data-stu-id="be2ec-103">DVD Filter Graph Configuration</span></span>

<span data-ttu-id="be2ec-104">Esta seção descreve as várias configurações de gráfico de filtro para reprodução de DVD no DirectShow.</span><span class="sxs-lookup"><span data-stu-id="be2ec-104">This section describes the various filter graph configurations for DVD playback in DirectShow.</span></span> <span data-ttu-id="be2ec-105">Esses diagramas são fornecidos principalmente para referência.</span><span class="sxs-lookup"><span data-stu-id="be2ec-105">These diagrams are provided mainly for reference.</span></span> <span data-ttu-id="be2ec-106">O navegador de DVD cria o grafo, de modo que, em geral, não é necessário entender os detalhes de como o grafo é configurado.</span><span class="sxs-lookup"><span data-stu-id="be2ec-106">The DVD Navigator builds the graph, so in general it is not necessary to understand the details of how the graph is configured.</span></span> <span data-ttu-id="be2ec-107">Para obter mais informações, consulte [criando o grafo de filtro de DVD](building-the-dvd-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="be2ec-107">For more information, see [Building the DVD Filter Graph](building-the-dvd-filter-graph.md).</span></span>

<span data-ttu-id="be2ec-108">A ilustração a seguir mostra um grafo de filtro de DVD com um decodificador de software.</span><span class="sxs-lookup"><span data-stu-id="be2ec-108">The following illustration shows a DVD filter graph with a software decoder.</span></span>

![Grafo de filtro de DVD para Windows XP](images/dvd-graph-xp.png)

<span data-ttu-id="be2ec-110">Quando um decodificador de hardware está presente, ele normalmente é conectado diretamente à placa de vídeo por uma porta de vídeo.</span><span class="sxs-lookup"><span data-stu-id="be2ec-110">When a hardware decoder is present, it is typically connected directly to the video card by a video port.</span></span> <span data-ttu-id="be2ec-111">Isso permite que os bits de vídeo decodificados sejam enviados diretamente para o buffer de quadro na placa gráfica sem passar na memória do host.</span><span class="sxs-lookup"><span data-stu-id="be2ec-111">This enables the decoded video bits to be sent directly to the frame buffer on the graphics card without passing into host memory.</span></span> <span data-ttu-id="be2ec-112">Para gerenciar essa conexão direta em versões anteriores do Windows, o DirectShow dá suporte a VPE (extensões de porta de vídeo) do DirectDraw por meio de uma interface no [filtro de mixer de sobreposição](overlay-mixer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="be2ec-112">To manage this direct connection on earlier versions of Windows, DirectShow supports DirectDraw Video Port Extensions (VPE) through an interface on the [Overlay Mixer Filter](overlay-mixer-filter.md).</span></span>

> [!Note]  
> <span data-ttu-id="be2ec-113">O mixer de sobreposição agora foi preterido.</span><span class="sxs-lookup"><span data-stu-id="be2ec-113">The Overlay Mixer is now deprecated.</span></span>

 

<span data-ttu-id="be2ec-114">No Windows XP e posterior, um decodificador de hardware pode se conectar ao filtro do [Gerenciador de portas de vídeo](video-port-manager.md) .</span><span class="sxs-lookup"><span data-stu-id="be2ec-114">In Windows XP and later, a hardware decoder can connect to the [Video Port Manager](video-port-manager.md) filter.</span></span>

![DVD Graph para Windows XP com um decodificador de hardware](images/dvd-hwgraph-xp.png)

<span data-ttu-id="be2ec-116">Em todos esses gráficos, o navegador de DVD é o filtro de origem; Ele executa várias tarefas:</span><span class="sxs-lookup"><span data-stu-id="be2ec-116">In all these graphs, the DVD Navigator is the source filter; it performs several tasks:</span></span>

-   <span data-ttu-id="be2ec-117">Lê os dados de navegação e vídeo do disco.</span><span class="sxs-lookup"><span data-stu-id="be2ec-117">Reads the navigation and video data from the disc.</span></span>
-   <span data-ttu-id="be2ec-118">Demultiplexa os dados de vídeo, áudio e subimagem em fluxos separados.</span><span class="sxs-lookup"><span data-stu-id="be2ec-118">Demultiplexes the video, audio, and subpicture data into separate streams.</span></span>
-   <span data-ttu-id="be2ec-119">Bombas os fluxos no grafo para processamento adicional e renderização eventual.</span><span class="sxs-lookup"><span data-stu-id="be2ec-119">Pumps the streams into the graph for further processing and eventual rendering.</span></span>
-   <span data-ttu-id="be2ec-120">Informa seu aplicativo de eventos relacionados a DVD.</span><span class="sxs-lookup"><span data-stu-id="be2ec-120">Informs your application of DVD-related events.</span></span>

<span data-ttu-id="be2ec-121">No fluxo de áudio, o navegador de DVD conecta o downstream a um decodificador de áudio, que se conecta ao [filtro de processador DirectSound](directsound-renderer-filter.md), o processador de áudio padrão.</span><span class="sxs-lookup"><span data-stu-id="be2ec-121">On the audio stream, the DVD Navigator connects downstream to an audio decoder, which connects to the [DirectSound Renderer Filter](directsound-renderer-filter.md), the default audio renderer.</span></span> <span data-ttu-id="be2ec-122">Nos fluxos de vídeo e subimagem, os filtros downstream são o decodificador de vídeo de terceiros e o processador de mixagem de vídeo (ou o [mixer de sobreposição](overlay-mixer-filter.md)e o [processador de vídeo](video-renderer-filter.md) em aplicativos de nível inferior).</span><span class="sxs-lookup"><span data-stu-id="be2ec-122">On the video and subpicture streams, the downstream filters are the third-party video decoder, and the Video Mixing Renderer (or the [Overlay Mixer](overlay-mixer-filter.md), and the [Video Renderer](video-renderer-filter.md) on downlevel applications).</span></span> <span data-ttu-id="be2ec-123">Se seu aplicativo tratar dados de linha 21 com legenda codificada, você deverá adicionar o filtro do DirectShow linha 21 do decodificador 2 ao grafo.</span><span class="sxs-lookup"><span data-stu-id="be2ec-123">If your application will handle line 21 closed-captioned data, you must add the DirectShow Line 21 Decoder 2 filter to the graph.</span></span> <span data-ttu-id="be2ec-124">Isso envolve uma única chamada de método; o filtro será conectado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="be2ec-124">This involves a single method call; the filter will be connected automatically.</span></span>

<span data-ttu-id="be2ec-125">Seu aplicativo se comunica com o e controla o navegador de DVD por meio das interfaces personalizadas que o navegador de DVD expõe: [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)– os métodos "set" — e [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)– os métodos "Get".</span><span class="sxs-lookup"><span data-stu-id="be2ec-125">Your application communicates with and controls the DVD Navigator through the custom interfaces that the DVD Navigator exposes: [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)—the "set" methods—and [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)—the "get" methods.</span></span> <span data-ttu-id="be2ec-126">Ele também deve se comunicar com o Gerenciador de gráficos de filtro (por meio de [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)) para parar, iniciar e controlar o grafo.</span><span class="sxs-lookup"><span data-stu-id="be2ec-126">It also must communicate with the filter graph manager (through [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)) to stop, start, and otherwise control the graph.</span></span> <span data-ttu-id="be2ec-127">Talvez você também precise controlar outros filtros individuais, como o filtro de mixer de sobreposição para alternar entre a exibição em janela e em tela inteira.</span><span class="sxs-lookup"><span data-stu-id="be2ec-127">You might also need to control other individual filters, such as the Overlay Mixer filter for switching between windowed and full-screen display.</span></span> <span data-ttu-id="be2ec-128">Para obter mais informações, consulte [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2).</span><span class="sxs-lookup"><span data-stu-id="be2ec-128">For more information, see [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2).</span></span> <span data-ttu-id="be2ec-129">A configuração exata do grafo variará dependendo do tipo de decodificador MPEG-2 que você instalou, independentemente de você precisar lidar com os dados de legenda oculta da linha 21 e outros fatores.</span><span class="sxs-lookup"><span data-stu-id="be2ec-129">The exact configuration of the graph will vary depending on what type of MPEG-2 decoder you have installed, whether you need to handle line 21 closed-captioned data, and other factors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be2ec-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="be2ec-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be2ec-131">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="be2ec-131">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



