---
description: Visualizando o projeto
ms.assetid: 00d72a39-f848-47ea-8460-8b826684eeea
title: Visualizando o projeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdf38fe19e500cfe9bd9a8dfb77f7ff56528a2f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103920000"
---
# <a name="previewing-the-project"></a><span data-ttu-id="75172-103">Visualizando o projeto</span><span class="sxs-lookup"><span data-stu-id="75172-103">Previewing the Project</span></span>

<span data-ttu-id="75172-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="75172-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="75172-105">Para visualizar o projeto, você precisa de um componente chamado *mecanismo de renderização*, que cria um grafo de filtro do DirectShow a partir de uma linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="75172-105">To preview the project, you need a component called a *render engine*, which builds a DirectShow filter graph from a timeline.</span></span> <span data-ttu-id="75172-106">O grafo de filtro é o que realmente renderiza o projeto.</span><span class="sxs-lookup"><span data-stu-id="75172-106">The filter graph is what actually renders the project.</span></span> <span data-ttu-id="75172-107">Você pode usar o mecanismo de renderização para visualizar um projeto ou gravar o arquivo de saída final.</span><span class="sxs-lookup"><span data-stu-id="75172-107">You can use the render engine to preview a project or to write the final output file.</span></span>

<span data-ttu-id="75172-108">Este artigo não entra em detalhes sobre o mecanismo de renderização.</span><span class="sxs-lookup"><span data-stu-id="75172-108">This article does not go into detail about the render engine.</span></span> <span data-ttu-id="75172-109">Para visualização, você só precisa de algumas chamadas de método.</span><span class="sxs-lookup"><span data-stu-id="75172-109">For preview, you only need a few method calls.</span></span> <span data-ttu-id="75172-110">Você pode encontrar uma discussão mais completa, incluindo como gravar arquivos de saída, na [renderização de um projeto](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="75172-110">You can find a more thorough discussion, including how to write output files, in [Rendering a Project](rendering-a-project.md).</span></span> <span data-ttu-id="75172-111">O exemplo de código a seguir mostra como construir um grafo de visualização.</span><span class="sxs-lookup"><span data-stu-id="75172-111">The following code example shows how to construct a preview graph.</span></span>


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
            IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
hr = pRender->RenderOutputPins( );
```



<span data-ttu-id="75172-112">Crie o mecanismo de renderização usando a função **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="75172-112">Create the render engine using the **CoCreateInstance** function.</span></span> <span data-ttu-id="75172-113">Em seguida, chame os seguintes métodos na interface [**IRenderEngine**](irenderengine.md) do mecanismo de renderização:</span><span class="sxs-lookup"><span data-stu-id="75172-113">Then call the following methods on the render engine's [**IRenderEngine**](irenderengine.md) interface:</span></span>

-   <span data-ttu-id="75172-114">[**Settimelineobject**](irenderengine-settimelineobject.md).</span><span class="sxs-lookup"><span data-stu-id="75172-114">[**SetTimelineObject**](irenderengine-settimelineobject.md).</span></span> <span data-ttu-id="75172-115">Especifica a linha do tempo a ser usada.</span><span class="sxs-lookup"><span data-stu-id="75172-115">Specifies the timeline to use.</span></span>
-   <span data-ttu-id="75172-116">[**ConnectFrontEnd**](irenderengine-connectfrontend.md).</span><span class="sxs-lookup"><span data-stu-id="75172-116">[**ConnectFrontEnd**](irenderengine-connectfrontend.md).</span></span> <span data-ttu-id="75172-117">Cria um gráfico de filtro parcial, com um pino de saída para cada grupo na linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="75172-117">Builds a partial filter graph, with one output pin for each group in the timeline.</span></span>
-   <span data-ttu-id="75172-118">[**RenderOutputPins**](irenderengine-renderoutputpins.md).</span><span class="sxs-lookup"><span data-stu-id="75172-118">[**RenderOutputPins**](irenderengine-renderoutputpins.md).</span></span> <span data-ttu-id="75172-119">Conclui o grafo de visualização conectando cada pino de saída a um processador de áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="75172-119">Completes the preview graph by connecting each output pin to a video or audio renderer.</span></span>

<span data-ttu-id="75172-120">Depois que o grafo for criado, você poderá visualizar o projeto executando o grafo, como faria com qualquer grafo de filtro do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="75172-120">Once the graph is built, you can preview the project by running the graph, as you would with any DirectShow filter graph.</span></span> <span data-ttu-id="75172-121">Primeiro, obtenha um ponteiro para o grafo de filtro chamando o método [**IRenderEngine:: GetFilterGraph**](irenderengine-getfiltergraph.md) .</span><span class="sxs-lookup"><span data-stu-id="75172-121">First, obtain a pointer to the filter graph by calling the [**IRenderEngine::GetFilterGraph**](irenderengine-getfiltergraph.md) method.</span></span>


```C++
IGraphBuilder   *pGraph = NULL;
hr = pRender->GetFilterGraph(&pGraph);
```



<span data-ttu-id="75172-122">Consulte o grafo de filtro para as interfaces [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) .</span><span class="sxs-lookup"><span data-stu-id="75172-122">Query the filter graph for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interfaces.</span></span> <span data-ttu-id="75172-123">Use essas duas interfaces para executar o grafo e aguardar a reprodução ser concluída.</span><span class="sxs-lookup"><span data-stu-id="75172-123">Use these two interfaces to run the graph and wait for playback to complete.</span></span> <span data-ttu-id="75172-124">Para obter uma explicação de como usar essas interfaces, consulte [como reproduzir um arquivo](how-to-play-a-file.md) e [responder a eventos](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="75172-124">For an explanation of how to use these interfaces, see [How To Play a File](how-to-play-a-file.md) and [Responding to Events](responding-to-events.md).</span></span> <span data-ttu-id="75172-125">O código a seguir mostra uma maneira de usar essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="75172-125">The following code shows one way to use these interfaces.</span></span>


```C++
IMediaControl   *pControl = NULL;
IMediaEvent     *pEvent = NULL;
long evCode;
pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
hr = pControl->Run();
hr = pEvent->WaitForCompletion(INFINITE, &evCode);
pControl->Stop();
```



<span data-ttu-id="75172-126">O código neste exemplo bloqueia a execução do programa até que a reprodução seja concluída, devido ao parâmetro infinito na chamada do método [**IMediaEvent:: WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) .</span><span class="sxs-lookup"><span data-stu-id="75172-126">The code in this example blocks program execution until playback completes, because of the INFINITE parameter in the [**IMediaEvent::WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) method call.</span></span> <span data-ttu-id="75172-127">No entanto, se algo der errado durante a reprodução, isso poderá fazer com que o programa pare de responder.</span><span class="sxs-lookup"><span data-stu-id="75172-127">If something goes wrong during playback, however, it could cause the program to stop responding.</span></span> <span data-ttu-id="75172-128">Em um aplicativo real, use um loop de mensagem para aguardar a reprodução ser concluída.</span><span class="sxs-lookup"><span data-stu-id="75172-128">In a real application, use a message loop to wait for playback to complete.</span></span> <span data-ttu-id="75172-129">Também é recomendável que você forneça ao usuário uma maneira de interromper a reprodução.</span><span class="sxs-lookup"><span data-stu-id="75172-129">It's also recommended that you provide the user with a way to interrupt playback.</span></span>

<span data-ttu-id="75172-130">Quando você terminar de usar o mecanismo de renderização, chame sempre o método [**IRenderEngine:: ScrapIt**](irenderengine-scrapit.md) .</span><span class="sxs-lookup"><span data-stu-id="75172-130">When you finish using the render engine, always call the [**IRenderEngine::ScrapIt**](irenderengine-scrapit.md) method.</span></span> <span data-ttu-id="75172-131">Esse método exclui o gráfico de filtro e libera todos os recursos mantidos pelo mecanismo de renderização.</span><span class="sxs-lookup"><span data-stu-id="75172-131">This method deletes the filter graph and releases any resources held by the render engine.</span></span>


```C++
pRender->ScrapIt();
```



## <a name="related-topics"></a><span data-ttu-id="75172-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="75172-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75172-133">Carregando e visualizando um projeto</span><span class="sxs-lookup"><span data-stu-id="75172-133">Loading and Previewing a Project</span></span>](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



