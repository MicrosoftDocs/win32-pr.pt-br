---
description: Capturar um arquivo DV tipo-1
ms.assetid: fba11e9b-4900-4b29-a0c9-702272cd7387
title: Capturar um arquivo DV tipo-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8098669f124bdd4c0168e3549cd8eed8e1825c47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104564955"
---
# <a name="capture-a-type-1-dv-file"></a><span data-ttu-id="81897-103">Capturar um arquivo DV tipo-1</span><span class="sxs-lookup"><span data-stu-id="81897-103">Capture a Type-1 DV File</span></span>

<span data-ttu-id="81897-104">Um arquivo AVI de tipo 1 DV contém um único fluxo intercalado.</span><span class="sxs-lookup"><span data-stu-id="81897-104">A type-1 DV AVI file contains a single interleaved stream.</span></span> <span data-ttu-id="81897-105">Para capturar um arquivo do tipo 1 durante a visualização, use o gráfico de filtro mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="81897-105">To capture a type-1 file while previewing, use the filter graph shown in the following diagram.</span></span>

![captura do tipo 1 com visualização](images/dv1-cap.png)

<span data-ttu-id="81897-107">Os filtros neste grafo incluem:</span><span class="sxs-lookup"><span data-stu-id="81897-107">Filters in this graph include:</span></span>

-   <span data-ttu-id="81897-108">O filtro de visões [inteligentes](smart-tee-filter.md) divide o DV intercalado em um fluxo de captura e um fluxo de visualização.</span><span class="sxs-lookup"><span data-stu-id="81897-108">The [Smart Tee](smart-tee-filter.md) filter splits the interleaved DV into a capture stream and a preview stream.</span></span> <span data-ttu-id="81897-109">Ambos os fluxos contêm os mesmos dados intercalados.</span><span class="sxs-lookup"><span data-stu-id="81897-109">Both streams contain the same interleaved data.</span></span>
-   <span data-ttu-id="81897-110">O [multiplexador AVI](avi-mux-filter.md) e o [gravador de arquivo](file-writer-filter.md) gravam o fluxo intercalado em disco.</span><span class="sxs-lookup"><span data-stu-id="81897-110">The [AVI Mux](avi-mux-filter.md) and [File Writer](file-writer-filter.md) write the interleaved stream to disk.</span></span>
-   <span data-ttu-id="81897-111">O [divisor de DV](dv-splitter-filter.md) divide o fluxo intercalado em um fluxo de vídeo DV e um fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="81897-111">The [DV Splitter](dv-splitter-filter.md) splits the interleaved stream into a DV video stream and an audio stream.</span></span> <span data-ttu-id="81897-112">Ambos os fluxos são renderizados para visualização.</span><span class="sxs-lookup"><span data-stu-id="81897-112">Both streams are rendererd for preview.</span></span>
-   <span data-ttu-id="81897-113">O [decodificador de vídeo DV](dv-video-decoder-filter.md) decodifica o fluxo de vídeo DV para visualização.</span><span class="sxs-lookup"><span data-stu-id="81897-113">The [DV Video Decoder](dv-video-decoder-filter.md) decodes the DV video stream for previewing.</span></span>

<span data-ttu-id="81897-114">Compile este grafo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="81897-114">Build this graph as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)
IBaseFilter           *pAviMux    // Avi Mux filter.

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Create the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("C:\\Example1.avi"), &pAviMux, 0);

// Render the capture stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Interleaved, 
    pDV, 0, pAviMux);

// Render the preview stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Interleaved,
    pDV, 0, 0);

// Remember to release all interfaces.
```



1.  <span data-ttu-id="81897-115">Chame [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) para conectar o filtro AVI Mux ao filtro do gravador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="81897-115">Call [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) to connect the AVI Mux filter to the File Writer filter.</span></span>
2.  <span data-ttu-id="81897-116">Chame [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) com a categoria de fixação fixar a \_ captura de categoria \_ para renderizar o fluxo de captura.</span><span class="sxs-lookup"><span data-stu-id="81897-116">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) with the pin category PIN\_CATEGORY\_CAPTURE to render the capture stream.</span></span> <span data-ttu-id="81897-117">O construtor do grafo de captura insere automaticamente o filtro de "t inteligente".</span><span class="sxs-lookup"><span data-stu-id="81897-117">The Capture Graph Builder automatically inserts the Smart Tee filter.</span></span>
3.  <span data-ttu-id="81897-118">Chame RenderStream novamente, mas com a categoria PIN Category de PIN \_ \_ Preview, para renderizar o fluxo de visualização.</span><span class="sxs-lookup"><span data-stu-id="81897-118">Call RenderStream again, but with the pin category PIN\_CATEGORY\_PREVIEW, to render the preview stream.</span></span> <span data-ttu-id="81897-119">Ignore esta chamada se não quiser visualizar o vídeo.</span><span class="sxs-lookup"><span data-stu-id="81897-119">Skip this call if you do not want to preview the video.</span></span>

<span data-ttu-id="81897-120">Para ambas as chamadas para RenderStream, o tipo de mídia é \_ dicalado de MediaType, o que significa vídeo intercalado em DV.</span><span class="sxs-lookup"><span data-stu-id="81897-120">For both calls to RenderStream, the media type is MEDIATYPE\_Interleaved, meaning interleaved DV video.</span></span> <span data-ttu-id="81897-121">Nesse código, o construtor do grafo de captura adiciona automaticamente cada filtro necessário, exceto para o filtro de captura MSDV.</span><span class="sxs-lookup"><span data-stu-id="81897-121">In this code, the Capture Graph Builder automatically adds every filter that is needed, except for the MSDV capture filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81897-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="81897-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81897-123">Vídeo digital no DirectShow</span><span class="sxs-lookup"><span data-stu-id="81897-123">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



