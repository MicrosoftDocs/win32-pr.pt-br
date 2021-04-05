---
description: Criando o grafo de recompactação
ms.assetid: 8f25c60e-30be-4cc4-b924-b8d6654604d3
title: Criando o grafo de recompactação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8ea604bead34c22c123bbabe5d88e985006a9e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825549"
---
# <a name="building-the-recompression-graph"></a><span data-ttu-id="392de-103">Criando o grafo de recompactação</span><span class="sxs-lookup"><span data-stu-id="392de-103">Building the Recompression Graph</span></span>

<span data-ttu-id="392de-104">Um grafo de filtro típico para a recompactação de arquivo AVI é semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="392de-104">A typical filter graph for AVI file recompression looks like the following:</span></span>

![Grafo de recompactação avi](images/avi2avi4.png)

<span data-ttu-id="392de-106">O [filtro de Splitter AVI](avi-splitter-filter.md) extrai dados do filtro de [origem de arquivo (Async)](file-source--async--filter.md) e os analisa em fluxos de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="392de-106">The [AVI Splitter Filter](avi-splitter-filter.md) pulls data from the [File Source (Async) Filter](file-source--async--filter.md) and parses it into video and audio streams.</span></span> <span data-ttu-id="392de-107">O descompactador de vídeo decodifica o vídeo compactado, onde é recompactado pelo compactador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="392de-107">The video decompressor decodes the compressed video, where it is recompressed by the video compressor.</span></span> <span data-ttu-id="392de-108">A escolha dos decompactadores depende do arquivo de origem; Ele será manipulado automaticamente pelo [Intelligent Connect](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="392de-108">The choice of decompressors depends on the source file; it will be handled automatically by [Intelligent Connect](intelligent-connect.md).</span></span> <span data-ttu-id="392de-109">O aplicativo deve escolher o compressor, normalmente apresentando uma lista para o usuário.</span><span class="sxs-lookup"><span data-stu-id="392de-109">The application must choose the compressor, typically by presenting a list to the user.</span></span> <span data-ttu-id="392de-110">(Consulte [escolher um filtro de compactação](choosing-a-compression-filter.md).)</span><span class="sxs-lookup"><span data-stu-id="392de-110">(See [Choosing a Compression Filter](choosing-a-compression-filter.md).)</span></span>

<span data-ttu-id="392de-111">Em seguida, o vídeo compactado vai para o [filtro AVI Mux](avi-mux-filter.md).</span><span class="sxs-lookup"><span data-stu-id="392de-111">The compressed video then goes to the [AVI Mux Filter](avi-mux-filter.md).</span></span> <span data-ttu-id="392de-112">O fluxo de áudio neste exemplo não é compactado, portanto, ele vai diretamente do divisor AVI para o AVI Mux.</span><span class="sxs-lookup"><span data-stu-id="392de-112">The audio stream in this example is not compressed, so it goes directly from the AVI Splitter to the AVI Mux.</span></span> <span data-ttu-id="392de-113">O AVI Mux intercala os dois fluxos e o filtro do [gravador de arquivo](file-writer-filter.md) grava a saída no disco.</span><span class="sxs-lookup"><span data-stu-id="392de-113">The AVI Mux interleaves the two streams, and the [File Writer Filter](file-writer-filter.md) writes the output to disk.</span></span> <span data-ttu-id="392de-114">Observe que o AVI Mux é necessário mesmo que o arquivo original não tenha um fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="392de-114">Note that the AVI Mux is required even if the original file does not have an audio stream.</span></span>

<span data-ttu-id="392de-115">A maneira mais fácil de criar esse grafo de filtro é usar o [Construtor de grafo de captura](capture-graph-builder.md), que é um componente do DirectShow para criar grafos de captura e outros gráficos de filtro personalizados.</span><span class="sxs-lookup"><span data-stu-id="392de-115">The easiest way to build this filter graph is to use the [Capture Graph Builder](capture-graph-builder.md), which is a DirectShow component for building capture graphs and other custom filter graphs.</span></span>

<span data-ttu-id="392de-116">Comece chamando CoCreateInstance para criar o construtor de grafo de captura:</span><span class="sxs-lookup"><span data-stu-id="392de-116">Start by calling CoCreateInstance to create the Capture Graph Builder:</span></span>


```C++
ICaptureGraphBuilder2 *pBuild = NULL;
hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 
                        NULL, CLSCTX_INPROC_SERVER,
    IID_ICaptureGraphBuilder2, (void **)&pBuild);
```



<span data-ttu-id="392de-117">Em seguida, use o construtor do grafo de captura para criar o grafo de filtro:</span><span class="sxs-lookup"><span data-stu-id="392de-117">Then use the Capture Graph Builder to build the filter graph:</span></span>

1.  <span data-ttu-id="392de-118">Crie a seção de renderização do grafo, que inclui o filtro AVI Mux e o [gravador de arquivos](file-writer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="392de-118">Build the rendering section of the graph, which includes the AVI Mux filter and the [File Writer](file-writer-filter.md).</span></span>
2.  <span data-ttu-id="392de-119">Adicione o filtro de origem e o filtro de compactação ao grafo.</span><span class="sxs-lookup"><span data-stu-id="392de-119">Add the source filter and the compression filter to the graph.</span></span>
3.  <span data-ttu-id="392de-120">Conecte o filtro de origem ao filtro do MUX.</span><span class="sxs-lookup"><span data-stu-id="392de-120">Connect the source filter to the MUX filter.</span></span> <span data-ttu-id="392de-121">O construtor de gráficos de captura insere quaisquer filtros de divisor e decodificador necessários para analisar o arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="392de-121">The capture graph builder inserts whatever splitter and decoder filters are needed to parse the source file.</span></span> <span data-ttu-id="392de-122">Ele também pode rotear os fluxos de áudio e vídeo por meio de filtros de compactação.</span><span class="sxs-lookup"><span data-stu-id="392de-122">It can also route the video and audio streams through compression filters.</span></span>

<span data-ttu-id="392de-123">As seções a seguir explicam cada uma dessas etapas.</span><span class="sxs-lookup"><span data-stu-id="392de-123">The following sections explain each of these steps.</span></span>

<span data-ttu-id="392de-124">Criar a seção de renderização</span><span class="sxs-lookup"><span data-stu-id="392de-124">Build the Rendering Section</span></span>

<span data-ttu-id="392de-125">Para criar a seção de renderização do grafo, chame o método [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) .</span><span class="sxs-lookup"><span data-stu-id="392de-125">To build the rendering section of the graph, call the [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) method.</span></span> <span data-ttu-id="392de-126">Esse método usa parâmetros de entrada que especificam o subtipo de mídia para a saída e o nome do arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="392de-126">This method takes input parameters that specify the media subtype for the output and the name of the output file.</span></span> <span data-ttu-id="392de-127">Ele retorna ponteiros para o filtro MUX e o gravador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="392de-127">It returns pointers to the MUX filter and the file writer.</span></span> <span data-ttu-id="392de-128">O filtro MUX é necessário para o próximo estágio da construção do grafo.</span><span class="sxs-lookup"><span data-stu-id="392de-128">The MUX filter is needed for the next stage of graph building.</span></span> <span data-ttu-id="392de-129">O ponteiro para o gravador de arquivo não é necessário para este exemplo, de modo que o parâmetro pode ser **nulo**:</span><span class="sxs-lookup"><span data-stu-id="392de-129">The pointer to the file writer is not needed for this example, so that parameter can be **NULL**:</span></span>


```C++
IBaseFilter *pMux = NULL;
hr = pBuild->SetOutputFileName(
        &MEDIASUBTYPE_Avi, // File type. 
        wszOutputFile,     // File name, as a wide-character string.
        &pMux,             // Receives a pointer to the multiplexer.
        NULL);             // Receives a pointer to the file writer. 
```



<span data-ttu-id="392de-130">Quando o método retorna, o filtro MUX tem uma contagem de referência pendente, portanto, certifique-se de liberar o ponteiro mais tarde.</span><span class="sxs-lookup"><span data-stu-id="392de-130">When the method returns, the MUX filter has an outstanding reference count, so be sure to release the pointer later.</span></span>

<span data-ttu-id="392de-131">O diagrama a seguir mostra o gráfico de filtro neste ponto.</span><span class="sxs-lookup"><span data-stu-id="392de-131">The following diagram shows the filter graph at this point.</span></span>

![seção de renderização do grafo de filtro](images/avi2avi1.png)

<span data-ttu-id="392de-133">O filtro MUX expõe duas interfaces para controlar o formato AVI:</span><span class="sxs-lookup"><span data-stu-id="392de-133">The MUX filter exposes two interfaces for controlling the AVI format:</span></span>

-   <span data-ttu-id="392de-134">[**Interface IConfigInterleaving**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving): define o modo de intercalação.</span><span class="sxs-lookup"><span data-stu-id="392de-134">[**IConfigInterleaving Interface**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving): Sets the interleaving mode.</span></span>
-   <span data-ttu-id="392de-135">[**Interface IConfigAviMux**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux): define o fluxo mestre e o índice de compatibilidade avi.</span><span class="sxs-lookup"><span data-stu-id="392de-135">[**IConfigAviMux Interface**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux): Sets the master stream and the AVI compatibility index.</span></span>

<span data-ttu-id="392de-136">Adicionar os filtros de origem e de compactação</span><span class="sxs-lookup"><span data-stu-id="392de-136">Add the Source and Compression Filters</span></span>

<span data-ttu-id="392de-137">A próxima etapa é adicionar os filtros de origem e de compactação ao grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="392de-137">The next step is to add the source and compression filters to the filter graph.</span></span> <span data-ttu-id="392de-138">O construtor do grafo de captura cria automaticamente uma instância do Gerenciador do grafo de filtro quando você chama SetOutputFileName.</span><span class="sxs-lookup"><span data-stu-id="392de-138">The Capture Graph Builder automatically creates an instance of the Filter Graph Manager when you call SetOutputFileName.</span></span> <span data-ttu-id="392de-139">Obtenha um ponteiro para ele chamando o método [**ICaptureGraphBuilder2:: GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-getfiltergraph) :</span><span class="sxs-lookup"><span data-stu-id="392de-139">Get a pointer to it by calling the [**ICaptureGraphBuilder2::GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-getfiltergraph) method:</span></span>


```C++
IGraphBuilder *pGraph = NULL;
hr = pBuild->GetFiltergraph(&pGraph);
```



<span data-ttu-id="392de-140">Agora, chame o método [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) para adicionar o filtro de origem de arquivo assíncrono e o método [**IFilterGraph:: addfiltro**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para adicionar o compressor de vídeo:</span><span class="sxs-lookup"><span data-stu-id="392de-140">Now call the [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) method to add the Async File Source filter, and the [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) method to add the video compressor:</span></span>


```C++
IBaseFilter *pSrc = NULL;
hr = pGraph->AddSourceFilter(wszInputFile, L"Source Filter", &pSrc);
hr = pGraph->AddFilter(pVComp, L"Compressor");
```



<span data-ttu-id="392de-141">Neste ponto, o filtro de origem e o filtro de compactação não estão conectados a nada mais no grafo, conforme mostrado na ilustração a seguir:</span><span class="sxs-lookup"><span data-stu-id="392de-141">At this point, the source filter and the compression filter are not connected to anything else in the graph, as shown in the following illustration:</span></span>

![gráfico de filtro com filtros de origem e de compactação](images/avi2avi2.png)

<span data-ttu-id="392de-143">Conectar a origem ao MUX</span><span class="sxs-lookup"><span data-stu-id="392de-143">Connect the Source to the Mux</span></span>

<span data-ttu-id="392de-144">A etapa final é conectar o filtro de origem ao filtro AVI Mux por meio do compactador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="392de-144">The final step is to connect the source filter to the AVI Mux filter, through the video compressor.</span></span> <span data-ttu-id="392de-145">Use o método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) , que conecta um pino de saída no filtro de origem a um filtro de coletor especificado, opcionalmente por meio de um filtro de compactação.</span><span class="sxs-lookup"><span data-stu-id="392de-145">Use the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method, which connects an output pin on the source filter to a specified sink filter, optionally through a compression filter.</span></span>

<span data-ttu-id="392de-146">Os dois primeiros parâmetros especificam qual dos Pins do filtro de origem se conectar, designando uma categoria de PIN e um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="392de-146">The first two parameters specify which of the source filter's pins to connect, by designating a pin category and a media type.</span></span> <span data-ttu-id="392de-147">O filtro de origem de arquivo assíncrono tem apenas um pino de saída, portanto, esses parâmetros devem ser **nulos**.</span><span class="sxs-lookup"><span data-stu-id="392de-147">The Async File Source filter has only one output pin, so these parameters should be **NULL**.</span></span> <span data-ttu-id="392de-148">Os próximos três parâmetros especificam o filtro de origem, o filtro de compactação (se houver) e o filtro Mux.</span><span class="sxs-lookup"><span data-stu-id="392de-148">The next three parameters specify the source filter, the compression filter (if any), and the Mux filter.</span></span>

<span data-ttu-id="392de-149">O exemplo de código a seguir renderiza a transmissão de vídeo por meio do compactador de vídeo:</span><span class="sxs-lookup"><span data-stu-id="392de-149">The following code example renders the video stream through the video compressor:</span></span>


```C++
hr = pBuild->RenderStream(
        NULL,       // Output pin category
        NULL,       // Media type
        pSrc,       // Source filter
        pVComp,     // Compression filter
        pMux);      // Sink filter (the AVI Mux)
```



<span data-ttu-id="392de-150">O diagrama a seguir mostra o gráfico de filtro até o momento.</span><span class="sxs-lookup"><span data-stu-id="392de-150">The following diagram shows the filter graph so far.</span></span>

![fluxo de vídeo renderizado](images/avi2avi3.png)

<span data-ttu-id="392de-152">Supondo que o arquivo de origem tenha um fluxo de áudio, o filtro de [Splitter AVI](avi-splitter-filter.md) criou um pino de saída para o áudio.</span><span class="sxs-lookup"><span data-stu-id="392de-152">Assuming that the source file has an audio stream, the [AVI Splitter](avi-splitter-filter.md) filter has created an output pin for the audio.</span></span> <span data-ttu-id="392de-153">Para conectar esse PIN, chame RenderStream novamente:</span><span class="sxs-lookup"><span data-stu-id="392de-153">To connect this pin, call RenderStream again:</span></span>


```C++
hr = pBuild->RenderStream(NULL, NULL, pSrc, NULL, pMux);
```



<span data-ttu-id="392de-154">Aqui, nenhum filtro de compactação foi especificado.</span><span class="sxs-lookup"><span data-stu-id="392de-154">Here, no compression filter is specified.</span></span> <span data-ttu-id="392de-155">O pino de saída do filtro de origem já está conectado, portanto, o método RenderStream procura um PIN de saída não conectado no filtro de divisão.</span><span class="sxs-lookup"><span data-stu-id="392de-155">The source filter's output pin is already connected, so the RenderStream method searches for an unconnected output pin on the splitter filter.</span></span> <span data-ttu-id="392de-156">Ele encontra o PIN de áudio e o conecta diretamente ao filtro do MUX.</span><span class="sxs-lookup"><span data-stu-id="392de-156">It finds the audio pin and connects it directly to the MUX filter.</span></span> <span data-ttu-id="392de-157">Se o arquivo de origem não tiver um fluxo de áudio, a segunda chamada para RenderStream falhará.</span><span class="sxs-lookup"><span data-stu-id="392de-157">If the source file does not have an audio stream, the second call to RenderStream will fail.</span></span> <span data-ttu-id="392de-158">Esse comportamento é esperado.</span><span class="sxs-lookup"><span data-stu-id="392de-158">This is expected behavior.</span></span> <span data-ttu-id="392de-159">O grafo é concluído após a primeira chamada para RenderStream, portanto, a falha na segunda chamada é inofensiva.</span><span class="sxs-lookup"><span data-stu-id="392de-159">The graph is complete after the first call to RenderStream, so the failure in the second call is harmless.</span></span>

<span data-ttu-id="392de-160">Neste exemplo, a ordem das duas chamadas RenderStream é importante.</span><span class="sxs-lookup"><span data-stu-id="392de-160">In this example, the order of the two RenderStream calls is important.</span></span> <span data-ttu-id="392de-161">Como a segunda chamada não especifica um compressor, ela conectará qualquer PIN não conectado do divisor AVI.</span><span class="sxs-lookup"><span data-stu-id="392de-161">Because the second call does not specify a compressor, it will connect any unconnected pin from the AVI Splitter.</span></span> <span data-ttu-id="392de-162">Se você fizer essa chamada antes da outra, ela poderá conectar a transmissão de vídeo ao AVI Mux sem o seu compressor de vídeo.</span><span class="sxs-lookup"><span data-stu-id="392de-162">If you make this call before the other one, it might connect the video stream to the AVI Mux, without your video compressor.</span></span> <span data-ttu-id="392de-163">Portanto, a chamada mais específica (com o filtro de compactação) deve ocorrer primeiro.</span><span class="sxs-lookup"><span data-stu-id="392de-163">Therefore, the more specific call (with the compression filter) must happen first.</span></span>

<span data-ttu-id="392de-164">A discussão anterior assumiu que o arquivo de origem é um arquivo AVI.</span><span class="sxs-lookup"><span data-stu-id="392de-164">The previous discussion has assumed that the source file is an AVI file.</span></span> <span data-ttu-id="392de-165">No entanto, essa técnica também funciona com outros tipos de arquivo, como arquivos MPEG.</span><span class="sxs-lookup"><span data-stu-id="392de-165">However, this technique also works with other file types, such as MPEG files.</span></span> <span data-ttu-id="392de-166">O grafo de filtro resultante será um pouco diferente.</span><span class="sxs-lookup"><span data-stu-id="392de-166">The resulting filter graph will be somewhat different.</span></span>

## <a name="related-topics"></a><span data-ttu-id="392de-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="392de-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="392de-168">Recompactando um arquivo AVI</span><span class="sxs-lookup"><span data-stu-id="392de-168">Recompressing an AVI File</span></span>](recompressing-an-avi-file.md)
</dt> </dl>

 

 



