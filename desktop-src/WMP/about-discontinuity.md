---
title: Sobre a descontinuidade
description: Sobre a descontinuidade
ms.assetid: 29210758-a1e6-47f2-9428-38f79623fbca
keywords:
- Plug-ins do Windows Media Player, DSP de áudio
- plug-ins, DSP de áudio
- plug-ins de processamento de sinal digital, descontinuidade de áudio
- Plug-ins do DSP, descontinuidade de áudio
- plug-ins do DSP de áudio, descontinuidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0448220d4616122b3c99670357bbbd78de11c392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363716"
---
# <a name="about-discontinuity"></a><span data-ttu-id="e22eb-108">Sobre a descontinuidade</span><span class="sxs-lookup"><span data-stu-id="e22eb-108">About Discontinuity</span></span>

<span data-ttu-id="e22eb-109">A qualquer momento, o Windows Media Player pode sinalizar uma interrupção no fluxo de entrada chamando o método **IMediaObject::D iscontinuity** .</span><span class="sxs-lookup"><span data-stu-id="e22eb-109">At any time, Windows Media Player can signal a break in the input stream by calling the **IMediaObject::Discontinuity** method.</span></span> <span data-ttu-id="e22eb-110">Isso ocorre rotineiramente no início e no final de um fluxo e também antes de cada operação de busca ou quando o conteúdo de streaming é interrompido por qualquer motivo.</span><span class="sxs-lookup"><span data-stu-id="e22eb-110">This occurs routinely at the start and end of a stream, and also prior to each seek operation or when streaming content is interrupted for any reason.</span></span> <span data-ttu-id="e22eb-111">O plug-in DSP de exemplo gerado pelo assistente de plug-in do Windows Media Player não precisa lidar com o descontinuidades pelos seguintes motivos:</span><span class="sxs-lookup"><span data-stu-id="e22eb-111">The sample DSP plug-in that the Windows Media Player Plug-in wizard generates does not need to deal with discontinuities for the following reasons:</span></span>

-   <span data-ttu-id="e22eb-112">As amostras de PCM são atômicas, o que significa que elas podem ser processadas sem considerar os outros exemplos no fluxo.</span><span class="sxs-lookup"><span data-stu-id="e22eb-112">PCM samples are atomic, meaning they can be processed without regard to the other samples in the stream.</span></span> <span data-ttu-id="e22eb-113">Alguns formatos de vídeo contêm dados que dependem de quadros-chave e amostras compactadas.</span><span class="sxs-lookup"><span data-stu-id="e22eb-113">Some video formats contain data that depends on key frames and compressed samples.</span></span>
-   <span data-ttu-id="e22eb-114">O código de exemplo é escrito para sempre forçar o cliente a processar toda a saída antes que o plug-in aceite mais entradas.</span><span class="sxs-lookup"><span data-stu-id="e22eb-114">The sample code is written to always force the client to process all output before the plug-in will accept more input.</span></span>

<span data-ttu-id="e22eb-115">A implementação padrão de **IMediaObject::D iscontinuity** simplesmente retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e22eb-115">The default implementation of **IMediaObject::Discontinuity** simply returns S\_OK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e22eb-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e22eb-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e22eb-117">**Implementando um plug-in do DSP de áudio**</span><span class="sxs-lookup"><span data-stu-id="e22eb-117">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




