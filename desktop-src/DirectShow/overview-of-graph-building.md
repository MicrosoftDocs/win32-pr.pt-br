---
description: Visão geral da construção de gráficos
ms.assetid: 5753f06c-ecfd-48d7-a8e9-768b798e9279
title: Visão geral da construção de gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69ef9ea0f4f9e21d33372ad2a37a59b512d5dcc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087554"
---
# <a name="overview-of-graph-building"></a><span data-ttu-id="c3106-103">Visão geral da construção de gráficos</span><span class="sxs-lookup"><span data-stu-id="c3106-103">Overview of Graph Building</span></span>

<span data-ttu-id="c3106-104">Para criar um gráfico de filtro, comece criando uma instância do Gerenciador do grafo de filtro:</span><span class="sxs-lookup"><span data-stu-id="c3106-104">To create a filter graph, begin by creating an instance of the Filter Graph Manager:</span></span>


```C++
IGraphBuilder* pIGB;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER, IID_IGraphBuilder,
    (void **)&pIGB);
```



<span data-ttu-id="c3106-105">O Gerenciador de gráficos de filtro dá suporte aos seguintes métodos de construção de grafo:</span><span class="sxs-lookup"><span data-stu-id="c3106-105">The Filter Graph Manager supports the following graph-building methods:</span></span>

-   <span data-ttu-id="c3106-106">[**IFilterGraph:: ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) tenta fazer uma conexão direta entre dois Pins.</span><span class="sxs-lookup"><span data-stu-id="c3106-106">[**IFilterGraph::ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) tries to make a direct connection between two pins.</span></span> <span data-ttu-id="c3106-107">Se os Pins não puderem se conectar, o método falhará.</span><span class="sxs-lookup"><span data-stu-id="c3106-107">If the pins cannot connect, the method fails.</span></span>
-   <span data-ttu-id="c3106-108">[**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) conecta dois Pins.</span><span class="sxs-lookup"><span data-stu-id="c3106-108">[**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) connects two pins.</span></span> <span data-ttu-id="c3106-109">Se possível, ele faz uma conexão direta.</span><span class="sxs-lookup"><span data-stu-id="c3106-109">If possible, it makes a direct connection.</span></span> <span data-ttu-id="c3106-110">Caso contrário, ele usa filtros intermediários para concluir a conexão.</span><span class="sxs-lookup"><span data-stu-id="c3106-110">Otherwise, it uses intermediate filters to complete the connection.</span></span>
-   <span data-ttu-id="c3106-111">[**IGraphBuilder:: render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) inicia a partir de um PIN de saída e compila o restante do grafo.</span><span class="sxs-lookup"><span data-stu-id="c3106-111">[**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) starts from an output pin and builds the rest of the graph.</span></span> <span data-ttu-id="c3106-112">Esse método adiciona filtros conforme necessário, trabalhando downstream, até alcançar um filtro de processador.</span><span class="sxs-lookup"><span data-stu-id="c3106-112">This methods adds filters as needed, working downstream, until it reaches a renderer filter.</span></span>
-   <span data-ttu-id="c3106-113">[**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) cria um grafo de reprodução de arquivo completo.</span><span class="sxs-lookup"><span data-stu-id="c3106-113">[**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) builds a complete file-playback graph.</span></span>
-   <span data-ttu-id="c3106-114">[**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) adiciona um filtro ao grafo.</span><span class="sxs-lookup"><span data-stu-id="c3106-114">[**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) adds a filter to the graph.</span></span> <span data-ttu-id="c3106-115">Ele não conecta o filtro.</span><span class="sxs-lookup"><span data-stu-id="c3106-115">It does not connect the filter.</span></span> <span data-ttu-id="c3106-116">Você deve criar o filtro antes de chamar esse método chamando **CoCreateInstance** ou usando o mapeador de filtro ou o enumerador de dispositivo do sistema.</span><span class="sxs-lookup"><span data-stu-id="c3106-116">You must create the filter before calling this method, either by calling **CoCreateInstance** or by using the Filter Mapper or System Device Enumerator.</span></span>

<span data-ttu-id="c3106-117">Esses métodos fornecem três abordagens básicas para criar o grafo:</span><span class="sxs-lookup"><span data-stu-id="c3106-117">These methods provide three basic approaches to building the graph:</span></span>

1.  <span data-ttu-id="c3106-118">O Gerenciador de gráfico de filtro cria o grafo inteiro.</span><span class="sxs-lookup"><span data-stu-id="c3106-118">The Filter Graph Manager builds the entire graph.</span></span>
2.  <span data-ttu-id="c3106-119">O Gerenciador de gráficos de filtro cria parte do grafo.</span><span class="sxs-lookup"><span data-stu-id="c3106-119">The Filter Graph Manager builds part of the graph.</span></span>
3.  <span data-ttu-id="c3106-120">O aplicativo cria todo o grafo.</span><span class="sxs-lookup"><span data-stu-id="c3106-120">The application builds the entire graph.</span></span>

