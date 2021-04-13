---
description: Sobre os mecanismos de renderização
ms.assetid: 80299b1a-09bf-4660-95d3-41a2b0074745
title: Sobre os mecanismos de renderização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70fe3a9956bee0d167de9e6618187bfd1f2a6e39
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500596"
---
# <a name="about-the-render-engines"></a><span data-ttu-id="a0207-103">Sobre os mecanismos de renderização</span><span class="sxs-lookup"><span data-stu-id="a0207-103">About the Render Engines</span></span>

<span data-ttu-id="a0207-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="a0207-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="a0207-105">Este artigo descreve como os [serviços de edição do DirectShow](directshow-editing-services.md) (des) renderizam um projeto de edição de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a0207-105">This article describes how [DirectShow Editing Services](directshow-editing-services.md) (DES) renders a video editing project.</span></span>

<span data-ttu-id="a0207-106">No DES, um projeto é representado como uma linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="a0207-106">In DES, a project is represented as a timeline.</span></span> <span data-ttu-id="a0207-107">A linha do tempo é útil porque simplifica as tarefas mais comuns na edição de vídeo, como reorganizar os clipes de origem e adicionar efeitos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a0207-107">The timeline is useful because it simplifies the most common tasks in video editing, such as rearranging source clips and adding video effects.</span></span> <span data-ttu-id="a0207-108">A arquitetura de fluxo do DirectShow, por outro lado, requer um grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="a0207-108">The DirectShow stream architecture, on the other hand, requires a filter graph.</span></span> <span data-ttu-id="a0207-109">Portanto, para renderizar seu projeto, você deve converter uma linha do tempo em um grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="a0207-109">Thus, to render your project, you must translate a timeline into a filter graph.</span></span> <span data-ttu-id="a0207-110">O componente que faz isso é chamado de *mecanismo de renderização*.</span><span class="sxs-lookup"><span data-stu-id="a0207-110">The component that does this is called a *render engine*.</span></span> <span data-ttu-id="a0207-111">O DirectShow fornece dois mecanismos de renderização:</span><span class="sxs-lookup"><span data-stu-id="a0207-111">DirectShow provides two render engines:</span></span>

-   <span data-ttu-id="a0207-112">Mecanismo de renderização básico: cria um grafo de filtro que fornece saída não compactada.</span><span class="sxs-lookup"><span data-stu-id="a0207-112">Basic render engine: Builds a filter graph that delivers uncompressed output.</span></span>
-   <span data-ttu-id="a0207-113">Mecanismo de processamento inteligente: compila um grafo de filtro que fornece saída compactada.</span><span class="sxs-lookup"><span data-stu-id="a0207-113">Smart render engine: Builds a filter graph that delivers compressed output.</span></span>

<span data-ttu-id="a0207-114">O mecanismo de processamento inteligente usa a recompactação inteligente para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="a0207-114">The smart render engine uses smart recompression to improve performance.</span></span> <span data-ttu-id="a0207-115">Com a recompactação inteligente, os arquivos de origem são recompactados somente quando o formato de arquivo original difere do formato de saída final.</span><span class="sxs-lookup"><span data-stu-id="a0207-115">With smart recompression, source files are recompressed only when the original file format differs from the final output format.</span></span> <span data-ttu-id="a0207-116">Se os formatos corresponderem, a origem nunca será descompactada.</span><span class="sxs-lookup"><span data-stu-id="a0207-116">If the formats match, the source is never decompressed.</span></span> <span data-ttu-id="a0207-117">A recompactação inteligente tem suporte apenas para compactação de vídeo, não para compactação de áudio.</span><span class="sxs-lookup"><span data-stu-id="a0207-117">Smart recompression is supported only for video compression, not for audio compression.</span></span>

<span data-ttu-id="a0207-118">Para visualização, use o mecanismo de renderização básico.</span><span class="sxs-lookup"><span data-stu-id="a0207-118">For preview, use the basic render engine.</span></span> <span data-ttu-id="a0207-119">O mecanismo de processamento inteligente também pode visualizar, mas com menos eficiência, porque ele precisa descompactar o fluxo compactado.</span><span class="sxs-lookup"><span data-stu-id="a0207-119">The smart render engine can also preview, but less efficiently because it has to decompress the compressed stream.</span></span> <span data-ttu-id="a0207-120">Para gravar arquivos, use o mecanismo de processamento inteligente se desejar a recompactação inteligente.</span><span class="sxs-lookup"><span data-stu-id="a0207-120">For writing files, use the smart render engine if you want smart recompression.</span></span> <span data-ttu-id="a0207-121">Caso contrário, use o mecanismo de renderização básico.</span><span class="sxs-lookup"><span data-stu-id="a0207-121">Otherwise, use the basic render engine.</span></span> <span data-ttu-id="a0207-122">A recompactação inteligente pode reduzir muito o tempo necessário para gravar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="a0207-122">Smart recompression can greatly reduce the time it takes to write the file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a0207-123">Não use o mecanismo de processamento inteligente para ler ou gravar arquivos de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="a0207-123">Do not use the smart render engine to read or write Windows Media files.</span></span>

 

