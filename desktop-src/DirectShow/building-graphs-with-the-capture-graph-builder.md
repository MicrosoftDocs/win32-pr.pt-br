---
description: Criando gráficos com o construtor de grafo de captura
ms.assetid: 0329c4f0-ee6f-423e-b38b-169204e3a31c
title: Criando gráficos com o construtor de grafo de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4e48347a73cdac545723ac226cc58a0175dec5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825986"
---
# <a name="building-graphs-with-the-capture-graph-builder"></a><span data-ttu-id="7ed73-103">Criando gráficos com o construtor de grafo de captura</span><span class="sxs-lookup"><span data-stu-id="7ed73-103">Building Graphs with the Capture Graph Builder</span></span>

<span data-ttu-id="7ed73-104">Apesar do seu nome, o construtor do grafo de captura é útil para criar muitos tipos de grafos de filtro personalizados, não apenas para capturar grafos.</span><span class="sxs-lookup"><span data-stu-id="7ed73-104">Despite its name, the Capture Graph Builder is useful for building many kinds of custom filter graphs, not only capture graphs.</span></span> <span data-ttu-id="7ed73-105">Este artigo fornece uma breve visão geral de como usar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="7ed73-105">This article provides a brief overview of how to use this object.</span></span>

<span data-ttu-id="7ed73-106">O construtor do grafo de captura expõe a interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) .</span><span class="sxs-lookup"><span data-stu-id="7ed73-106">The Capture Graph Builder exposes the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface.</span></span> <span data-ttu-id="7ed73-107">Comece chamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar o construtor de grafo de captura e o Gerenciador de gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="7ed73-107">Start by calling [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Capture Graph Builder and the Filter Graph Manager.</span></span> <span data-ttu-id="7ed73-108">Em seguida, inicialize o construtor do grafo de captura chamando [**ICaptureGraphBuilder2:: SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) com um ponteiro para o Gerenciador do grafo de filtro, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7ed73-108">Then initialize the Capture Graph Builder by calling [**ICaptureGraphBuilder2::SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) with a pointer to the Filter Graph Manager, as follows:</span></span>


```C++
IGraphBuilder *pGraph = NULL;
ICaptureGraphBuilder2 *pBuilder = NULL;

// Create the Filter Graph Manager.
HRESULT hr =  CoCreateInstance(CLSID_FilterGraph, NULL,
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);

if (SUCCEEDED(hr))
{
    // Create the Capture Graph Builder.
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL,
        CLSCTX_INPROC_SERVER, IID_ICaptureGraphBuilder2, 
        (void **)&pBuilder);
    if (SUCCEEDED(hr))
    {
        pBuilder->SetFiltergraph(pGraph);
    }
};
```



## <a name="connecting-filters"></a><span data-ttu-id="7ed73-109">Filtros de conexão</span><span class="sxs-lookup"><span data-stu-id="7ed73-109">Connecting Filters</span></span>

<span data-ttu-id="7ed73-110">O método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) conecta dois ou três filtros juntos em uma cadeia.</span><span class="sxs-lookup"><span data-stu-id="7ed73-110">The [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method connects two or three filters together in a chain.</span></span> <span data-ttu-id="7ed73-111">Em geral, o método funciona melhor quando cada filtro tem no máximo um PIN de entrada ou um pino de saída do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="7ed73-111">Generally, the method works best when each filter has no more than one input pin or output pin of the same type.</span></span> <span data-ttu-id="7ed73-112">Essa discussão começa ignorando os dois primeiros parâmetros de **RenderStream** e concentrando-se nos últimos três parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7ed73-112">This discussion begins by ignoring the first two parameters of **RenderStream** and focusing on the last three parameters.</span></span> <span data-ttu-id="7ed73-113">O terceiro parâmetro é um ponteiro [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , que pode especificar um filtro (como um ponteiro de interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) ) ou um pino de saída (como um ponteiro de interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) ).</span><span class="sxs-lookup"><span data-stu-id="7ed73-113">The third parameter is an [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer, which can specify either a filter (as an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface pointer) or an output pin (as an [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface pointer).</span></span> <span data-ttu-id="7ed73-114">O quarto e o quinto parâmetros especificam ponteiros **IBaseFilter** .</span><span class="sxs-lookup"><span data-stu-id="7ed73-114">The fourth and fifth parameters specify **IBaseFilter** pointers.</span></span> <span data-ttu-id="7ed73-115">O método **RenderStream** conecta todos os três filtros em uma cadeia.</span><span class="sxs-lookup"><span data-stu-id="7ed73-115">The **RenderStream** method connects all three filters in a chain.</span></span> <span data-ttu-id="7ed73-116">Por exemplo, suponha que *A*, *B* e *C* sejam filtros.</span><span class="sxs-lookup"><span data-stu-id="7ed73-116">For example, suppose that *A*, *B*, and *C* are filters.</span></span> <span data-ttu-id="7ed73-117">Suponha que, por enquanto, cada filtro tenha exatamente um PIN de entrada e um pino de saída.</span><span class="sxs-lookup"><span data-stu-id="7ed73-117">Assume for now that each filter has exactly one input pin and one output pin.</span></span> <span data-ttu-id="7ed73-118">A chamada a seguir conecta a a B e, em seguida, B a C:</span><span class="sxs-lookup"><span data-stu-id="7ed73-118">The following call connects A to B, and then B to C:</span></span>

<dl> `RenderStream(NULL, NULL, A, B, C)`  
</dl>

<span data-ttu-id="7ed73-119">Todas as conexões são "inteligentes", o que significa que filtros adicionais são adicionados ao grafo, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="7ed73-119">All connections are "intelligent," meaning that additional filters are added to the graph as needed.</span></span> <span data-ttu-id="7ed73-120">Para obter detalhes, consulte [conexão inteligente](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="7ed73-120">For details, see [Intelligent Connect](intelligent-connect.md).</span></span> <span data-ttu-id="7ed73-121">Para conectar apenas dois filtros, defina o valor intermediário como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="7ed73-121">To connect just two filters, set the middle value to **NULL**.</span></span> <span data-ttu-id="7ed73-122">Por exemplo, essa chamada conecta a a C:</span><span class="sxs-lookup"><span data-stu-id="7ed73-122">For example, this call connects A to C:</span></span>

<dl> `RenderStream(NULL, NULL, A, NULL, C)`  
</dl>

<span data-ttu-id="7ed73-123">Você pode criar cadeias mais longas chamando o método duas vezes:</span><span class="sxs-lookup"><span data-stu-id="7ed73-123">You can create longer chains by calling the method twice:</span></span>

<dl> `RenderStream(NULL, NULL, A, B, C)`  
`RenderStream(NULL, NULL, C, D, E)`  
</dl>

<span data-ttu-id="7ed73-124">Se o último parâmetro for **nulo**, o método localizará automaticamente um renderizador padrão.</span><span class="sxs-lookup"><span data-stu-id="7ed73-124">If the last parameter is **NULL**, the method automatically locates a default renderer.</span></span> <span data-ttu-id="7ed73-125">Ele usa o [processador de vídeo](video-renderer-filter.md) para vídeo e o [renderizador DirectSound](directsound-renderer-filter.md) para áudio.</span><span class="sxs-lookup"><span data-stu-id="7ed73-125">It uses the [Video Renderer](video-renderer-filter.md) for video and the [DirectSound Renderer](directsound-renderer-filter.md) for audio.</span></span> <span data-ttu-id="7ed73-126">Dessa</span><span class="sxs-lookup"><span data-stu-id="7ed73-126">Thus:</span></span>

<dl> `RenderStream(NULL, NULL, A, NULL, NULL)`  
</dl>

<span data-ttu-id="7ed73-127">é equivalente a</span><span class="sxs-lookup"><span data-stu-id="7ed73-127">is equivalent to</span></span>

<dl> `RenderStream(NULL, NULL, A, NULL, R)`  
</dl>

<span data-ttu-id="7ed73-128">em que *R* é o renderizador apropriado.</span><span class="sxs-lookup"><span data-stu-id="7ed73-128">where *R* is the appropriate renderer.</span></span> <span data-ttu-id="7ed73-129">Para conectar o filtro de processador de mixagem de vídeo em vez do processador de vídeo, no entanto, você deve especificá-lo explicitamente.</span><span class="sxs-lookup"><span data-stu-id="7ed73-129">To connect the Video Mixing Renderer filter instead of the Video Renderer, however, you must specify it explicitly.</span></span>

<span data-ttu-id="7ed73-130">Se você especificar um filtro no terceiro parâmetro, em vez de um PIN, talvez seja necessário indicar qual pino de saída deve ser usado para a conexão.</span><span class="sxs-lookup"><span data-stu-id="7ed73-130">If you specify a filter in the third parameter, rather than a pin, you may need to indicate which output pin should be used for the connection.</span></span> <span data-ttu-id="7ed73-131">Essa é a finalidade dos dois primeiros parâmetros do método.</span><span class="sxs-lookup"><span data-stu-id="7ed73-131">That is the purpose of the method's first two parameters.</span></span> <span data-ttu-id="7ed73-132">O primeiro parâmetro se aplica somente a filtros de captura.</span><span class="sxs-lookup"><span data-stu-id="7ed73-132">The first parameter applies only to capture filters.</span></span> <span data-ttu-id="7ed73-133">Especifica um GUID que indica uma categoria de PIN.</span><span class="sxs-lookup"><span data-stu-id="7ed73-133">It specifies a GUID that indicates a pin category.</span></span> <span data-ttu-id="7ed73-134">Para obter uma lista completa de categorias, consulte [Pin Property Set](pin-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="7ed73-134">For a complete list of categories, see [Pin Property Set](pin-property-set.md).</span></span> <span data-ttu-id="7ed73-135">Duas das categorias são válidas para todos os filtros de captura:</span><span class="sxs-lookup"><span data-stu-id="7ed73-135">Two of the categories are valid for all capture filters:</span></span>

-   <span data-ttu-id="7ed73-136">**FIXAR \_ captura de categoria \_**</span><span class="sxs-lookup"><span data-stu-id="7ed73-136">**PIN\_CATEGORY\_CAPTURE**</span></span>
-   <span data-ttu-id="7ed73-137">**FIXAR \_ Visualização da categoria \_**</span><span class="sxs-lookup"><span data-stu-id="7ed73-137">**PIN\_CATEGORY\_PREVIEW**</span></span>

<span data-ttu-id="7ed73-138">Se um filtro de captura não fornecer Pins separados para captura e visualização, o método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) inserirá um filtro de " [t" inteligente](smart-tee-filter.md) , que dividirá o fluxo em um fluxo de captura e um fluxo de visualização.</span><span class="sxs-lookup"><span data-stu-id="7ed73-138">If a capture filter does not supply separate pins for capture and preview, the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method inserts a [Smart Tee](smart-tee-filter.md) filter, which splits the stream into a capture stream and a preview stream.</span></span> <span data-ttu-id="7ed73-139">Do ponto de vista do aplicativo, você pode simplesmente tratar todos os filtros de captura como tendo os Pins separados e ignorar a topologia subjacente do grafo.</span><span class="sxs-lookup"><span data-stu-id="7ed73-139">From the application's standpoint, you can simply treat all capture filters as having separate pins and ignore the underlying topology of the graph.</span></span>

