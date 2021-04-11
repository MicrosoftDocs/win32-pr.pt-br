---
title: Implementando um plug-in de DSP de vídeo
description: Implementando um plug-in de DSP de vídeo
ms.assetid: 36c06c57-7623-430b-8280-9dba7b0a2e9b
keywords:
- Plug-ins do Windows Media Player, DSP de vídeo
- plug-ins, DSP de vídeo
- plug-ins de processamento de sinal digital, implementando código
- Plug-ins do DSP, implementando código
- plug-ins de processamento de sinal digital, modificando código de exemplo
- Plug-ins do DSP, modificando código de exemplo
- plug-ins de processamento de sinal digital, implementação de vídeo
- Plug-ins do DSP, implementação de vídeo
- plug-ins de DSP de vídeo, implementando código
- plug-ins de DSP de vídeo, modificando código de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f1b819f328fc586d21208c00b6f0d03dca4fe9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292298"
---
# <a name="implementing-a-video-dsp-plug-in"></a><span data-ttu-id="db8bd-113">Implementando um plug-in de DSP de vídeo</span><span class="sxs-lookup"><span data-stu-id="db8bd-113">Implementing a Video DSP Plug-in</span></span>

<span data-ttu-id="db8bd-114">Os adaptadores de vídeo do computador dão suporte a um conjunto de formatos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="db8bd-114">Computer video display adapters support a set of video formats.</span></span> <span data-ttu-id="db8bd-115">Os codecs de vídeo digital também dão suporte a um conjunto de formatos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="db8bd-115">Digital video codecs also support a set of video formats.</span></span> <span data-ttu-id="db8bd-116">Ao tentar reproduzir um arquivo de vídeo específico, o Windows Media Player deve escolher um formato a ser usado para renderização.</span><span class="sxs-lookup"><span data-stu-id="db8bd-116">When attempting to play a particular video file, Windows Media Player must choose a format to use for rendering.</span></span> <span data-ttu-id="db8bd-117">O Player tenta encontrar a melhor correspondência entre os formatos suportados pelo codec de vídeo e os formatos suportados pelo adaptador de vídeo, ou seja, aquele que produz a qualidade mais alta.</span><span class="sxs-lookup"><span data-stu-id="db8bd-117">The Player attempts to find the best match between the formats supported by the video codec and the formats supported by the video display adapter—that is, the one that yields the highest quality.</span></span>

<span data-ttu-id="db8bd-118">Para criar um plug-in de DSP do Windows Media Player que processa vídeo, primeiro você precisará decidir quais formatos de vídeo deseja que seu plug-in processe.</span><span class="sxs-lookup"><span data-stu-id="db8bd-118">To create a Windows Media Player DSP plug-in that processes video, you'll first need to decide which video formats you'd like your plug-in to process.</span></span> <span data-ttu-id="db8bd-119">O plug-in DSP de vídeo de exemplo funciona com os seguintes formatos de vídeo:</span><span class="sxs-lookup"><span data-stu-id="db8bd-119">The sample video DSP plug-in works with the following video formats:</span></span>

-   <span data-ttu-id="db8bd-120">NV12</span><span class="sxs-lookup"><span data-stu-id="db8bd-120">NV12</span></span>
-   <span data-ttu-id="db8bd-121">YV12</span><span class="sxs-lookup"><span data-stu-id="db8bd-121">YV12</span></span>
-   <span data-ttu-id="db8bd-122">YUY2</span><span class="sxs-lookup"><span data-stu-id="db8bd-122">YUY2</span></span>
-   <span data-ttu-id="db8bd-123">UYVY</span><span class="sxs-lookup"><span data-stu-id="db8bd-123">UYVY</span></span>
-   <span data-ttu-id="db8bd-124">RGB32</span><span class="sxs-lookup"><span data-stu-id="db8bd-124">RGB32</span></span>
-   <span data-ttu-id="db8bd-125">RGB24</span><span class="sxs-lookup"><span data-stu-id="db8bd-125">RGB24</span></span>
-   <span data-ttu-id="db8bd-126">RGB555</span><span class="sxs-lookup"><span data-stu-id="db8bd-126">RGB555</span></span>
-   <span data-ttu-id="db8bd-127">RGB565</span><span class="sxs-lookup"><span data-stu-id="db8bd-127">RGB565</span></span>

<span data-ttu-id="db8bd-128">Quais formatos você escolherá para processar cabe a você.</span><span class="sxs-lookup"><span data-stu-id="db8bd-128">Which formats you choose to process is up to you.</span></span> <span data-ttu-id="db8bd-129">Você pode remover formatos do plug-in de exemplo para que eles não sejam mais suportados e você possa adicionar código para processar formatos adicionais.</span><span class="sxs-lookup"><span data-stu-id="db8bd-129">You can remove formats from the sample plug-in so that they aren't supported any longer and you can add code to process additional formats.</span></span>

<span data-ttu-id="db8bd-130">As seções a seguir fornecem informações adicionais que você deve saber antes de criar seu próprio plug-in de DSP de vídeo para o Windows Media Player:</span><span class="sxs-lookup"><span data-stu-id="db8bd-130">The following sections provide additional information you should know before creating your own video DSP plug-in for Windows Media Player:</span></span>

-   [<span data-ttu-id="db8bd-131">Negociação de formato de vídeo no plug-in de DSP de vídeo de exemplo</span><span class="sxs-lookup"><span data-stu-id="db8bd-131">Video Format Negotiation in the Sample Video DSP Plug-in</span></span>](video-format-negotiation-in-the-sample-video-dsp-plug-in.md)
-   [<span data-ttu-id="db8bd-132">DoProcessOutput no plug-in de DSP de vídeo de exemplo</span><span class="sxs-lookup"><span data-stu-id="db8bd-132">DoProcessOutput in the Sample Video DSP Plug-in</span></span>](doprocessoutput-in-the-sample-video-dsp-plug-in.md)
-   [<span data-ttu-id="db8bd-133">Processando o vídeo</span><span class="sxs-lookup"><span data-stu-id="db8bd-133">Processing the Video</span></span>](processing-the-video.md)

## <a name="related-topics"></a><span data-ttu-id="db8bd-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="db8bd-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db8bd-135">**Implementando seu código do DSP**</span><span class="sxs-lookup"><span data-stu-id="db8bd-135">**Implementing Your DSP Code**</span></span>](implementing-your-dsp-code.md)
</dt> </dl>

 

 




