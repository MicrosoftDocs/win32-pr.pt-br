---
description: Visualizando um projeto
ms.assetid: 2efa3f25-a93f-4362-b461-b67475e5d78c
title: Visualizando um projeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd9d299a99a0a7315cec986fbc044d427385647
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104295995"
---
# <a name="previewing-a-project"></a><span data-ttu-id="1e510-103">Visualizando um projeto</span><span class="sxs-lookup"><span data-stu-id="1e510-103">Previewing a Project</span></span>

<span data-ttu-id="1e510-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="1e510-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="1e510-105">Para visualizar um projeto, primeiro chame **CoCreateInstance** para criar uma instância do mecanismo de renderização básico.</span><span class="sxs-lookup"><span data-stu-id="1e510-105">To preview a project, first call **CoCreateInstance** to create an instance of the Basic Render Engine.</span></span> <span data-ttu-id="1e510-106">O identificador de classe é CLSID \_ RenderEngine.</span><span class="sxs-lookup"><span data-stu-id="1e510-106">The class identifier is CLSID\_RenderEngine.</span></span> <span data-ttu-id="1e510-107">Em seguida, chame o método [**IRenderEngine:: Settimelineobject**](irenderengine-settimelineobject.md) para especificar a linha do tempo que você está renderizando.</span><span class="sxs-lookup"><span data-stu-id="1e510-107">Then call the [**IRenderEngine::SetTimelineObject**](irenderengine-settimelineobject.md) method to specify the timeline that you are rendering.</span></span>

<span data-ttu-id="1e510-108">Na primeira vez que você visualizar a linha do tempo, execute as seguintes chamadas na ordem listada:</span><span class="sxs-lookup"><span data-stu-id="1e510-108">The first time that you preview the timeline, perform the following calls in the order listed:</span></span>

1.  <span data-ttu-id="1e510-109">Chame [**IRenderEngine:: SetRenderRange**](irenderengine-setrenderrange.md) para especificar qual parte da linha do tempo será visualizada.</span><span class="sxs-lookup"><span data-stu-id="1e510-109">Call [**IRenderEngine::SetRenderRange**](irenderengine-setrenderrange.md) to specify which portion of the timeline to preview.</span></span> <span data-ttu-id="1e510-110">(Opcional)</span><span class="sxs-lookup"><span data-stu-id="1e510-110">(Optional)</span></span>
2.  <span data-ttu-id="1e510-111">Chame [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) para criar o front-end do grafo.</span><span class="sxs-lookup"><span data-stu-id="1e510-111">Call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) to build the front end of the graph.</span></span>
3.  <span data-ttu-id="1e510-112">Chame [**IRenderEngine:: RenderOutputPins**](irenderengine-renderoutputpins.md).</span><span class="sxs-lookup"><span data-stu-id="1e510-112">Call [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md).</span></span> <span data-ttu-id="1e510-113">Esse método conecta cada pino de saída a um processador de vídeo ou processador de áudio, concluindo o grafo.</span><span class="sxs-lookup"><span data-stu-id="1e510-113">This method connects each output pin to a video renderer or audio renderer, completing the graph.</span></span>

<span data-ttu-id="1e510-114">O exemplo de código a seguir mostra estas etapas:</span><span class="sxs-lookup"><span data-stu-id="1e510-114">The following code example shows these steps:</span></span>


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, 
    CLSCTX_INPROC_SERVER, IID_IRenderEngine, (void**)&pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd();
