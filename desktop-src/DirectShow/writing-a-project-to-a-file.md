---
description: Gravando um projeto em um arquivo
ms.assetid: 84499e4f-4f45-4aa6-aa89-d95c3b6b47d0
title: Gravando um projeto em um arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f63ddbc6a021362134d420220f7e25c662553f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757831"
---
# <a name="writing-a-project-to-a-file"></a><span data-ttu-id="3fa99-103">Gravando um projeto em um arquivo</span><span class="sxs-lookup"><span data-stu-id="3fa99-103">Writing a Project to a File</span></span>

<span data-ttu-id="3fa99-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="3fa99-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="3fa99-105">Este artigo descreve como gravar um projeto de [serviços de edição do DirectShow](directshow-editing-services.md) em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="3fa99-105">This article describes how to write a [DirectShow Editing Services](directshow-editing-services.md) project to a file.</span></span> <span data-ttu-id="3fa99-106">Primeiro, ele descreve como gravar um arquivo com o mecanismo de processamento básico.</span><span class="sxs-lookup"><span data-stu-id="3fa99-106">First it describes how to write a file with the basic render engine.</span></span> <span data-ttu-id="3fa99-107">Em seguida, ele descreve a recompactação inteligente com o mecanismo de processamento inteligente.</span><span class="sxs-lookup"><span data-stu-id="3fa99-107">Then it describes smart recompression with the smart render engine.</span></span>

<span data-ttu-id="3fa99-108">Para obter uma visão geral de como os serviços de edição do DirectShow renderizam projetos, consulte [sobre os mecanismos de renderização](about-the-render-engines.md).</span><span class="sxs-lookup"><span data-stu-id="3fa99-108">For an overview of how DirectShow Editing Services renders projects, see [About the Render Engines](about-the-render-engines.md).</span></span>

<span data-ttu-id="3fa99-109">**Usando o mecanismo de renderização básico**</span><span class="sxs-lookup"><span data-stu-id="3fa99-109">**Using the Basic Render Engine**</span></span>

<span data-ttu-id="3fa99-110">Comece criando o front-end do grafo, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="3fa99-110">Start by building the front end of the graph, as follows:</span></span>

1.  <span data-ttu-id="3fa99-111">Crie o mecanismo de renderização.</span><span class="sxs-lookup"><span data-stu-id="3fa99-111">Create the render engine.</span></span>
2.  <span data-ttu-id="3fa99-112">Especifique a linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="3fa99-112">Specify the timeline.</span></span>
3.  <span data-ttu-id="3fa99-113">Defina o intervalo de renderização.</span><span class="sxs-lookup"><span data-stu-id="3fa99-113">Set the render range.</span></span> <span data-ttu-id="3fa99-114">(Opcional)</span><span class="sxs-lookup"><span data-stu-id="3fa99-114">(Optional)</span></span>
4.  <span data-ttu-id="3fa99-115">Crie o front-end do grafo.</span><span class="sxs-lookup"><span data-stu-id="3fa99-115">Build the front end of the graph.</span></span>

<span data-ttu-id="3fa99-116">O exemplo de código a seguir mostra essas etapas.</span><span class="sxs-lookup"><span data-stu-id="3fa99-116">The following code example shows these steps.</span></span>


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC,
    IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
