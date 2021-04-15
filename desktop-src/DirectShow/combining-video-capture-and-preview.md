---
description: Combinando captura de vídeo e visualização
ms.assetid: bffc1900-be05-4d7e-ab8d-3177365aeb7a
title: Combinando captura de vídeo e visualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d1a3dd3df30bd13aa6fdae7e39894941071df8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456488"
---
# <a name="combining-video-capture-and-preview"></a><span data-ttu-id="42da1-103">Combinando captura de vídeo e visualização</span><span class="sxs-lookup"><span data-stu-id="42da1-103">Combining Video Capture and Preview</span></span>

<span data-ttu-id="42da1-104">As seções anteriores descrevem como capturar vídeos para vários formatos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="42da1-104">The previous sections describe how to capture video to various file formats.</span></span> <span data-ttu-id="42da1-105">A seção [vídeo](previewing-video.md) de visualização descreve como criar um grafo de visualização dinâmica.</span><span class="sxs-lookup"><span data-stu-id="42da1-105">The section [Previewing Video](previewing-video.md) describes how to build a live preview graph.</span></span> <span data-ttu-id="42da1-106">No entanto, muitos aplicativos devem fazer ambos ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="42da1-106">However, many applications must do both at once.</span></span> <span data-ttu-id="42da1-107">Para criar uma visualização combinada e um grafo de gravação de arquivos, basta fazer duas chamadas para [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream):</span><span class="sxs-lookup"><span data-stu-id="42da1-107">To build a combined preview and file-writing graph, simply make two calls to [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream):</span></span>


```C++
// Render the preview stream to the video renderer.
hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap, 
    NULL, NULL);

// Render the capture stream to the mux.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap, 
    NULL, pMux);
```



<span data-ttu-id="42da1-108">Nesse código, o construtor do grafo de captura está ocultando alguns detalhes:</span><span class="sxs-lookup"><span data-stu-id="42da1-108">In this code, the Capture Graph Builder is hiding some details:</span></span>

-   <span data-ttu-id="42da1-109">Se o filtro de captura tiver um PIN de visualização ou um PIN de porta de vídeo, além de um PIN de captura, o método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) simplesmente renderiza ambos os Pins, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="42da1-109">If the capture filter has a preview pin or video port pin, plus a capture pin, the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method simply renders both pins, as shown in the following illustration.</span></span>

    ![Grafo de captura e visualização](images/vidcap04.png)

-   <span data-ttu-id="42da1-111">Se o filtro tiver apenas um PIN de captura, o construtor de gráficos de captura usará o filtro de uso [inteligente](smart-tee-filter.md) para dividir o fluxo de captura.</span><span class="sxs-lookup"><span data-stu-id="42da1-111">If the filter has only a capture pin, the Capture Graph Builder uses the [Smart Tee](smart-tee-filter.md) filter to split the capture stream.</span></span> <span data-ttu-id="42da1-112">A ilustração a seguir mostra o grafo com um "t" inteligente.</span><span class="sxs-lookup"><span data-stu-id="42da1-112">The following illustration shows the graph with a Smart Tee.</span></span>

    ![capturar e visualizar o grafo com o filtro de "t" inteligente](images/vidcap05.png)

