---
description: Arquitetura de serviços de edição do DirectShow
ms.assetid: ba6cc3f1-9130-4197-8501-c2d0a088e847
title: Arquitetura de serviços de edição do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c6059eebe9228e61d3de9677972eedfcb51c62
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105751669"
---
# <a name="directshow-editing-services-architecture"></a><span data-ttu-id="bf7c4-103">Arquitetura de serviços de edição do DirectShow</span><span class="sxs-lookup"><span data-stu-id="bf7c4-103">DirectShow Editing Services Architecture</span></span>

<span data-ttu-id="bf7c4-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="bf7c4-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="bf7c4-105">A ilustração a seguir mostra a arquitetura dos [serviços de edição do DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="bf7c4-105">The following illustration shows the architecture of [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

![arquitetura de serviços de edição do DirectShow](images/architecture.png)

-   <span data-ttu-id="bf7c4-107">Linha do tempo: representa uma produção de vídeo como uma coleção de clipes de origem, transições e efeitos, organizados em um conjunto de faixas aninhadas.</span><span class="sxs-lookup"><span data-stu-id="bf7c4-107">Timeline: Represents a video production as a collection of source clips, transitions, and effects, organized into a set of nested tracks.</span></span> <span data-ttu-id="bf7c4-108">Para obter mais informações, consulte [o modelo de linha do tempo](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="bf7c4-108">For more information, see [The Timeline Model](the-timeline-model.md).</span></span>
-   <span data-ttu-id="bf7c4-109">Analisador XML: analisa a linha do tempo e gera um arquivo de saída, ou lê um arquivo de entrada e gera uma linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="bf7c4-109">XML Parser: Parses the timeline and generates an output file, or reads an input file and generates a timeline.</span></span> <span data-ttu-id="bf7c4-110">O DES dá suporte a um formato de persistência baseado em XML.</span><span class="sxs-lookup"><span data-stu-id="bf7c4-110">DES supports an XML-based persistence format.</span></span>
-   <span data-ttu-id="bf7c4-111">Mecanismo de renderização: traduz a linha do tempo em um formulário que pode ser renderizado como mídia de streaming.</span><span class="sxs-lookup"><span data-stu-id="bf7c4-111">Render engine: Translates the timeline into a form that can be rendered as streaming media.</span></span> <span data-ttu-id="bf7c4-112">Por padrão, o mecanismo de renderização produz um grafo de filtro do DirectShow (consulte a próxima seção).</span><span class="sxs-lookup"><span data-stu-id="bf7c4-112">By default, the render engine produces a DirectShow filter graph (see next section).</span></span>
-   <span data-ttu-id="bf7c4-113">Localizador de mídia: mantém um cache de locais de elementos de mídia.</span><span class="sxs-lookup"><span data-stu-id="bf7c4-113">Media locator: Maintains a cache of locations of media elements.</span></span> <span data-ttu-id="bf7c4-114">Quando uma tentativa de abrir um elemento de mídia falha, o DES usa o cache para localizar o elemento, com base em um histórico de aberturas bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="bf7c4-114">When an attempt to open a media element fails, DES uses the cache to locate the element, based on a history of successful opens.</span></span>

<span data-ttu-id="bf7c4-115">A linha do tempo é uma descrição abstrata de um projeto de edição de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bf7c4-115">The timeline is an abstract description of a video editing project.</span></span> <span data-ttu-id="bf7c4-116">Ele especifica os clipes de origem usados no projeto, os horários de início e de parada, efeitos e transições e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="bf7c4-116">It specifies the source clips used in the project, start and stop times, effects and transitions, and so forth.</span></span> <span data-ttu-id="bf7c4-117">No entanto, a linha do tempo não renderiza os fluxos de vídeo e áudio.</span><span class="sxs-lookup"><span data-stu-id="bf7c4-117">The timeline does not render the video and audio streams, however.</span></span> <span data-ttu-id="bf7c4-118">Em vez disso, o mecanismo de renderização converte a linha do tempo em um grafo de filtro, para visualização ou saída de arquivo.</span><span class="sxs-lookup"><span data-stu-id="bf7c4-118">Instead, the render engine translates the timeline into a filter graph, for either preview or file output.</span></span> <span data-ttu-id="bf7c4-119">Um aplicativo manipula a linha do tempo em vez de manipular diretamente o grafo de filtro, o que seria complicado e propenso a erros.</span><span class="sxs-lookup"><span data-stu-id="bf7c4-119">An application manipulates the timeline rather than directly manipulating the filter graph, which would be cumbersome and error prone.</span></span>

<span data-ttu-id="bf7c4-120">A tabela a seguir lista as principais tarefas que um aplicativo de edição de vídeo típico executa, juntamente com as interfaces que oferecem suporte a cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="bf7c4-120">The following table lists the main tasks that a typical video editing application performs, along with the interfaces that support each task.</span></span> <span data-ttu-id="bf7c4-121">As seções posteriores descrevem essas tarefas e as interfaces mais detalhadamente.</span><span class="sxs-lookup"><span data-stu-id="bf7c4-121">Later sections describe these tasks and the interfaces in more detail.</span></span>



| <span data-ttu-id="bf7c4-122">Tarefa</span><span class="sxs-lookup"><span data-stu-id="bf7c4-122">Task</span></span>                                     | <span data-ttu-id="bf7c4-123">Interface (s)</span><span class="sxs-lookup"><span data-stu-id="bf7c4-123">Interface(s)</span></span>                                                                             |
|------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf7c4-124">Construa ou modifique uma linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="bf7c4-124">Construct or modify a timeline.</span></span>          | <span data-ttu-id="bf7c4-125">[**IAMTimeline**](iamtimeline.md) e as outras interfaces **IAMTimelineXXXX**</span><span class="sxs-lookup"><span data-stu-id="bf7c4-125">[**IAMTimeline**](iamtimeline.md) and the other **IAMTimelineXXXX** interfaces</span></span>          |
| <span data-ttu-id="bf7c4-126">Salvar e carregar arquivos de projeto.</span><span class="sxs-lookup"><span data-stu-id="bf7c4-126">Save and load project files.</span></span>             | [<span data-ttu-id="bf7c4-127">**IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="bf7c4-127">**IXml2Dex**</span></span>](ixml2dex.md)                                                             |
| <span data-ttu-id="bf7c4-128">Visualizar um projeto ou gravá-lo em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="bf7c4-128">Preview a project or write it to a file.</span></span> | <span data-ttu-id="bf7c4-129">[**IRenderEngine**](irenderengine.md), [ **ISmartRenderEngine**](ismartrenderengine.md)</span><span class="sxs-lookup"><span data-stu-id="bf7c4-129">[**IRenderEngine**](irenderengine.md), [**ISmartRenderEngine**](ismartrenderengine.md)</span></span> |



 

<span data-ttu-id="bf7c4-130">Além disso, um aplicativo pode executar algumas ou todas as tarefas secundárias a seguir.</span><span class="sxs-lookup"><span data-stu-id="bf7c4-130">In addition, an application might perform some or all of the following secondary tasks.</span></span>



| <span data-ttu-id="bf7c4-131">Tarefa</span><span class="sxs-lookup"><span data-stu-id="bf7c4-131">Task</span></span>                                                                                           | <span data-ttu-id="bf7c4-132">Interface (s)</span><span class="sxs-lookup"><span data-stu-id="bf7c4-132">Interface(s)</span></span>                                                                 |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="bf7c4-133">Obtenha informações sobre arquivos de mídia.</span><span class="sxs-lookup"><span data-stu-id="bf7c4-133">Obtain information about media files.</span></span> <span data-ttu-id="bf7c4-134">(Número de fluxos; formato e duração de cada fluxo.)</span><span class="sxs-lookup"><span data-stu-id="bf7c4-134">(Number of streams; format and duration of each stream.)</span></span> | [<span data-ttu-id="bf7c4-135">**IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="bf7c4-135">**IMediaDet**</span></span>](imediadet.md)                                               |
| <span data-ttu-id="bf7c4-136">Defina as propriedades em transições e efeitos.</span><span class="sxs-lookup"><span data-stu-id="bf7c4-136">Set properties on transitions and effects.</span></span>                                                     | [<span data-ttu-id="bf7c4-137">**IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="bf7c4-137">**IPropertySetter**</span></span>](ipropertysetter.md)                                   |
| <span data-ttu-id="bf7c4-138">Receber notificação quando ocorrerem erros durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="bf7c4-138">Receive notification when errors occur during rendering.</span></span>                                       | <span data-ttu-id="bf7c4-139">[**IAMSetErrorLog**](iamseterrorlog.md), [ **IAMErrorLog**](iamerrorlog.md)</span><span class="sxs-lookup"><span data-stu-id="bf7c4-139">[**IAMSetErrorLog**](iamseterrorlog.md), [**IAMErrorLog**](iamerrorlog.md)</span></span> |
| <span data-ttu-id="bf7c4-140">Recuperar quadros de pôster.</span><span class="sxs-lookup"><span data-stu-id="bf7c4-140">Retrieve poster frames.</span></span>                                                                        | <span data-ttu-id="bf7c4-141">[**IMediaDet**](imediadet.md), [ **ISampleGrabber**](isamplegrabber.md)</span><span class="sxs-lookup"><span data-stu-id="bf7c4-141">[**IMediaDet**](imediadet.md), [**ISampleGrabber**](isamplegrabber.md)</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="bf7c4-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bf7c4-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf7c4-143">Introdução com os serviços de edição do DirectShow</span><span class="sxs-lookup"><span data-stu-id="bf7c4-143">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



