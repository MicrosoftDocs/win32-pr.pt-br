---
description: Transmitir do arquivo do tipo-1
ms.assetid: 5be2248b-7917-4c1b-9ae7-29e06779eac6
title: Transmitir do arquivo do tipo-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e38ed3e549b6cd671248ba1df9b24df8fbfe3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011170"
---
# <a name="transmit-from-type-1-file"></a><span data-ttu-id="43e87-103">Transmitir do arquivo do tipo-1</span><span class="sxs-lookup"><span data-stu-id="43e87-103">Transmit from Type-1 File</span></span>

<span data-ttu-id="43e87-104">Para transmitir um arquivo do tipo 1 durante a visualização do arquivo, use o gráfico de filtro mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="43e87-104">To transmit a type-1 file while previewing the file, use the filter graph shown in the following diagram.</span></span>

![tipo-1 transmissão com visualização](images/dv1-transmit.png)

<span data-ttu-id="43e87-106">Os filtros neste grafo incluem:</span><span class="sxs-lookup"><span data-stu-id="43e87-106">Filters in this graph include:</span></span>

-   <span data-ttu-id="43e87-107">O [divisor AVI](avi-splitter-filter.md) analisa o arquivo avi.</span><span class="sxs-lookup"><span data-stu-id="43e87-107">The [AVI Splitter](avi-splitter-filter.md) parses the AVI file.</span></span> <span data-ttu-id="43e87-108">Para um arquivo DV tipo-1, o pino de saída entrega exemplos de DV intercalados.</span><span class="sxs-lookup"><span data-stu-id="43e87-108">For a type-1 DV file, the output pin delivers interleaved DV samples.</span></span>
-   <span data-ttu-id="43e87-109">O filtro de [t de PIN infinito](infinite-pin-tee-filter.md) divide o DV intercalado em um fluxo de transmissão e um fluxo de visualização.</span><span class="sxs-lookup"><span data-stu-id="43e87-109">The [Infinite Pin Tee](infinite-pin-tee-filter.md) filter splits the interleaved DV into a transmit stream and a preview stream.</span></span> <span data-ttu-id="43e87-110">Ambos os fluxos contêm os mesmos dados intercalados.</span><span class="sxs-lookup"><span data-stu-id="43e87-110">Both streams contain the same interleaved data.</span></span> <span data-ttu-id="43e87-111">(Esse grafo usa o "t" de PIN infinito, em vez do ativo [inteligente](smart-tee-filter.md), porque não há nenhum risco de descartar quadros ao ler de um arquivo, pois há com a captura dinâmica.)</span><span class="sxs-lookup"><span data-stu-id="43e87-111">(This graph uses the Infinite Pin Tee instead of the [Smart Tee](smart-tee-filter.md), because there is no danger of dropping frames when reading from a file, as there is with live capture.)</span></span>
-   <span data-ttu-id="43e87-112">O [divisor de DV](dv-splitter-filter.md) divide o fluxo intercalado em um fluxo de vídeo DV, que é decodificado pelo [codificador de vídeo DV](dv-video-decoder-filter.md)e um fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="43e87-112">The [DV Splitter](dv-splitter-filter.md) splits the interleaved stream into a DV video stream, which is decoded by the [DV Video Decoder](dv-video-decoder-filter.md), and an audio stream.</span></span> <span data-ttu-id="43e87-113">Ambos os fluxos são renderizados para visualização.</span><span class="sxs-lookup"><span data-stu-id="43e87-113">Both streams are rendererd for preview.</span></span>

<span data-ttu-id="43e87-114">Compile este grafo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="43e87-114">Build this graph as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Add the Infinite Pin Tee filter to the graph.
IBaseFilter *pTee;
hr = CoCreateInstance(CLSID_InfTee, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pTee));
hr = pGraph->AddFilter(pTee, L"Tee");