```



<span data-ttu-id="3fa99-117">Em seguida, adicione os filtros Multiplexador e gravação de arquivo ao grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="3fa99-117">Next, add multiplexer and file-writing filters to the filter graph.</span></span> <span data-ttu-id="3fa99-118">A maneira mais fácil de fazer isso é com o [Construtor de grafo de captura](capture-graph-builder.md), um componente do DirectShow para criar grafos de captura.</span><span class="sxs-lookup"><span data-stu-id="3fa99-118">The easiest way to do this is with the [Capture Graph Builder](capture-graph-builder.md), a DirectShow component for building capture graphs.</span></span> <span data-ttu-id="3fa99-119">O construtor do grafo de captura expõe a interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) .</span><span class="sxs-lookup"><span data-stu-id="3fa99-119">The capture graph builder exposes the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface.</span></span> <span data-ttu-id="3fa99-120">Execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="3fa99-120">Perform the following steps:</span></span>

1.  <span data-ttu-id="3fa99-121">Crie uma instância do construtor de gráficos de captura.</span><span class="sxs-lookup"><span data-stu-id="3fa99-121">Create an instance of the capture graph builder.</span></span>
2.  <span data-ttu-id="3fa99-122">Obtenha um ponteiro para o grafo e passe-o para o construtor de gráficos.</span><span class="sxs-lookup"><span data-stu-id="3fa99-122">Obtain a pointer to the graph and pass it to the graph builder.</span></span>
3.  <span data-ttu-id="3fa99-123">Especifique o nome e o tipo de mídia do arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="3fa99-123">Specify the name and media type of the output file.</span></span> <span data-ttu-id="3fa99-124">Essa etapa também obtém um ponteiro para o filtro Mux, que é necessário posteriormente.</span><span class="sxs-lookup"><span data-stu-id="3fa99-124">This step also obtains a pointer to the mux filter, which is required later.</span></span>

<span data-ttu-id="3fa99-125">O exemplo de código a seguir mostra essas etapas.</span><span class="sxs-lookup"><span data-stu-id="3fa99-125">The following code example shows these steps.</span></span>


```C++
CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL, CLSCTX_INPROC, 
    IID_ICaptureGraphBuilder2, (void **)&pBuilder);

// Get a pointer to the graph front end.
IGraphBuilder *pGraph;
pRender->GetFilterGraph(&pGraph);
pBuilder->SetFiltergraph(pGraph);

// Create the file-writing section.
IBaseFilter *pMux;
pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("Output.avi"), &pMux, NULL);
```



<span data-ttu-id="3fa99-126">Por fim, conecte os Pins de saída no front-end ao filtro Mux.</span><span class="sxs-lookup"><span data-stu-id="3fa99-126">Finally, connect the output pins on the front end to the mux filter.</span></span>

1.  <span data-ttu-id="3fa99-127">Recupere o número de grupos.</span><span class="sxs-lookup"><span data-stu-id="3fa99-127">Retrieve the number of groups.</span></span>
2.  <span data-ttu-id="3fa99-128">Para cada PIN, obtenha um ponteiro para o PIN.</span><span class="sxs-lookup"><span data-stu-id="3fa99-128">For each pin, obtain a pointer to the pin.</span></span>
3.  <span data-ttu-id="3fa99-129">Opcionalmente, crie uma instância de um filtro de compactação para compactar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="3fa99-129">Optionally, create an instance of a compression filter to compress the stream.</span></span> <span data-ttu-id="3fa99-130">O tipo de compressor dependerá do tipo de mídia do grupo.</span><span class="sxs-lookup"><span data-stu-id="3fa99-130">The type of compressor will depend on the media type of the group.</span></span> <span data-ttu-id="3fa99-131">Você pode usar o [enumerador de dispositivo do sistema](system-device-enumerator.md) para enumerar os filtros de compactação disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3fa99-131">You can use the [System Device Enumerator](system-device-enumerator.md) to enumerate the available compression filters.</span></span> <span data-ttu-id="3fa99-132">Para obter mais informações, consulte [enumerando dispositivos e filtros](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="3fa99-132">For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>
4.  <span data-ttu-id="3fa99-133">Opcionalmente, defina os parâmetros de compactação, como a taxa de quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="3fa99-133">Optionally, set compression parameters such as the key-frame rate.</span></span> <span data-ttu-id="3fa99-134">Esta etapa será discutida em detalhes posteriormente neste artigo.</span><span class="sxs-lookup"><span data-stu-id="3fa99-134">This step is discussed in detail later in the article.</span></span>
5.  <span data-ttu-id="3fa99-135">Chame [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span><span class="sxs-lookup"><span data-stu-id="3fa99-135">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span></span> <span data-ttu-id="3fa99-136">Esse método usa ponteiros para o pino, o filtro de compactação (se houver) e o multiplexador.</span><span class="sxs-lookup"><span data-stu-id="3fa99-136">This method takes pointers to the pin, the compression filter (if any), and the multiplexer.</span></span>

<span data-ttu-id="3fa99-137">O exemplo de código a seguir mostra como conectar os Pins de saída.</span><span class="sxs-lookup"><span data-stu-id="3fa99-137">The following code example shows how to connect the output pins.</span></span>


```C++
long NumGroups;
pTimeline->GetGroupCount(&NumGroups);