<span data-ttu-id="42da1-114">O filtro de "t" inteligente tem um PIN de captura e um PIN de visualização.</span><span class="sxs-lookup"><span data-stu-id="42da1-114">The Smart Tee filter has a capture pin and a preview pin.</span></span> <span data-ttu-id="42da1-115">Ele usa um fluxo de vídeo único do filtro de captura e o divide em dois fluxos, um para captura e outro para visualização.</span><span class="sxs-lookup"><span data-stu-id="42da1-115">It takes a single video stream from the capture filter and splits it into two streams, one for capture and one for preview.</span></span> <span data-ttu-id="42da1-116">Para manter a taxa de transferência no pino de captura, o pino de visualização descarta os quadros conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="42da1-116">To maintain throughput on the capture pin, the preview pin drops frames as needed.</span></span> <span data-ttu-id="42da1-117">Ele também retira os carimbos de data/hora de cada amostra antes de entregá-lo, pelos motivos discutidos no tópico [filtros de captura de vídeo do DirectShow](directshow-video-capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="42da1-117">It also strips the time stamps from each sample before delivering it, for the reasons discussed in the topic [DirectShow Video Capture Filters](directshow-video-capture-filters.md).</span></span>

<span data-ttu-id="42da1-118">Embora o monitor inteligente divida o fluxo, ele não duplica fisicamente os dados de vídeo.</span><span class="sxs-lookup"><span data-stu-id="42da1-118">Although the Smart Tee splits the stream, it does not physically duplicate the video data.</span></span> <span data-ttu-id="42da1-119">Em vez disso, ele usa objetos de exemplo de mídia personalizados que compartilham os buffers.</span><span class="sxs-lookup"><span data-stu-id="42da1-119">Instead, it uses custom media sample objects that share the buffers.</span></span> <span data-ttu-id="42da1-120">Os exemplos são marcados como "somente leitura" para garantir que os filtros downstream não sejam gravados nos dados.</span><span class="sxs-lookup"><span data-stu-id="42da1-120">The samples are marked "read-only" to ensure that downstream filters do not write on the data.</span></span>

<span data-ttu-id="42da1-121">Se o grafo de captura tiver uma janela de visualização, várias coisas poderão fazer com que o Gerenciador de gráfico de filtro interrompa todo o grafo, incluindo o fluxo de captura:</span><span class="sxs-lookup"><span data-stu-id="42da1-121">If your capture graph has a preview window, several things can cause the Filter Graph Manager to stop the entire graph, including the capture stream:</span></span>

-   <span data-ttu-id="42da1-122">Bloqueando o computador.</span><span class="sxs-lookup"><span data-stu-id="42da1-122">Locking the computer.</span></span>
-   <span data-ttu-id="42da1-123">Pressionar CTRL + ALT + DELETE em um computador que seja membro de um domínio.</span><span class="sxs-lookup"><span data-stu-id="42da1-123">Pressing CTRL+ALT+DELETE on a computer that is a member of a domain.</span></span>
-   <span data-ttu-id="42da1-124">Execução de um aplicativo Direct3D de tela inteira, como um jogo ou uma proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="42da1-124">Running a full-screen Direct3D application, such as a game or screen saver.</span></span>
-   <span data-ttu-id="42da1-125">Alternando monitores ou alterando a resolução de vídeo.</span><span class="sxs-lookup"><span data-stu-id="42da1-125">Switching monitors or changing the display resolution.</span></span>
-   <span data-ttu-id="42da1-126">Executar um programa que faz com que o Windows exiba uma caixa de diálogo UAC (controle de conta de usuário).</span><span class="sxs-lookup"><span data-stu-id="42da1-126">Running a program that causes Windows to display a User Account Control (UAC) dialog.</span></span> <span data-ttu-id="42da1-127">(Windows Vista ou posterior.)</span><span class="sxs-lookup"><span data-stu-id="42da1-127">(Windows Vista or later.)</span></span>
-   <span data-ttu-id="42da1-128">Executando uma janela do DOS em tela inteira.</span><span class="sxs-lookup"><span data-stu-id="42da1-128">Running a full-screen DOS window.</span></span>

<span data-ttu-id="42da1-129">Qualquer um desses eventos pode interromper a sessão de captura, possivelmente causando perda de dados.</span><span class="sxs-lookup"><span data-stu-id="42da1-129">Any of these events might interrupt the capture session, possibly causing data loss.</span></span> <span data-ttu-id="42da1-130">(Aqui está o que acontece internamente: o renderizador de vídeo perde os recursos de Direct3D ou DirectDraw necessários.</span><span class="sxs-lookup"><span data-stu-id="42da1-130">(Here is what happens internally: The video renderer loses the Direct3D or DirectDraw resources that it needs.</span></span> <span data-ttu-id="42da1-131">No processo de recuperação desses recursos, o renderizador de vídeo deve se reconectar com o filtro upstream, fazendo com que o Gerenciador do grafo de filtro pare o grafo.)</span><span class="sxs-lookup"><span data-stu-id="42da1-131">In the process of recovering those resources, the video renderer must reconnect with the upstream filter, causing the Filter Graph Manager to stop the graph.)</span></span>

<span data-ttu-id="42da1-132">Duas soluções possíveis para esse problema são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="42da1-132">Two possible solutions to this problem are the following:</span></span>

-   <span data-ttu-id="42da1-133">Não inclua um fluxo de visualização.</span><span class="sxs-lookup"><span data-stu-id="42da1-133">Do not include a preview stream.</span></span> <span data-ttu-id="42da1-134">No entanto, lembre-se de que o método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) adiciona automaticamente uma janela de visualização quando o dispositivo de captura tem um PIN de porta de vídeo.</span><span class="sxs-lookup"><span data-stu-id="42da1-134">However, be aware that the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method automatically adds a preview window when the capture device has a video port pin.</span></span> <span data-ttu-id="42da1-135">Consulte [Pins de porta de vídeo na captura de arquivo](video-port-pins-in-file-capture.md).</span><span class="sxs-lookup"><span data-stu-id="42da1-135">See [Video Port Pins in File Capture](video-port-pins-in-file-capture.md).</span></span>
-   <span data-ttu-id="42da1-136">Use o mecanismo de buffer de fluxo para enviar o fluxo de visualização para um grafo em outro processo.</span><span class="sxs-lookup"><span data-stu-id="42da1-136">Use the Stream Buffer Engine to send the preview stream to a graph in another process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="42da1-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="42da1-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42da1-138">Capturando vídeo em um arquivo</span><span class="sxs-lookup"><span data-stu-id="42da1-138">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