> [!IMPORTANT]
> <span data-ttu-id="a0207-124">Ambos os mecanismos de renderização criam uma janela invisível que processa as mensagens.</span><span class="sxs-lookup"><span data-stu-id="a0207-124">Both render engines create an invisible window that processes messages.</span></span> <span data-ttu-id="a0207-125">O thread que cria o mecanismo de renderização deve ter um loop de mensagem para enviar mensagens.</span><span class="sxs-lookup"><span data-stu-id="a0207-125">The thread that creates the render engine must have a message loop, to dispatch messages.</span></span> <span data-ttu-id="a0207-126">Além disso, esse thread não deve ser encerrado até que o mecanismo de renderização e o Gerenciador do grafo de filtro sejam liberados.</span><span class="sxs-lookup"><span data-stu-id="a0207-126">Also, that thread must not exit until the Render Engine and the Filter Graph Manager are released.</span></span> <span data-ttu-id="a0207-127">Caso contrário, o aplicativo poderá ser bloqueado.</span><span class="sxs-lookup"><span data-stu-id="a0207-127">Otherwise, the application might deadlock.</span></span>

 

<span data-ttu-id="a0207-128">Construindo o grafo de filtro</span><span class="sxs-lookup"><span data-stu-id="a0207-128">Constructing the Filter Graph</span></span>

<span data-ttu-id="a0207-129">O grafo de filtro é criado em dois estágios.</span><span class="sxs-lookup"><span data-stu-id="a0207-129">The filter graph is built in two stages.</span></span> <span data-ttu-id="a0207-130">No primeiro estágio, o mecanismo de renderização constrói um "front-end", que é um grafo de filtro parcial.</span><span class="sxs-lookup"><span data-stu-id="a0207-130">In the first stage, the render engine constructs a "front end," which is a partial filter graph.</span></span> <span data-ttu-id="a0207-131">O diagrama a seguir ilustra um front-end típico:</span><span class="sxs-lookup"><span data-stu-id="a0207-131">The following diagram illustrates a typical front end:</span></span>

![front-end do grafo de filtro](images/rendeng1.png)

<span data-ttu-id="a0207-133">Os subsistemas contêm vários filtros especializados, que o mecanismo de renderização monta automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a0207-133">The subsystems contain various specialized filters, which the render engine assembles automatically.</span></span> <span data-ttu-id="a0207-134">O front-end contém um pino de saída para cada grupo na linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="a0207-134">The front end contains one output pin for each group in the timeline.</span></span> <span data-ttu-id="a0207-135">Os Pins de saída entregam dados descompactados se você usar o mecanismo de processamento básico ou dados compactados se usar o mecanismo de processamento inteligente.</span><span class="sxs-lookup"><span data-stu-id="a0207-135">The output pins deliver uncompressed data if you use the basic render engine, or compressed data if you use the smart render engine.</span></span>

<span data-ttu-id="a0207-136">Na segunda etapa, os Pins de saída são conectados aos filtros de renderização.</span><span class="sxs-lookup"><span data-stu-id="a0207-136">In the second step, the output pins are connected to rendering filters.</span></span> <span data-ttu-id="a0207-137">Para visualização, os filtros de renderização são renderizadores de vídeo e áudio.</span><span class="sxs-lookup"><span data-stu-id="a0207-137">For preview, the rendering filters are video and audio renderers.</span></span> <span data-ttu-id="a0207-138">Para gravação de arquivo, os filtros de renderização são filtros multiplexadores (MUX) e filtros de gravador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="a0207-138">For file writing, the rendering filters are multiplexer (mux) filters and file-writer filters.</span></span>

![Concluindo o gráfico de filtro](images/rendeng2.png)

## <a name="related-topics"></a><span data-ttu-id="a0207-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a0207-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0207-141">Visualizando um projeto</span><span class="sxs-lookup"><span data-stu-id="a0207-141">Previewing a Project</span></span>](previewing-a-project.md)
</dt> <dt>

[<span data-ttu-id="a0207-142">Gravando um projeto em um arquivo</span><span class="sxs-lookup"><span data-stu-id="a0207-142">Writing a Project to a File</span></span>](writing-a-project-to-a-file.md)
</dt> </dl>

 

 