<span data-ttu-id="7ed73-140">Para a captura de arquivos, conecte o PIN de captura a um filtro Mux.</span><span class="sxs-lookup"><span data-stu-id="7ed73-140">For file capture, connect the capture pin to a mux filter.</span></span> <span data-ttu-id="7ed73-141">Para a visualização dinâmica, conecte o pino de visualização a um processador.</span><span class="sxs-lookup"><span data-stu-id="7ed73-141">For live preview, connect the preview pin to a renderer.</span></span> <span data-ttu-id="7ed73-142">Se você alternar as duas categorias, o grafo poderá remover um número excessivo de quadros durante a captura de arquivo; Mas se o grafo estiver conectado corretamente, ele descartará os quadros de visualização conforme necessário para manter a taxa de transferência no fluxo de captura.</span><span class="sxs-lookup"><span data-stu-id="7ed73-142">If you switch the two categories, the graph might drop an excessive number of frames during the file capture; but if the graph is connected properly, it drops preview frames as needed in order to maintain throughput on the capture stream.</span></span>

<span data-ttu-id="7ed73-143">O exemplo a seguir mostra como conectar ambos os fluxos:</span><span class="sxs-lookup"><span data-stu-id="7ed73-143">The following example shows how to connect both streams:</span></span>


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, NULL, pCapFilter, NULL, pMux);
// Preview:
pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, NULL, pCapFilter, NULL, NULL);
```



<span data-ttu-id="7ed73-144">Alguns filtros de captura também dão suporte a legendas codificadas, indicadas pela **categoria de PIN \_ \_ VBI**.</span><span class="sxs-lookup"><span data-stu-id="7ed73-144">Some capture filters also support closed captions, indicated by **PIN\_CATEGORY\_VBI**.</span></span> <span data-ttu-id="7ed73-145">Para capturar as legendas ocultas em um arquivo, processe essa categoria para o filtro Mux.</span><span class="sxs-lookup"><span data-stu-id="7ed73-145">To capture the closed captions to a file, render this category to the mux filter.</span></span> <span data-ttu-id="7ed73-146">Para exibir as legendas ocultas na janela de visualização, conecte-se ao renderizador:</span><span class="sxs-lookup"><span data-stu-id="7ed73-146">To view the closed captions in your preview window, connect to the renderer:</span></span>


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, pMux);
// Preview on screen:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, NULL);
```



