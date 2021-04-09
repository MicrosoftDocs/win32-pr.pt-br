---
description: Modos de Run-Time Demux MPEG-2
ms.assetid: b0d0c725-9220-43a5-af1c-d3c5c72e1ef3
title: Modos de Run-Time Demux MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e4e7a1dea0bfeccd60d8680a31b99cc10271ee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087838"
---
# <a name="mpeg-2-demux-run-time-modes"></a><span data-ttu-id="f50f2-103">Modos de Run-Time Demux MPEG-2</span><span class="sxs-lookup"><span data-stu-id="f50f2-103">MPEG-2 Demux Run-Time Modes</span></span>

<span data-ttu-id="f50f2-104">O [demultiplexador MPEG-2](mpeg-2-demultiplexer.md) ("Demux") pode operar no modo de Push ou no modo de pull.</span><span class="sxs-lookup"><span data-stu-id="f50f2-104">The [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) ("demux") can operate in push mode or pull mode.</span></span> <span data-ttu-id="f50f2-105">No modo de push, os dados são provenientes de uma fonte dinâmica, como uma difusão de rede.</span><span class="sxs-lookup"><span data-stu-id="f50f2-105">In push mode, the data comes from a live source, such as a network broadcast.</span></span> <span data-ttu-id="f50f2-106">No modo de pull, os dados vêm de um arquivo local.</span><span class="sxs-lookup"><span data-stu-id="f50f2-106">In pull mode, the data comes from a local file.</span></span>

-   <span data-ttu-id="f50f2-107">O modo de pull está disponível no Windows XP e posterior, somente para fluxos de programa.</span><span class="sxs-lookup"><span data-stu-id="f50f2-107">Pull mode is available in Windows XP and later, for program streams only.</span></span> <span data-ttu-id="f50f2-108">Em plataformas de nível inferior, use o filtro [divisor MPEG-2](mpeg-2-splitter.md) .</span><span class="sxs-lookup"><span data-stu-id="f50f2-108">On down-level platforms, use the [MPEG-2 Splitter](mpeg-2-splitter.md) filter.</span></span>
-   <span data-ttu-id="f50f2-109">O modo de Push está disponível em todas as plataformas, para fluxos de programa e fluxos de transporte.</span><span class="sxs-lookup"><span data-stu-id="f50f2-109">Push mode is available on all platforms, for both program streams and transport streams.</span></span>

<span data-ttu-id="f50f2-110">O Demux, portanto, dá suporte a três modos possíveis: fluxos de programa no modo de pull, fluxos de programa no modo de push e fluxos de transporte no modo de push.</span><span class="sxs-lookup"><span data-stu-id="f50f2-110">The demux therefore supports three possible modes: Program streams in pull mode, program streams in push mode, and transport streams in push mode.</span></span> <span data-ttu-id="f50f2-111">O Demux determina qual modo usar em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="f50f2-111">The demux determines which mode to use at run time.</span></span> <span data-ttu-id="f50f2-112">O modo é determinado quando o PIN de entrada se conecta ou quando o primeiro PIN de saída é configurado, o que acontecer primeiro:</span><span class="sxs-lookup"><span data-stu-id="f50f2-112">The mode is determined when the input pin connects, or when the first output pin is configured, whichever happens first:</span></span>

-   <span data-ttu-id="f50f2-113">Quando o PIN de entrada se conecta: no Windows XP e posterior, o Demux consulta o filtro upstream para a interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) ; Se o filtro upstream expõe essa interface, o Demux se configura para fluxos de programa no modo de pull.</span><span class="sxs-lookup"><span data-stu-id="f50f2-113">When the input pin connects: On Windows XP and later, the demux queries the upstream filter for the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface; if the upstream filter exposes that interface, the demux configures itself for program streams in pull mode.</span></span> <span data-ttu-id="f50f2-114">Caso contrário, o Demux usará o modo de push e o tipo de mídia determinará o tipo de fluxo (fluxo do programa ou fluxo de transporte).</span><span class="sxs-lookup"><span data-stu-id="f50f2-114">Otherwise, the demux uses push mode, and the media type determines the stream type (program stream or transport stream).</span></span> <span data-ttu-id="f50f2-115">Consulte [**tipos de mídia do demultiplexador MPEG-2**](mpeg-2-demultiplexer-media-types.md) para obter uma lista de tipos de entrada.</span><span class="sxs-lookup"><span data-stu-id="f50f2-115">See [**MPEG-2 Demultiplexer Media Types**](mpeg-2-demultiplexer-media-types.md) for a list of input types.</span></span>
-   <span data-ttu-id="f50f2-116">Quando o primeiro PIN de saída estiver configurado: se você criar um PIN de saída e consultá-lo para [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap), o Demux se configurará para fluxos de transporte no modo de push.</span><span class="sxs-lookup"><span data-stu-id="f50f2-116">When the first output pin is configured: If you create an output pin and query it for [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap), the demux configures itself for transport streams in push mode.</span></span> <span data-ttu-id="f50f2-117">Se você consultar o PIN para [**IMPEG2StreamIdMap**](/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap), o Demux se configurará para fluxos de programa, também no modo de push.</span><span class="sxs-lookup"><span data-stu-id="f50f2-117">If you query the pin for [**IMPEG2StreamIdMap**](/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap), the demux configures itself for program streams, also in push mode.</span></span> <span data-ttu-id="f50f2-118">Todas as consultas subsequentes para a outra interface falham, porque o Demux não pode operar em dois modos de uma vez.</span><span class="sxs-lookup"><span data-stu-id="f50f2-118">Any subsequent queries for the other interface fail, because the demux cannot operate in two modes at once.</span></span>

<span data-ttu-id="f50f2-119">Depois que o Demux tiver se configurado para um modo específico, ele permanecerá nesse modo.</span><span class="sxs-lookup"><span data-stu-id="f50f2-119">Once the demux has configured itself for a particular mode, it remains in that mode.</span></span> <span data-ttu-id="f50f2-120">Para usar um modo diferente, você deve criar uma nova instância do Demux.</span><span class="sxs-lookup"><span data-stu-id="f50f2-120">To use a different mode, you must create a new instance of the demux.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f50f2-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f50f2-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f50f2-122">Usando o demultiplexador MPEG-2</span><span class="sxs-lookup"><span data-stu-id="f50f2-122">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



