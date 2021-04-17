---
description: Este artigo descreve como escrever um apresentador personalizado para o processador de vídeo avançado (EVR).
ms.assetid: 1135b309-b158-4b70-9f76-5c93d0ad3250
title: Como escrever um apresentador EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94933d9eb53b0b03105edc7056ace4fe73238d16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555538"
---
# <a name="how-to-write-an-evr-presenter"></a><span data-ttu-id="e1c2f-103">Como escrever um apresentador EVR</span><span class="sxs-lookup"><span data-stu-id="e1c2f-103">How to Write an EVR Presenter</span></span>

<span data-ttu-id="e1c2f-104">Este artigo descreve como escrever um apresentador personalizado para o processador de vídeo avançado (EVR).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-104">This article describes how to write a custom presenter for the enhanced video renderer (EVR).</span></span> <span data-ttu-id="e1c2f-105">Um apresentador personalizado pode ser usado com o DirectShow e o Media Foundation; as interfaces e o modelo de objeto são os mesmos para ambas as tecnologias, embora a seqüência exata de operações possa variar.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-105">A custom presenter can be used with both DirectShow and Media Foundation; the interfaces and object model are the same for both technologies, although the exact sequence of operations might vary.</span></span>

<span data-ttu-id="e1c2f-106">O código de exemplo neste tópico é adaptado do [exemplo EVRPresenter](evrpresenter-sample.md), que é fornecido na SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-106">The example code in this topic is adapted from the [EVRPresenter Sample](evrpresenter-sample.md), which is provided in the Windows SDK.</span></span>