<span data-ttu-id="7ed73-147">O segundo parâmetro para [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) identifica o tipo de mídia e, normalmente, é um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="7ed73-147">The second parameter to [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) identifies the media type, and is typically one of the following:</span></span>

-   <span data-ttu-id="7ed73-148">Áudio de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="7ed73-148">MEDIATYPE\_Audio</span></span>
-   <span data-ttu-id="7ed73-149">Vídeo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="7ed73-149">MEDIATYPE\_Video</span></span>
-   <span data-ttu-id="7ed73-150">MEDIATYPE \_ intercalado (DV)</span><span class="sxs-lookup"><span data-stu-id="7ed73-150">MEDIATYPE\_Interleaved (DV)</span></span>

<span data-ttu-id="7ed73-151">Você pode usar esse parâmetro sempre que os Pins de saída do filtro suportarem a enumeração de tipos de mídia preferenciais.</span><span class="sxs-lookup"><span data-stu-id="7ed73-151">You can use this parameter whenever the filter's output pins support the enumeration of preferred media types.</span></span> <span data-ttu-id="7ed73-152">Para fontes de arquivo, o construtor de grafo de captura adiciona automaticamente um filtro de analisador, se necessário, e, em seguida, consulta os tipos de mídia no analisador.</span><span class="sxs-lookup"><span data-stu-id="7ed73-152">For file sources, the Capture Graph Builder automatically adds a parser filter if needed, and then queries the media types on the parser.</span></span> <span data-ttu-id="7ed73-153">(Para obter um exemplo, consulte [recompactando um arquivo AVI](recompressing-an-avi-file.md).) Além disso, se o último filtro na cadeia tiver vários Pins de entrada, o método tentará enumerar seus tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="7ed73-153">(For an example, see [Recompressing an AVI File](recompressing-an-avi-file.md).) Also, if the last filter in the chain has several input pins, the method attempts to enumerate their media types.</span></span> <span data-ttu-id="7ed73-154">No entanto, nem todos os filtros dão suporte a essa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="7ed73-154">However, not all filters support this functionality.</span></span>