hr = pRender->RenderOutputPins();
```



<span data-ttu-id="1e510-115">Agora, execute o gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="1e510-115">Now run the filter graph.</span></span> <span data-ttu-id="1e510-116">Primeiro, chame o método [**IRenderEngine:: GetFilterGraph**](irenderengine-getfiltergraph.md) para recuperar um ponteiro para a interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) do Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="1e510-116">First, call the [**IRenderEngine::GetFilterGraph**](irenderengine-getfiltergraph.md) method to retrieve a pointer to the Filter Graph Manager's [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface.</span></span> <span data-ttu-id="1e510-117">Em seguida, consulte o Gerenciador do grafo de filtro para a interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e chame [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), conforme mostrado no código a seguir:</span><span class="sxs-lookup"><span data-stu-id="1e510-117">Then query the Filter Graph Manager for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface and call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), as shown in the following code:</span></span>


```C++
IGraphBuilder   *pGraph = NULL;
IMediaControl   *pControl = NULL;
hr = pRender->GetFilterGraph(&pGraph);
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pControl->Run();
```



<span data-ttu-id="1e510-118">Use a interface [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) do Gerenciador de grafo de filtro para aguardar a conclusão da visualização.</span><span class="sxs-lookup"><span data-stu-id="1e510-118">Use the Filter Graph Manager's [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface to wait for the preview to complete.</span></span> <span data-ttu-id="1e510-119">Você também pode buscar o grafo usando a interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) do Gerenciador de grafo de filtro, assim como faria com um grafo de reprodução de arquivo.</span><span class="sxs-lookup"><span data-stu-id="1e510-119">You can also seek the graph using the Filter Graph Manager's [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, just as you would with a file playback graph.</span></span>

<span data-ttu-id="1e510-120">Para visualizar o projeto novamente, busque o grafo de volta para o tempo zero e chame a **execução** novamente.</span><span class="sxs-lookup"><span data-stu-id="1e510-120">To preview the project again, seek the graph back to time zero and call **Run** again.</span></span> <span data-ttu-id="1e510-121">Se você alterar o conteúdo da linha do tempo, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1e510-121">If you change the contents of the timeline, do the following:</span></span>

1.  <span data-ttu-id="1e510-122">Chame **SetRenderRange**.</span><span class="sxs-lookup"><span data-stu-id="1e510-122">Call **SetRenderRange**.</span></span> <span data-ttu-id="1e510-123">(Opcional)</span><span class="sxs-lookup"><span data-stu-id="1e510-123">(Optional)</span></span>
2.  <span data-ttu-id="1e510-124">Chame **ConnectFrontEnd**.</span><span class="sxs-lookup"><span data-stu-id="1e510-124">Call **ConnectFrontEnd**.</span></span>
3.  <span data-ttu-id="1e510-125">Se o método **ConnectFrontEnd** retornar S \_ \_ OUTPUTRESET de aviso, chame **RenderOutputPins**.</span><span class="sxs-lookup"><span data-stu-id="1e510-125">If the **ConnectFrontEnd** method returns S\_WARN\_OUTPUTRESET, call **RenderOutputPins**.</span></span> <span data-ttu-id="1e510-126">(Se **ConnectFrontEnd** retornar S \_ OK, você pode ignorar esta etapa.)</span><span class="sxs-lookup"><span data-stu-id="1e510-126">(If **ConnectFrontEnd** returns S\_OK, you can skip this step.)</span></span>
4.  <span data-ttu-id="1e510-127">Busque o grafo de volta para o tempo zero.</span><span class="sxs-lookup"><span data-stu-id="1e510-127">Seek the graph back to time zero.</span></span>
5.  <span data-ttu-id="1e510-128">Execute o grafo.</span><span class="sxs-lookup"><span data-stu-id="1e510-128">Run the graph.</span></span>

<span data-ttu-id="1e510-129">O exemplo a seguir mostra estas etapas:</span><span class="sxs-lookup"><span data-stu-id="1e510-129">The following example shows these steps:</span></span>


```C++
hr = pRender->ConnectFrontEnd();
if (hr == S_WARN_OUTPUTRESET)
{
    hr = pRender->RenderOutputPins();
}
LONGLONG llStart = 0; 
hr = pSeek->SetPositions(&llStart, AM_SEEKING_AbsolutePositioning, 0, 0); 
hr = pControl->Run();
```



<span data-ttu-id="1e510-130">Para obter um exemplo completo que carrega e visualiza um arquivo de projeto, consulte [carregando e visualizando um projeto](loading-and-previewing-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="1e510-130">For a complete example that loads and previews a project file, see [Loading and Previewing a Project](loading-and-previewing-a-project.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e510-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1e510-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e510-132">Gerenciando projetos de edição de vídeo</span><span class="sxs-lookup"><span data-stu-id="1e510-132">Managing Video Editing Projects</span></span>](managing-video-editing-projects.md)
</dt> <dt>

[<span data-ttu-id="1e510-133">Renderizando um projeto</span><span class="sxs-lookup"><span data-stu-id="1e510-133">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