<span data-ttu-id="e1c2f-107">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="e1c2f-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="e1c2f-108">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="e1c2f-109">Modelo de objeto do apresentador</span><span class="sxs-lookup"><span data-stu-id="e1c2f-109">Presenter Object Model</span></span>](#presenter-object-model)
    -   [<span data-ttu-id="e1c2f-110">Fluxo de dados dentro do EVR</span><span class="sxs-lookup"><span data-stu-id="e1c2f-110">Data Flow Inside the EVR</span></span>](#data-flow-inside-the-evr)
    -   [<span data-ttu-id="e1c2f-111">Estados do apresentador</span><span class="sxs-lookup"><span data-stu-id="e1c2f-111">Presenter States</span></span>](#presenter-states)
    -   [<span data-ttu-id="e1c2f-112">Interfaces do apresentador</span><span class="sxs-lookup"><span data-stu-id="e1c2f-112">Presenter Interfaces</span></span>](#presenter-interfaces)
    -   [<span data-ttu-id="e1c2f-113">Implementando IMFVideoDeviceID</span><span class="sxs-lookup"><span data-stu-id="e1c2f-113">Implementing IMFVideoDeviceID</span></span>](#implementing-imfvideodeviceid)
    -   [<span data-ttu-id="e1c2f-114">Implementando IMFTopologyServiceLookupClient</span><span class="sxs-lookup"><span data-stu-id="e1c2f-114">Implementing IMFTopologyServiceLookupClient</span></span>](#implementing-imftopologyservicelookupclient)
    -   [<span data-ttu-id="e1c2f-115">Implementando IMFVideoPresenter</span><span class="sxs-lookup"><span data-stu-id="e1c2f-115">Implementing IMFVideoPresenter</span></span>](#implementing-imfvideopresenter)
    -   [<span data-ttu-id="e1c2f-116">Implementando IMFClockStateSink</span><span class="sxs-lookup"><span data-stu-id="e1c2f-116">Implementing IMFClockStateSink</span></span>](#implementing-imfclockstatesink)
    -   [<span data-ttu-id="e1c2f-117">Implementando IMFRateSupport</span><span class="sxs-lookup"><span data-stu-id="e1c2f-117">Implementing IMFRateSupport</span></span>](#implementing-imfratesupport)
    -   [<span data-ttu-id="e1c2f-118">Enviando eventos para o EVR</span><span class="sxs-lookup"><span data-stu-id="e1c2f-118">Sending Events to the EVR</span></span>](#sending-events-to-the-evr)
-   [<span data-ttu-id="e1c2f-119">Negociando formatos</span><span class="sxs-lookup"><span data-stu-id="e1c2f-119">Negotiating Formats</span></span>](#negotiating-formats)
-   [<span data-ttu-id="e1c2f-120">Gerenciando o dispositivo Direct3D</span><span class="sxs-lookup"><span data-stu-id="e1c2f-120">Managing the Direct3D Device</span></span>](#managing-the-direct3d-device)
    -   [<span data-ttu-id="e1c2f-121">Alocando superfícies do Direct3D</span><span class="sxs-lookup"><span data-stu-id="e1c2f-121">Allocating Direct3D Surfaces</span></span>](#allocating-direct3d-surfaces)
    -   [<span data-ttu-id="e1c2f-122">Amostras de rastreamento</span><span class="sxs-lookup"><span data-stu-id="e1c2f-122">Tracking Samples</span></span>](#tracking-samples)
-   [<span data-ttu-id="e1c2f-123">Processando saída</span><span class="sxs-lookup"><span data-stu-id="e1c2f-123">Processing Output</span></span>](#processing-output)
    -   [<span data-ttu-id="e1c2f-124">Repintando quadros</span><span class="sxs-lookup"><span data-stu-id="e1c2f-124">Repainting Frames</span></span>](#repainting-frames)
    -   [<span data-ttu-id="e1c2f-125">Exemplos de agendamento</span><span class="sxs-lookup"><span data-stu-id="e1c2f-125">Scheduling Samples</span></span>](#scheduling-samples)
    -   [<span data-ttu-id="e1c2f-126">Apresentando exemplos</span><span class="sxs-lookup"><span data-stu-id="e1c2f-126">Presenting Samples</span></span>](#presenting-samples)
    -   [<span data-ttu-id="e1c2f-127">Retângulos de origem e de destino</span><span class="sxs-lookup"><span data-stu-id="e1c2f-127">Source and Destination Rectangles</span></span>](#source-and-destination-rectangles)
    -   [<span data-ttu-id="e1c2f-128">Fim do fluxo</span><span class="sxs-lookup"><span data-stu-id="e1c2f-128">End of Stream</span></span>](#end-of-stream)
-   [<span data-ttu-id="e1c2f-129">Revisão do quadro</span><span class="sxs-lookup"><span data-stu-id="e1c2f-129">Frame Stepping</span></span>](#frame-stepping)
    -   [<span data-ttu-id="e1c2f-130">Implementando a revisão do quadro</span><span class="sxs-lookup"><span data-stu-id="e1c2f-130">Implementing Frame Stepping</span></span>](#implementing-frame-stepping)
-   [<span data-ttu-id="e1c2f-131">Configurando o apresentador no EVR</span><span class="sxs-lookup"><span data-stu-id="e1c2f-131">Setting the Presenter on the EVR</span></span>](#setting-the-presenter-on-the-evr)
    -   [<span data-ttu-id="e1c2f-132">Configurando o apresentador no DirectShow</span><span class="sxs-lookup"><span data-stu-id="e1c2f-132">Setting the Presenter in DirectShow</span></span>](#setting-the-presenter-in-directshow)
    -   [<span data-ttu-id="e1c2f-133">Configurando o apresentador no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e1c2f-133">Setting the Presenter in Media Foundation</span></span>](#setting-the-presenter-in-media-foundation)
-   [<span data-ttu-id="e1c2f-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e1c2f-134">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="e1c2f-135">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="e1c2f-135">Prerequisites</span></span>

<span data-ttu-id="e1c2f-136">Antes de escrever um apresentador personalizado, você deve estar familiarizado com as seguintes tecnologias:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-136">Before writing a custom presenter, you should be familiar with the following technologies:</span></span>

-   <span data-ttu-id="e1c2f-137">O processador de vídeo aprimorado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-137">The enhanced video renderer.</span></span> <span data-ttu-id="e1c2f-138">Consulte [processador de vídeo aprimorado](enhanced-video-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-138">See [Enhanced Video Renderer](enhanced-video-renderer.md).</span></span>
-   <span data-ttu-id="e1c2f-139">Gráficos do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-139">Direct3D graphics.</span></span> <span data-ttu-id="e1c2f-140">Você não precisa entender gráficos 3D para escrever um apresentador, mas deve saber como criar um dispositivo Direct3D e gerenciar superfícies de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-140">You don't need to understand 3-D graphics to write a presenter, but you must know how to create a Direct3D device and manage Direct3D surfaces.</span></span> <span data-ttu-id="e1c2f-141">Se você não estiver familiarizado com o Direct3D, leia as seções "dispositivos Direct3D" e "recursos do Direct3D" na documentação do SDK de gráficos do DirectX.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-141">If you aren't familiar with Direct3D, read the sections "Direct3D Devices" and "Direct3D Resources" in the DirectX Graphics SDK documentation.</span></span>
-   <span data-ttu-id="e1c2f-142">Os gráficos de filtro do DirectShow ou o pipeline Media Foundation, dependendo da tecnologia que seu aplicativo usará para renderizar o vídeo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-142">DirectShow filter graphs or the Media Foundation pipeline, depending on which technology your application will use to render video.</span></span>
-   <span data-ttu-id="e1c2f-143">[Transformações de Media Foundation](media-foundation-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-143">[Media Foundation Transforms](media-foundation-transforms.md).</span></span> <span data-ttu-id="e1c2f-144">O mixer EVR é uma transformação Media Foundation e o apresentador chama métodos diretamente no mixer.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-144">The EVR mixer is a Media Foundation transform, and the presenter calls methods directly on the mixer.</span></span>
-   <span data-ttu-id="e1c2f-145">Implementando objetos COM.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-145">Implementing COM objects.</span></span> <span data-ttu-id="e1c2f-146">O apresentador é um objeto COM COM thread livre em processo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-146">The presenter is an in-process, free-threaded COM object.</span></span>

## <a name="presenter-object-model"></a><span data-ttu-id="e1c2f-147">Modelo de objeto do apresentador</span><span class="sxs-lookup"><span data-stu-id="e1c2f-147">Presenter Object Model</span></span>

<span data-ttu-id="e1c2f-148">Esta seção contém uma visão geral do modelo de objeto e das interfaces do apresentador.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-148">This section contains an overview the presenter object model and interfaces.</span></span>

### <a name="data-flow-inside-the-evr"></a><span data-ttu-id="e1c2f-149">Fluxo de dados dentro do EVR</span><span class="sxs-lookup"><span data-stu-id="e1c2f-149">Data Flow Inside the EVR</span></span>

<span data-ttu-id="e1c2f-150">O EVR usa dois componentes de plug-in para renderizar o vídeo: o *mixer* e o *apresentador*.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-150">The EVR uses two plug-in components to render video: the *mixer* and the *presenter*.</span></span> <span data-ttu-id="e1c2f-151">O mixer mescla os fluxos de vídeo e desentrelaça o vídeo, se necessário.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-151">The mixer blends the video streams and deinterlaces the video if needed.</span></span> <span data-ttu-id="e1c2f-152">O apresentador desenha (ou *apresenta*) o vídeo na exibição e agenda quando cada quadro é desenhado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-152">The presenter draws (or *presents*) the video onto the display and schedules when each frame is drawn.</span></span> <span data-ttu-id="e1c2f-153">Os aplicativos podem substituir qualquer um desses objetos por uma implementação personalizada.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-153">Applications can replace either of these objects with a custom implementation.</span></span>

<span data-ttu-id="e1c2f-154">O EVR tem um ou mais fluxos de entrada, e o mixer tem um número correspondente de fluxos de entrada.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-154">The EVR has one or more input streams, and the mixer has a corresponding number of input streams.</span></span> <span data-ttu-id="e1c2f-155">O fluxo 0 é sempre o *fluxo de referência*.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-155">Stream 0 is always the *reference stream*.</span></span> <span data-ttu-id="e1c2f-156">Os outros fluxos são *subfluxos*, que o mixer Alpha mistura no fluxo de referência.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-156">The other streams are *substreams*, which the mixer alpha-blends onto the reference stream.</span></span> <span data-ttu-id="e1c2f-157">O fluxo de referência determina a taxa de quadros mestre para o vídeo composto.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-157">The reference stream determines the master frame-rate for the composited video.</span></span> <span data-ttu-id="e1c2f-158">Para cada quadro de referência, o mixer usa o quadro mais recente de cada Subfluxo, mistura-o alfa para o quadro de referência e gera um único quadro composto.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-158">For each reference frame, the mixer takes the most recent frame from each substream, alpha-blends them onto the reference frame, and outputs a single composited frame.</span></span> <span data-ttu-id="e1c2f-159">O mixer também executa desentrelaçamento e conversão de cores de YUV para RGB, se necessário.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-159">The mixer also performs deinterlacing and color conversion from YUV to RGB if needed.</span></span> <span data-ttu-id="e1c2f-160">O EVR sempre insere o mixer no pipeline de vídeo, independentemente do número de fluxos de entrada ou do formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-160">The EVR always inserts the mixer into the video pipeline, regardless of the number of input streams or the video format.</span></span> <span data-ttu-id="e1c2f-161">A imagem a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-161">The following image illustrates this process.</span></span>

![diagrama que mostra o fluxo de referência e o Subfluxo apontando para o mixer, que aponta para o apresentador, que aponta para a exibição](images/459338c4-cff8-4d20-bffd-ff1cbbe6f332.gif)

<span data-ttu-id="e1c2f-163">O apresentador executa as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-163">The presenter performs the following tasks:</span></span>

-   <span data-ttu-id="e1c2f-164">Define o formato de saída no mixer.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-164">Sets the output format on the mixer.</span></span> <span data-ttu-id="e1c2f-165">Antes de o streaming começar, o apresentador define um tipo de mídia no fluxo de saída do mixer.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-165">Before streaming begins, the presenter sets a media type on the mixer's output stream.</span></span> <span data-ttu-id="e1c2f-166">Esse tipo de mídia define o formato da imagem compostada.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-166">This media type defines the format of the composited image.</span></span>
-   <span data-ttu-id="e1c2f-167">Cria o dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-167">Creates the Direct3D device.</span></span>
-   <span data-ttu-id="e1c2f-168">Aloca superfícies de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-168">Allocates Direct3D surfaces.</span></span> <span data-ttu-id="e1c2f-169">O mixer blits os quadros compostos nessas superfícies.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-169">The mixer blits the composited frames onto these surfaces.</span></span>
-   <span data-ttu-id="e1c2f-170">Obtém a saída do mixer.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-170">Gets the output from the mixer.</span></span>
-   <span data-ttu-id="e1c2f-171">Agenda quando os quadros são apresentados.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-171">Schedules when the frames are presented.</span></span> <span data-ttu-id="e1c2f-172">O EVR fornece o relógio de apresentação e o apresentador agenda quadros de acordo com esse relógio.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-172">The EVR provides the presentation clock, and the presenter schedules frames according to this clock.</span></span>
-   <span data-ttu-id="e1c2f-173">Apresenta cada quadro usando o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-173">Presents each frame using Direct3D.</span></span>
-   <span data-ttu-id="e1c2f-174">Executa a depuração e a limpeza do quadro.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-174">Performs frame stepping and scrubbing.</span></span>

### <a name="presenter-states"></a><span data-ttu-id="e1c2f-175">Estados do apresentador</span><span class="sxs-lookup"><span data-stu-id="e1c2f-175">Presenter States</span></span>

<span data-ttu-id="e1c2f-176">A qualquer momento, o apresentador está em um dos seguintes Estados:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-176">At any time, the presenter is in one of following states:</span></span>

-   <span data-ttu-id="e1c2f-177">*Iniciado*.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-177">*Started*.</span></span> <span data-ttu-id="e1c2f-178">O relógio de apresentação do EVR está em execução.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-178">The EVR's presentation clock is running.</span></span> <span data-ttu-id="e1c2f-179">O apresentador agenda quadros de vídeo para apresentação à medida que eles chegam.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-179">The presenter schedules video frames for presentation as they arrive.</span></span>
-   <span data-ttu-id="e1c2f-180">Em *pausa*.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-180">*Paused*.</span></span> <span data-ttu-id="e1c2f-181">O relógio de apresentação está suspenso.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-181">The presentation clock is suspended.</span></span> <span data-ttu-id="e1c2f-182">O apresentador não apresenta novos exemplos, mas mantém sua fila de exemplos agendados.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-182">The presenter does not present any new samples but maintains its queue of scheduled samples.</span></span> <span data-ttu-id="e1c2f-183">Se novos exemplos forem recebidos, o apresentador os adicionará à fila.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-183">If new samples are received, the presenter adds them to the queue.</span></span>
-   <span data-ttu-id="e1c2f-184">*Parado*.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-184">*Stopped*.</span></span> <span data-ttu-id="e1c2f-185">O relógio de apresentação foi interrompido.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-185">The presentation clock is stopped.</span></span> <span data-ttu-id="e1c2f-186">O apresentador descarta quaisquer exemplos que foram agendados.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-186">The presenter discards any samples that were scheduled.</span></span>
-   <span data-ttu-id="e1c2f-187">*Desligar*.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-187">*Shut down*.</span></span> <span data-ttu-id="e1c2f-188">O apresentador libera todos os recursos relacionados ao streaming, como superfícies de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-188">The presenter releases any resources related to streaming, such as Direct3D surfaces.</span></span> <span data-ttu-id="e1c2f-189">Este é o estado inicial do apresentador e o estado final antes de o apresentador ser destruído.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-189">This is the presenter's initial state, and the final state before the presenter is destroyed.</span></span>

<span data-ttu-id="e1c2f-190">No código de exemplo neste tópico, o estado do apresentador é representado por uma enumeração:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-190">In the example code in this topic, the presenter state is represented by an enumeration:</span></span>


```C++
enum RENDER_STATE
{
    RENDER_STATE_STARTED = 1,
    RENDER_STATE_STOPPED,
    RENDER_STATE_PAUSED,
    RENDER_STATE_SHUTDOWN,  // Initial state.
};
```



<span data-ttu-id="e1c2f-191">Algumas operações não são válidas enquanto o apresentador está no estado de desligamento.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-191">Some operations are not valid while the presenter is in the shutdown state.</span></span> <span data-ttu-id="e1c2f-192">O código de exemplo verifica esse estado chamando um método auxiliar:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-192">The example code checks for this state by calling a helper method:</span></span>


```C++
    HRESULT CheckShutdown() const
    {
        if (m_RenderState == RENDER_STATE_SHUTDOWN)
        {
            return MF_E_SHUTDOWN;
        }
        else
        {
            return S_OK;
        }
    }
```



### <a name="presenter-interfaces"></a><span data-ttu-id="e1c2f-193">Interfaces do apresentador</span><span class="sxs-lookup"><span data-stu-id="e1c2f-193">Presenter Interfaces</span></span>

<span data-ttu-id="e1c2f-194">Um apresentador é necessário para implementar as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-194">A presenter is required to implement the following interfaces:</span></span>



| <span data-ttu-id="e1c2f-195">Interface</span><span class="sxs-lookup"><span data-stu-id="e1c2f-195">Interface</span></span>                                                                | <span data-ttu-id="e1c2f-196">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1c2f-196">Description</span></span>                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1c2f-197">**IMFClockStateSink**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-197">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                           | <span data-ttu-id="e1c2f-198">Notifica o apresentador quando o relógio do EVR muda de estado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-198">Notifies the presenter when the EVR's clock changes state.</span></span> <span data-ttu-id="e1c2f-199">Consulte [implementando IMFClockStateSink](#implementing-imfclockstatesink).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-199">See [Implementing IMFClockStateSink](#implementing-imfclockstatesink).</span></span>                                   |
| [<span data-ttu-id="e1c2f-200">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-200">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                   | <span data-ttu-id="e1c2f-201">Fornece uma maneira para o aplicativo e outros componentes no pipeline obterem interfaces do apresentador.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-201">Provides a way for the application and other components in the pipeline to get interfaces from the presenter.</span></span>                                                       |
| [<span data-ttu-id="e1c2f-202">**IMFTopologyServiceLookupClient**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-202">**IMFTopologyServiceLookupClient**</span></span>](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | <span data-ttu-id="e1c2f-203">Permite que o apresentador obtenha interfaces do EVR ou do mixer.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-203">Enables the presenter to get interfaces from the EVR or the mixer.</span></span> <span data-ttu-id="e1c2f-204">Consulte [implementando IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-204">See [Implementing IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient).</span></span> |
| [<span data-ttu-id="e1c2f-205">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-205">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | <span data-ttu-id="e1c2f-206">Garante que o apresentador e o mixer usem tecnologias compatíveis.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-206">Ensures that the presenter and the mixer use compatible technologies.</span></span> <span data-ttu-id="e1c2f-207">Consulte [implementando IMFVideoDeviceID](#implementing-imfvideodeviceid).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-207">See [Implementing IMFVideoDeviceID](#implementing-imfvideodeviceid).</span></span>                          |
| [<span data-ttu-id="e1c2f-208">**IMFVideoPresenter**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-208">**IMFVideoPresenter**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopresenter)                           | <span data-ttu-id="e1c2f-209">Processa mensagens do EVR.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-209">Processes messages from the EVR.</span></span> <span data-ttu-id="e1c2f-210">Consulte [implementando IMFVideoPresenter](#implementing-imfvideopresenter).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-210">See [Implementing IMFVideoPresenter](#implementing-imfvideopresenter).</span></span>                                                             |



 

<span data-ttu-id="e1c2f-211">As seguintes interfaces são opcionais:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-211">The following interfaces are optional:</span></span>



| <span data-ttu-id="e1c2f-212">Interface</span><span class="sxs-lookup"><span data-stu-id="e1c2f-212">Interface</span></span>                                                | <span data-ttu-id="e1c2f-213">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1c2f-213">Description</span></span>                                                                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1c2f-214">**IEVRTrustedVideoPlugin**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-214">**IEVRTrustedVideoPlugin**</span></span>](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | <span data-ttu-id="e1c2f-215">Permite que o apresentador trabalhe com mídia protegida.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-215">Enables the presenter to work with protected media.</span></span> <span data-ttu-id="e1c2f-216">Implemente essa interface se o apresentador for um componente confiável projetado para funcionar no caminho de mídia protegido (PMP).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-216">Implement this interface if your presenter is a trusted component designed to work in the protected media path (PMP).</span></span> |
| [<span data-ttu-id="e1c2f-217">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-217">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | <span data-ttu-id="e1c2f-218">Relata o intervalo de taxas de reprodução que o apresentador dá suporte.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-218">Reports the range of playback rates that the presenter supports.</span></span> <span data-ttu-id="e1c2f-219">Consulte [implementando IMFRateSupport](#implementing-imfratesupport).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-219">See [Implementing IMFRateSupport](#implementing-imfratesupport).</span></span>                                         |
| [<span data-ttu-id="e1c2f-220">**IMFVideoPositionMapper**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-220">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | <span data-ttu-id="e1c2f-221">Mapeia coordenadas no quadro de vídeo de saída para coordenadas no quadro de vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-221">Maps coordinates on the output video frame to coordinates on the input video frame.</span></span>                                                                                       |
| [<span data-ttu-id="e1c2f-222">**IQualProp**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-222">**IQualProp**</span></span>](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop)                         | <span data-ttu-id="e1c2f-223">Relata informações de desempenho.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-223">Reports performance information.</span></span> <span data-ttu-id="e1c2f-224">O EVR usa essas informações para o gerenciamento de controle de qualidade.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-224">The EVR uses this information for quality-control management.</span></span> <span data-ttu-id="e1c2f-225">Essa interface está documentada no SDK do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-225">This interface is documented in the DirectShow SDK.</span></span>                        |



 

<span data-ttu-id="e1c2f-226">Você também pode fornecer interfaces para que o aplicativo se comunique com o apresentador.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-226">You can also provide interfaces for the application to communicate with the presenter.</span></span> <span data-ttu-id="e1c2f-227">O apresentador padrão implementa a interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-227">The standard presenter implements the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface for this purpose.</span></span> <span data-ttu-id="e1c2f-228">Você pode implementar essa interface ou definir a sua própria.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-228">You can implement this interface or define your own.</span></span> <span data-ttu-id="e1c2f-229">O aplicativo obtém interfaces do apresentador chamando [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) no EVR.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-229">The application obtains interfaces from the presenter by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the EVR.</span></span> <span data-ttu-id="e1c2f-230">Quando o GUID do serviço é **MR_VIDEO_RENDER_SERVICE**, o EVR passa a solicitação **GetService** para o apresentador.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-230">When the service GUID is **MR_VIDEO_RENDER_SERVICE**, the EVR passes the **GetService** request to the presenter.</span></span>

### <a name="implementing-imfvideodeviceid"></a><span data-ttu-id="e1c2f-231">Implementando IMFVideoDeviceID</span><span class="sxs-lookup"><span data-stu-id="e1c2f-231">Implementing IMFVideoDeviceID</span></span>

<span data-ttu-id="e1c2f-232">A interface [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) contém um método, [**DeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), que retorna um GUID de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-232">The [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) interface contains one method, [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), which returns a device GUID.</span></span> <span data-ttu-id="e1c2f-233">O GUID do dispositivo garante que o apresentador e o mixer usem tecnologias compatíveis.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-233">The device GUID ensures that the presenter and the mixer use compatible technologies.</span></span> <span data-ttu-id="e1c2f-234">Se os GUIDs do dispositivo não corresponderem, o EVR não será inicializado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-234">If the device GUIDs do not match, the EVR fails to initialize.</span></span>

<span data-ttu-id="e1c2f-235">O mixer e o apresentador padrão usam o Direct3D 9, com o GUID do dispositivo igual a **IID_IDirect3DDevice9**.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-235">The standard mixer and presenter both use Direct3D 9, with the device GUID equal to **IID_IDirect3DDevice9**.</span></span> <span data-ttu-id="e1c2f-236">Se você pretende usar seu apresentador personalizado com o mixer padrão, o GUID do dispositivo do apresentador deve ser **IID_IDirect3DDevice9**.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-236">If you intend to use your custom presenter with the standard mixer, the presenter's device GUID must be **IID_IDirect3DDevice9**.</span></span> <span data-ttu-id="e1c2f-237">Se você substituir ambos os componentes, poderá definir um novo GUID de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-237">If you replace both components, you could define a new device GUID.</span></span> <span data-ttu-id="e1c2f-238">No restante deste artigo, supõe-se que o apresentador usa o Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-238">For the remainder of this article, it is assumed that the presenter uses Direct3D 9.</span></span> <span data-ttu-id="e1c2f-239">Aqui está a implementação padrão de [**DeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid):</span><span class="sxs-lookup"><span data-stu-id="e1c2f-239">Here is the standard implementation of [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid):</span></span>


```C++
HRESULT EVRCustomPresenter::GetDeviceID(IID* pDeviceID)
{
    if (pDeviceID == NULL)
    {
        return E_POINTER;
    }

    *pDeviceID = __uuidof(IDirect3DDevice9);
    return S_OK;
}
```



<span data-ttu-id="e1c2f-240">O método deve ter sucesso mesmo quando o apresentador é desligado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-240">The method should succeed even when the presenter is shut down.</span></span>

### <a name="implementing-imftopologyservicelookupclient"></a><span data-ttu-id="e1c2f-241">Implementando IMFTopologyServiceLookupClient</span><span class="sxs-lookup"><span data-stu-id="e1c2f-241">Implementing IMFTopologyServiceLookupClient</span></span>

<span data-ttu-id="e1c2f-242">A interface [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) permite que o apresentador obtenha ponteiros de interface do EVR e do mixer da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-242">The [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) interface enables the presenter to get interface pointers from the EVR and from the mixer as follows:</span></span>

1.  <span data-ttu-id="e1c2f-243">Quando o EVR Inicializa o apresentador, ele chama o método [**IMFTopologyServiceLookupClient:: InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) do apresentador.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-243">When the EVR initializes the presenter, it calls the presenter's [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method.</span></span> <span data-ttu-id="e1c2f-244">O argumento é um ponteiro para a interface [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) do EVR.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-244">The argument is a pointer to the EVR's [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) interface.</span></span>
2.  <span data-ttu-id="e1c2f-245">O apresentador chama [**IMFTopologyServiceLookup:: LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) para obter ponteiros de interface do EVR ou do mixer.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-245">The presenter calls [**IMFTopologyServiceLookup::LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) to get interface pointers from either the EVR or the mixer.</span></span>

<span data-ttu-id="e1c2f-246">O método [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) é semelhante ao método [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-246">The [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) method is similar to the [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) method.</span></span> <span data-ttu-id="e1c2f-247">Os dois métodos usam um GUID de serviço e um IID (identificador de interface) como entrada, mas **LookupService** retorna uma matriz de ponteiros de interface, enquanto **GetService** retorna um único ponteiro.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-247">Both methods take a service GUID and an interface identifier (IID) as input, but **LookupService** returns an array of interface pointers, while **GetService** returns a single pointer.</span></span> <span data-ttu-id="e1c2f-248">Na prática, no entanto, você sempre pode definir o tamanho da matriz como 1.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-248">In practice, however, you can always set the array size to 1.</span></span> <span data-ttu-id="e1c2f-249">O objeto consultado depende do GUID do serviço:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-249">The object queried depends on the service GUID:</span></span>

-   <span data-ttu-id="e1c2f-250">Se o GUID do serviço for **MR_VIDEO_RENDER_SERVICE**, o EVR será consultado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-250">If the service GUID is **MR_VIDEO_RENDER_SERVICE**, the EVR is queried.</span></span>
-   <span data-ttu-id="e1c2f-251">Se o GUID do serviço for **MR_VIDEO_MIXER_SERVICE**, o mixer será consultado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-251">If the service GUID is **MR_VIDEO_MIXER_SERVICE**, the mixer is queried.</span></span>

<span data-ttu-id="e1c2f-252">Em sua implementação do [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers), obtenha as seguintes interfaces no EVR:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-252">In your implementation of [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers), get the following interfaces from the EVR:</span></span>



| <span data-ttu-id="e1c2f-253">Interface EVR</span><span class="sxs-lookup"><span data-stu-id="e1c2f-253">EVR Interface</span></span>                                | <span data-ttu-id="e1c2f-254">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1c2f-254">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1c2f-255">**IMediaEventSink**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-255">**IMediaEventSink**</span></span>](/windows/win32/api/strmif/nn-strmif-imediaeventsink) | <span data-ttu-id="e1c2f-256">Fornece uma maneira para o apresentador enviar mensagens para o EVR.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-256">Provides a way for the presenter to send messages to the EVR.</span></span> <span data-ttu-id="e1c2f-257">Essa interface é definida no SDK do DirectShow, portanto, as mensagens seguem o padrão para eventos do DirectShow, não Media Foundation eventos.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-257">This interface is defined in the DirectShow SDK, so the messages follow the pattern for DirectShow events, not Media Foundation events.</span></span><br/>                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="e1c2f-258">**IMFClock**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-258">**IMFClock**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclock)                 | <span data-ttu-id="e1c2f-259">Representa o relógio do EVR.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-259">Represents the EVR's clock.</span></span> <span data-ttu-id="e1c2f-260">O apresentador usa essa interface para agendar amostras para apresentação.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-260">The presenter uses this interface to schedule samples for presentation.</span></span> <span data-ttu-id="e1c2f-261">O EVR pode ser executado sem um relógio, portanto, essa interface pode não estar disponível.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-261">The EVR can run without a clock, so this interface might not be available.</span></span> <span data-ttu-id="e1c2f-262">Caso contrário, ignore o código de erro de [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-262">If not, ignore the error code from [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice).</span></span><br/> <span data-ttu-id="e1c2f-263">O relógio também implementa a interface [**IMFTimer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer) .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-263">The clock also implements the [**IMFTimer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer) interface.</span></span> <span data-ttu-id="e1c2f-264">No pipeline de Media Foundation, o relógio implementa a interface [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-264">In the Media Foundation pipeline, the clock implements the [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) interface.</span></span> <span data-ttu-id="e1c2f-265">Ele não implementa essa interface no DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-265">It does not implement this interface in DirectShow.</span></span><br/> |



 

<span data-ttu-id="e1c2f-266">Obtenha as seguintes interfaces do mixer:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-266">Get the following interfaces from the mixer:</span></span>



| <span data-ttu-id="e1c2f-267">Interface do mixer</span><span class="sxs-lookup"><span data-stu-id="e1c2f-267">Mixer Interface</span></span>                              | <span data-ttu-id="e1c2f-268">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1c2f-268">Description</span></span>                                                |
|----------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="e1c2f-269">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-269">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)         | <span data-ttu-id="e1c2f-270">Permite que o apresentador se comunique com o mixer.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-270">Enables the presenter to communicate with the mixer.</span></span>       |
| [<span data-ttu-id="e1c2f-271">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-271">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) | <span data-ttu-id="e1c2f-272">Habilita o apresentador para validar o GUID do dispositivo do mixer.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-272">Enables the presenter to validate the mixer's device GUID.</span></span> |



 

<span data-ttu-id="e1c2f-273">O código a seguir implementa o método [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) :</span><span class="sxs-lookup"><span data-stu-id="e1c2f-273">The following code implements the [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method :</span></span>


```C++
HRESULT EVRCustomPresenter::InitServicePointers(
    IMFTopologyServiceLookup *pLookup
    )
{
    if (pLookup == NULL)
    {
        return E_POINTER;
    }

    HRESULT             hr = S_OK;
    DWORD               dwObjectCount = 0;

    EnterCriticalSection(&m_ObjectLock);

    // Do not allow initializing when playing or paused.
    if (IsActive())
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    // Ask for the clock. Optional, because the EVR might not have a clock.
    dwObjectCount = 1;

    (void)pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL,   // Not used.
        0,                          // Reserved.
        MR_VIDEO_RENDER_SERVICE,    // Service to look up.
        IID_PPV_ARGS(&m_pClock),    // Interface to retrieve.
        &dwObjectCount              // Number of elements retrieved.
        );

    // Ask for the mixer. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_MIXER_SERVICE, IID_PPV_ARGS(&m_pMixer), &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Make sure that we can work with this mixer.
    hr = ConfigureMixer(m_pMixer);
    if (FAILED(hr))
    {
        goto done;
    }

    // Ask for the EVR's event-sink interface. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_RENDER_SERVICE, IID_PPV_ARGS(&m_pMediaEventSink),
        &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Successfully initialized. Set the state to "stopped."
    m_RenderState = RENDER_STATE_STOPPED;

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



<span data-ttu-id="e1c2f-274">Quando os ponteiros de interface obtidos de [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) não são mais válidos, o EVR chama [**IMFTopologyServiceLookupClient:: ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-274">When the interface pointers obtained from [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) are no longer valid, the EVR calls [**IMFTopologyServiceLookupClient::ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers).</span></span> <span data-ttu-id="e1c2f-275">Dentro desse método, libere todos os ponteiros de interface e defina o estado do apresentador como desligar:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-275">Inside this method, release all interface pointers and set the presenter state to shut down:</span></span>


```C++
HRESULT EVRCustomPresenter::ReleaseServicePointers()
{
    // Enter the shut-down state.
    EnterCriticalSection(&m_ObjectLock);

    m_RenderState = RENDER_STATE_SHUTDOWN;

    LeaveCriticalSection(&m_ObjectLock);

    // Flush any samples that were scheduled.
    Flush();

    // Clear the media type and release related resources.
    SetMediaType(NULL);

    // Release all services that were acquired from InitServicePointers.
    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    return S_OK;
}
```



<span data-ttu-id="e1c2f-276">O EVR chama [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) por vários motivos, incluindo:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-276">The EVR calls [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) for various reasons, including:</span></span>

-   <span data-ttu-id="e1c2f-277">Desconectar ou reconectar Pins (DirectShow) ou adicionar ou remover coletores de fluxo (Media Foundation).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-277">Disconnecting or reconnecting pins (DirectShow), or adding or removing stream sinks (Media Foundation).</span></span>
-   <span data-ttu-id="e1c2f-278">Alterando o formato.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-278">Changing format.</span></span>
-   <span data-ttu-id="e1c2f-279">Definindo um novo relógio.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-279">Setting a new clock.</span></span>
-   <span data-ttu-id="e1c2f-280">Desligamento final do EVR.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-280">Final shutdown of the EVR.</span></span>

<span data-ttu-id="e1c2f-281">Durante o tempo de vida do apresentador, o EVR poderia chamar [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) e [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) várias vezes.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-281">During the lifetime of the presenter, the EVR might call [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) and [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) several times.</span></span>

### <a name="implementing-imfvideopresenter"></a><span data-ttu-id="e1c2f-282">Implementando IMFVideoPresenter</span><span class="sxs-lookup"><span data-stu-id="e1c2f-282">Implementing IMFVideoPresenter</span></span>

<span data-ttu-id="e1c2f-283">A interface [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) herda [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) e adiciona dois métodos:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-283">The [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) interface inherits [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) and adds two methods:</span></span>



| <span data-ttu-id="e1c2f-284">Método</span><span class="sxs-lookup"><span data-stu-id="e1c2f-284">Method</span></span>                                                               | <span data-ttu-id="e1c2f-285">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1c2f-285">Description</span></span>                                            |
|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="e1c2f-286">**GetCurrentMediaType**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-286">**GetCurrentMediaType**</span></span>](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) | <span data-ttu-id="e1c2f-287">Retorna o tipo de mídia dos quadros de vídeo compostos.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-287">Returns the media type of the composited video frames.</span></span> |
| [<span data-ttu-id="e1c2f-288">**ProcessMessage**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-288">**ProcessMessage**</span></span>](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage)           | <span data-ttu-id="e1c2f-289">Sinaliza o apresentador para executar várias ações.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-289">Signals the presenter to perform various actions.</span></span>      |



 

<span data-ttu-id="e1c2f-290">O método [**GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) retorna o tipo de mídia do apresentador.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-290">The [**GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) method returns the presenter's media type.</span></span> <span data-ttu-id="e1c2f-291">(Para obter detalhes sobre como definir o tipo de mídia, consulte [negociando formatos](#negotiating-formats).) O tipo de mídia é retornado como um ponteiro de interface [**IMFVideoMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-291">(For details about setting the media type, see [Negotiating Formats](#negotiating-formats).) The media type is returned as an [**IMFVideoMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) interface pointer.</span></span> <span data-ttu-id="e1c2f-292">O exemplo a seguir pressupõe que o apresentador armazena o tipo de mídia como um ponteiro [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-292">The following example assumes that the presenter stores the media type as an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) pointer.</span></span> <span data-ttu-id="e1c2f-293">Para obter a interface **IMFVideoMediaType** do tipo de mídia, chame **QueryInterface**:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-293">To get the **IMFVideoMediaType** interface from the media type, call **QueryInterface**:</span></span>


```C++
HRESULT EVRCustomPresenter::GetCurrentMediaType(
    IMFVideoMediaType** ppMediaType
    )
{
    HRESULT hr = S_OK;

    if (ppMediaType == NULL)
    {
        return E_POINTER;
    }

    *ppMediaType = NULL;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_pMediaType == NULL)
    {
        hr = MF_E_NOT_INITIALIZED;
        goto done;
    }

    hr = m_pMediaType->QueryInterface(IID_PPV_ARGS(ppMediaType));

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



<span data-ttu-id="e1c2f-294">O método [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) é o mecanismo principal para o EVR se comunicar com o apresentador.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-294">The [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) method is the primary mechanism for the EVR to communicate with the presenter.</span></span> <span data-ttu-id="e1c2f-295">As seguintes mensagens são definidas.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-295">The following messages are defined.</span></span> <span data-ttu-id="e1c2f-296">Os detalhes da implementação de cada mensagem são fornecidos no restante deste tópico.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-296">The details of implementing each message are given in the remainder of this topic.</span></span>



| <span data-ttu-id="e1c2f-297">Mensagem</span><span class="sxs-lookup"><span data-stu-id="e1c2f-297">Message</span></span>                                | <span data-ttu-id="e1c2f-298">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1c2f-298">Description</span></span>                                                                                                                                                                                                                                        |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1c2f-299">**MFVP_MESSAGE_INVALIDATEMEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-299">**MFVP_MESSAGE_INVALIDATEMEDIATYPE**</span></span> | <span data-ttu-id="e1c2f-300">O tipo de mídia de saída do mixer é inválido.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-300">The mixer's output media type is invalid.</span></span> <span data-ttu-id="e1c2f-301">O apresentador deve negociar um novo tipo de mídia com o mixer.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-301">The presenter should negotiate a new media type with the mixer.</span></span> <span data-ttu-id="e1c2f-302">Consulte [negociando formatos](#negotiating-formats).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-302">See [Negotiating Formats](#negotiating-formats).</span></span>                                                                                         |
| <span data-ttu-id="e1c2f-303">**MFVP_MESSAGE_BEGINSTREAMING**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-303">**MFVP_MESSAGE_BEGINSTREAMING**</span></span>      | <span data-ttu-id="e1c2f-304">O streaming foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-304">Streaming has started.</span></span> <span data-ttu-id="e1c2f-305">Nenhuma ação específica é exigida por essa mensagem, mas você pode usá-la para alocar recursos.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-305">No particular action is required by this message, but you can use it to allocate resources.</span></span>                                                                                                                                 |
| <span data-ttu-id="e1c2f-306">**MFVP_MESSAGE_ENDSTREAMING**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-306">**MFVP_MESSAGE_ENDSTREAMING**</span></span>        | <span data-ttu-id="e1c2f-307">O streaming foi encerrado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-307">Streaming has ended.</span></span> <span data-ttu-id="e1c2f-308">Libere todos os recursos que você alocou em resposta à mensagem de **MFVP_MESSAGE_BEGINSTREAMING** .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-308">Release any resources that you allocated in response to the **MFVP_MESSAGE_BEGINSTREAMING** message.</span></span>                                                                                                                        |
| <span data-ttu-id="e1c2f-309">**MFVP_MESSAGE_PROCESSINPUTNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-309">**MFVP_MESSAGE_PROCESSINPUTNOTIFY**</span></span>  | <span data-ttu-id="e1c2f-310">O mixer recebeu um novo exemplo de entrada e pode ser capaz de gerar um novo quadro de saída.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-310">The mixer has received a new input sample and might be able to generate a new output frame.</span></span> <span data-ttu-id="e1c2f-311">O apresentador deve chamar [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) no mixer.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-311">The presenter should call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="e1c2f-312">Consulte [processamento de saída](#processing-output).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-312">See [Processing Output](#processing-output).</span></span> |
| <span data-ttu-id="e1c2f-313">**MFVP_MESSAGE_ENDOFSTREAM**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-313">**MFVP_MESSAGE_ENDOFSTREAM**</span></span>         | <span data-ttu-id="e1c2f-314">A apresentação terminou.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-314">The presentation has ended.</span></span> <span data-ttu-id="e1c2f-315">Consulte [fim do fluxo](#end-of-stream).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-315">See [End of Stream](#end-of-stream).</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="e1c2f-316">**MFVP_MESSAGE_FLUSH**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-316">**MFVP_MESSAGE_FLUSH**</span></span>               | <span data-ttu-id="e1c2f-317">O EVR está liberando os dados em seu pipeline de renderização.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-317">The EVR is flushing the data in its rendering pipeline.</span></span> <span data-ttu-id="e1c2f-318">O apresentador deve descartar todos os quadros de vídeo agendados para apresentação.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-318">The presenter should discard any video frames that are scheduled for presentation.</span></span>                                                                                                         |
| <span data-ttu-id="e1c2f-319">**MFVP_MESSAGE_STEP**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-319">**MFVP_MESSAGE_STEP**</span></span>                | <span data-ttu-id="e1c2f-320">Solicita que o apresentador passe a avançar N quadros.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-320">Requests the presenter to step forward N frames.</span></span> <span data-ttu-id="e1c2f-321">O apresentador deve descartar os próximos N-1 quadros e exibir o enésimo quadro.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-321">The presenter should discard the next N-1 frames and display the Nth frame.</span></span> <span data-ttu-id="e1c2f-322">Confira [revisão de quadro](#frame-stepping).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-322">See [Frame Stepping](#frame-stepping).</span></span>                                                                                |
| <span data-ttu-id="e1c2f-323">**MFVP_MESSAGE_CANCELSTEP**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-323">**MFVP_MESSAGE_CANCELSTEP**</span></span>          | <span data-ttu-id="e1c2f-324">Cancela a revisão do quadro.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-324">Cancels frame stepping.</span></span>                                                                                                                                                                                                                            |



 

### <a name="implementing-imfclockstatesink"></a><span data-ttu-id="e1c2f-325">Implementando IMFClockStateSink</span><span class="sxs-lookup"><span data-stu-id="e1c2f-325">Implementing IMFClockStateSink</span></span>

<span data-ttu-id="e1c2f-326">O apresentador deve implementar a interface [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) como parte de sua implementação de [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter), que herda **IMFClockStateSink**.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-326">The presenter must implement the [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) interface as part of its implementation of [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter), which inherits **IMFClockStateSink**.</span></span> <span data-ttu-id="e1c2f-327">O EVR usa essa interface para notificar o apresentador sempre que o relógio do EVR muda de estado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-327">The EVR uses this interface to notify the presenter whenever the EVR's clock changes state.</span></span> <span data-ttu-id="e1c2f-328">Para obter mais informações sobre os Estados do relógio, consulte [relógio de apresentação](presentation-clock.md).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-328">For more information about the clock states, see [Presentation Clock](presentation-clock.md).</span></span>

<span data-ttu-id="e1c2f-329">Aqui estão algumas diretrizes para implementar os métodos nesta interface.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-329">Here are some guidelines for implementing the methods in this interface.</span></span> <span data-ttu-id="e1c2f-330">Todos os métodos devem falhar se o apresentador for desligado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-330">All of the methods should fail if the presenter is shut down.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1c2f-331"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="e1c2f-331"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="e1c2f-332">Defina o estado do apresentador como iniciado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-332">Set the presenter state to started.</span></span></li>
<li><span data-ttu-id="e1c2f-333">Se o <em>llClockStartOffset</em> não for <strong>PRESENTATION_CURRENT_POSITION</strong>, libere a fila de exemplos do apresentador.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-333">If the <em>llClockStartOffset</em> is not <strong>PRESENTATION_CURRENT_POSITION</strong>, flush the presenter's queue of samples.</span></span> <span data-ttu-id="e1c2f-334">(Isso é equivalente a receber uma mensagem de <strong>MFVP_MESSAGE_FLUSH</strong> .)</span><span class="sxs-lookup"><span data-stu-id="e1c2f-334">(This is equivalent to receiving an <strong>MFVP_MESSAGE_FLUSH</strong> message.)</span></span></li>
<li><span data-ttu-id="e1c2f-335">Se uma solicitação de etapa de quadro anterior ainda estiver pendente, processe a solicitação (Confira <a href="#frame-stepping">revisão de quadro</a>).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-335">If a previous frame-step request is still pending, process the request (see <a href="#frame-stepping">Frame Stepping</a>).</span></span> <span data-ttu-id="e1c2f-336">Caso contrário, tente processar a saída do mixer (consulte <a href="#processing-output">processamento de saída</a>.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-336">Otherwise, try to process output from the mixer (see <a href="#processing-output">Processing Output</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1c2f-337"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>OnClockStop</strong></a></span><span class="sxs-lookup"><span data-stu-id="e1c2f-337"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>OnClockStop</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="e1c2f-338">Defina o estado do apresentador como parado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-338">Set the presenter state to stopped.</span></span></li>
<li><span data-ttu-id="e1c2f-339">Libere a fila de exemplos do apresentador.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-339">Flush the presenter's queue of samples.</span></span></li>
<li><span data-ttu-id="e1c2f-340">Cancele qualquer operação de etapa de quadro pendente.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-340">Cancel any pending frame-step operation.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1c2f-341"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>OnClockPause</strong></a></span><span class="sxs-lookup"><span data-stu-id="e1c2f-341"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>OnClockPause</strong></a></span></span></td>
<td><span data-ttu-id="e1c2f-342">Defina o estado do apresentador como em pausa.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-342">Set the presenter state to paused.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1c2f-343"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>OnClockRestart</strong></a></span><span class="sxs-lookup"><span data-stu-id="e1c2f-343"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>OnClockRestart</strong></a></span></span></td>
<td><span data-ttu-id="e1c2f-344">Trate o mesmo que <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a> , mas não libere a fila de amostras.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-344">Treat the same as <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a> but do not flush the queue of samples.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1c2f-345"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>OnClockSetRate</strong></a></span><span class="sxs-lookup"><span data-stu-id="e1c2f-345"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>OnClockSetRate</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="e1c2f-346">Se a taxa estiver mudando de zero para zero, cancele a revisão do quadro.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-346">If the rate is changing from zero to nonzero, cancel frame stepping.</span></span></li>
<li><span data-ttu-id="e1c2f-347">Armazene a nova taxa de clock.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-347">Store the new clock rate.</span></span> <span data-ttu-id="e1c2f-348">A taxa de clock afeta quando exemplos são apresentados.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-348">The clock rate affects when samples are presented.</span></span> <span data-ttu-id="e1c2f-349">Para obter mais informações, consulte <a href="#scheduling-samples">programação de exemplos</a>.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-349">For more information, see <a href="#scheduling-samples">Scheduling Samples</a>.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="implementing-imfratesupport"></a><span data-ttu-id="e1c2f-350">Implementando IMFRateSupport</span><span class="sxs-lookup"><span data-stu-id="e1c2f-350">Implementing IMFRateSupport</span></span>

<span data-ttu-id="e1c2f-351">Para dar suporte a taxas de reprodução diferentes de 1 × velocidade, o apresentador deve implementar a interface [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-351">To support playback rates other than 1× speed, the presenter must implement the [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface.</span></span> <span data-ttu-id="e1c2f-352">Aqui estão algumas diretrizes para implementar os métodos nesta interface.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-352">Here are some guidelines for implementing the methods in this interface.</span></span> <span data-ttu-id="e1c2f-353">Todos os métodos devem falhar depois que o apresentador é desligado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-353">All of the methods should fail after the presenter is shut down.</span></span> <span data-ttu-id="e1c2f-354">Para obter mais informações sobre essa interface, consulte [controle de taxa](rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-354">For more information about this interface, see [Rate Control](rate-control.md).</span></span>



|                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1c2f-355">**GetSlowestRate**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-355">**GetSlowestRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)   | <span data-ttu-id="e1c2f-356">Retorna zero para indicar que não há taxa de reprodução mínima.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-356">Return zero to indicate no minimum playback rate.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="e1c2f-357">**GetFastestRate**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-357">**GetFastestRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)   | <span data-ttu-id="e1c2f-358">Para reprodução não-finada, a taxa de reprodução não deve exceder a taxa de atualização do monitor: taxa máxima de atualização da *taxa*  =   (Hz)/ *taxa de quadros do vídeo* (FPS).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-358">For non-thinned playback, the playback rate should not exceed the refresh rate of the monitor: *maximum rate* = *refresh rate* (Hz) / *video frame rate* (fps).</span></span> <span data-ttu-id="e1c2f-359">A taxa de quadros de vídeo é especificada no tipo de mídia do apresentador.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-359">The video frame rate is specified in the presenter's media type.</span></span> <br/> <span data-ttu-id="e1c2f-360">Para reprodução fina, a taxa de reprodução é desassociada; retornar o valor **FLT_MAX**.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-360">For thinned playback, the playback rate is unbounded; return the value **FLT_MAX**.</span></span> <span data-ttu-id="e1c2f-361">Na prática, a origem e o decodificador serão os fatores limitantes durante a reprodução fina.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-361">In practice, the source and the decoder will be the limiting factors during thinned playback.</span></span> <br/> <span data-ttu-id="e1c2f-362">Para reprodução reversa, retorne o negativo da taxa máxima.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-362">For reverse playback, return the negative of the maximum rate.</span></span><br/> |
| [<span data-ttu-id="e1c2f-363">**IsRateSupported**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-363">**IsRateSupported**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) | <span data-ttu-id="e1c2f-364">Retorne **MF_E_UNSUPPORTED_RATE** se o valor absoluto de *flRate* exceder a taxa de reprodução máxima do apresentador.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-364">Return **MF_E_UNSUPPORTED_RATE** if the absolute value of *flRate* exceeds the presenter's maximum playback rate.</span></span> <span data-ttu-id="e1c2f-365">Calcule a taxa máxima de reprodução conforme descrito para [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-365">Calculate the maximum playback rate as described for [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate).</span></span>                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="e1c2f-366">O exemplo a seguir mostra como implementar o método [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate) :</span><span class="sxs-lookup"><span data-stu-id="e1c2f-366">The following example shows how to implement the [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate) method:</span></span>


```C++
float EVRCustomPresenter::GetMaxRate(BOOL bThin)
{
    // Non-thinned:
    // If we have a valid frame rate and a monitor refresh rate, the maximum
    // playback rate is equal to the refresh rate. Otherwise, the maximum rate
    // is unbounded (FLT_MAX).

    // Thinned: The maximum rate is unbounded.

    float   fMaxRate = FLT_MAX;
    MFRatio fps = { 0, 0 };
    UINT    MonitorRateHz = 0;

    if (!bThin && (m_pMediaType != NULL))
    {
        GetFrameRate(m_pMediaType, &fps);
        MonitorRateHz = m_pD3DPresentEngine->RefreshRate();

        if (fps.Denominator && fps.Numerator && MonitorRateHz)
        {
            // Max Rate = Refresh Rate / Frame Rate
            fMaxRate = (float)MulDiv(
                MonitorRateHz, fps.Denominator, fps.Numerator);
        }
    }

    return fMaxRate;
}
```



<span data-ttu-id="e1c2f-367">O exemplo anterior chama um método auxiliar, GetMaxRate, para calcular a taxa máxima de reprodução de encaminhamento:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-367">The previous example calls a helper method, GetMaxRate, to calculate the maximum forward playback rate:</span></span>

<span data-ttu-id="e1c2f-368">O exemplo a seguir mostra como implementar o método [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) :</span><span class="sxs-lookup"><span data-stu-id="e1c2f-368">The following example shows how to implement the [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) method:</span></span>


```C++
HRESULT EVRCustomPresenter::IsRateSupported(
    BOOL bThin,
    float fRate,
    float *pfNearestSupportedRate
    )
{
    EnterCriticalSection(&m_ObjectLock);

    float   fMaxRate = 0.0f;
    float   fNearestRate = fRate;  // If we support fRate, that is the nearest.

    HRESULT hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Find the maximum forward rate.
    // Note: We have no minimum rate (that is, we support anything down to 0).
    fMaxRate = GetMaxRate(bThin);

    if (fabsf(fRate) > fMaxRate)
    {
        // The (absolute) requested rate exceeds the maximum rate.
        hr = MF_E_UNSUPPORTED_RATE;

        // The nearest supported rate is fMaxRate.
        fNearestRate = fMaxRate;
        if (fRate < 0)
        {
            // Negative for reverse playback.
            fNearestRate = -fNearestRate;
        }
    }

    // Return the nearest supported rate.
    if (pfNearestSupportedRate != NULL)
    {
        *pfNearestSupportedRate = fNearestRate;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



### <a name="sending-events-to-the-evr"></a><span data-ttu-id="e1c2f-369">Enviando eventos para o EVR</span><span class="sxs-lookup"><span data-stu-id="e1c2f-369">Sending Events to the EVR</span></span>

<span data-ttu-id="e1c2f-370">O apresentador deve notificar o EVR de vários eventos.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-370">The presenter must notify the EVR of various events.</span></span> <span data-ttu-id="e1c2f-371">Para fazer isso, ele usa a interface [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) do EVR, obtida quando o EVR chama o método [**IMFTopologyServiceLookupClient:: InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) do apresentador.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-371">To do so, it uses the EVR's [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) interface, obtained when the EVR calls the presenter's [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method.</span></span> <span data-ttu-id="e1c2f-372">(A interface **IMediaEventSink** é originalmente uma interface do DirectShow, mas é usada tanto no DirectShow EVR quanto no Media Foundation.) O código a seguir mostra como enviar um evento para o EVR:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-372">(The **IMediaEventSink** interface is originally a DirectShow interface, but is used in both the DirectShow EVR and the Media Foundation.) The following code shows how to send an event to the EVR:</span></span>


```C++
    // NotifyEvent: Send an event to the EVR through its IMediaEventSink interface.
    void NotifyEvent(long EventCode, LONG_PTR Param1, LONG_PTR Param2)
    {
        if (m_pMediaEventSink)
        {
            m_pMediaEventSink->Notify(EventCode, Param1, Param2);
        }
    }
```



<span data-ttu-id="e1c2f-373">A tabela a seguir lista os eventos que o apresentador envia, juntamente com os parâmetros de evento.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-373">The following table lists the events that the presenter sends, along with the event parameters.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e1c2f-374">Evento</span><span class="sxs-lookup"><span data-stu-id="e1c2f-374">Event</span></span></th>
<th><span data-ttu-id="e1c2f-375">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1c2f-375">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1c2f-376"><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e1c2f-376"><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></span></span></td>
<td><span data-ttu-id="e1c2f-377">O apresentador terminou de renderizar todos os quadros após a mensagem de MFVP_MESSAGE_ENDOFSTREAM.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-377">The presenter has finished rendering all frames after the MFVP_MESSAGE_ENDOFSTREAM message.</span></span><br/>
<ul>
<li><span data-ttu-id="e1c2f-378"><em>Param1</em>: HRESULT que indica o status da operação.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-378"><em>Param1</em>: HRESULT indicating the status of the operation.</span></span></li>
<li><span data-ttu-id="e1c2f-379"><em>Param2</em>: não usado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-379"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="e1c2f-380">Para obter mais informações, consulte <a href="#end-of-stream">end of Stream</a>.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-380">For more information, see <a href="#end-of-stream">End of Stream</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1c2f-381"><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="e1c2f-381"><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></span></span></td>
<td><span data-ttu-id="e1c2f-382">O dispositivo Direct3D foi alterado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-382">The Direct3D device has changed.</span></span><br/>
<ul>
<li><span data-ttu-id="e1c2f-383"><em>Param1</em>: não usado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-383"><em>Param1</em>: Not used.</span></span></li>
<li><span data-ttu-id="e1c2f-384"><em>Param2</em>: não usado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-384"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="e1c2f-385">Para obter mais informações, consulte <a href="#managing-the-direct3d-device">Gerenciando o dispositivo Direct3D</a>.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-385">For more information, see <a href="#managing-the-direct3d-device">Managing the Direct3D Device</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1c2f-386"><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="e1c2f-386"><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></span></span></td>
<td><span data-ttu-id="e1c2f-387">Ocorreu um erro que requer a interrupção do streaming.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-387">An error has occurred that requires streaming to stop.</span></span><br/>
<ul>
<li><span data-ttu-id="e1c2f-388"><em>Param1</em>: <strong>HRESULT</strong> que indica o erro que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-388"><em>Param1</em>: <strong>HRESULT</strong> indicating the error that occurred.</span></span></li>
<li><span data-ttu-id="e1c2f-389"><em>Param2</em>: não usado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-389"><em>Param2</em>: Not used.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1c2f-390"><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="e1c2f-390"><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></span></span></td>
<td><span data-ttu-id="e1c2f-391">Especifica a quantidade de tempo que o apresentador está demorando para renderizar cada quadro.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-391">Specifies the amount of time that the presenter is taking to render each frame.</span></span> <span data-ttu-id="e1c2f-392">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-392">(Optional.)</span></span><br/>
<ul>
<li><span data-ttu-id="e1c2f-393"><em>Param1</em>: ponteiro para um valor de <strong>LONGLONG</strong> constante que contém a quantidade de tempo para processar o quadro, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-393"><em>Param1</em>: Pointer to a constant <strong>LONGLONG</strong> value that contains the amount of time to process the frame, in 100-nanosecond units.</span></span></li>
<li><span data-ttu-id="e1c2f-394"><em>Param2</em>: não usado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-394"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="e1c2f-395">Para obter mais informações, consulte <a href="#processing-output">processamento de saída</a>.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-395">For more information, see <a href="#processing-output">Processing Output</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1c2f-396"><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="e1c2f-396"><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></span></span></td>
<td><span data-ttu-id="e1c2f-397">Especifica o tempo de retardo atual em exemplos de renderização.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-397">Specifies the current lag time in rendering samples.</span></span> <span data-ttu-id="e1c2f-398">Se o valor for positivo, os exemplos estarão atrás da agenda.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-398">If the value is positive, samples are behind schedule.</span></span> <span data-ttu-id="e1c2f-399">Se o valor for negativo, as amostras ficarão à frente da agenda.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-399">If the value is negative, samples are ahead of schedule.</span></span> <span data-ttu-id="e1c2f-400">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-400">(Optional.)</span></span><br/>
<ul>
<li><span data-ttu-id="e1c2f-401"><em>Param1</em>: ponteiro para um valor <strong>LONGLONG</strong> constante que contém o tempo de retardo, em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-401"><em>Param1</em>: Pointer to a constant <strong>LONGLONG</strong> value that contains the lag time, in 100-nanosecond units.</span></span></li>
<li><span data-ttu-id="e1c2f-402"><em>Param2</em>: não usado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-402"><em>Param2</em>: Not used.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1c2f-403"><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></span><span class="sxs-lookup"><span data-stu-id="e1c2f-403"><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></span></span></td>
<td><span data-ttu-id="e1c2f-404">Enviado imediatamente após <strong>EC_STEP_COMPLETE</strong> se a taxa de reprodução for zero.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-404">Sent immediately after <strong>EC_STEP_COMPLETE</strong> if the playback rate is zero.</span></span> <span data-ttu-id="e1c2f-405">Esse evento contém o carimbo de data/hora do quadro que foi exibido.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-405">This event contains the time stamp of the frame that was displayed.</span></span><br/>
<ul>
<li><span data-ttu-id="e1c2f-406"><em>Param1</em>: menores 32 bits do carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-406"><em>Param1</em>: Lower 32 bits of the time stamp.</span></span></li>
<li><span data-ttu-id="e1c2f-407"><em>Param2</em>: 32 bits superiores do carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-407"><em>Param2</em>: Upper 32 bits of the time stamp.</span></span></li>
</ul>
<span data-ttu-id="e1c2f-408">Para obter mais informações, consulte <a href="#frame-stepping">revisão de quadros</a>.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-408">For more information, see <a href="#frame-stepping">Frame Stepping</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1c2f-409"><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e1c2f-409"><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></span></span></td>
<td><span data-ttu-id="e1c2f-410">O apresentador concluiu ou cancelou uma etapa de quadro.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-410">The presenter has completed or canceled a frame step.</span></span><br/>
<ul>
<li><span data-ttu-id="e1c2f-411"><em>Param1</em>: não usado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-411"><em>Param1</em>: Not used.</span></span></li>
<li><span data-ttu-id="e1c2f-412"><em>Param2</em>: não usado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-412"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="e1c2f-413">Para obter mais informações, consulte <a href="#frame-stepping">revisão de quadros</a>.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-413">For more information, see <a href="#frame-stepping">Frame Stepping</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e1c2f-414">Uma versão anterior da documentação descreveu <em>param1</em> incorretamente.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-414">A previous version of the documentation described <em>Param1</em> incorrectly.</span></span> <span data-ttu-id="e1c2f-415">Esse parâmetro não é usado para este evento.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-415">This parameter is not used for this event.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="negotiating-formats"></a><span data-ttu-id="e1c2f-416">Negociando formatos</span><span class="sxs-lookup"><span data-stu-id="e1c2f-416">Negotiating Formats</span></span>

<span data-ttu-id="e1c2f-417">Sempre que o apresentador recebe uma mensagem de **MFVP_MESSAGE_INVALIDATEMEDIATYPE** do EVR, ele deve definir o formato de saída no mixer, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-417">Whenever the presenter receives an **MFVP_MESSAGE_INVALIDATEMEDIATYPE** message from the EVR, it must set the output format on the mixer, as follows:</span></span>

1.  <span data-ttu-id="e1c2f-418">Chame [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) no mixer para obter um possível tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-418">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) on the mixer to get a possible output type.</span></span> <span data-ttu-id="e1c2f-419">Esse tipo descreve um formato que o mixer pode produzir, considerando os fluxos de entrada e os recursos de processamento de vídeo do dispositivo de gráficos.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-419">This type describes a format that the mixer can produce given the input streams and the video processing capabilities of the graphics device.</span></span>
2.  <span data-ttu-id="e1c2f-420">Verifique se o apresentador pode usar esse tipo de mídia como seu formato de renderização.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-420">Check whether the presenter can use this media type as its rendering format.</span></span> <span data-ttu-id="e1c2f-421">Aqui estão algumas coisas a serem verificadas, embora sua implementação possa ter seus próprios requisitos:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-421">Here are some things to check, although your implementation might have its own requirements:</span></span>

    -   <span data-ttu-id="e1c2f-422">O vídeo deve ser descompactado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-422">The video must be uncompressed.</span></span>
    -   <span data-ttu-id="e1c2f-423">O vídeo deve ter apenas quadros progressivos.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-423">The video must have progressive frames only.</span></span> <span data-ttu-id="e1c2f-424">Verifique se o atributo [**MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) é igual a **MFVideoInterlace_Progressive**.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-424">Check that the [**MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) attribute equals **MFVideoInterlace_Progressive**.</span></span>
    -   <span data-ttu-id="e1c2f-425">O formato deve ser compatível com o dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-425">The format must be compatible with the Direct3D device.</span></span>

    <span data-ttu-id="e1c2f-426">Se o tipo não for aceitável, retorne para a etapa 1 e obtenha o próximo tipo proposto do mixer.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-426">If the type is not acceptable, return to step 1 and get the mixer's next proposed type.</span></span>

3.  <span data-ttu-id="e1c2f-427">Crie um novo tipo de mídia que seja um clone do tipo original e, em seguida, altere os seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-427">Create a new media type that is a clone of the original type and then change the following attributes:</span></span>

    -   <span data-ttu-id="e1c2f-428">Defina o atributo [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) igual à largura e altura desejadas para as superfícies do Direct3D que serão alocadas.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-428">Set the [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) attribute equal to the width and height that you want for the Direct3D surfaces you will allocate.</span></span>
    -   <span data-ttu-id="e1c2f-429">Defina o atributo [**MF_MT_PAN_SCAN_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) como **false**.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-429">Set the [**MF_MT_PAN_SCAN_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) attribute to **FALSE**.</span></span>
    -   <span data-ttu-id="e1c2f-430">Defina o atributo [**MF_MT_PIXEL_ASPECT_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) igual ao par da exibição (normalmente 1:1).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-430">Set the [**MF_MT_PIXEL_ASPECT_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) attribute equal to the PAR of the display (typically 1:1).</span></span>
    -   <span data-ttu-id="e1c2f-431">Defina a abertura geométrica (atributo [**MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) ) igual a um retângulo dentro da superfície do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-431">Set the geometric aperture ([**MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) attribute) equal to a rectangle within the Direct3D surface.</span></span> <span data-ttu-id="e1c2f-432">Quando o mixer gera um quadro de saída, ele blits a imagem de origem para esse retângulo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-432">When the mixer generates an output frame, it blits the source image onto this rectangle.</span></span> <span data-ttu-id="e1c2f-433">A abertura geométrica pode ser tão grande quanto a superfície, ou pode ser um subretângulo dentro da superfície.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-433">The geometric aperture can be as large as the surface, or it can be a subrectangle within the surface.</span></span> <span data-ttu-id="e1c2f-434">Para obter mais informações, consulte [retângulos de origem e de destino](#source-and-destination-rectangles).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-434">For more information, see [Source and Destination Rectangles](#source-and-destination-rectangles).</span></span>

4.  <span data-ttu-id="e1c2f-435">Para testar se o mixer aceitará o tipo de saída modificado, chame [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) com o sinalizador **MFT_SET_TYPE_TEST_ONLY** .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-435">To test whether the mixer will accept the modified output type, call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) with the **MFT_SET_TYPE_TEST_ONLY** flag.</span></span> <span data-ttu-id="e1c2f-436">Se o mixer rejeitar o tipo, volte para a etapa 1 e obtenha o próximo tipo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-436">If the mixer rejects the type, go back to step 1 and get the next type.</span></span>
5.  <span data-ttu-id="e1c2f-437">Aloque um pool de superfícies do Direct3D, conforme descrito em [alocando superfícies do Direct3D](#allocating-direct3d-surfaces).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-437">Allocate a pool of Direct3D surfaces, as described in [Allocating Direct3D Surfaces](#allocating-direct3d-surfaces).</span></span> <span data-ttu-id="e1c2f-438">O mixer usará essas superfícies ao desenhar os quadros de vídeo compostos.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-438">The mixer will use these surfaces when it draws the composited video frames.</span></span>
6.  <span data-ttu-id="e1c2f-439">Defina o tipo de saída no mixer chamando [**Setoutputtypetype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) sem sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-439">Set the output type on the mixer by calling [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) with no flags.</span></span> <span data-ttu-id="e1c2f-440">Se a primeira chamada para **Setoutputtypetype** for bem-sucedida na etapa 4, o método deverá ter êxito novamente.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-440">If the first call to **SetOutputType** succeeded in step 4, the method should succeed again.</span></span>

<span data-ttu-id="e1c2f-441">Se o mixer ficar sem tipos, o método [**GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) retornará **MF_E_NO_MORE_TYPES**.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-441">If the mixer runs out of types, the [**GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method returns **MF_E_NO_MORE_TYPES**.</span></span> <span data-ttu-id="e1c2f-442">Se o apresentador não conseguir encontrar um tipo de saída adequado para o mixer, o fluxo não poderá ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-442">If the presenter cannot find a suitable output type for the mixer, the stream cannot be rendered.</span></span> <span data-ttu-id="e1c2f-443">Nesse caso, o DirectShow ou o Media Foundation pode tentar outro formato de fluxo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-443">In that case, DirectShow or Media Foundation might try another stream format.</span></span> <span data-ttu-id="e1c2f-444">Portanto, o apresentador pode receber várias **MFVP_MESSAGE_INVALIDATEMEDIATYPE** mensagens em uma linha até que um tipo válido seja encontrado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-444">Therefore, the presenter might receive several **MFVP_MESSAGE_INVALIDATEMEDIATYPE** messages in a row until a valid type is found.</span></span>

<span data-ttu-id="e1c2f-445">O mixer letterboxes automaticamente o vídeo, levando em conta a taxa de proporção de pixel (PAR) da origem e do destino.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-445">The mixer automatically letterboxes the video, taking into account the pixel aspect ratio (PAR) of the source and destination.</span></span> <span data-ttu-id="e1c2f-446">Para obter melhores resultados, a largura e a altura da superfície e a abertura geométrica devem ser iguais ao tamanho real que você deseja que o vídeo apareça na exibição.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-446">For best results, the surface width and height and the geometric aperture should be equal to the actual size that you want the video to appear on the display.</span></span> <span data-ttu-id="e1c2f-447">A imagem a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-447">The following image illustrates this process.</span></span>

![diagrama mostrando um fram composto que leva a uma superfície do Direct3D, que leva a uma janela](images/b746edca-8830-4c88-aa59-0067b020d4af.gif)

<span data-ttu-id="e1c2f-449">O código a seguir mostra a estrutura de tópicos do processo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-449">The following code shows the outline of the process.</span></span> <span data-ttu-id="e1c2f-450">Algumas das etapas são colocadas em funções auxiliares, os detalhes exatos que dependerão dos requisitos do seu apresentador.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-450">Some of the steps are placed in helper functions, the exact details of which will depend on the requirements of your presenter.</span></span>


```C++
HRESULT EVRCustomPresenter::RenegotiateMediaType()
{
    HRESULT hr = S_OK;
    BOOL bFoundMediaType = FALSE;

    IMFMediaType *pMixerType = NULL;
    IMFMediaType *pOptimalType = NULL;
    IMFVideoMediaType *pVideoType = NULL;

    if (!m_pMixer)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Loop through all of the mixer's proposed output types.
    DWORD iTypeIndex = 0;
    while (!bFoundMediaType && (hr != MF_E_NO_MORE_TYPES))
    {
        SafeRelease(&pMixerType);
        SafeRelease(&pOptimalType);

        // Step 1. Get the next media type supported by mixer.
        hr = m_pMixer->GetOutputAvailableType(0, iTypeIndex++, &pMixerType);
        if (FAILED(hr))
        {
            break;
        }

        // From now on, if anything in this loop fails, try the next type,
        // until we succeed or the mixer runs out of types.

        // Step 2. Check if we support this media type.
        if (SUCCEEDED(hr))
        {
            // Note: None of the modifications that we make later in CreateOptimalVideoType
            // will affect the suitability of the type, at least for us. (Possibly for the mixer.)
            hr = IsMediaTypeSupported(pMixerType);
        }

        // Step 3. Adjust the mixer's type to match our requirements.
        if (SUCCEEDED(hr))
        {
            hr = CreateOptimalVideoType(pMixerType, &pOptimalType);
        }

        // Step 4. Check if the mixer will accept this media type.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, MFT_SET_TYPE_TEST_ONLY);
        }

        // Step 5. Try to set the media type on ourselves.
        if (SUCCEEDED(hr))
        {
            hr = SetMediaType(pOptimalType);
        }

        // Step 6. Set output media type on mixer.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, 0);

            assert(SUCCEEDED(hr)); // This should succeed unless the MFT lied in the previous call.

            // If something went wrong, clear the media type.
            if (FAILED(hr))
            {
                SetMediaType(NULL);
            }
        }

        if (SUCCEEDED(hr))
        {
            bFoundMediaType = TRUE;
        }
    }

    SafeRelease(&pMixerType);
    SafeRelease(&pOptimalType);
    SafeRelease(&pVideoType);

    return hr;
}
```



<span data-ttu-id="e1c2f-451">Para obter mais informações sobre tipos de mídia de vídeo, consulte [tipos de mídia de vídeo](video-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-451">For more information about video media types, see [Video Media Types](video-media-types.md).</span></span>

## <a name="managing-the-direct3d-device"></a><span data-ttu-id="e1c2f-452">Gerenciando o dispositivo Direct3D</span><span class="sxs-lookup"><span data-stu-id="e1c2f-452">Managing the Direct3D Device</span></span>

<span data-ttu-id="e1c2f-453">O apresentador cria o dispositivo Direct3D e manipula qualquer perda de dispositivo durante o streaming.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-453">The presenter creates the Direct3D device and handles any device loss during streaming.</span></span> <span data-ttu-id="e1c2f-454">O apresentador também hospeda o Direct3D Device Manager, que fornece uma maneira para que outros componentes usem o mesmo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-454">The presenter also hosts the Direct3D device manager, which provides a way for other components to use the same device.</span></span> <span data-ttu-id="e1c2f-455">Por exemplo, o mixer usa o dispositivo Direct3D para misturar subfluxos, desentrelaçar e executar ajustes de cores.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-455">For example, the mixer uses the Direct3D device to mix substreams, deinterlace, and perform color adjustments.</span></span> <span data-ttu-id="e1c2f-456">Os decodificadores podem usar o dispositivo Direct3D para decodificação acelerada por vídeo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-456">Decoders can use the Direct3D device for video-accelerated decoding.</span></span> <span data-ttu-id="e1c2f-457">(Para obter mais informações sobre aceleração de vídeo, consulte [aceleração de vídeo do DirectX 2,0](directx-video-acceleration-2-0.md).)</span><span class="sxs-lookup"><span data-stu-id="e1c2f-457">(For more information about video acceleration, see [DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md).)</span></span>

<span data-ttu-id="e1c2f-458">Para configurar o dispositivo Direct3D, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-458">To set up the Direct3D device, perform the following steps:</span></span>

1.  <span data-ttu-id="e1c2f-459">Crie o objeto do Direct3D chamando **Direct3DCreate9** ou **Direct3DCreate9Ex**.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-459">Create the Direct3D object by calling **Direct3DCreate9** or **Direct3DCreate9Ex**.</span></span>
2.  <span data-ttu-id="e1c2f-460">Crie o dispositivo chamando **IDirect3D9:: CreateDevice** ou **IDirect3D9Ex:: CreateDevice**.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-460">Create the device by calling **IDirect3D9::CreateDevice** or **IDirect3D9Ex::CreateDevice**.</span></span>
3.  <span data-ttu-id="e1c2f-461">Crie o Gerenciador de dispositivos chamando [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-461">Create the device manager by calling [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span></span>
4.  <span data-ttu-id="e1c2f-462">Defina o dispositivo no Gerenciador de dispositivos chamando [**IDirect3DDeviceManager9:: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-462">Set the device on the device manager by calling [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span></span>

<span data-ttu-id="e1c2f-463">Se outro componente de pipeline precisar do Gerenciador de dispositivos, ele chamará [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) no EVR, especificando **MR_VIDEO_ACCELERATION_SERVICE** para o GUID do serviço.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-463">If another pipeline component needs the device manager, it calls [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the EVR, specifying **MR_VIDEO_ACCELERATION_SERVICE** for the service GUID.</span></span> <span data-ttu-id="e1c2f-464">O EVR passa a solicitação para o apresentador.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-464">The EVR passes the request to the presenter.</span></span> <span data-ttu-id="e1c2f-465">Depois que o objeto obtém o ponteiro [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) , ele pode obter um identificador para o dispositivo chamando [**IDirect3DDeviceManager9:: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-465">After the object gets the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) pointer, it can get a handle to the device by calling [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle).</span></span> <span data-ttu-id="e1c2f-466">Quando o objeto precisa usar o dispositivo, ele passa o identificador do dispositivo para o método [**IDirect3DDeviceManager9:: LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) , que retorna um ponteiro **IDirect3DDevice9** .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-466">When the object needs to use the device, it passes the device handle to the [**IDirect3DDeviceManager9::LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) method, which returns an **IDirect3DDevice9** pointer.</span></span>

<span data-ttu-id="e1c2f-467">Depois que o dispositivo for criado, se o apresentador destruir o dispositivo e criar um novo, o apresentador deverá chamar [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) novamente.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-467">After the device is created, if the presenter destroys the device and creates a new one, the presenter must call [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) again.</span></span> <span data-ttu-id="e1c2f-468">O método **ResetDevice** invalida quaisquer identificadores de dispositivo existentes, o que faz com que [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) retorne **DXVA2_E_NEW_VIDEO_DEVICE**.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-468">The **ResetDevice** method invalidates any existing device handles, which causes [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) to return **DXVA2_E_NEW_VIDEO_DEVICE**.</span></span> <span data-ttu-id="e1c2f-469">Esse código de erro sinaliza para outros objetos usando o dispositivo que eles devem abrir um novo identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-469">This error code signals to other objects using the device that they should open a new device handle.</span></span> <span data-ttu-id="e1c2f-470">Para obter mais informações sobre como usar o Gerenciador de dispositivos, consulte [Direct3D gerenciador de dispositivos](direct3d-device-manager.md).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-470">For more information about using the device manager, see [Direct3D Device Manager](direct3d-device-manager.md).</span></span>

<span data-ttu-id="e1c2f-471">O apresentador pode criar o dispositivo em modo de janela ou em modo exclusivo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-471">The presenter can create the device in windowed mode or full-screen exclusive mode.</span></span> <span data-ttu-id="e1c2f-472">Para o modo em janela, você deve fornecer uma maneira para o aplicativo especificar a janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-472">For windowed mode, you should provide a way for the application to specify the video window.</span></span> <span data-ttu-id="e1c2f-473">O apresentador padrão implementa o método [**IMFVideoDisplayControl:: SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-473">The standard presenter implements the [**IMFVideoDisplayControl::SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) method for this purpose.</span></span> <span data-ttu-id="e1c2f-474">Você deve criar o dispositivo quando o apresentador é criado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-474">You must create the device when the presenter is first created.</span></span> <span data-ttu-id="e1c2f-475">Normalmente, você não conhecerá todos os parâmetros do dispositivo no momento, como a janela ou o formato de buffer de fundo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-475">Typically, you won't know all of the device parameters at this time, such as the window or the back buffer format.</span></span> <span data-ttu-id="e1c2f-476">Você pode criar um dispositivo temporário e substituí-lo mais tarde&\# ; apenas lembre-se de chamar [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) no Gerenciador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-476">You can create a temporary device and replace it later&\#;just remember to call [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) on the device manager.</span></span>

<span data-ttu-id="e1c2f-477">Se você criar um novo dispositivo ou se chamar **IDirect3DDevice9:: Reset** ou **IDirect3DDevice9Ex:: ResetEx** em um dispositivo existente, envie um evento de [**EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) para o EVR.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-477">If you create a new device, or if you call **IDirect3DDevice9::Reset** or **IDirect3DDevice9Ex::ResetEx** on an existing device, send an [**EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) event to the EVR.</span></span> <span data-ttu-id="e1c2f-478">Esse evento notifica o EVR para renegociar o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-478">This event notifies the EVR to renegotiate the media type.</span></span> <span data-ttu-id="e1c2f-479">O EVR ignora os parâmetros de evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-479">The EVR ignores the event parameters for this event.</span></span>

### <a name="allocating-direct3d-surfaces"></a><span data-ttu-id="e1c2f-480">Alocando superfícies do Direct3D</span><span class="sxs-lookup"><span data-stu-id="e1c2f-480">Allocating Direct3D Surfaces</span></span>

<span data-ttu-id="e1c2f-481">Depois que o apresentador definir o tipo de mídia, ele poderá alocar as superfícies do Direct3D, que o mixer usará para gravar os quadros de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-481">After the presenter sets the media type, it can allocate the Direct3D surfaces, which the mixer will use to write the video frames.</span></span> <span data-ttu-id="e1c2f-482">A superfície deve corresponder ao tipo de mídia do apresentador:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-482">The surface must match the presenter's media type:</span></span>

-   <span data-ttu-id="e1c2f-483">O formato da superfície deve corresponder ao subtipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-483">The surface format must match the media subtype.</span></span> <span data-ttu-id="e1c2f-484">Por exemplo, se o subtipo for **MFVideoFormat_RGB24**, o formato da superfície deverá ser **D3DFMT_X8R8G8B8**.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-484">For example, if the subtype is **MFVideoFormat_RGB24**, the surface format must be **D3DFMT_X8R8G8B8**.</span></span> <span data-ttu-id="e1c2f-485">Para obter mais informações sobre subtipos e formatos de Direct3D, consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-485">For more information about subtypes and Direct3D formats, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>
-   <span data-ttu-id="e1c2f-486">A largura e a altura da superfície devem corresponder às dimensões fornecidas no atributo [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-486">The surface width and height must match the dimensions given in the [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) attribute of the media type.</span></span>

<span data-ttu-id="e1c2f-487">A maneira recomendada para alocar superfícies depende se o apresentador é executado em janela ou em tela inteira.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-487">The recommended way to allocate surfaces depends on whether the presenter runs windowed or full-screen.</span></span>

<span data-ttu-id="e1c2f-488">Se o dispositivo Direct3D estiver em janela, você poderá criar várias cadeias de permuta, cada uma com um único buffer de fundo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-488">If the Direct3D device is windowed, you can create several swap chains, each with a single back buffer.</span></span> <span data-ttu-id="e1c2f-489">Usando essa abordagem, você pode apresentar cada superfície de forma independente, pois a apresentação de uma cadeia de permuta não interferirá nas outras cadeias de permuta.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-489">Using this approach, you can present each surface independently, because presenting one swap chain will not interfere with the other swap chains.</span></span> <span data-ttu-id="e1c2f-490">O mixer pode gravar dados em uma superfície enquanto outra superfície está agendada para apresentação.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-490">The mixer can write data to a surface while another surface is scheduled for presentation.</span></span>

<span data-ttu-id="e1c2f-491">Primeiro, decida quantas cadeias de permuta deseja criar.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-491">First, decide how many swap chains to create.</span></span> <span data-ttu-id="e1c2f-492">É recomendável um mínimo de três.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-492">A minimum of three is recommended.</span></span> <span data-ttu-id="e1c2f-493">Para cada cadeia de permuta, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-493">For each swap chain, do the following:</span></span>

1.  <span data-ttu-id="e1c2f-494">Chame **IDirect3DDevice9:: CreateAdditionalSwapChain** para criar a cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-494">Call **IDirect3DDevice9::CreateAdditionalSwapChain** to create the swap chain.</span></span>
2.  <span data-ttu-id="e1c2f-495">Chame **IDirect3DSwapChain9:: GetBackBuffer** para obter um ponteiro para a superfície de buffer de fundo da cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-495">Call **IDirect3DSwapChain9::GetBackBuffer** to get a pointer to the swap chain's back buffer surface.</span></span>
3.  <span data-ttu-id="e1c2f-496">Chame [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) e transmita um ponteiro para a superfície.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-496">Call [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) and pass in a pointer to the surface.</span></span> <span data-ttu-id="e1c2f-497">Essa função retorna um ponteiro para um objeto de exemplo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-497">This function returns a pointer to a video sample object.</span></span> <span data-ttu-id="e1c2f-498">O objeto de exemplo de vídeo implementa a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) e o apresentador usa essa interface para entregar a superfície ao mixer quando o apresentador chama o método [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) do mixer.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-498">The video sample object implements the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, and the presenter uses this interface to deliver the surface to the mixer when the presenter calls the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method.</span></span> <span data-ttu-id="e1c2f-499">Para obter mais informações sobre o objeto de exemplo de vídeo, consulte [amostras de vídeo](video-samples.md).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-499">For more information about the video sample object, see [Video Samples](video-samples.md).</span></span>
4.  <span data-ttu-id="e1c2f-500">Armazene o ponteiro [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) em uma fila.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-500">Store the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointer in a queue.</span></span> <span data-ttu-id="e1c2f-501">O apresentador extrairá amostras desta fila durante o processamento, conforme descrito em [processando a saída](#processing-output).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-501">The presenter will pull samples from this queue during processing as described in [Processing Output](#processing-output).</span></span>
5.  <span data-ttu-id="e1c2f-502">Mantenha uma referência ao ponteiro **IDirect3DSwapChain9** para que a cadeia de permuta não seja liberada.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-502">Keep a reference to the **IDirect3DSwapChain9** pointer so the swap chain is not released.</span></span>

<span data-ttu-id="e1c2f-503">No modo de tela inteira exclusiva, o dispositivo não pode ter mais de uma cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-503">In full-screen exclusive mode, the device cannot have more than one swap chain.</span></span> <span data-ttu-id="e1c2f-504">Essa cadeia de permuta é criada implicitamente quando você cria o dispositivo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-504">This swap chain is created implicitly when you create the full-screen device.</span></span> <span data-ttu-id="e1c2f-505">A cadeia de permuta pode ter mais de um buffer de fundo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-505">The swap chain can have more than one back buffer.</span></span> <span data-ttu-id="e1c2f-506">No entanto, infelizmente, se você apresentar um buffer de fundo enquanto grava em outro buffer de fundo na mesma cadeia de permuta, não há uma maneira fácil de coordenar as duas operações.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-506">Unfortunately, however, if you present one back buffer while you write to another back buffer in the same swap chain, there is no easy way to coordinate the two operations.</span></span> <span data-ttu-id="e1c2f-507">Isso ocorre devido à maneira como o Direct3D implementa a inversão da superfície.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-507">This is because of the way Direct3D implements surface flipping.</span></span> <span data-ttu-id="e1c2f-508">Quando você chama o presente, o driver de gráficos atualiza os ponteiros de superfície na memória gráfica.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-508">When you call Present, the graphics driver updates the surface pointers in graphics memory.</span></span> <span data-ttu-id="e1c2f-509">Se você estiver mantendo quaisquer ponteiros **IDirect3DSurface9** quando você chamar **Present**, eles apontarão para buffers diferentes depois que a chamada **atual** for retornada.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-509">If you are holding any **IDirect3DSurface9** pointers when you call **Present**, they will point to different buffers after the **Present** call returns.</span></span>

<span data-ttu-id="e1c2f-510">A opção mais simples é criar um exemplo de vídeo para a cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-510">The simplest option is to create one video sample for the swap chain.</span></span> <span data-ttu-id="e1c2f-511">Se você escolher essa opção, siga as mesmas etapas fornecidas para o modo de janela.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-511">If you choose this option, follow the same steps given for windowed mode.</span></span> <span data-ttu-id="e1c2f-512">A única diferença é que a fila de exemplo contém um único exemplo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-512">The only difference is that the sample queue contains a single video sample.</span></span> <span data-ttu-id="e1c2f-513">Outra opção é criar superfícies fora da tela e, em seguida, blit-las ao buffer de fundo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-513">Another option is to create offscreen surfaces and then blit them to the back buffer.</span></span> <span data-ttu-id="e1c2f-514">As superfícies que você cria devem oferecer suporte ao método [**IDirectXVideoProcessor:: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) , que o mixer usa para compor os quadros de saída.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-514">The surfaces that you create must support the [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) method, which the mixer uses to composite the output frames.</span></span>

### <a name="tracking-samples"></a><span data-ttu-id="e1c2f-515">Amostras de rastreamento</span><span class="sxs-lookup"><span data-stu-id="e1c2f-515">Tracking Samples</span></span>

<span data-ttu-id="e1c2f-516">Quando o apresentador primeiro aloca os exemplos de vídeo, ele os coloca em uma fila.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-516">When the presenter first allocates the video samples, it places them in a queue.</span></span> <span data-ttu-id="e1c2f-517">O apresentador se baseia nessa fila sempre que precisa obter um novo quadro do mixer.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-517">The presenter draws from this queue whenever it needs to get a new frame from the mixer.</span></span> <span data-ttu-id="e1c2f-518">Depois que o mixer gera o quadro, o apresentador move o exemplo para uma segunda fila.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-518">After the mixer outputs the frame, the presenter moves the sample into a second queue.</span></span> <span data-ttu-id="e1c2f-519">A segunda fila é para exemplos que estão aguardando seus horários de apresentação agendados.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-519">The second queue is for samples that are waiting for their scheduled presentation times.</span></span>

<span data-ttu-id="e1c2f-520">Para facilitar o acompanhamento do status de cada exemplo, o objeto de exemplo de vídeo implementa a interface [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-520">To make it easier to track the status of each sample, the video sample object implements the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) interface.</span></span> <span data-ttu-id="e1c2f-521">Você pode usar essa interface da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-521">You can use this interface as follows:</span></span>

1.  <span data-ttu-id="e1c2f-522">Implemente a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) em seu apresentador.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-522">Implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface in your presenter.</span></span>
2.  <span data-ttu-id="e1c2f-523">Antes de colocar um exemplo na fila agendada, consulte o objeto de exemplo de vídeo para a interface [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-523">Before you place a sample in the scheduled queue, query the video sample object for the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) interface.</span></span>

3.  <span data-ttu-id="e1c2f-524">Chame [**IMFTrackedSample:: Setalocador**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) com um ponteiro para sua interface de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-524">Call [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) with a pointer to your callback interface.</span></span>
4.  <span data-ttu-id="e1c2f-525">Quando o exemplo estiver pronto para apresentação, remova-o da fila agendada, apresente-o e libere todas as referências ao exemplo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-525">When the sample is ready for presentation, remove it from the scheduled queue, present it, and release all references to the sample.</span></span>
5.  <span data-ttu-id="e1c2f-526">O exemplo invoca o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-526">The sample invokes the callback.</span></span> <span data-ttu-id="e1c2f-527">(O objeto de exemplo não é excluído nesse caso porque ele contém uma contagem de referência em si até que o retorno de chamada seja invocado.)</span><span class="sxs-lookup"><span data-stu-id="e1c2f-527">(The sample object is not deleted in this case because it holds a reference count on itself until the callback is invoked.)</span></span>
6.  <span data-ttu-id="e1c2f-528">Dentro do retorno de chamada, retorne o exemplo para a fila disponível.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-528">Inside the callback, return the sample to the available queue.</span></span>

<span data-ttu-id="e1c2f-529">Um apresentador não é necessário para usar o [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) para rastrear exemplos; Você pode implementar qualquer técnica que funcione melhor para seu design.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-529">A presenter is not required to use [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) to track samples; you can implement any technique that works best for your design.</span></span> <span data-ttu-id="e1c2f-530">Uma vantagem do **IMFTrackedSample** é que você pode mover as funções de agendamento e renderização do apresentador em objetos auxiliares, e esses objetos não precisam de nenhum mecanismo especial para chamar de volta para o apresentador quando lançam amostras de vídeo porque o objeto de exemplo fornece esse mecanismo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-530">One advantage of **IMFTrackedSample** is that you can move the presenter's scheduling and rendering functions into helper objects, and these objects do not need any special mechanism for calling back to the presenter when they release video samples because the sample object provides that mechanism.</span></span>

<span data-ttu-id="e1c2f-531">O código a seguir mostra como definir o retorno de chamada:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-531">The following code shows how to set the callback:</span></span>


```C++
HRESULT EVRCustomPresenter::TrackSample(IMFSample *pSample)
{
    IMFTrackedSample *pTracked = NULL;

    HRESULT hr = pSample->QueryInterface(IID_PPV_ARGS(&pTracked));

    if (SUCCEEDED(hr))
    {
        hr = pTracked->SetAllocator(&m_SampleFreeCB, NULL);
    }

    SafeRelease(&pTracked);
    return hr;
}
```



<span data-ttu-id="e1c2f-532">No retorno de chamada, chame [**IMFAsyncResult:: GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) no objeto de resultado assíncrono para recuperar um ponteiro para o exemplo:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-532">In the callback, call [**IMFAsyncResult::GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) on the asynchronous result object to retrieve a pointer to the sample:</span></span>


```C++
HRESULT EVRCustomPresenter::OnSampleFree(IMFAsyncResult *pResult)
{
    IUnknown *pObject = NULL;
    IMFSample *pSample = NULL;
    IUnknown *pUnk = NULL;

    // Get the sample from the async result object.
    HRESULT hr = pResult->GetObject(&pObject);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pObject->QueryInterface(IID_PPV_ARGS(&pSample));
    if (FAILED(hr))
    {
        goto done;
    }

    // If this sample was submitted for a frame-step, the frame step operation
    // is complete.

    if (m_FrameStep.state == FRAMESTEP_SCHEDULED)
    {
        // Query the sample for IUnknown and compare it to our cached value.
        hr = pSample->QueryInterface(IID_PPV_ARGS(&pUnk));
        if (FAILED(hr))
        {
            goto done;
        }

        if (m_FrameStep.pSampleNoRef == (DWORD_PTR)pUnk)
        {
            // Notify the EVR.
            hr = CompleteFrameStep(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Note: Although pObject is also an IUnknown pointer, it is not
        // guaranteed to be the exact pointer value returned through
        // QueryInterface. Therefore, the second QueryInterface call is
        // required.
    }

    /*** Begin lock **_/

    EnterCriticalSection(&m_ObjectLock);

    UINT32 token = MFGetAttributeUINT32(
        pSample, MFSamplePresenter_SampleCounter, (UINT32)-1);

    if (token == m_TokenCounter)
    {
        // Return the sample to the sample pool.
        hr = m_SamplePool.ReturnSample(pSample);
        if (SUCCEEDED(hr))
        {
            // A free sample is available. Process more data if possible.
            (void)ProcessOutputLoop();
        }
    }

    LeaveCriticalSection(&m_ObjectLock);

    /_*_ End lock _*_/

done:
    if (FAILED(hr))
    {
        NotifyEvent(EC_ERRORABORT, hr, 0);
    }
    SafeRelease(&pObject);
    SafeRelease(&pSample);
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="processing-output"></a><span data-ttu-id="e1c2f-533">Processando saída</span><span class="sxs-lookup"><span data-stu-id="e1c2f-533">Processing Output</span></span>

<span data-ttu-id="e1c2f-534">Sempre que o mixer recebe um novo exemplo de entrada, o EVR envia uma mensagem _ *MFVP_MESSAGE_PROCESSINPUTNOTIFY*\* para o apresentador.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-534">Whenever the mixer receives a new input sample, the EVR sends an _ *MFVP_MESSAGE_PROCESSINPUTNOTIFY*\* message to the presenter.</span></span> <span data-ttu-id="e1c2f-535">Essa mensagem indica que o mixer pode ter um novo quadro de vídeo a ser entregue.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-535">This message indicates that the mixer might have a new video frame to deliver.</span></span> <span data-ttu-id="e1c2f-536">Em resposta, o apresentador chama [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) no mixer.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-536">In response, the presenter calls [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="e1c2f-537">Se o método tiver sucesso, o apresentador agendará a amostra para apresentação.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-537">If the method succeeds, the presenter schedules the sample for presentation.</span></span>

<span data-ttu-id="e1c2f-538">Para obter a saída do mixer, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-538">To get output from the mixer, perform the following steps:</span></span>

1.  <span data-ttu-id="e1c2f-539">Verifique o estado do relógio.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-539">Check the clock state.</span></span> <span data-ttu-id="e1c2f-540">Se o relógio estiver em pausa, ignore a **MFVP_MESSAGE_PROCESSINPUTNOTIFY** mensagem, a menos que este seja o primeiro quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-540">If the clock is paused, ignore the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message unless this is the first video frame.</span></span> <span data-ttu-id="e1c2f-541">Se o relógio estiver em execução ou se este for o primeiro quadro de vídeo, continue.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-541">If the clock is running, or if this is the first video frame, continue.</span></span>
2.  <span data-ttu-id="e1c2f-542">Obtenha um exemplo da fila de exemplos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-542">Get a sample from the queue of available samples.</span></span> <span data-ttu-id="e1c2f-543">Se a fila estiver vazia, significa que todos os exemplos alocados estão atualmente agendados para apresentação.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-543">If the queue is empty, it means that all allocated samples are currently scheduled for presenting.</span></span> <span data-ttu-id="e1c2f-544">Nesse caso, ignore a mensagem **MFVP_MESSAGE_PROCESSINPUTNOTIFYda** neste momento.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-544">In that case, ignore the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message at this time.</span></span> <span data-ttu-id="e1c2f-545">Quando o próximo exemplo for disponibilizado, repita as etapas listadas aqui.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-545">When the next sample becomes available, repeat the steps listed here.</span></span>
3.  <span data-ttu-id="e1c2f-546">(Opcional.) Se o relógio estiver disponível, obtenha a hora do relógio atual (*T1*) chamando [**IMFClock:: GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-546">(Optional.) If the clock is available, get the current clock time (*T1*) by calling [**IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span></span>
4.  <span data-ttu-id="e1c2f-547">Chame [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) no mixer.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-547">Call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="e1c2f-548">Se **ProcessOutput** tiver sucesso, o exemplo conterá um quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-548">If **ProcessOutput** succeeds, the sample contains a video frame.</span></span> <span data-ttu-id="e1c2f-549">Se o método falhar, verifique o código de retorno.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-549">If the method fails, check the return code.</span></span> <span data-ttu-id="e1c2f-550">Os seguintes códigos de erro de **ProcessOutput** não são falhas críticas:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-550">The following error codes from **ProcessOutput** are not critical failures:</span></span>

    

    | <span data-ttu-id="e1c2f-551">Código do erro</span><span class="sxs-lookup"><span data-stu-id="e1c2f-551">Error code</span></span>                              | <span data-ttu-id="e1c2f-552">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1c2f-552">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
    |-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="e1c2f-553">**MF_E_TRANSFORM_NEED_MORE_INPUT**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-553">**MF_E_TRANSFORM_NEED_MORE_INPUT**</span></span> | <span data-ttu-id="e1c2f-554">O mixer precisa de mais entrada para poder produzir um novo quadro de saída.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-554">The mixer needs more input before it can produce a new output frame.</span></span><br/> <span data-ttu-id="e1c2f-555">Se você receber esse código de erro, verifique se o EVR atingiu o final do fluxo e respondeu de acordo, conforme descrito no [final do fluxo](#end-of-stream).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-555">If you get this error code, check whether the EVR has reached the end of the stream and respond accordingly, as described in [End of Stream](#end-of-stream).</span></span> <span data-ttu-id="e1c2f-556">Caso contrário, ignore esta mensagem de **MF_E_TRANSFORM_NEED_MORE_INPUT** .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-556">Otherwise, ignore this **MF_E_TRANSFORM_NEED_MORE_INPUT** message.</span></span> <span data-ttu-id="e1c2f-557">O EVR enviará outro quando o mixer receber mais entradas.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-557">The EVR will send another one when the mixer gets more input.</span></span><br/> |
    | <span data-ttu-id="e1c2f-558">**MF_E_TRANSFORM_STREAM_CHANGE**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-558">**MF_E_TRANSFORM_STREAM_CHANGE**</span></span>    | <span data-ttu-id="e1c2f-559">O tipo de saída do mixer se tornou inválido, possivelmente devido a uma alteração de formato upstream.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-559">The mixer's output type has become invalid, possibly due to a format change upstream.</span></span><br/> <span data-ttu-id="e1c2f-560">Se você receber esse código de erro, defina o tipo de mídia do apresentador como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-560">If you get this error code, set the presenter's media type to **NULL**.</span></span> <span data-ttu-id="e1c2f-561">O EVR solicitará um novo formato.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-561">The EVR will request a new format.</span></span><br/>                                                                                                                                                                         |
    | <span data-ttu-id="e1c2f-562">**MF_E_TRANSFORM_TYPE_NOT_SET**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-562">**MF_E_TRANSFORM_TYPE_NOT_SET**</span></span>    | <span data-ttu-id="e1c2f-563">O mixer requer um novo tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-563">The mixer requires a new media type.</span></span><br/> <span data-ttu-id="e1c2f-564">Se você receber esse código de erro, renegocie o tipo de saída do mixer conforme descrito em [negociando formatos](#negotiating-formats).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-564">If you get this error code, renegotiate the mixer's output type as described in [Negotiating Formats](#negotiating-formats).</span></span><br/>                                                                                                                                                                                                        |

    

     

    <span data-ttu-id="e1c2f-565">Se [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) tiver sucesso, continue.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-565">If [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) succeeds, continue.</span></span>

5.  <span data-ttu-id="e1c2f-566">(Opcional.) Se o relógio estiver disponível, obtenha a hora do relógio atual (*T2*).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-566">(Optional.) If the clock is available, get the current clock time (*T2*).</span></span> <span data-ttu-id="e1c2f-567">A quantidade de latência introduzida pelo mixer é (*T2*  -  *T1*).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-567">The amount of latency introduced by the mixer is (*T2* - *T1*).</span></span> <span data-ttu-id="e1c2f-568">Envie um evento de **EC_PROCESSING_LATENCY** com esse valor para o EVR.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-568">Send an **EC_PROCESSING_LATENCY** event with this value to the EVR.</span></span> <span data-ttu-id="e1c2f-569">O EVR usa esse valor para controle de qualidade.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-569">The EVR uses this value for quality control.</span></span> <span data-ttu-id="e1c2f-570">Se nenhum relógio estiver disponível, não haverá motivo para enviar o evento de **EC_PROCESSING_LATENCY** .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-570">If no clock is available, there is no reason to send the **EC_PROCESSING_LATENCY** event.</span></span>
6.  <span data-ttu-id="e1c2f-571">(Opcional.) Consulte o exemplo para [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) e chame [**IMFTrackedSample:: setalocador**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) conforme descrito em [exemplos de rastreamento](#tracking-samples).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-571">(Optional.) Query the sample for [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) and call [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) as described in [Tracking Samples](#tracking-samples).</span></span>
7.  <span data-ttu-id="e1c2f-572">Agendar o exemplo para apresentação.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-572">Schedule the sample for presentation.</span></span>

<span data-ttu-id="e1c2f-573">Essa sequência de etapas pode terminar antes que o apresentador obtenha qualquer saída do mixer.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-573">This sequence of steps can terminate before the presenter gets any output from the mixer.</span></span> <span data-ttu-id="e1c2f-574">Para garantir que nenhuma solicitação seja descartada, você deve repetir as mesmas etapas quando ocorrer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-574">To ensure that no requests are dropped, you should repeat the same steps when the following occur:</span></span>

-   <span data-ttu-id="e1c2f-575">O método [**IMFClockStateSink:: OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) ou **IMFClockStateSink:: OnClockStart** do apresentador é chamado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-575">The presenter's [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) or **IMFClockStateSink::OnClockStart** method is called.</span></span> <span data-ttu-id="e1c2f-576">Isso manipula o caso em que o mixer ignora a entrada porque o relógio está em pausa (etapa 1).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-576">This handles the case where the mixer ignores input because the clock is paused (step 1).</span></span>
-   <span data-ttu-id="e1c2f-577">O retorno de chamada [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) é invocado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-577">The [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback is invoked.</span></span> <span data-ttu-id="e1c2f-578">Isso manipula o caso em que o mixer recebe a entrada, mas todas as amostras de vídeo do apresentador estão em uso (etapa 2).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-578">This handles the case where the mixer receives input but all of the presenter's video samples are in use (step 2).</span></span>

<span data-ttu-id="e1c2f-579">Os vários exemplos de código a seguir mostram essas etapas mais detalhadamente.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-579">The next several code examples show these steps in more detail.</span></span> <span data-ttu-id="e1c2f-580">O apresentador chama o `ProcessInputNotify` método (mostrado no exemplo a seguir) quando ele obtém a mensagem de **MFVP_MESSAGE_PROCESSINPUTNOTIFY** .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-580">The presenter calls the `ProcessInputNotify` method (shown in the following example) when it gets the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message.</span></span>


```C++
//-----------------------------------------------------------------------------
// ProcessInputNotify
//
// Attempts to get a new output sample from the mixer.
//
// This method is called when the EVR sends an MFVP_MESSAGE_PROCESSINPUTNOTIFY
// message, which indicates that the mixer has a new input sample.
//
// Note: If there are multiple input streams, the mixer might not deliver an
// output sample for every input sample.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessInputNotify()
{
    HRESULT hr = S_OK;

    // Set the flag that says the mixer has a new sample.
    m_bSampleNotify = TRUE;

    if (m_pMediaType == NULL)
    {
        // We don't have a valid media type yet.
        hr = MF_E_TRANSFORM_TYPE_NOT_SET;
    }
    else
    {
        // Try to process an output sample.
        ProcessOutputLoop();
    }
    return hr;
}
```



<span data-ttu-id="e1c2f-581">Esse `ProcessInputNotify` método define um sinalizador booliano para registrar o fato de que o mixer tem nova entrada.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-581">This `ProcessInputNotify` method sets a Boolean flag to record the fact that the mixer has new input.</span></span> <span data-ttu-id="e1c2f-582">Em seguida, ele chama o `ProcessOutputLoop` método, mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-582">Then it calls the `ProcessOutputLoop` method, shown in the next example.</span></span> <span data-ttu-id="e1c2f-583">Esse método tenta extrair o máximo de amostras possível do mixer:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-583">This method attempts to pull as many samples as possible from the mixer:</span></span>


```C++
void EVRCustomPresenter::ProcessOutputLoop()
{
    HRESULT hr = S_OK;

    // Process as many samples as possible.
    while (hr == S_OK)
    {
        // If the mixer doesn't have a new input sample, break from the loop.
        if (!m_bSampleNotify)
        {
            hr = MF_E_TRANSFORM_NEED_MORE_INPUT;
            break;
        }

        // Try to process a sample.
        hr = ProcessOutput();

        // NOTE: ProcessOutput can return S_FALSE to indicate it did not
        // process a sample. If so, break out of the loop.
    }

    if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
    {
        // The mixer has run out of input data. Check for end-of-stream.
        CheckEndOfStream();
    }
}
```



<span data-ttu-id="e1c2f-584">O `ProcessOutput` método, mostrado no exemplo a seguir, tenta obter um único quadro de vídeo do mixer.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-584">The `ProcessOutput` method, shown in the next example, attempts to get a single video frame from the mixer.</span></span> <span data-ttu-id="e1c2f-585">Se nenhum quadro de vídeo estiver disponível, `ProcessSample` o retornará S_FALSE ou um código de erro, que interrompe o loop `ProcessOutputLoop` .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-585">If no video frame is available, `ProcessSample` returns S_FALSE or an error code, either of which interrupts the loop in `ProcessOutputLoop`.</span></span> <span data-ttu-id="e1c2f-586">A maior parte do trabalho é feita dentro do `ProcessOutput` método:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-586">Most of the work is done inside the `ProcessOutput` method:</span></span>


```C++
//-----------------------------------------------------------------------------
// ProcessOutput
//
// Attempts to get a new output sample from the mixer.
//
// Called in two situations:
// (1) ProcessOutputLoop, if the mixer has a new input sample.
// (2) Repainting the last frame.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessOutput()
{
    assert(m_bSampleNotify || m_bRepaint);  // See note above.

    HRESULT     hr = S_OK;
    DWORD       dwStatus = 0;
    LONGLONG    mixerStartTime = 0, mixerEndTime = 0;
    MFTIME      systemTime = 0;
    BOOL        bRepaint = m_bRepaint; // Temporarily store this state flag.

    MFT_OUTPUT_DATA_BUFFER dataBuffer;
    ZeroMemory(&dataBuffer, sizeof(dataBuffer));

    IMFSample *pSample = NULL;

    // If the clock is not running, we present the first sample,
    // and then don't present any more until the clock starts.

    if ((m_RenderState != RENDER_STATE_STARTED) &&  // Not running.
         !m_bRepaint &&             // Not a repaint request.
         m_bPrerolled               // At least one sample has been presented.
         )
    {
        return S_FALSE;
    }

    // Make sure we have a pointer to the mixer.
    if (m_pMixer == NULL)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Try to get a free sample from the video sample pool.
    hr = m_SamplePool.GetSample(&pSample);
    if (hr == MF_E_SAMPLEALLOCATOR_EMPTY)
    {
        // No free samples. Try again when a sample is released.
        return S_FALSE;
    }
    else if (FAILED(hr))
    {
        return hr;
    }

    // From now on, we have a valid video sample pointer, where the mixer will
    // write the video data.
    assert(pSample != NULL);

    // (If the following assertion fires, it means we are not managing the sample pool correctly.)
    assert(MFGetAttributeUINT32(pSample, MFSamplePresenter_SampleCounter, (UINT32)-1) == m_TokenCounter);

    if (m_bRepaint)
    {
        // Repaint request. Ask the mixer for the most recent sample.
        SetDesiredSampleTime(
            pSample,
            m_scheduler.LastSampleTime(),
            m_scheduler.FrameDuration()
            );

        m_bRepaint = FALSE; // OK to clear this flag now.
    }
    else
    {
        // Not a repaint request. Clear the desired sample time; the mixer will
        // give us the next frame in the stream.
        ClearDesiredSampleTime(pSample);

        if (m_pClock)
        {
            // Latency: Record the starting time for ProcessOutput.
            (void)m_pClock->GetCorrelatedTime(0, &mixerStartTime, &systemTime);
        }
    }

    // Now we are ready to get an output sample from the mixer.
    dataBuffer.dwStreamID = 0;
    dataBuffer.pSample = pSample;
    dataBuffer.dwStatus = 0;

    hr = m_pMixer->ProcessOutput(0, 1, &dataBuffer, &dwStatus);

    if (FAILED(hr))
    {
        // Return the sample to the pool.
        HRESULT hr2 = m_SamplePool.ReturnSample(pSample);
        if (FAILED(hr2))
        {
            hr = hr2;
            goto done;
        }
        // Handle some known error codes from ProcessOutput.
        if (hr == MF_E_TRANSFORM_TYPE_NOT_SET)
        {
            // The mixer's format is not set. Negotiate a new format.
            hr = RenegotiateMediaType();
        }
        else if (hr == MF_E_TRANSFORM_STREAM_CHANGE)
        {
            // There was a dynamic media type change. Clear our media type.
            SetMediaType(NULL);
        }
        else if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
        {
            // The mixer needs more input.
            // We have to wait for the mixer to get more input.
            m_bSampleNotify = FALSE;
        }
    }
    else
    {
        // We got an output sample from the mixer.

        if (m_pClock && !bRepaint)
        {
            // Latency: Record the ending time for the ProcessOutput operation,
            // and notify the EVR of the latency.

            (void)m_pClock->GetCorrelatedTime(0, &mixerEndTime, &systemTime);

            LONGLONG latencyTime = mixerEndTime - mixerStartTime;
            NotifyEvent(EC_PROCESSING_LATENCY, (LONG_PTR)&latencyTime, 0);
        }

        // Set up notification for when the sample is released.
        hr = TrackSample(pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Schedule the sample.
        if ((m_FrameStep.state == FRAMESTEP_NONE) || bRepaint)
        {
            hr = DeliverSample(pSample, bRepaint);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else
        {
            // We are frame-stepping (and this is not a repaint request).
            hr = DeliverFrameStepSample(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        m_bPrerolled = TRUE; // We have presented at least one sample now.
    }

done:
    SafeRelease(&pSample);

    // Important: Release any events returned from the ProcessOutput method.
    SafeRelease(&dataBuffer.pEvents);
    return hr;
}
```



<span data-ttu-id="e1c2f-587">Alguns comentários sobre este exemplo:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-587">Some remarks about this example:</span></span>

-   <span data-ttu-id="e1c2f-588">Pressupõe-se que a variável *m_SamplePool* seja um objeto de coleção que contém a fila de exemplos de vídeo disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-588">The *m_SamplePool* variable is assumed to be a collection object that holds the queue of available video samples.</span></span> <span data-ttu-id="e1c2f-589">O método do objeto `GetSample` retornará **MF_E_SAMPLEALLOCATOR_EMPTY** se a fila estiver vazia.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-589">The object's `GetSample` method returns **MF_E_SAMPLEALLOCATOR_EMPTY** if the queue is empty.</span></span>
-   <span data-ttu-id="e1c2f-590">Se o método [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) do mixer retornar MF_E_TRANSFORM_NEED_MORE_INPUT, significa que o mixer não pode produzir mais nenhuma saída, portanto, o apresentador limpa o sinalizador *m_fSampleNotify* .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-590">If the mixer's [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method returns MF_E_TRANSFORM_NEED_MORE_INPUT, it means the mixer cannot produce any more output, so the presenter clears the *m_fSampleNotify* flag.</span></span>
-   <span data-ttu-id="e1c2f-591">O `TrackSample` método, que define o retorno de chamada [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) , é mostrado na seção [acompanhamento de amostras](#tracking-samples).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-591">The `TrackSample` method, which sets the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback, is shown in the section [Tracking Samples](#tracking-samples).</span></span>

### <a name="repainting-frames"></a><span data-ttu-id="e1c2f-592">Repintando quadros</span><span class="sxs-lookup"><span data-stu-id="e1c2f-592">Repainting Frames</span></span>

<span data-ttu-id="e1c2f-593">Ocasionalmente, o apresentador pode precisar redesenhar o quadro de vídeo mais recente.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-593">Occasionally the presenter might need to repaint the most recent video frame.</span></span> <span data-ttu-id="e1c2f-594">Por exemplo, o apresentador padrão redesenha o quadro nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-594">For example, the standard presenter repaints the frame in the following situations:</span></span>

-   <span data-ttu-id="e1c2f-595">No modo de janela, em resposta a **WM_PAINT** mensagens recebidas pela janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-595">In windowed mode, in response to **WM_PAINT** messages received by the application's window.</span></span> <span data-ttu-id="e1c2f-596">Consulte [**IMFVideoDisplayControl:: RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-596">See [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span></span>
-   <span data-ttu-id="e1c2f-597">Se o retângulo de destino for alterado quando o aplicativo chamar [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-597">If the destination rectangle changes when the application calls [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="e1c2f-598">Use as etapas a seguir para solicitar que o mixer recrie o quadro mais recente:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-598">Use the following steps to request the mixer to re-create the most recent frame:</span></span>

1.  <span data-ttu-id="e1c2f-599">Obtenha um exemplo de vídeo da fila.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-599">Get a video sample from the queue.</span></span>
2.  <span data-ttu-id="e1c2f-600">Consulte o exemplo para a interface [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample) .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-600">Query the sample for the [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample) interface.</span></span>
3.  <span data-ttu-id="e1c2f-601">Chame [**IMFDesiredSample:: SetDesiredSampleTimeAndDuration**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-601">Call [**IMFDesiredSample::SetDesiredSampleTimeAndDuration**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration).</span></span> <span data-ttu-id="e1c2f-602">Especifique o carimbo de data/hora do quadro de vídeo mais recente.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-602">Specify the time stamp of the most recent video frame.</span></span> <span data-ttu-id="e1c2f-603">(Você precisará armazenar esse valor em cache e atualizá-lo para cada quadro.)</span><span class="sxs-lookup"><span data-stu-id="e1c2f-603">(You will need to cache this value and update it for each frame.)</span></span>
4.  <span data-ttu-id="e1c2f-604">Chame [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) no mixer.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-604">Call [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span>

<span data-ttu-id="e1c2f-605">Ao repintar um quadro, você pode ignorar o relógio de apresentação e apresentar o quadro imediatamente.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-605">When repainting a frame, you can ignore the presentation clock and present the frame immediately.</span></span>

### <a name="scheduling-samples"></a><span data-ttu-id="e1c2f-606">Exemplos de agendamento</span><span class="sxs-lookup"><span data-stu-id="e1c2f-606">Scheduling Samples</span></span>

<span data-ttu-id="e1c2f-607">Os quadros de vídeo podem alcançar o EVR a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-607">Video frames can reach the EVR at any time.</span></span> <span data-ttu-id="e1c2f-608">O apresentador é responsável por apresentar cada quadro no horário correto, com base no carimbo de data/hora do quadro.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-608">The presenter is responsible for presenting each frame at the correct time, based on the time stamp of the frame.</span></span> <span data-ttu-id="e1c2f-609">Quando o apresentador Obtém um novo exemplo do mixer, ele coloca o exemplo na fila agendada.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-609">When the presenter gets a new sample from the mixer, it puts the sample on the scheduled queue.</span></span> <span data-ttu-id="e1c2f-610">Em um thread separado, o apresentador Obtém continuamente a primeira amostra do início da fila e determina se deve:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-610">On a separate thread, the presenter continually gets the first sample from the head of the queue and determines whether to:</span></span>

-   <span data-ttu-id="e1c2f-611">Apresente o exemplo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-611">Present the sample.</span></span>
-   <span data-ttu-id="e1c2f-612">Mantenha a amostra na fila porque ela é antecipada.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-612">Keep the sample on the queue because it is early.</span></span>
-   <span data-ttu-id="e1c2f-613">Descarte o exemplo porque ele está atrasado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-613">Discard the sample because it is late.</span></span> <span data-ttu-id="e1c2f-614">Embora você deva evitar a remoção de quadros, se possível, talvez seja necessário se o apresentador ficar continuamente atrás.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-614">Although you should avoid dropping frames if possible, you might need to if the presenter is continually falling behind.</span></span>

<span data-ttu-id="e1c2f-615">Para obter o carimbo de data/hora de um quadro de vídeo, chame [**IMFSample:: Getsampletime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) no exemplo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-615">To get the time stamp for a video frame, call [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) on the video sample.</span></span> <span data-ttu-id="e1c2f-616">O carimbo de data/hora é relativo ao relógio de apresentação do EVR.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-616">The time stamp is relative to the EVR's presentation clock.</span></span> <span data-ttu-id="e1c2f-617">Para obter a hora do relógio atual, chame [**IMFClock:: GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-617">To get the current clock time, call [**IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span></span> <span data-ttu-id="e1c2f-618">Se o EVR não tiver um relógio de apresentação ou se um exemplo não tiver um carimbo de data/hora, você poderá apresentar o exemplo imediatamente depois de obtê-lo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-618">If the EVR does not have a presentation clock, or if a sample does not have a time stamp, you can present the sample immediately after you get it.</span></span>

<span data-ttu-id="e1c2f-619">Para obter a duração de cada amostra, chame [**IMFSample:: GetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-619">To get the duration of each sample, call [**IMFSample::GetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration).</span></span> <span data-ttu-id="e1c2f-620">Se o exemplo não tiver uma duração, você poderá usar a função [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) para calcular a duração da taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-620">If the sample does not have a duration, you can use the [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) function to calculate the duration from the frame rate.</span></span>

<span data-ttu-id="e1c2f-621">Ao agendar exemplos, tenha em mente o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-621">When you schedule samples, keep in mind the following:</span></span>

-   <span data-ttu-id="e1c2f-622">Se a taxa de reprodução for mais rápida ou mais lenta do que a velocidade normal, o relógio será executado a uma taxa mais rápida ou mais lenta.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-622">If the playback rate is faster or slower than normal speed, the clock runs at a faster or slower rate.</span></span> <span data-ttu-id="e1c2f-623">Isso significa que o carimbo de data/hora em um exemplo sempre fornece o tempo de destino correto relativo ao relógio de apresentação.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-623">That means the time stamp on a sample always gives the correct target time relative to the presentation clock.</span></span> <span data-ttu-id="e1c2f-624">No entanto, se você traduzir os tempos de apresentação em algum outro horário de relógio (por exemplo, o contador desempenho de alta resolução), será necessário dimensionar os horários com base na velocidade do relógio.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-624">However, if you translate presentation times into some other clock time (for example, the high-resolution performace counter), then you must scale the times based on the clock speed.</span></span> <span data-ttu-id="e1c2f-625">Se a velocidade do relógio for alterada, o EVR chamará o método [**IMFClockStateSink:: OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) do apresentador.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-625">If the clock speed changes, the EVR calls the presenter's [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) method.</span></span>
-   <span data-ttu-id="e1c2f-626">A taxa de reprodução pode ser negativa para reprodução reversa.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-626">The playback rate can be negative for reverse playback.</span></span> <span data-ttu-id="e1c2f-627">Quando a taxa de reprodução é negativa, o relógio de apresentação é executado de forma retroativa.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-627">When the playback rate is negative, the presentation clock runs backward.</span></span> <span data-ttu-id="e1c2f-628">Em outras palavras, a hora *n* + 1 ocorre antes da hora *n*.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-628">In other words, time *N* + 1 occurs before time *N*.</span></span>

<span data-ttu-id="e1c2f-629">O exemplo a seguir calcula o quão cedo ou tarde é uma amostra, em relação ao relógio de apresentação:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-629">The following example calculates how early or late a sample is, relative to the presentation clock:</span></span>


```C++
    LONGLONG hnsPresentationTime = 0;
    LONGLONG hnsTimeNow = 0;
    MFTIME   hnsSystemTime = 0;

    BOOL bPresentNow = TRUE;
    LONG lNextSleep = 0;

    if (m_pClock)
    {
        // Get the sample's time stamp. It is valid for a sample to
        // have no time stamp.
        hr = pSample->GetSampleTime(&hnsPresentationTime);

        // Get the clock time. (But if the sample does not have a time stamp,
        // we don't need the clock time.)
        if (SUCCEEDED(hr))
        {
            hr = m_pClock->GetCorrelatedTime(0, &hnsTimeNow, &hnsSystemTime);
        }

        // Calculate the time until the sample's presentation time.
        // A negative value means the sample is late.
        LONGLONG hnsDelta = hnsPresentationTime - hnsTimeNow;
        if (m_fRate < 0)
        {
            // For reverse playback, the clock runs backward. Therefore, the
            // delta is reversed.
            hnsDelta = - hnsDelta;
        }
```



<span data-ttu-id="e1c2f-630">O relógio de apresentação geralmente é orientado pelo relógio do sistema ou pelo processador de áudio.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-630">The presentation clock is usually driven by the system clock or the audio renderer.</span></span> <span data-ttu-id="e1c2f-631">(O processador de áudio deriva o tempo da taxa na qual a placa de som consome áudio.) Em geral, o relógio de apresentação não é sincronizado com a taxa de atualização do monitor.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-631">(The audio renderer derives the time from the rate at which the sound card consumes audio.) In general, the presentation clock is not synchronized with the refresh rate of the monitor.</span></span>

<span data-ttu-id="e1c2f-632">Se os parâmetros de apresentação do Direct3D especificarem **D3DPRESENT_INTERVAL_DEFAULT** ou **D3DPRESENT_INTERVAL_ONE** para o intervalo de apresentação, a operação **atual** aguardará o rerastreamento vertical do monitor.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-632">If your Direct3D presentation parameters specify **D3DPRESENT_INTERVAL_DEFAULT** or **D3DPRESENT_INTERVAL_ONE** for the presentation interval, the **Present** operation waits for the monitor's vertical retrace.</span></span> <span data-ttu-id="e1c2f-633">Essa é uma maneira fácil de evitar a subdivisão, mas reduz a precisão do seu algoritmo de agendamento.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-633">This is an easy way to prevent tearing, but reduces the accuracy of your scheduling algorithm.</span></span> <span data-ttu-id="e1c2f-634">Por outro lado, se o intervalo de apresentação for **D3DPRESENT_INTERVAL_IMMEDIATE**, o método **presente** será executado imediatamente, o que causa a subdivisão, a menos que o algoritmo de agendamento seja preciso o suficiente para que você chame **Present** somente durante o período de retrace vertical.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-634">Conversely, if the presentation interval is **D3DPRESENT_INTERVAL_IMMEDIATE**, the **Present** method executes immediately, which causes tearing unless your scheduling algorithm is accurate enough that you call **Present** only during the vertical retrace period.</span></span>

<span data-ttu-id="e1c2f-635">As funções a seguir podem ajudá-lo a obter informações precisas sobre o tempo:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-635">The following functions can help you get accurate timing information:</span></span>

-   <span data-ttu-id="e1c2f-636">**IDirect3DDevice9:: GetRasterStatus** retorna informações sobre a varredura, incluindo a linha de varredura atual e se a rasterização está no período vertical em branco.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-636">**IDirect3DDevice9::GetRasterStatus** returns information about the raster, including the current scan line and whether the raster is in the vertical blank period.</span></span>
-   <span data-ttu-id="e1c2f-637">**DwmGetCompositionTimingInfo** retorna informações de tempo para o Gerenciador de janelas da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-637">**DwmGetCompositionTimingInfo** returns timing information for the desktop window manager.</span></span> <span data-ttu-id="e1c2f-638">Essas informações serão úteis se a composição de área de trabalho estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-638">This information is useful if desktop composition is enabled.</span></span>

### <a name="presenting-samples"></a><span data-ttu-id="e1c2f-639">Apresentando exemplos</span><span class="sxs-lookup"><span data-stu-id="e1c2f-639">Presenting Samples</span></span>

<span data-ttu-id="e1c2f-640">Esta seção pressupõe que você criou uma cadeia de permuta separada para cada superfície, conforme descrito em [alocando superfícies do Direct3D](#allocating-direct3d-surfaces).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-640">This section assumes that you created a separate swap chain for each surface as described in [Allocating Direct3D Surfaces](#allocating-direct3d-surfaces).</span></span> <span data-ttu-id="e1c2f-641">Para apresentar um exemplo, obtenha a cadeia de troca da amostra de vídeo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-641">To present a sample, get the swap chain from the video sample as follows:</span></span>

1.  <span data-ttu-id="e1c2f-642">Chame [**IMFSample:: GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) no exemplo de vídeo para obter o buffer.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-642">Call [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) on the video sample to get the buffer.</span></span>
2.  <span data-ttu-id="e1c2f-643">Consulte o buffer para a interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-643">Query the buffer for the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
3.  <span data-ttu-id="e1c2f-644">Chame [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obter a interface **IDirect3DSurface9** da superfície do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-644">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get the **IDirect3DSurface9** interface of the Direct3D surface.</span></span> <span data-ttu-id="e1c2f-645">(Você pode combinar essa etapa e a etapa anterior em uma chamando [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).)</span><span class="sxs-lookup"><span data-stu-id="e1c2f-645">(You can combine this step and the previous step into one by calling [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).)</span></span>
4.  <span data-ttu-id="e1c2f-646">Chame **IDirect3DSurface9:: GetContainer** na superfície para obter um ponteiro para a cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-646">Call **IDirect3DSurface9::GetContainer** on the surface to get a pointer to the swap chain.</span></span>
5.  <span data-ttu-id="e1c2f-647">Chame **IDirect3DSwapChain9::P reenviada** na cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-647">Call **IDirect3DSwapChain9::Present** on the swap chain.</span></span>

<span data-ttu-id="e1c2f-648">O código a seguir mostra estas etapas:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-648">The following code shows these steps:</span></span>


```C++
HRESULT D3DPresentEngine::PresentSample(IMFSample* pSample, LONGLONG llTarget)
{
    HRESULT hr = S_OK;

    IMFMediaBuffer* pBuffer = NULL;
    IDirect3DSurface9* pSurface = NULL;
    IDirect3DSwapChain9* pSwapChain = NULL;

    if (pSample)
    {
        // Get the buffer from the sample.
        hr = pSample->GetBufferByIndex(0, &pBuffer);
        if (FAILED(hr))
        {
            goto done;
        }

        // Get the surface from the buffer.
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(&pSurface));
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (m_pSurfaceRepaint)
    {
        // Redraw from the last surface.
        pSurface = m_pSurfaceRepaint;
        pSurface->AddRef();
    }

    if (pSurface)
    {
        // Get the swap chain from the surface.
        hr = pSurface->GetContainer(IID_PPV_ARGS(&pSwapChain));
        if (FAILED(hr))
        {
            goto done;
        }

        // Present the swap chain.
        hr = PresentSwapChain(pSwapChain, pSurface);
        if (FAILED(hr))
        {
            goto done;
        }

        // Store this pointer in case we need to repaint the surface.
        CopyComPointer(m_pSurfaceRepaint, pSurface);
    }
    else
    {
        // No surface. All we can do is paint a black rectangle.
        PaintFrameWithGDI();
    }

done:
    SafeRelease(&pSwapChain);
    SafeRelease(&pSurface);
    SafeRelease(&pBuffer);

    if (FAILED(hr))
    {
        if (hr == D3DERR_DEVICELOST || hr == D3DERR_DEVICENOTRESET || hr == D3DERR_DEVICEHUNG)
        {
            // We failed because the device was lost. Fill the destination rectangle.
            PaintFrameWithGDI();

            // Ignore. We need to reset or re-create the device, but this method
            // is probably being called from the scheduler thread, which is not the
            // same thread that created the device. The Reset(Ex) method must be
            // called from the thread that created the device.

            // The presenter will detect the state when it calls CheckDeviceState()
            // on the next sample.
            hr = S_OK;
        }
    }
    return hr;
}
```



### <a name="source-and-destination-rectangles"></a><span data-ttu-id="e1c2f-649">Retângulos de origem e de destino</span><span class="sxs-lookup"><span data-stu-id="e1c2f-649">Source and Destination Rectangles</span></span>

<span data-ttu-id="e1c2f-650">O *retângulo de origem* é a parte do quadro de vídeo a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-650">The *source rectangle* is the portion of the video frame to display.</span></span> <span data-ttu-id="e1c2f-651">Ele é definido em relação a um sistema de coordenadas normalizado, no qual todo o quadro de vídeo ocupa um retângulo com coordenadas {0, 0, 1, 1}.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-651">It is defined relative to a normalized coordinate system, in which the entire video frame occupies a rectangle with coordinates {0, 0, 1, 1}.</span></span> <span data-ttu-id="e1c2f-652">O *retângulo de destino* é a área dentro da superfície de destino onde o quadro de vídeo é desenhado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-652">The *destination rectangle* is the area within the destination surface where the video frame is drawn.</span></span> <span data-ttu-id="e1c2f-653">O apresentador padrão permite que um aplicativo defina esses retângulos chamando [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-653">The standard presenter enables an application to set these rectangles by calling [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="e1c2f-654">Há várias opções para aplicar retângulos de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-654">There are several options for applying source and destination rectangles.</span></span> <span data-ttu-id="e1c2f-655">A primeira opção é permitir que o mixer os aplique:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-655">The first option is to let the mixer apply them:</span></span>

-   <span data-ttu-id="e1c2f-656">Defina o retângulo de origem usando o atributo [**VIDEO_ZOOM_RECT**](video-zoom-rect-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-656">Set the source rectangle using the [**VIDEO_ZOOM_RECT**](video-zoom-rect-attribute.md) attribute.</span></span> <span data-ttu-id="e1c2f-657">O mixer aplicará o retângulo de origem quando blits o vídeo à superfície de destino.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-657">The mixer will apply the source rectangle when it blits the video to the destination surface.</span></span> <span data-ttu-id="e1c2f-658">O retângulo de origem padrão do mixer é o quadro inteiro.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-658">The mixer's default source rectangle is the entire frame.</span></span>
-   <span data-ttu-id="e1c2f-659">Defina o retângulo de destino como a abertura geométrica no tipo de saída do mixer.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-659">Set the destination rectangle as the geometric aperture in the mixer's output type.</span></span> <span data-ttu-id="e1c2f-660">Para obter mais informações, consulte [negociando formatos](#negotiating-formats).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-660">For more information, see [Negotiating Formats](#negotiating-formats).</span></span>

<span data-ttu-id="e1c2f-661">A segunda opção é aplicar os retângulos quando você **IDirect3DSwapChain9::P reenviado** especificando os parâmetros *pSourceRect* e *pDestRect* no método **Present** .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-661">The second option is to apply the rectangles when you **IDirect3DSwapChain9::Present** by specifying the *pSourceRect* and *pDestRect* parameters in the **Present** method.</span></span> <span data-ttu-id="e1c2f-662">Você pode combinar essas opções.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-662">You can combine these options.</span></span> <span data-ttu-id="e1c2f-663">Por exemplo, você pode definir o retângulo de origem no mixer, mas aplicar o retângulo de destino no método **atual** .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-663">For example, you could set the source rectangle on the mixer but apply the destination rectangle in the **Present** method.</span></span>

<span data-ttu-id="e1c2f-664">Se o aplicativo alterar o retângulo de destino ou redimensionar a janela, talvez seja necessário alocar novas superfícies.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-664">If the application changes the destination rectangle or resizes the window, you might need to allocate new surfaces.</span></span> <span data-ttu-id="e1c2f-665">Nesse caso, você deve ter cuidado para sincronizar essa operação com seu thread de agendamento.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-665">If so, you must be careful to synchronize this operation with your scheduling thread.</span></span> <span data-ttu-id="e1c2f-666">Libere a fila de agendamento e descarte os exemplos antigos antes de alocar novas superfícies.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-666">Flush the scheduling queue and discard the old samples before allocating new surfaces.</span></span>

### <a name="end-of-stream"></a><span data-ttu-id="e1c2f-667">Fim do fluxo</span><span class="sxs-lookup"><span data-stu-id="e1c2f-667">End of Stream</span></span>

<span data-ttu-id="e1c2f-668">Quando cada fluxo de entrada no EVR termina, o EVR envia uma mensagem de **MFVP_MESSAGE_ENDOFSTREAM** para o apresentador.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-668">When every input stream on the EVR has ended, the EVR sends an **MFVP_MESSAGE_ENDOFSTREAM** message to the presenter.</span></span> <span data-ttu-id="e1c2f-669">No momento em que você recebe a mensagem, no entanto, pode haver alguns quadros de vídeo restantes para serem processados.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-669">At the point when you receive the message, however, there might be a few video frames remaining to be processed.</span></span> <span data-ttu-id="e1c2f-670">Antes de responder à mensagem de fim de fluxo, você deve drenar toda a saída do mixer e apresentar todos os quadros restantes.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-670">Before you respond to the end-of-stream message, you must drain all of the output from the mixer and present all of the remaining frames.</span></span> <span data-ttu-id="e1c2f-671">Depois que o último quadro for apresentado, envie um evento de **EC_COMPLETE** para o EVR.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-671">After the last frame is presented, send an **EC_COMPLETE** event to the EVR.</span></span>

<span data-ttu-id="e1c2f-672">O exemplo a seguir mostra um método que envia o evento **EC_COMPLETE** se várias condições forem atendidas.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-672">The next example shows a method that sends the **EC_COMPLETE** event if various conditions are met.</span></span> <span data-ttu-id="e1c2f-673">Caso contrário, ele retornará S_OK sem enviar o evento:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-673">Otherwise, it returns S_OK without sending the event:</span></span>


```C++
HRESULT EVRCustomPresenter::CheckEndOfStream()
{
    if (!m_bEndStreaming)
    {
        // The EVR did not send the MFVP_MESSAGE_ENDOFSTREAM message.
        return S_OK;
    }

    if (m_bSampleNotify)
    {
        // The mixer still has input.
        return S_OK;
    }

    if (m_SamplePool.AreSamplesPending())
    {
        // Samples are still scheduled for rendering.
        return S_OK;
    }

    // Everything is complete. Now we can tell the EVR that we are done.
    NotifyEvent(EC_COMPLETE, (LONG_PTR)S_OK, 0);
    m_bEndStreaming = FALSE;
    return S_OK;
}
```



<span data-ttu-id="e1c2f-674">Esse método verifica os seguintes Estados:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-674">This method checks the following states:</span></span>

-   <span data-ttu-id="e1c2f-675">Se a variável de *m_fSampleNotify* for **true**, significa que o mixer tem um ou mais quadros que ainda não foram processados.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-675">If the *m_fSampleNotify* variable is **TRUE**, it means the mixer has one or more frames that have not been processed yet.</span></span> <span data-ttu-id="e1c2f-676">(Para obter detalhes, consulte [processamento de saída](#processing-output).)</span><span class="sxs-lookup"><span data-stu-id="e1c2f-676">(For details, see [Processing Output](#processing-output).)</span></span>
-   <span data-ttu-id="e1c2f-677">A variável *m_fEndStreaming* é um sinalizador booliano cujo valor inicial é **false**.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-677">The *m_fEndStreaming* variable is a Boolean flag whose initial value **FALSE**.</span></span> <span data-ttu-id="e1c2f-678">O apresentador define o sinalizador como **true** quando o EVR envia a mensagem de **MFVP_MESSAGE_ENDOFSTREAM** .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-678">The presenter sets the flag to **TRUE** when the EVR sends the **MFVP_MESSAGE_ENDOFSTREAM** message.</span></span>
-   <span data-ttu-id="e1c2f-679">Presume-se que o `AreSamplesPending` método retorne **true** , desde que um ou mais quadros estejam aguardando na fila agendada.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-679">The `AreSamplesPending` method is assumed to return **TRUE** as long as one or more frames are waiting in the scheduled queue.</span></span>

<span data-ttu-id="e1c2f-680">No método [**IMFVideoPresenter::P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) , defina *m_fEndStreaming* como **true** e chame `CheckEndOfStream` quando EVR enviar a mensagem de **MFVP_MESSAGE_ENDOFSTREAM** :</span><span class="sxs-lookup"><span data-stu-id="e1c2f-680">In the [**IMFVideoPresenter::ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) method, set *m_fEndStreaming* to **TRUE** and call `CheckEndOfStream` when the EVR sends the **MFVP_MESSAGE_ENDOFSTREAM** message:</span></span>


```C++
HRESULT EVRCustomPresenter::ProcessMessage(
    MFVP_MESSAGE_TYPE eMessage,
    ULONG_PTR ulParam
    )
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    switch (eMessage)
    {
    // Flush all pending samples.
    case MFVP_MESSAGE_FLUSH:
        hr = Flush();
        break;

    // Renegotiate the media type with the mixer.
    case MFVP_MESSAGE_INVALIDATEMEDIATYPE:
        hr = RenegotiateMediaType();
        break;

    // The mixer received a new input sample.
    case MFVP_MESSAGE_PROCESSINPUTNOTIFY:
        hr = ProcessInputNotify();
        break;

    // Streaming is about to start.
    case MFVP_MESSAGE_BEGINSTREAMING:
        hr = BeginStreaming();
        break;

    // Streaming has ended. (The EVR has stopped.)
    case MFVP_MESSAGE_ENDSTREAMING:
        hr = EndStreaming();
        break;

    // All input streams have ended.
    case MFVP_MESSAGE_ENDOFSTREAM:
        // Set the EOS flag.
        m_bEndStreaming = TRUE;
        // Check if it's time to send the EC_COMPLETE event to the EVR.
        hr = CheckEndOfStream();
        break;

    // Frame-stepping is starting.
    case MFVP_MESSAGE_STEP:
        hr = PrepareFrameStep(LODWORD(ulParam));
        break;

    // Cancels frame-stepping.
    case MFVP_MESSAGE_CANCELSTEP:
        hr = CancelFrameStep();
        break;

    default:
        hr = E_INVALIDARG; // Unknown message. This case should never occur.
        break;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



<span data-ttu-id="e1c2f-681">Além disso, chame `CheckEndOfStream` se o método [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) do mixer retornar **MF_E_TRANSFORM_NEED_MORE_INPUT**.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-681">In addition, call `CheckEndOfStream` if the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method returns **MF_E_TRANSFORM_NEED_MORE_INPUT**.</span></span> <span data-ttu-id="e1c2f-682">Esse código de erro indica que o mixer não tem mais exemplos de entrada (consulte [processamento de saída](#processing-output)).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-682">This error code indicates that the mixer has no more input samples (see [Processing Output](#processing-output)).</span></span>

## <a name="frame-stepping"></a><span data-ttu-id="e1c2f-683">Revisão do quadro</span><span class="sxs-lookup"><span data-stu-id="e1c2f-683">Frame Stepping</span></span>

<span data-ttu-id="e1c2f-684">O EVR foi projetado para dar suporte à depuração de quadro no DirectShow e na depuração em Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-684">The EVR is designed to support frame stepping in DirectShow and scrubbing in Media Foundation.</span></span> <span data-ttu-id="e1c2f-685">Depuração e depuração de quadros são conceitualmente semelhantes.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-685">Frame stepping and scrubbing are conceptually similar.</span></span> <span data-ttu-id="e1c2f-686">Em ambos os casos, o aplicativo solicita um quadro de vídeo por vez.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-686">In both cases, the application requests one video frame at a time.</span></span> <span data-ttu-id="e1c2f-687">Internamente, o apresentador usa o mesmo mecanismo para implementar os dois recursos.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-687">Internally, the presenter uses the same mechanism to implement both features.</span></span>

<span data-ttu-id="e1c2f-688">A revisão do quadro no DirectShow funciona da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-688">Frame stepping in DirectShow works as follows:</span></span>

-   <span data-ttu-id="e1c2f-689">O aplicativo chama [**IVideoFrameStep:: Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-689">The application calls [**IVideoFrameStep::Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step).</span></span> <span data-ttu-id="e1c2f-690">O número de etapas é fornecido no parâmetro *dwSteps* .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-690">The number of steps is given in the *dwSteps* parameter.</span></span> <span data-ttu-id="e1c2f-691">O EVR envia uma mensagem de **MFVP_MESSAGE_STEP** para o apresentador, onde o parâmetro de mensagem (*ulParam*) é o número de etapas.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-691">The EVR sends an **MFVP_MESSAGE_STEP** message to the presenter, where the message parameter (*ulParam*) is the number of steps.</span></span>
-   <span data-ttu-id="e1c2f-692">Se o aplicativo chamar [**IVideoFrameStep:: CancelStep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) ou alterar o estado do grafo (em execução, em pausa ou parado), o EVR enviará uma mensagem de **MFVP_MESSAGE_CANCELSTEP** .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-692">If the application calls [**IVideoFrameStep::CancelStep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) or changes the graph state (running, paused, or stopped), the EVR sends an **MFVP_MESSAGE_CANCELSTEP** message.</span></span>

<span data-ttu-id="e1c2f-693">A depuração no Media Foundation funciona da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-693">Scrubbing in Media Foundation works as follows:</span></span>

-   <span data-ttu-id="e1c2f-694">O aplicativo define a taxa de reprodução como zero chamando [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-694">The application sets the playback rate to zero by calling [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).</span></span>
-   <span data-ttu-id="e1c2f-695">Para renderizar um novo quadro, o aplicativo chama [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) com a posição desejada.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-695">To render a new frame, the application calls [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) with the desired position.</span></span> <span data-ttu-id="e1c2f-696">O EVR envia uma mensagem de **MFVP_MESSAGE_STEP** com *ulParam* igual a 1.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-696">The EVR sends an **MFVP_MESSAGE_STEP** message with *ulParam* equal to 1.</span></span>
-   <span data-ttu-id="e1c2f-697">Para interromper a depuração, o aplicativo define a taxa de reprodução para um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-697">To stop scrubbing, the application sets the playback rate to a nonzero value.</span></span> <span data-ttu-id="e1c2f-698">O EVR envia a mensagem de **MFVP_MESSAGE_CANCELSTEP** .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-698">The EVR sends the **MFVP_MESSAGE_CANCELSTEP** message.</span></span>

<span data-ttu-id="e1c2f-699">Depois de receber a mensagem de **MFVP_MESSAGE_STEP** , o apresentador aguarda a chegada do quadro de destino.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-699">After receiving the **MFVP_MESSAGE_STEP** message, the presenter waits for the target frame to arrive.</span></span> <span data-ttu-id="e1c2f-700">Se o número de etapas for *N*, o apresentador descartará as próximas (*N* -1) amostras e apresentará o *N* º de amostra.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-700">If the number of steps is *N*, the presenter discards the next (*N* - 1) samples and presents the *N* th sample.</span></span> <span data-ttu-id="e1c2f-701">Quando o apresentador conclui a etapa do quadro, ele envia um evento [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) para o EVR com *LParam1* definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-701">When the presenter completes the frame step, it sends an [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) event to the EVR with *lParam1* set to **FALSE**.</span></span> <span data-ttu-id="e1c2f-702">Além disso, se a taxa de reprodução for zero, o apresentador enviará um evento [**EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-702">In addition, if the playback rate is zero, the presenter sends an [**EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) event.</span></span> <span data-ttu-id="e1c2f-703">Se o EVR cancelar a revisão do quadro enquanto uma operação de quadro de quadros ainda estiver pendente, o apresentador enviará um evento de **EC_STEP_COMPLETE** com *LParam1* definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-703">If the EVR cancels frame stepping while a frame-step operation is still pending, the presenter sends an **EC_STEP_COMPLETE** event with *lParam1* set to **TRUE**.</span></span>

<span data-ttu-id="e1c2f-704">O aplicativo pode emoldurar a etapa ou a limpeza várias vezes, portanto, o apresentador pode receber várias mensagens de **MFVP_MESSAGE_STEP** antes de obter uma mensagem de **MFVP_MESSAGE_CANCELSTEP** .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-704">The application can frame step or scrub multiple times, so the presenter might receive multiple **MFVP_MESSAGE_STEP** messages before it gets an **MFVP_MESSAGE_CANCELSTEP** message.</span></span> <span data-ttu-id="e1c2f-705">Além disso, o apresentador pode receber a mensagem de **MFVP_MESSAGE_STEP** antes de o relógio ser iniciado ou enquanto o relógio estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-705">Also, the presenter can receive the **MFVP_MESSAGE_STEP** message before the clock starts or while the clock is running.</span></span>

### <a name="implementing-frame-stepping"></a><span data-ttu-id="e1c2f-706">Implementando a revisão do quadro</span><span class="sxs-lookup"><span data-stu-id="e1c2f-706">Implementing Frame Stepping</span></span>

<span data-ttu-id="e1c2f-707">Esta seção descreve um algoritmo para implementar a depuração de quadros.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-707">This section describes an algorithm to implement frame stepping.</span></span> <span data-ttu-id="e1c2f-708">O algoritmo de revisão do quadro usa as seguintes variáveis:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-708">The frame stepping algorithm uses the following variables:</span></span>

-   <span data-ttu-id="e1c2f-709">*step_count*.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-709">*step_count*.</span></span> <span data-ttu-id="e1c2f-710">Um inteiro sem sinal que especifica o número de etapas na operação de depuração do quadro atual.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-710">An unsigned integer that specifies the number of steps in the current frame stepping operation.</span></span>
-   <span data-ttu-id="e1c2f-711">*step_queue*.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-711">*step_queue*.</span></span> <span data-ttu-id="e1c2f-712">Uma fila de ponteiros [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-712">A queue of [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointers.</span></span>
-   <span data-ttu-id="e1c2f-713">*step_state*.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-713">*step_state*.</span></span> <span data-ttu-id="e1c2f-714">A qualquer momento, o apresentador pode estar em um dos seguintes Estados em relação à revisão do quadro:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-714">At any time, the presenter can be in one of the following states with respect to frame stepping:</span></span> 

    | <span data-ttu-id="e1c2f-715">Estado</span><span class="sxs-lookup"><span data-stu-id="e1c2f-715">State</span></span>         | <span data-ttu-id="e1c2f-716">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1c2f-716">Description</span></span>                                                                                                                                                                                                     |
    |---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="e1c2f-717">NOT_STEPPING</span><span class="sxs-lookup"><span data-stu-id="e1c2f-717">NOT_STEPPING</span></span> | <span data-ttu-id="e1c2f-718">Sem revisão de quadro.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-718">Not frame stepping.</span></span>                                                                                                                                                                                             |
    | <span data-ttu-id="e1c2f-719">AGUARDANDO</span><span class="sxs-lookup"><span data-stu-id="e1c2f-719">WAITING</span></span>       | <span data-ttu-id="e1c2f-720">O apresentador recebeu a mensagem de **MFVP_MESSAGE_STEP** , mas o relógio não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-720">The presenter has received the **MFVP_MESSAGE_STEP** message, but the clock has not started.</span></span>                                                                                                                  |
    | <span data-ttu-id="e1c2f-721">PENDING</span><span class="sxs-lookup"><span data-stu-id="e1c2f-721">PENDING</span></span>       | <span data-ttu-id="e1c2f-722">O apresentador recebeu a mensagem de **MFVP_MESSAGE_STEP** e o relógio foi iniciado, mas o apresentador está aguardando para receber o quadro de destino.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-722">The presenter has received the **MFVP_MESSAGE_STEP** message and the clock has started, but the presenter is waiting to receive the target frame.</span></span>                                                             |
    | <span data-ttu-id="e1c2f-723">AGENDADA</span><span class="sxs-lookup"><span data-stu-id="e1c2f-723">SCHEDULED</span></span>     | <span data-ttu-id="e1c2f-724">O apresentador recebeu o quadro de destino e o agendou para apresentação, mas o quadro não foi apresentado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-724">The presenter has received the target frame and has scheduled it for presentation, but the frame has not been presented.</span></span>                                                                                        |
    | <span data-ttu-id="e1c2f-725">CONCLUÍ</span><span class="sxs-lookup"><span data-stu-id="e1c2f-725">COMPLETE</span></span>      | <span data-ttu-id="e1c2f-726">O apresentador apresentou o quadro de destino e enviou o evento de [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) e está aguardando a próxima mensagem de **MFVP_MESSAGE_STEP** ou **MFVP_MESSAGE_CANCELSTEP** .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-726">The presenter has presented the target frame and sent the [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) event, and is waiting for the next **MFVP_MESSAGE_STEP** or **MFVP_MESSAGE_CANCELSTEP** message.</span></span> |

    

     

    <span data-ttu-id="e1c2f-727">Esses Estados são independentes dos Estados do apresentador listados na seção [Estados do apresentador](#presenter-states).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-727">These states are independent of the presenter states listed in the section [Presenter States](#presenter-states).</span></span>

<span data-ttu-id="e1c2f-728">Os procedimentos a seguir são definidos para o algoritmo de depuração de quadro:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-728">The following procedures are defined for the frame-stepping algorithm:</span></span>

<span data-ttu-id="e1c2f-729">Procedimento PrepareFrameStep</span><span class="sxs-lookup"><span data-stu-id="e1c2f-729">PrepareFrameStep Procedure</span></span>

1.  <span data-ttu-id="e1c2f-730">*Step_count* de incremento.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-730">Increment *step_count*.</span></span>
2.  <span data-ttu-id="e1c2f-731">Defina *step_state* como aguardando.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-731">Set *step_state* to WAITING.</span></span>
3.  <span data-ttu-id="e1c2f-732">Se o relógio estiver em execução, chame StartFrameStep.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-732">If the clock is running, call StartFrameStep.</span></span>

<span data-ttu-id="e1c2f-733">Procedimento StartFrameStep</span><span class="sxs-lookup"><span data-stu-id="e1c2f-733">StartFrameStep Procedure</span></span>

1.  <span data-ttu-id="e1c2f-734">Se *step_state* for igual a Wait, defina *step_state* como pendente.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-734">If *step_state* equals WAITING, set *step_state* to PENDING.</span></span> <span data-ttu-id="e1c2f-735">Para cada exemplo em *step_queue*, chame DeliverFrameStepSample.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-735">For each sample in *step_queue*, call DeliverFrameStepSample.</span></span>
2.  <span data-ttu-id="e1c2f-736">Se *step_state* for igual a NOT_STEPPING, remova os exemplos de *step_queue* e agende-os para apresentação.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-736">If *step_state* equals NOT_STEPPING, remove any samples from *step_queue* and schedule them for presentation.</span></span>

<span data-ttu-id="e1c2f-737">Procedimento CompleteFrameStep</span><span class="sxs-lookup"><span data-stu-id="e1c2f-737">CompleteFrameStep Procedure</span></span>

1.  <span data-ttu-id="e1c2f-738">Defina *step_state* como concluir.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-738">Set *step_state* to COMPLETE.</span></span>
2.  <span data-ttu-id="e1c2f-739">Envie o evento EC_STEP_COMPLETE com *lParam1*  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-739">Send the EC_STEP_COMPLETE event with *lParam1* = **FALSE**.</span></span>
3.  <span data-ttu-id="e1c2f-740">Se a taxa de relógio for zero, envie o evento **EC_SCRUB_TIME** com o tempo de exemplo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-740">If the clock rate is zero, send the **EC_SCRUB_TIME** event with the sample time.</span></span>

<span data-ttu-id="e1c2f-741">Procedimento DeliverFrameStepSample</span><span class="sxs-lookup"><span data-stu-id="e1c2f-741">DeliverFrameStepSample Procedure</span></span>

1.  <span data-ttu-id="e1c2f-742">Se a taxa de relógio for zero e o tempo de *amostragem* da duração de exemplo  +    <  , descarte o exemplo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-742">If the clock rate is zero and *sample time* + *sample duration* < *clock time*, discard the sample.</span></span> <span data-ttu-id="e1c2f-743">Sair.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-743">Exit.</span></span>
2.  <span data-ttu-id="e1c2f-744">Se *step_state* for igual a agendada ou concluída, adicione o exemplo a *step_queue*.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-744">If *step_state* equals SCHEDULED or COMPLETE, add the sample to *step_queue*.</span></span> <span data-ttu-id="e1c2f-745">Sair.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-745">Exit.</span></span>
3.  <span data-ttu-id="e1c2f-746">Decrementar *step_count*.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-746">Decrement *step_count*.</span></span>
4.  <span data-ttu-id="e1c2f-747">Se *step_count* > 0, descarte o exemplo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-747">If *step_count* > 0, discard the sample.</span></span> <span data-ttu-id="e1c2f-748">Sair.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-748">Exit.</span></span>
5.  <span data-ttu-id="e1c2f-749">Se *step_state* for igual a Wait, adicione o exemplo a *step_queue*.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-749">If *step_state* equals WAITING, add the sample to *step_queue*.</span></span> <span data-ttu-id="e1c2f-750">Sair.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-750">Exit.</span></span>
6.  <span data-ttu-id="e1c2f-751">Agendar o exemplo para apresentação.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-751">Schedule the sample for presentation.</span></span>
7.  <span data-ttu-id="e1c2f-752">Defina *step_state* como agendado.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-752">Set *step_state* to SCHEDULED.</span></span>

<span data-ttu-id="e1c2f-753">Procedimento CancelFrameStep</span><span class="sxs-lookup"><span data-stu-id="e1c2f-753">CancelFrameStep Procedure</span></span>

1.  <span data-ttu-id="e1c2f-754">Definir *step_state* como NOT_STEPPING</span><span class="sxs-lookup"><span data-stu-id="e1c2f-754">Set *step_state* to NOT_STEPPING</span></span>
2.  <span data-ttu-id="e1c2f-755">Redefinir *step_count* como zero.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-755">Reset *step_count* to zero.</span></span>
3.  <span data-ttu-id="e1c2f-756">Se o valor anterior de *step_state* estava aguardando, pendente ou agendado, envie EC_STEP_COMPLETE com *lParam1*  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-756">If the previous value of *step_state* was WAITING, PENDING, or SCHEDULED, send EC_STEP_COMPLETE with *lParam1* = **TRUE**.</span></span>

<span data-ttu-id="e1c2f-757">Chame estes procedimentos da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-757">Call these procedures as follows:</span></span>



| <span data-ttu-id="e1c2f-758">Mensagem ou método do apresentador</span><span class="sxs-lookup"><span data-stu-id="e1c2f-758">Presenter message or method</span></span>                                                   | <span data-ttu-id="e1c2f-759">Procedimento</span><span class="sxs-lookup"><span data-stu-id="e1c2f-759">Procedure</span></span>           |
|-------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="e1c2f-760">**MFVP_MESSAGE_STEP** mensagem</span><span class="sxs-lookup"><span data-stu-id="e1c2f-760">**MFVP_MESSAGE_STEP** message</span></span>                                               | `PrepareFrameStep`  |
| <span data-ttu-id="e1c2f-761">**MFVP_MESSAGE_STEP** mensagem</span><span class="sxs-lookup"><span data-stu-id="e1c2f-761">**MFVP_MESSAGE_STEP** message</span></span>                                               | `CancelStep`        |
| [<span data-ttu-id="e1c2f-762">**IMFClockStateSink::OnClockStart**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-762">**IMFClockStateSink::OnClockStart**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | `StartFrameStep`    |
| [<span data-ttu-id="e1c2f-763">**IMFClockStateSink::OnClockRestart**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-763">**IMFClockStateSink::OnClockRestart**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | `StartFrameStep`    |
| <span data-ttu-id="e1c2f-764">Retorno de chamada [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)</span><span class="sxs-lookup"><span data-stu-id="e1c2f-764">[**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback</span></span>                         | `CompleteFrameStep` |
| [<span data-ttu-id="e1c2f-765">**IMFClockStateSink::OnClockStop**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-765">**IMFClockStateSink::OnClockStop**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | `CancelFrameStep`   |
| [<span data-ttu-id="e1c2f-766">**IMFClockStateSink::OnClockSetRate**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-766">**IMFClockStateSink::OnClockSetRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) | `CancelFrameStep`   |



 

<span data-ttu-id="e1c2f-767">O fluxograma a seguir mostra os procedimentos de depuração de quadro.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-767">The following flow chart shows the frame-stepping procedures.</span></span>

![fluxograma mostrando caminhos que começam com a \- etapa da mensagem mfvp \- e mfvp da \- mensagem \- processinputnotify e terminam em "estado = concluído"](images/d9baaa67-a9b1-4e27-9a32-08a45b0677d3.gif)

## <a name="setting-the-presenter-on-the-evr"></a><span data-ttu-id="e1c2f-769">Configurando o apresentador no EVR</span><span class="sxs-lookup"><span data-stu-id="e1c2f-769">Setting the Presenter on the EVR</span></span>

<span data-ttu-id="e1c2f-770">Depois de implementar o apresentador, a próxima etapa é configurar o EVR para usá-lo.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-770">After implementing the presenter, the next step is to configure the EVR to use it.</span></span>

### <a name="setting-the-presenter-in-directshow"></a><span data-ttu-id="e1c2f-771">Configurando o apresentador no DirectShow</span><span class="sxs-lookup"><span data-stu-id="e1c2f-771">Setting the Presenter in DirectShow</span></span>

<span data-ttu-id="e1c2f-772">Em um aplicativo do DirectShow, defina o apresentador no EVR da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-772">In a DirectShow application, set the presenter on the EVR as follows:</span></span>

1.  <span data-ttu-id="e1c2f-773">Crie o filtro EVR chamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-773">Create the EVR filter by calling **CoCreateInstance**.</span></span> <span data-ttu-id="e1c2f-774">O CLSID é **CLSID_EnhancedVideoRenderer**.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-774">The CLSID is **CLSID_EnhancedVideoRenderer**.</span></span>
2.  <span data-ttu-id="e1c2f-775">Adicione o EVR ao gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-775">Add the EVR to the filter graph.</span></span>
3.  <span data-ttu-id="e1c2f-776">Crie uma instância do seu apresentador.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-776">Create an instance of your presenter.</span></span> <span data-ttu-id="e1c2f-777">Seu apresentador pode dar suporte à criação de objeto COM padrão por meio de **IClassFactory**, mas isso não é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-777">Your presenter can support standard COM object creation through **IClassFactory**, but this is not mandatory.</span></span>
4.  <span data-ttu-id="e1c2f-778">Consulte o filtro EVR para a interface [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-778">Query the EVR filter for the [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) interface.</span></span>
5.  <span data-ttu-id="e1c2f-779">Chame [**IMFVideoRenderer:: InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-779">Call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>

### <a name="setting-the-presenter-in-media-foundation"></a><span data-ttu-id="e1c2f-780">Configurando o apresentador no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e1c2f-780">Setting the Presenter in Media Foundation</span></span>

<span data-ttu-id="e1c2f-781">No Media Foundation, você tem várias opções, dependendo se você criar o coletor de mídia EVR ou o objeto de ativação EVR.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-781">In Media Foundation, you have several options, depending on whether you create the EVR media sink or the EVR activation object.</span></span> <span data-ttu-id="e1c2f-782">Para obter mais informações sobre objetos de ativação, consulte [Activation Objects](activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-782">For more information about activation objects, see [Activation Objects](activation-objects.md).</span></span>

<span data-ttu-id="e1c2f-783">Para o coletor de mídia do EVR, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-783">For the EVR media sink, do the following:</span></span>

1.  <span data-ttu-id="e1c2f-784">Chame [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) para criar o coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-784">Call [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) to create the media sink.</span></span>
2.  <span data-ttu-id="e1c2f-785">Crie uma instância do seu apresentador.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-785">Create an instance of your presenter.</span></span>
3.  <span data-ttu-id="e1c2f-786">Consulte o coletor de mídia do EVR para a interface [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-786">Query the EVR media sink for the [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) interface.</span></span>
4.  <span data-ttu-id="e1c2f-787">Chame [**IMFVideoRenderer:: InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span><span class="sxs-lookup"><span data-stu-id="e1c2f-787">Call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>

<span data-ttu-id="e1c2f-788">Para o objeto de ativação EVR, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-788">For the EVR activation object, do the following:</span></span>

1.  <span data-ttu-id="e1c2f-789">Chame [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para criar o objeto de ativação.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-789">Call [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) to create the activation object.</span></span>
2.  <span data-ttu-id="e1c2f-790">Defina um dos seguintes atributos no objeto de ativação:</span><span class="sxs-lookup"><span data-stu-id="e1c2f-790">Set one of the following attributes on the activation object:</span></span> 

    | <span data-ttu-id="e1c2f-791">Atributo</span><span class="sxs-lookup"><span data-stu-id="e1c2f-791">Attribute</span></span>                                                                                                         | <span data-ttu-id="e1c2f-792">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1c2f-792">Description</span></span>                                                                                                                                                                                                                               |
    |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="e1c2f-793">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-793">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**</span></span>](mf-activate-custom-video-presenter-activate-attribute.md) | <span data-ttu-id="e1c2f-794">Ponteiro para um objeto de ativação para o apresentador.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-794">Pointer to an activation object for the presenter.</span></span><br/> <span data-ttu-id="e1c2f-795">Com esse sinalizador, você deve fornecer um objeto de ativação para o apresentador.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-795">With this flag, you must provide an activation object for your presenter.</span></span> <span data-ttu-id="e1c2f-796">O objeto de ativação deve implementar a interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="e1c2f-796">The activation object must implement the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span><br/> |
    | [<span data-ttu-id="e1c2f-797">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**</span><span class="sxs-lookup"><span data-stu-id="e1c2f-797">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**</span></span>](mf-activate-custom-video-presenter-clsid-attribute.md)       | <span data-ttu-id="e1c2f-798">CLSID do apresentador.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-798">CLSID of the presenter.</span></span><br/> <span data-ttu-id="e1c2f-799">Com esse sinalizador, o apresentador deve dar suporte à criação de objeto COM padrão por meio de **IClassFactory**.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-799">With this flag, your presenter must support standard COM object creation through **IClassFactory**.</span></span><br/>                                                                                         |

    

     

3.  <span data-ttu-id="e1c2f-800">Opcionalmente, defina o atributo [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md) no objeto de ativação.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-800">Optionally, set the [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md) attribute on the activation object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1c2f-801">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e1c2f-801">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1c2f-802">Processador de vídeo aprimorado</span><span class="sxs-lookup"><span data-stu-id="e1c2f-802">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="e1c2f-803">Exemplo de EVRPresenter</span><span class="sxs-lookup"><span data-stu-id="e1c2f-803">EVRPresenter Sample</span></span>](evrpresenter-sample.md)
</dt> </dl>

 

 