// Loop through the groups and get the output pins.
for (i = 0; i < NumGroups; i++)
{
    IPin *pPin;
    if (pRender->GetGroupOutputPin(i, &pPin) == S_OK) 
    {
        IBaseFilter *pCompressor;
        // Create a compressor filter. (Not shown.)
        // Set compression parameters. (Not shown.)

        // Connect the pin.
        pBuilder->RenderStream(NULL, NULL, pPin, pCompressor, pMux);
        pCompressor->Release();
        pPin->Release();
    }
}
```



<span data-ttu-id="3fa99-138">Para definir os parâmetros de compactação (etapa 4, anteriormente), use a interface [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) .</span><span class="sxs-lookup"><span data-stu-id="3fa99-138">To set compression parameters (step 4, previously), use the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface.</span></span> <span data-ttu-id="3fa99-139">Essa interface é exposta nos Pins de saída dos filtros de compactação.</span><span class="sxs-lookup"><span data-stu-id="3fa99-139">This interface is exposed on the output pins of compression filters.</span></span> <span data-ttu-id="3fa99-140">Enumere os Pins do filtro de compactação e consulte cada PIN de saída para **IAMVideoCompression**.</span><span class="sxs-lookup"><span data-stu-id="3fa99-140">Enumerate the compression filter's pins, and query each output pin for **IAMVideoCompression**.</span></span> <span data-ttu-id="3fa99-141">(Para obter informações sobre como enumerar Pins, consulte [enumerando Pins](enumerating-pins.md).) Certifique-se de liberar todos os ponteiros de interface que você obteve durante esta etapa.</span><span class="sxs-lookup"><span data-stu-id="3fa99-141">(For information about enumerating pins, see [Enumerating Pins](enumerating-pins.md).) Be sure to release all the interface pointers that you obtained during this step.</span></span>

<span data-ttu-id="3fa99-142">Depois de criar o grafo de filtro, chame o método [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) no Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="3fa99-142">After you build the filter graph, call the [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) method on the filter graph manager.</span></span> <span data-ttu-id="3fa99-143">À medida que o gráfico de filtro é executado, ele grava os dados em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="3fa99-143">As the filter graph runs, it writes the data to a file.</span></span> <span data-ttu-id="3fa99-144">Use a notificação de eventos para aguardar a reprodução ser concluída.</span><span class="sxs-lookup"><span data-stu-id="3fa99-144">Use event notification to wait for playback to complete.</span></span> <span data-ttu-id="3fa99-145">(Consulte [respondendo a eventos](responding-to-events.md).) Quando a reprodução for concluída, você deverá chamar explicitamente [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) para parar o grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="3fa99-145">(See [Responding to Events](responding-to-events.md).) When playback finishes, you must explicitly call [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) to stop the filter graph.</span></span> <span data-ttu-id="3fa99-146">Caso contrário, o arquivo não será gravado corretamente.</span><span class="sxs-lookup"><span data-stu-id="3fa99-146">Otherwise, the file is not written correctly.</span></span>

<span data-ttu-id="3fa99-147">**Usando o mecanismo de processamento inteligente**</span><span class="sxs-lookup"><span data-stu-id="3fa99-147">**Using the Smart Render Engine**</span></span>

<span data-ttu-id="3fa99-148">Para obter os benefícios da recompactação inteligente, use o mecanismo de processamento inteligente no lugar do mecanismo de renderização básico.</span><span class="sxs-lookup"><span data-stu-id="3fa99-148">To get the benefits of smart recompression, use the smart render engine in place of the basic render engine.</span></span> <span data-ttu-id="3fa99-149">As etapas na criação do grafo são quase iguais.</span><span class="sxs-lookup"><span data-stu-id="3fa99-149">The steps in building the graph are almost the same.</span></span> <span data-ttu-id="3fa99-150">A principal diferença é que a compactação é tratada no front-end do grafo, não na seção de gravação de arquivos.</span><span class="sxs-lookup"><span data-stu-id="3fa99-150">The major difference is that compression is handled in the front end of the graph, not in the file-writing section.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3fa99-151">Não use o mecanismo de processamento inteligente para ler ou gravar arquivos de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="3fa99-151">Do not use the smart render engine to read or write Windows Media files.</span></span>

 

<span data-ttu-id="3fa99-152">Cada grupo de vídeos tem uma propriedade que especifica o formato de compactação para esse grupo.</span><span class="sxs-lookup"><span data-stu-id="3fa99-152">Each video group has a property that specifies the compression format for that group.</span></span> <span data-ttu-id="3fa99-153">O formato de compactação deve corresponder exatamente ao formato descompactado do grupo em altura, largura, profundidade de bits e taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="3fa99-153">The compression format must exactly match the group's uncompressed format in height, width, bit depth, and frame rate.</span></span> <span data-ttu-id="3fa99-154">O mecanismo de processamento inteligente usa o formato de compactação quando constrói o grafo.</span><span class="sxs-lookup"><span data-stu-id="3fa99-154">The smart render engine uses the compression format when it constructs the graph.</span></span> <span data-ttu-id="3fa99-155">Antes de definir o formato de compactação, certifique-se de definir o formato descompactado para esse grupo chamando [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="3fa99-155">Before you set the compression format, make sure to set the uncompressed format for that group by calling [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md).</span></span>

<span data-ttu-id="3fa99-156">Para definir o formato de compactação de um grupo, chame o método [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) .</span><span class="sxs-lookup"><span data-stu-id="3fa99-156">To set a group's compression format, call the [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) method.</span></span> <span data-ttu-id="3fa99-157">Esse método usa um ponteiro para uma estrutura [**SCompFmt0**](scompfmt0.md) .</span><span class="sxs-lookup"><span data-stu-id="3fa99-157">This method takes a pointer to an [**SCompFmt0**](scompfmt0.md) structure.</span></span> <span data-ttu-id="3fa99-158">A estrutura **SCompFmt0** tem dois membros: **nFormatId**, que deve ser zero e **MediaType**, que é uma estrutura [**de \_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="3fa99-158">The **SCompFmt0** structure has two members: **nFormatId**, which must be zero, and **MediaType**, which is an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="3fa99-159">Inicialize a estrutura do **\_ \_ tipo de mídia am** com as informações de formato.</span><span class="sxs-lookup"><span data-stu-id="3fa99-159">Initialize the **AM\_MEDIA\_TYPE** structure with the format information.</span></span>

> [!Note]  
> <span data-ttu-id="3fa99-160">Se você quiser que o projeto final tenha o mesmo formato que um dos seus arquivos de origem, você pode obter a \_ estrutura do tipo de mídia am \_ diretamente do arquivo de origem, usando o detector de mídia.</span><span class="sxs-lookup"><span data-stu-id="3fa99-160">If you want the final project to have the same format as one of your source files, you can get the AM\_MEDIA\_TYPE structure directly from the source file, using the media detector.</span></span> <span data-ttu-id="3fa99-161">Consulte [**IMediaDet:: get \_ StreamMediaType**](imediadet-get-streammediatype.md).</span><span class="sxs-lookup"><span data-stu-id="3fa99-161">See [**IMediaDet::get\_StreamMediaType**](imediadet-get-streammediatype.md).</span></span>

 

<span data-ttu-id="3fa99-162">Converta a variável [**SCompFmt0**](scompfmt0.md) para um ponteiro do tipo **Long**, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="3fa99-162">Cast the [**SCompFmt0**](scompfmt0.md) variable to a pointer of type **long**, as shown in the following example.</span></span>


```C++
SCompFmt0 *pFormat = new SCompFmt0;
memset(pFormat, 0, sizeof(SCompFmt0));
pFormat->nFormatId = 0;