<span data-ttu-id="c3106-121">**O Gerenciador do grafo de filtro cria o grafo inteiro**</span><span class="sxs-lookup"><span data-stu-id="c3106-121">**The Filter Graph Manager Builds the Entire Graph**</span></span>

<span data-ttu-id="c3106-122">Se você simplesmente deseja reproduzir um arquivo que é criado em um formato reconhecido, como AVI, MPEG, WAV ou MP3, use o método **RenderFile** .</span><span class="sxs-lookup"><span data-stu-id="c3106-122">If you simply want to play a file that is authored in a recognized format, such as AVI, MPEG, WAV, or MP3, use the **RenderFile** method.</span></span> <span data-ttu-id="c3106-123">O artigo [como reproduzir um arquivo](how-to-play-a-file.md) mostra como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="c3106-123">The article [How To Play a File](how-to-play-a-file.md) shows how to do this.</span></span>

<span data-ttu-id="c3106-124">O método **RenderFile** começa examinando o registro de um filtro de origem que pode analisar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="c3106-124">The **RenderFile** method starts by looking in the registry for a source filter that can parse the file.</span></span> <span data-ttu-id="c3106-125">Ele usa o protocolo (como " `https://` " na URL), a extensão de arquivo ou os padrões de byte predefinidos no arquivo para determinar o filtro de origem.</span><span class="sxs-lookup"><span data-stu-id="c3106-125">It uses the protocol (such as " `https://` " in the URL), the file extension, or pre-defined byte patterns in the file to determine the source filter.</span></span> <span data-ttu-id="c3106-126">Para obter detalhes, consulte [registrando um tipo de arquivo personalizado](registering-a-custom-file-type.md).</span><span class="sxs-lookup"><span data-stu-id="c3106-126">For details, see [Registering a Custom File Type](registering-a-custom-file-type.md).</span></span>

<span data-ttu-id="c3106-127">Para compilar o restante do grafo, o Gerenciador de gráficos de filtro usa um processo iterativo em que ele usa os tipos de mídia aos quais um filtro dá suporte em seus PINs de saída e pesquisa o registro em busca de filtros que aceitarão esse tipo de mídia como entrada.</span><span class="sxs-lookup"><span data-stu-id="c3106-127">To build the rest of the graph, the Filter Graph Manager uses an iterative process wherein it takes the media types that a filter supports on its output pins, and searches the registry for filters that will accept that media type as input.</span></span> <span data-ttu-id="c3106-128">Ele usa vários critérios para restringir os filtros de pesquisa e priorização:</span><span class="sxs-lookup"><span data-stu-id="c3106-128">It uses several criteria to narrow the search and prioritize filters:</span></span>

-   <span data-ttu-id="c3106-129">A *categoria de filtro* identifica a funcionalidade geral do filtro.</span><span class="sxs-lookup"><span data-stu-id="c3106-129">The *filter category* identifies the general functionality of the filter.</span></span>
-   <span data-ttu-id="c3106-130">O tipo de mídia descreve que tipo de dados o filtro pode aceitar como entrada ou entrega como saída.</span><span class="sxs-lookup"><span data-stu-id="c3106-130">The media type describes what kind of data the filter can accept as input or deliver as output.</span></span>
-   <span data-ttu-id="c3106-131">O *mérito* determina a ordem em que os filtros são tentados.</span><span class="sxs-lookup"><span data-stu-id="c3106-131">The *merit* determines the order in which filters are tried.</span></span> <span data-ttu-id="c3106-132">Se dois filtros na mesma categoria de filtro oferecerem suporte aos mesmos tipos de entrada, o Gerenciador de gráfico de filtro selecionará aquele com o maior valor de mérito.</span><span class="sxs-lookup"><span data-stu-id="c3106-132">If two filters in the same filter category both support the same input types, the Filter Graph Manager selects the one with the highest merit value.</span></span> <span data-ttu-id="c3106-133">Alguns filtros são intencionalmente concedidos a um valor de mérito baixo, pois eles são projetados para fins especializados e devem ser adicionados somente ao grafo pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c3106-133">Some filters are purposely given a low merit value because they are designed for specialized purposes and should only be added to the graph by the application.</span></span>

<span data-ttu-id="c3106-134">O Gerenciador de gráfico de filtro usa o objeto [mapeador de filtro](filter-mapper.md) para pesquisar o registro.</span><span class="sxs-lookup"><span data-stu-id="c3106-134">The Filter Graph Manager uses the [Filter Mapper](filter-mapper.md) object to search the registry.</span></span>