## <a name="finding-interfaces-on-filters-and-pins"></a><span data-ttu-id="7ed73-155">Localizando interfaces em filtros e Pins</span><span class="sxs-lookup"><span data-stu-id="7ed73-155">Finding Interfaces on Filters and Pins</span></span>

<span data-ttu-id="7ed73-156">Depois de criar um grafo, você normalmente precisará localizar várias interfaces expostas por filtros e Pins no grafo.</span><span class="sxs-lookup"><span data-stu-id="7ed73-156">After you build a graph, you will typically need to locate various interfaces exposed by filters and pins in the graph.</span></span> <span data-ttu-id="7ed73-157">Por exemplo, um filtro de captura pode expor a interface [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) , enquanto os Pins de saída do filtro podem expor a interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="7ed73-157">For example, a capture filter might expose the [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) interface, while the filter's output pins might expose the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface.</span></span>

<span data-ttu-id="7ed73-158">A maneira mais simples de encontrar uma interface é usar o método [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) .</span><span class="sxs-lookup"><span data-stu-id="7ed73-158">The simplest way to find an interface is to use the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method.</span></span> <span data-ttu-id="7ed73-159">Esse método percorre o grafo (filtros e Pins) até localizar a interface desejada.</span><span class="sxs-lookup"><span data-stu-id="7ed73-159">This method walks the graph (filters and pins) until it locates the desired interface.</span></span> <span data-ttu-id="7ed73-160">Você pode especificar o ponto de partida para a pesquisa e pode limitar a pesquisa para filtrar upstream ou downstream a partir do ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="7ed73-160">You can specify the starting point for the search, and you can limit the search to filters upstream or downstream from the starting point.</span></span>