// Initialize pFormat->MediaType. (Not shown.)

pGroup->SetSmartRecompressFormat( (long*) pFormat );
```



<span data-ttu-id="3fa99-163">O mecanismo de processamento inteligente procura automaticamente por um filtro de compactação compatível.</span><span class="sxs-lookup"><span data-stu-id="3fa99-163">The smart render engine automatically searches for a compatible compression filter.</span></span> <span data-ttu-id="3fa99-164">Você também pode especificar um filtro de compactação para um grupo chamando [**ISmartRenderEngine:: SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md).</span><span class="sxs-lookup"><span data-stu-id="3fa99-164">You can also specify a compression filter for a group by calling [**ISmartRenderEngine::SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md).</span></span>

<span data-ttu-id="3fa99-165">Para criar o grafo, use as mesmas etapas que foram descritas para o mecanismo de renderização básico na seção anterior.</span><span class="sxs-lookup"><span data-stu-id="3fa99-165">To build the graph, use the same steps that were described for the Basic Render Engine in the previous section.</span></span> <span data-ttu-id="3fa99-166">As únicas diferenças são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="3fa99-166">The only differences are the following:</span></span>

-   <span data-ttu-id="3fa99-167">Use o mecanismo de processamento inteligente, não o mecanismo de renderização básico.</span><span class="sxs-lookup"><span data-stu-id="3fa99-167">Use the smart render engine, not the basic render engine.</span></span> <span data-ttu-id="3fa99-168">O identificador de classe é CLSID \_ SmartRenderEngine.</span><span class="sxs-lookup"><span data-stu-id="3fa99-168">The class identifier is CLSID\_SmartRenderEngine.</span></span>
-   <span data-ttu-id="3fa99-169">Defina os parâmetros de compactação depois de criar o front-end, mas antes de renderizar os Pins de saída.</span><span class="sxs-lookup"><span data-stu-id="3fa99-169">Set compression parameters after you build the front end but before you render the output pins.</span></span> <span data-ttu-id="3fa99-170">Chame o método [**ISmartRenderEngine:: GetGroupCompressor**](ismartrenderengine-getgroupcompressor.md) para obter um ponteiro para o filtro de compactação de um grupo.</span><span class="sxs-lookup"><span data-stu-id="3fa99-170">Call the [**ISmartRenderEngine::GetGroupCompressor**](ismartrenderengine-getgroupcompressor.md) method to obtain a pointer to a group's compression filter.</span></span> <span data-ttu-id="3fa99-171">Em seguida, consulte a interface [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) , conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="3fa99-171">Then query for the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface, as described previously.</span></span>
-   <span data-ttu-id="3fa99-172">Quando você renderiza os Pins de saída, não é necessário inserir um filtro de compactação.</span><span class="sxs-lookup"><span data-stu-id="3fa99-172">When you render the output pins, there is no need to insert a compression filter.</span></span> <span data-ttu-id="3fa99-173">O fluxo já está compactado.</span><span class="sxs-lookup"><span data-stu-id="3fa99-173">The stream is already compressed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fa99-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3fa99-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fa99-175">Renderizando um projeto</span><span class="sxs-lookup"><span data-stu-id="3fa99-175">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