// Add the File Source filter to the graph.
IBaseFilter *pFileSource;
hr = pGraph->AddSourceFilter(
    L"C:\\YourFileNameHere.avi",
    L"Source", 
    &pFileSource);

// Add the AVI Splitter filter to the graph.
IBaseFilter *pAviSplit;
hr = CoCreateInstance(CLSID_AviSplitter, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pAviSplit));
hr = pGraph->AddFilter(pAviSplit, L"AVI Splitter");

// Connect the file source to the AVI Splitter.
hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pAviSplit);
if (FAILED(hr))
{
    // This is not an AVI file. 
}

// Connect the file source to the Infinite Pin Tee.
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pAviSplit, 0, pTee);
if (FAILED(hr))
{
    // This is not a type-1 DV file.
}

// Render one stream from the Infinite Pin Tee to MSDV, for transmit.
hr = pBuilder->RenderStream(0, 0, pTee, 0, pDV);

// Render another stream from the Infinite Pin Tee for preview.
hr = pBuilder->RenderStream(0, 0, pTee, 0, 0);
```



1.  <span data-ttu-id="43e87-115">Chame [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) para adicionar o filtro de origem ao grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="43e87-115">Call [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) to add the source filter to the filter graph.</span></span>
2.  <span data-ttu-id="43e87-116">Crie o separador AVI e o "t" de PIN infinito e adicione-os ao grafo.</span><span class="sxs-lookup"><span data-stu-id="43e87-116">Create the AVI Splitter and the Infinite Pin Tee, and add them to the graph.</span></span>
3.  <span data-ttu-id="43e87-117">Chame [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar o filtro de origem ao divisor avi.</span><span class="sxs-lookup"><span data-stu-id="43e87-117">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) to connect the source filter to the AVI Splitter.</span></span> <span data-ttu-id="43e87-118">Especificar MEDIATYPE \_ intercalado para garantir que o método falhe se o arquivo de origem não for um arquivo DV tipo-1.</span><span class="sxs-lookup"><span data-stu-id="43e87-118">Specifying MEDIATYPE\_Interleaved to ensure that the method fails if the source file is not a type-1 DV file.</span></span> <span data-ttu-id="43e87-119">Nesse caso, você pode fazer backup e tentar criar um grafo de transmissão tipo 2 em vez disso.</span><span class="sxs-lookup"><span data-stu-id="43e87-119">In that case, you can back out and attempt to build a type-2 transmit graph instead.</span></span>
4.  <span data-ttu-id="43e87-120">Chame **RenderStream** novamente para rotear o fluxo intercalado do separador AVI para o "t" de PIN infinito</span><span class="sxs-lookup"><span data-stu-id="43e87-120">Call **RenderStream** again to route the interleaved stream from the AVI Splitter to the Infinite Pin Tee</span></span>
5.  <span data-ttu-id="43e87-121">Chame o RenderStream uma terceira vez para rotear um fluxo do "t" de PIN infinito para o filtro MSDV, para transmitir para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43e87-121">Call RenderStream a third time to route one stream from the Infinite Pin Tee to the MSDV filter, for transmit to the device.</span></span>
6.  <span data-ttu-id="43e87-122">Chame **RenderStream** uma última vez para criar a seção de visualização do grafo.</span><span class="sxs-lookup"><span data-stu-id="43e87-122">Call **RenderStream** one last time, to build the preview section of the graph.</span></span>

<span data-ttu-id="43e87-123">Se você não quiser a visualização, basta conectar a origem do arquivo ao filtro MSDV:</span><span class="sxs-lookup"><span data-stu-id="43e87-123">If you do not want preview, simply connect the file source to the MSDV filter:</span></span>


```C++
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pFileSource, 0, pDV);
```



## <a name="related-topics"></a><span data-ttu-id="43e87-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="43e87-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43e87-125">Vídeo digital no DirectShow</span><span class="sxs-lookup"><span data-stu-id="43e87-125">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



