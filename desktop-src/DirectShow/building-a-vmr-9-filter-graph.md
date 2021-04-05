---
description: Criando um grafo de filtro do VMR-9
ms.assetid: fd83a89c-f1b6-48a3-971e-04ae4ac14c66
title: Criando um grafo de filtro do VMR-9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d7fc1eb0982b47f5ef50a00a1c7a275dd8bf60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825905"
---
# <a name="building-a-vmr-9-filter-graph"></a><span data-ttu-id="d443b-103">Criando um grafo de filtro do VMR-9</span><span class="sxs-lookup"><span data-stu-id="d443b-103">Building a VMR-9 Filter Graph</span></span>

<span data-ttu-id="d443b-104">Como o filtro de mixagem do vídeo 9 Filter (VMR-9) não é o renderizador de vídeo padrão, um aplicativo que usa o VMR-9 deve adicioná-lo explicitamente ao grafo e conectá-lo.</span><span class="sxs-lookup"><span data-stu-id="d443b-104">Because the Video Mixing Renderer 9 Filter (VMR-9) is not the default video renderer, an application that uses the VMR-9 must explicitly add it to the graph and connect it.</span></span> <span data-ttu-id="d443b-105">Esta seção apresenta duas abordagens diferentes para a criação de gráficos de filtro com o VMR-9.</span><span class="sxs-lookup"><span data-stu-id="d443b-105">This section presents two different approaches to building filter graphs with the VMR-9.</span></span>

<span data-ttu-id="d443b-106">Usando o construtor de grafo de captura</span><span class="sxs-lookup"><span data-stu-id="d443b-106">Using the Capture Graph Builder</span></span>

<span data-ttu-id="d443b-107">O construtor do grafo de captura é um objeto auxiliar para criar gráficos de filtro personalizados.</span><span class="sxs-lookup"><span data-stu-id="d443b-107">The Capture Graph Builder is a helper object for building custom filter graphs.</span></span> <span data-ttu-id="d443b-108">Você pode usá-lo para criar gráficos do VMR-9 da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d443b-108">You can use it to build VMR-9 graphs as follows:</span></span>

1.  <span data-ttu-id="d443b-109">Crie e inicialize o construtor do grafo de captura, conforme descrito no tópico [sobre o construtor do grafo de captura](about-the-capture-graph-builder.md).</span><span class="sxs-lookup"><span data-stu-id="d443b-109">Create and initialize the Capture Graph Builder, as described in the topic [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
2.  <span data-ttu-id="d443b-110">Chame CoCreateInstance para criar o VMR-9:</span><span class="sxs-lookup"><span data-stu-id="d443b-110">Call CoCreateInstance to create the VMR-9:</span></span>
    ```C++
    IBaseFilter *pVmr = NULL;
    hr = CoCreateInstance(CLSID_VideoMixingRenderer9, 0, 
        CLSCTX_INPROC_SERVER, IID_IBaseFilter, (void**)&pVmr);
    ```

    

3.  <span data-ttu-id="d443b-111">Chame [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) no Gerenciador do grafo de filtro para adicionar o VMR-9 ao grafo de filtro:</span><span class="sxs-lookup"><span data-stu-id="d443b-111">Call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) on the Filter Graph Manager to add the VMR-9 to the filter graph:</span></span>
    ```C++
    hr = pGraph->AddFilter(pVmr, L"VMR9");
    ```

    

4.  <span data-ttu-id="d443b-112">Chame [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) para adicionar um filtro de origem para o arquivo de vídeo:</span><span class="sxs-lookup"><span data-stu-id="d443b-112">Call [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) to add a source filter for the video file:</span></span>
    ```C++
    IBaseFilter *pSource;
    hr = pGraph->AddSourceFilter(L"C:\\Example.avi", L"Source1", &pSource);
    ```

    

5.  <span data-ttu-id="d443b-113">Chame o método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para renderizar o fluxo de vídeo para o VMR:</span><span class="sxs-lookup"><span data-stu-id="d443b-113">Call the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method to render the video stream to the VMR:</span></span>
    ```C++
    hr = pBuild->RenderStream(0, 0, pSource, 0, pVmr);  
    ```

    

