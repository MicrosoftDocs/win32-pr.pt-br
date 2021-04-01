---
description: Capturar um arquivo DV tipo-2
ms.assetid: c7d49c86-1b5d-43bf-98a5-78b297682375
title: Capturar um arquivo DV tipo-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b919928a4c02ce9e3f3f3e6fcf3d2cd376f880a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825547"
---
# <a name="capture-a-type-2-dv-file"></a><span data-ttu-id="a9f4c-103">Capturar um arquivo DV tipo-2</span><span class="sxs-lookup"><span data-stu-id="a9f4c-103">Capture a Type-2 DV File</span></span>

<span data-ttu-id="a9f4c-104">Um arquivo AVI de tipo 2 DV tem dois fluxos, um que contém vídeo DV e outro que contém áudio.</span><span class="sxs-lookup"><span data-stu-id="a9f4c-104">A type-2 DV AVI file has two streams, one that contains DV video and another that contains audio.</span></span> <span data-ttu-id="a9f4c-105">Para capturar um arquivo de tipo 2 durante a visualização, use o gráfico de filtro mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="a9f4c-105">To capture a type-2 file while previewing, use the filter graph shown in the following diagram.</span></span>

![captura do tipo 2 com visualização](images/dv2-cap.png)

<span data-ttu-id="a9f4c-107">Esse grafo é quase o mesmo que o grafo para captura de tipo 1 (consulte [capturar um arquivo DV de tipo 1](capture-a-type-1-dv-file.md)).</span><span class="sxs-lookup"><span data-stu-id="a9f4c-107">This graph is almost the same as the graph for type-1 capture (see [Capture a Type-1 DV File](capture-a-type-1-dv-file.md)).</span></span> <span data-ttu-id="a9f4c-108">No entanto, o fluxo de captura passa pelo filtro de [Splitter de DV](dv-splitter-filter.md) antes de alcançar o filtro [AVI Mux](avi-mux-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="a9f4c-108">However, the capture stream goes through the [DV Splitter](dv-splitter-filter.md) filter before reaching the [AVI Mux](avi-mux-filter.md) filter.</span></span> <span data-ttu-id="a9f4c-109">Portanto, o AVI Mux recebe dois fluxos, um fluxo de áudio e um fluxo de vídeo codificado em DV.</span><span class="sxs-lookup"><span data-stu-id="a9f4c-109">The AVI Mux therefore receives two streams, an audio stream and a DV-encoded video stream.</span></span>

<span data-ttu-id="a9f4c-110">Compile este grafo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a9f4c-110">Build this graph as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)
IBaseFilter           *pAviMux    // Avi Mux filter.
IBaseFilter           *pDVSplit;  // DV Splitter

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Create the DV Splitter and add it to the filter graph.
hr = CoCreateInstance(CLSID_DVSplitter, 0, CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, reinterpret_cast<void**>)(&pDVSplit));
hr = pGraph->AddFilter(pDVSplit, L"DV Splitter");

// Create the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi,
    OLESTR("C:\\Example2.avi"), &pAviMux, 0);

// Connect the capture pin to the DV Splitter, and render one stream from
// the DV Splitter to the AVI Mux. 
hr = pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Interleaved, 
    pDV, pDVSplit, pAviMux);

// Render the other stream from the DV splitter to the AVI Mux.
hr = pBuilder->RenderStream(0, 0, pDVSplit, 0, pAviMux);

// Render the preview stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Interleaved, 
    pDV, 0, 0);

// Remember to release all interfaces.
```



1.  <span data-ttu-id="a9f4c-111">Crie o divisor de DV e adicione-o ao grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="a9f4c-111">Create the DV Splitter and add it to the filter graph.</span></span>
2.  <span data-ttu-id="a9f4c-112">Chame [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) para conectar o filtro AVI Mux ao filtro do gravador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="a9f4c-112">Call [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) to connect the AVI Mux filter to the File Writer filter.</span></span>
3.  <span data-ttu-id="a9f4c-113">Chame [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar o filtro de captura do MSDV ao divisor de DV.</span><span class="sxs-lookup"><span data-stu-id="a9f4c-113">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) to connect the MSDV capture filter to the DV Splitter.</span></span> <span data-ttu-id="a9f4c-114">Essa chamada também conecta um dos Pins de saída do separador de DV ao multiplexador AVI.</span><span class="sxs-lookup"><span data-stu-id="a9f4c-114">This call also connects one of the DV Splitter's output pins to the AVI Mux.</span></span>
4.  <span data-ttu-id="a9f4c-115">Chame RenderStream novamente para conectar o outro PIN do divisor de DV ao AVI Mux.</span><span class="sxs-lookup"><span data-stu-id="a9f4c-115">Call RenderStream again to connect the DV Splitter's other pin to the AVI Mux.</span></span>
5.  <span data-ttu-id="a9f4c-116">Chame RenderStream uma terceira vez para renderizar o fluxo de visualização.</span><span class="sxs-lookup"><span data-stu-id="a9f4c-116">Call RenderStream a third time to render the preview stream.</span></span> <span data-ttu-id="a9f4c-117">Ignore esta etapa se não quiser visualizar o vídeo.</span><span class="sxs-lookup"><span data-stu-id="a9f4c-117">Skip this step if do not want to preview the video.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9f4c-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a9f4c-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9f4c-119">Vídeo digital no DirectShow</span><span class="sxs-lookup"><span data-stu-id="a9f4c-119">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



