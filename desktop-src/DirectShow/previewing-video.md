---
description: Visualizando vídeo
ms.assetid: 9b401de1-910a-41f7-bf80-dda73ee4a204
title: Visualizando vídeo (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0a8f0d0a422794c4e887693e80391a99bd8d70
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104550652"
---
# <a name="previewing-video-directshow"></a><span data-ttu-id="bf19b-103">Visualizando vídeo (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="bf19b-103">Previewing Video (DirectShow)</span></span>

<span data-ttu-id="bf19b-104">Para criar um grafo de visualização de vídeo, chame o método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="bf19b-104">To build a video preview graph, call the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuild; // Capture Graph Builder
// Initialize pBuild (not shown).

IBaseFilter *pCap; // Video capture filter.

/* Initialize pCap and add it to the filter graph (not shown). */

hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
    pCap, NULL, NULL);
```



<span data-ttu-id="bf19b-105">Este exemplo pressupõe o seguinte:</span><span class="sxs-lookup"><span data-stu-id="bf19b-105">This example assumes the following:</span></span>

-   <span data-ttu-id="bf19b-106">o *pBuild* foi inicializado, conforme descrito em [sobre o construtor do grafo de captura](about-the-capture-graph-builder.md).</span><span class="sxs-lookup"><span data-stu-id="bf19b-106">*pBuild* was initialized, as described in [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
-   <span data-ttu-id="bf19b-107">o *pcap* foi inicializado, criando uma instância do filtro de captura e adicionando-a ao grafo de filtro, conforme descrito em [selecionando um dispositivo de captura](selecting-a-capture-device.md).</span><span class="sxs-lookup"><span data-stu-id="bf19b-107">*pCap* was initialized, by creating an instance of the capture filter and adding it to the filter graph, as described in [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>

<span data-ttu-id="bf19b-108">O primeiro parâmetro para o método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) especifica uma categoria de PIN; para um grafo de visualização, use a **\_ \_ Visualização da categoria de PIN**.</span><span class="sxs-lookup"><span data-stu-id="bf19b-108">The first parameter to the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method specifies a pin category; for a preview graph, use **PIN\_CATEGORY\_PREVIEW**.</span></span> <span data-ttu-id="bf19b-109">O segundo parâmetro especifica um tipo de mídia, como um GUID de tipo principal.</span><span class="sxs-lookup"><span data-stu-id="bf19b-109">The second parameter specifies a media type, as a major type GUID.</span></span> <span data-ttu-id="bf19b-110">Para vídeo, use **o \_ vídeo de MediaType**.</span><span class="sxs-lookup"><span data-stu-id="bf19b-110">For video, use **MEDIATYPE\_Video**.</span></span> <span data-ttu-id="bf19b-111">Os dispositivos DV entregam áudio e vídeo intercalados, para os quais o tipo de mídia é a **\_ dicalada de MediaType**.</span><span class="sxs-lookup"><span data-stu-id="bf19b-111">DV devices deliver interleaved audio and video, for which the media type is **MEDIATYPE\_Interleaved**.</span></span> <span data-ttu-id="bf19b-112">(Para obter mais informações sobre o DV Capture, consulte [vídeo digital no DirectShow](digital-video-in-directshow.md).)</span><span class="sxs-lookup"><span data-stu-id="bf19b-112">(For more information about DV capture, see [Digital Video in DirectShow](digital-video-in-directshow.md).)</span></span>

<span data-ttu-id="bf19b-113">O terceiro parâmetro é um ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="bf19b-113">The third parameter is a pointer to the capture filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="bf19b-114">Os próximos dois parâmetros não são necessários neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="bf19b-114">The next two parameters are not needed in this example.</span></span> <span data-ttu-id="bf19b-115">Eles são usados para especificar filtros adicionais que podem ser necessários para renderizar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="bf19b-115">They are used to specify additional filters that might be needed to render the stream.</span></span> <span data-ttu-id="bf19b-116">Definir o último parâmetro como **NULL** faz com que o construtor do grafo de captura selecione um renderizador padrão para o fluxo, com base no tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="bf19b-116">Setting the last parameter to **NULL** causes the Capture Graph Builder to select a default renderer for the stream, based on the media type.</span></span> <span data-ttu-id="bf19b-117">Para vídeo, o construtor de gráficos de captura sempre usa o filtro de [processador de vídeo](video-renderer-filter.md) como o renderizador padrão.</span><span class="sxs-lookup"><span data-stu-id="bf19b-117">For video, the Capture Graph Builder always uses the [Video Renderer](video-renderer-filter.md) filter as the default renderer.</span></span>

> [!Note]  
> <span data-ttu-id="bf19b-118">No Windows XP e posterior, embora o VMR (Video mixagem Renderer) seja o processador de vídeo padrão para os métodos [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) , ele não é o renderizador padrão para o método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) .</span><span class="sxs-lookup"><span data-stu-id="bf19b-118">In Windows XP and later, although the Video Mixing Renderer (VMR) is the default video renderer for [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) methods, it is not the default renderer for the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method.</span></span> <span data-ttu-id="bf19b-119">Em qualquer plataforma, o construtor de grafo de captura sempre usa o filtro de processamento de vídeo antigo, a menos que você especifique o contrário.</span><span class="sxs-lookup"><span data-stu-id="bf19b-119">On any platform, the Capture Graph Builder always uses the old Video Renderer filter unless you specify otherwise.</span></span>

 

<span data-ttu-id="bf19b-120">Embora a categoria de PIN seja fornecida **como \_ \_ visualização de categoria de PIN**, não importa se o filtro realmente tem um pino de visualização; ele pode ter um PIN de porta de vídeo ou apenas um PIN de captura.</span><span class="sxs-lookup"><span data-stu-id="bf19b-120">Although the pin category is given as **PIN\_CATEGORY\_PREVIEW**, it does not matter whether the filter actually has a preview pin; it could have a video port pin or just a capture pin.</span></span> <span data-ttu-id="bf19b-121">Em ambos os casos, o construtor do grafo de captura cria automaticamente o grafo correto.</span><span class="sxs-lookup"><span data-stu-id="bf19b-121">In either case, the Capture Graph Builder automatically builds the correct graph.</span></span>

<span data-ttu-id="bf19b-122">O diagrama a seguir mostra o grafo mais simples possível para visualização de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bf19b-122">The following diagram shows the simplest possible graph for previewing video.</span></span>

![Grafo de visualização de vídeo](images/vidcap01.png)

<span data-ttu-id="bf19b-124">Neste diagrama, o filtro de captura tem um pino de visualização, que se conecta diretamente ao processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bf19b-124">In this diagram, the capture filter has a preview pin, which connects directly to the video renderer.</span></span>

<span data-ttu-id="bf19b-125">Se o filtro de captura tiver apenas um PIN de captura, o construtor do grafo de captura inserirá um filtro de " [t" inteligente](smart-tee-filter.md) , que dividirá o fluxo em um fluxo de captura e um fluxo de visualização.</span><span class="sxs-lookup"><span data-stu-id="bf19b-125">If the capture filter has only a capture pin, the Capture Graph Builder inserts a [Smart Tee](smart-tee-filter.md) filter, which splits the stream into a capture stream and a preview stream.</span></span> <span data-ttu-id="bf19b-126">Isso é descrito mais detalhadamente na [combinação de captura de vídeo e visualização](combining-video-capture-and-preview.md).</span><span class="sxs-lookup"><span data-stu-id="bf19b-126">This is described in more detail in [Combining Video Capture and Preview](combining-video-capture-and-preview.md).</span></span>

<span data-ttu-id="bf19b-127">Em alguns casos, o fluxo de vídeo deve passar pelo filtro de mixer de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="bf19b-127">In some cases, the video stream must go through the Overlay Mixer filter.</span></span> <span data-ttu-id="bf19b-128">Nesse caso, o método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) o adiciona automaticamente ao grafo.</span><span class="sxs-lookup"><span data-stu-id="bf19b-128">If so, the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method adds it to the graph automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf19b-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bf19b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf19b-130">Combinando captura de vídeo e visualização</span><span class="sxs-lookup"><span data-stu-id="bf19b-130">Combining Video Capture and Preview</span></span>](combining-video-capture-and-preview.md)
</dt> <dt>

[<span data-ttu-id="bf19b-131">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="bf19b-131">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