6.  <span data-ttu-id="d443b-114">Opcionalmente, chame RenderStream novamente para renderizar o fluxo de áudio:</span><span class="sxs-lookup"><span data-stu-id="d443b-114">Optionally, call RenderStream again to render the audio stream:</span></span>
    ```C++
    hr = pBuild->RenderStream(0, &MEDIATYPE_Audio, pSource, 0, NULL);
    ```

    

<span data-ttu-id="d443b-115">Você pode misturar vários fluxos de vídeo chamando AddSourceFilter e RenderStream para cada arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="d443b-115">You can mix several video streams by calling AddSourceFilter and RenderStream for each source file.</span></span>

<span data-ttu-id="d443b-116">Usando o Gerenciador de gráficos de filtro</span><span class="sxs-lookup"><span data-stu-id="d443b-116">Using the Filter Graph Manager</span></span>

<span data-ttu-id="d443b-117">Se preferir não usar o construtor do grafo de captura, você poderá criar um grafo do VMR-9 simplesmente usando métodos no Gerenciador do grafo de filtro, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d443b-117">If you prefer not to use the Capture Graph Builder, you can build a VMR-9 graph simply using methods on the Filter Graph Manager, as follows:</span></span>

1.  <span data-ttu-id="d443b-118">Crie o VMR-9 e adicione-o ao grafo, conforme mostrado no procedimento anterior.</span><span class="sxs-lookup"><span data-stu-id="d443b-118">Create the VMR-9 and add it to the graph, as shown in the previous procedure.</span></span>
2.  <span data-ttu-id="d443b-119">Use AddSourceFilter para adicionar um filtro de origem para o arquivo de vídeo, conforme mostrado no procedimento anterior.</span><span class="sxs-lookup"><span data-stu-id="d443b-119">Use AddSourceFilter to add a source filter for the video file, as shown in the previous procedure.</span></span>
3.  <span data-ttu-id="d443b-120">Se você quiser renderizar o áudio, crie uma instância do filtro de [renderizador DirectSound](directsound-renderer-filter.md) e adicione-o ao grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="d443b-120">If you want to render the audio, create an instance of the [DirectSound Renderer](directsound-renderer-filter.md) filter and add it to the filter graph.</span></span>
4.  <span data-ttu-id="d443b-121">Use o método IBaseFilter:: EnumPins para localizar um PIN de saída no filtro de origem.</span><span class="sxs-lookup"><span data-stu-id="d443b-121">Use the IBaseFilter::EnumPins method to find an output pin on the source filter.</span></span> <span data-ttu-id="d443b-122">Consulte [enumerando Pins](enumerating-pins.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="d443b-122">See [Enumerating Pins](enumerating-pins.md) for details.</span></span>
5.  <span data-ttu-id="d443b-123">Consulte o Gerenciador de gráfico de filtro para a interface IFilterGraph2.</span><span class="sxs-lookup"><span data-stu-id="d443b-123">Query the Filter Graph Manager for the IFilterGraph2 interface.</span></span>
6.  <span data-ttu-id="d443b-124">Chame [**IFilterGraph2:: RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) com o \_ sinalizador am RenderEx \_ RENDERTOEXISTINGRENDERERS.</span><span class="sxs-lookup"><span data-stu-id="d443b-124">Call [**IFilterGraph2::RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) with the AM\_RENDEREX\_RENDERTOEXISTINGRENDERERS flag.</span></span> <span data-ttu-id="d443b-125">Essa chamada renderiza o pino de saída, usando apenas os filtros de processador que já estão no grafo — nesse caso, o VMR-9 e o renderizador DirectSound.</span><span class="sxs-lookup"><span data-stu-id="d443b-125">This call renders the output pin, using only the renderer filters already in the graph — in this case, the VMR-9 and the DirectSound Renderer.</span></span> <span data-ttu-id="d443b-126">Isso impede que a lógica de conexão inteligente adicione o renderizador de vídeo padrão ao grafo, o que deixaria o VMR-9 desconectado.</span><span class="sxs-lookup"><span data-stu-id="d443b-126">This prevents the Intelligent Connect logic from adding the default video renderer to the graph, which would leave the VMR-9 unconnected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d443b-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d443b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d443b-128">Criando gráficos com o construtor de grafo de captura</span><span class="sxs-lookup"><span data-stu-id="d443b-128">Building Graphs with the Capture Graph Builder</span></span>](building-graphs-with-the-capture-graph-builder.md)
</dt> </dl>

 

 