<span data-ttu-id="c3106-135">À medida que cada filtro é adicionado, o Gerenciador do grafo de filtro tenta conectá-lo ao pino de saída do filtro anterior.</span><span class="sxs-lookup"><span data-stu-id="c3106-135">As each filter is added, the Filter Graph Manager tries to connect it to the previous filter's output pin.</span></span> <span data-ttu-id="c3106-136">Os filtros negociam para determinar se podem se conectar e, em caso afirmativo, qual tipo de mídia usar para a conexão.</span><span class="sxs-lookup"><span data-stu-id="c3106-136">The filters negotiate to determine whether they can connect, and if so, what media type to use for the connection.</span></span> <span data-ttu-id="c3106-137">Se o novo filtro não puder se conectar, o Gerenciador de gráfico de filtro o descartará e tentará outro filtro.</span><span class="sxs-lookup"><span data-stu-id="c3106-137">If the new filter cannot connect, the Filter Graph Manager discards it and tries another filter.</span></span> <span data-ttu-id="c3106-138">Esse processo continua até que cada fluxo seja renderizado.</span><span class="sxs-lookup"><span data-stu-id="c3106-138">This process continues until every stream is rendered.</span></span>

<span data-ttu-id="c3106-139">**O Gerenciador de gráficos de filtro cria parte do grafo**</span><span class="sxs-lookup"><span data-stu-id="c3106-139">**The Filter Graph Manager Builds Part of the Graph**</span></span>

<span data-ttu-id="c3106-140">Para fazer algo além de simplesmente reproduzir um arquivo, seu aplicativo deve executar pelo menos parte do trabalho de construção do grafo.</span><span class="sxs-lookup"><span data-stu-id="c3106-140">To do something beyond simply playing a file, your application must perform at least some of the graph building work.</span></span> <span data-ttu-id="c3106-141">Por exemplo, um aplicativo de captura de vídeo deve selecionar um filtro de origem de captura e adicioná-lo ao grafo.</span><span class="sxs-lookup"><span data-stu-id="c3106-141">For example, a video capture application must select a capture source filter and add it to the graph.</span></span> <span data-ttu-id="c3106-142">Se você estiver gravando dados em um arquivo AVI, deverá adicionar os filtros AVI Mux e gravador de arquivo ao grafo.</span><span class="sxs-lookup"><span data-stu-id="c3106-142">If you are writing data to an AVI file, you must add the AVI Mux and File Writer filters to the graph.</span></span> <span data-ttu-id="c3106-143">No entanto, muitas vezes é possível deixar o Gerenciador de gráfico de filtro concluir o grafo.</span><span class="sxs-lookup"><span data-stu-id="c3106-143">However, it is often possible to let the Filter Graph Manager complete the graph.</span></span> <span data-ttu-id="c3106-144">Por exemplo, você pode renderizar um PIN para visualização chamando o método **render** .</span><span class="sxs-lookup"><span data-stu-id="c3106-144">For example, you can render a pin for preview by calling the **Render** method.</span></span>

<span data-ttu-id="c3106-145">**O aplicativo cria o grafo inteiro**</span><span class="sxs-lookup"><span data-stu-id="c3106-145">**The Application Builds the Entire Graph**</span></span>

<span data-ttu-id="c3106-146">Em alguns cenários, seu aplicativo pode precisar criar o grafo adicionando e conectando cada filtro.</span><span class="sxs-lookup"><span data-stu-id="c3106-146">In some scenarios, your application may need to build the graph by adding and connecting each filter.</span></span> <span data-ttu-id="c3106-147">Nesse caso, você provavelmente saberá especificamente quais filtros devem ser adicionados ao grafo.</span><span class="sxs-lookup"><span data-stu-id="c3106-147">In this case, you probably know specifically which filters should be added to the graph.</span></span> <span data-ttu-id="c3106-148">Com essa abordagem, o aplicativo adiciona cada filtro chamando **AddFilter**, enumera os Pins nos filtros e os conecta chamando **Connect** ou **ConnectDirect**.</span><span class="sxs-lookup"><span data-stu-id="c3106-148">With this approach, the application adds each filter by calling **AddFilter**, enumerates the pins on the filters, and connects them by calling either **Connect** or **ConnectDirect**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3106-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c3106-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3106-150">Criando gráficos com o construtor de grafo de captura</span><span class="sxs-lookup"><span data-stu-id="c3106-150">Building Graphs with the Capture Graph Builder</span></span>](building-graphs-with-the-capture-graph-builder.md)
</dt> <dt>

[<span data-ttu-id="c3106-151">Enumerando dispositivos e filtros</span><span class="sxs-lookup"><span data-stu-id="c3106-151">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="c3106-152">Enumerando objetos em um grafo de filtro</span><span class="sxs-lookup"><span data-stu-id="c3106-152">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="c3106-153">Técnicas de Graph-Building geral</span><span class="sxs-lookup"><span data-stu-id="c3106-153">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="c3106-154">Criando o grafo de filtro</span><span class="sxs-lookup"><span data-stu-id="c3106-154">Building the Filter Graph</span></span>](building-the-filter-graph.md)
</dt> </dl>

 

 