<span data-ttu-id="7ed73-161">O exemplo a seguir pesquisa a interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) em um pino de visualização de vídeo:</span><span class="sxs-lookup"><span data-stu-id="7ed73-161">The following example searches for the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface on a video preview pin:</span></span>


```C++
IAMStreamConfig *pConfig = NULL;
HRESULT hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, 
    &MEDIATYPE_Video,
    pVCap, 
    IID_IAMStreamConfig, 
    (void**)&pConfig
);
if (SUCCESSFUL(hr))
{
    /* ... */
    pConfig->Release();
}
```



> [!Note]  
> <span data-ttu-id="7ed73-162">O tópico [Localizar uma interface em um filtro ou PIN](find-an-interface-on-a-filter-or-pin.md) mostra uma abordagem alternativa que usa a interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) em vez de [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2).</span><span class="sxs-lookup"><span data-stu-id="7ed73-162">The topic [Find an Interface on a Filter or Pin](find-an-interface-on-a-filter-or-pin.md) shows an alternative approach that uses the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface instead of [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2).</span></span> <span data-ttu-id="7ed73-163">Qual abordagem usar depende do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7ed73-163">Which approach to use depends on your application.</span></span> <span data-ttu-id="7ed73-164">Se seu aplicativo já usa **ICaptureGraphBuilder2** para criar o grafo, [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) é uma boa abordagem.</span><span class="sxs-lookup"><span data-stu-id="7ed73-164">If your application already uses **ICaptureGraphBuilder2** to build the graph, then [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) is a good approach.</span></span> <span data-ttu-id="7ed73-165">Caso contrário, considere o uso dos métodos **IGraphBuilder** .</span><span class="sxs-lookup"><span data-stu-id="7ed73-165">Otherwise, consider using the **IGraphBuilder** methods.</span></span>

 

## <a name="finding-pins"></a><span data-ttu-id="7ed73-166">Localizando Pins</span><span class="sxs-lookup"><span data-stu-id="7ed73-166">Finding Pins</span></span>

<span data-ttu-id="7ed73-167">Com menos frequência, talvez seja necessário localizar um PIN individual em um filtro, embora, na maioria dos casos, os métodos [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) e [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) possam poupar a você o problema.</span><span class="sxs-lookup"><span data-stu-id="7ed73-167">Less commonly, you may need to locate an individual pin on a filter, although in most cases the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) and [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) methods will save you the trouble.</span></span> <span data-ttu-id="7ed73-168">Se você precisar localizar um PIN específico em um filtro, o método auxiliar [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) será útil.</span><span class="sxs-lookup"><span data-stu-id="7ed73-168">If you do need to find a particular pin on a filter, the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) helper method is useful.</span></span> <span data-ttu-id="7ed73-169">Especifique a categoria, o tipo de mídia (vídeo ou áudio), a direção e se o PIN deve ser desconectado.</span><span class="sxs-lookup"><span data-stu-id="7ed73-169">Specify the category, the media type (video or audio), the direction, and whether the pin must be unconnected.</span></span>

<span data-ttu-id="7ed73-170">Por exemplo, o código a seguir procura um PIN de visualização de vídeo desconectado em um filtro de captura:</span><span class="sxs-lookup"><span data-stu-id="7ed73-170">For example, the following code searches for an unconnected video preview pin on a capture filter:</span></span>


```C++
IPin *pPin = NULL;
hr = pBuild->FindPin(
    pCap,                   // Pointer to the filter to search.
    PINDIR_OUTPUT,          // Search for an output pin.
    &PIN_CATEGORY_PREVIEW,  // Search for a preview pin.
    &MEDIATYPE_Video,       // Search for a video pin.
    TRUE,                   // The pin must be unconnected. 
    0,                      // Return the first matching pin (index 0).
    &pPin);                 // This variable receives the IPin pointer.
if (SUCCESSFUL(hr))
{
    /* ... */
    pPin->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="7ed73-171">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ed73-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ed73-172">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="7ed73-172">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 
