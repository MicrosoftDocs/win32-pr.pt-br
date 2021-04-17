---
description: Sobre exemplos de mídia e alocadores
ms.assetid: d6283bf0-0460-4519-9a56-fd4c78cfaabc
title: Sobre exemplos de mídia e alocadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9105228e70f82aaa7c36b7e7d28cf7e748e1e2f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105782858"
---
# <a name="about-media-samples-and-allocators"></a><span data-ttu-id="41d88-103">Sobre exemplos de mídia e alocadores</span><span class="sxs-lookup"><span data-stu-id="41d88-103">About Media Samples and Allocators</span></span>

<span data-ttu-id="41d88-104">Os filtros entregam dados entre conexões de PIN.</span><span class="sxs-lookup"><span data-stu-id="41d88-104">Filters deliver data across pin connections.</span></span> <span data-ttu-id="41d88-105">Os dados se movem do pino de saída de um filtro para o pino de entrada de outro filtro.</span><span class="sxs-lookup"><span data-stu-id="41d88-105">Data moves from the output pin of one filter to the input pin of another filter.</span></span> <span data-ttu-id="41d88-106">A maneira mais comum para o pino de saída entregar os dados é chamar o método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) na entrada, embora alguns outros mecanismos também existam.</span><span class="sxs-lookup"><span data-stu-id="41d88-106">The most common way for the output pin to deliver the data is by calling the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the input, although a few other mechanisms exist as well.</span></span>

<span data-ttu-id="41d88-107">Dependendo do filtro, a memória para os dados de mídia pode ser alocada de várias maneiras: no heap, em uma superfície do DirectDraw, usando a memória GDI compartilhada ou usando algum outro mecanismo de alocação.</span><span class="sxs-lookup"><span data-stu-id="41d88-107">Depending on the filter, memory for the media data can be allocated in various ways: on the heap, in a DirectDraw surface, using shared GDI memory, or using some other allocation mechanism.</span></span> <span data-ttu-id="41d88-108">O objeto responsável pela alocação da memória é chamado de *alocador*, que é um objeto com que expõe a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="41d88-108">The object responsible for allocating the memory is called an *allocator*, which is a COM object that exposes the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="41d88-109">Quando dois Pins se conectam, um dos Pins deve fornecer um alocador.</span><span class="sxs-lookup"><span data-stu-id="41d88-109">When two pins connect, one of the pins must provide an allocator.</span></span> <span data-ttu-id="41d88-110">O DirectShow define uma sequência de chamadas de método que é usada para estabelecer qual PIN fornece o alocador.</span><span class="sxs-lookup"><span data-stu-id="41d88-110">DirectShow defines a sequence of method calls that is used to establish which pin provides the allocator.</span></span> <span data-ttu-id="41d88-111">Os Pins também concordam com o número de buffers que o alocador criará e o tamanho dos buffers.</span><span class="sxs-lookup"><span data-stu-id="41d88-111">The pins also agree on the number of buffers that the allocator will create, and the size of the buffers.</span></span>

<span data-ttu-id="41d88-112">Antes de o streaming começar, o alocador cria um pool de buffers.</span><span class="sxs-lookup"><span data-stu-id="41d88-112">Before streaming begins, the allocator creates a pool of buffers.</span></span> <span data-ttu-id="41d88-113">Durante o streaming, o filtro upstream preenche os buffers com os dados e os entrega para o filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="41d88-113">During streaming, the upstream filter fills buffers with data and delivers them to the downstream filter.</span></span> <span data-ttu-id="41d88-114">Mas o filtro upstream não fornece os ponteiros brutos do filtro downstream para os buffers.</span><span class="sxs-lookup"><span data-stu-id="41d88-114">But the upstream filter does not give the downstream filter raw pointers to the buffers.</span></span> <span data-ttu-id="41d88-115">Em vez disso, ele usa objetos COM chamados *amostras de mídia*, que o alocador cria para gerenciar os buffers.</span><span class="sxs-lookup"><span data-stu-id="41d88-115">Instead, it uses COM objects called *media samples*, which the allocator creates to manage the buffers.</span></span> <span data-ttu-id="41d88-116">Amostras de mídia expõem a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .</span><span class="sxs-lookup"><span data-stu-id="41d88-116">Media samples expose the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span> <span data-ttu-id="41d88-117">Um exemplo de mídia contém:</span><span class="sxs-lookup"><span data-stu-id="41d88-117">A media sample contains:</span></span>

-   <span data-ttu-id="41d88-118">um ponteiro para o buffer subjacente</span><span class="sxs-lookup"><span data-stu-id="41d88-118">a pointer to the underlying buffer</span></span>
-   <span data-ttu-id="41d88-119">um carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="41d88-119">a time stamp</span></span>
-   <span data-ttu-id="41d88-120">vários sinalizadores</span><span class="sxs-lookup"><span data-stu-id="41d88-120">various flags</span></span>
-   <span data-ttu-id="41d88-121">Opcionalmente, um tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="41d88-121">optionally, a media type</span></span>

<span data-ttu-id="41d88-122">O carimbo de data/hora define o tempo de apresentação, que o filtro de processador usa para agendar a renderização.</span><span class="sxs-lookup"><span data-stu-id="41d88-122">The time stamp defines the presentation time, which the renderer filter uses to schedule rendering.</span></span> <span data-ttu-id="41d88-123">Os sinalizadores indicam coisas como se houvesse uma interrupção nos dados desde o exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="41d88-123">The flags indicate things like whether there was a break in the data since the previous sample.</span></span> <span data-ttu-id="41d88-124">O tipo de mídia fornece uma maneira de filtros para alterar os formatos intermediários.</span><span class="sxs-lookup"><span data-stu-id="41d88-124">The media type provides a way for filters to change formats mid-stream.</span></span> <span data-ttu-id="41d88-125">Normalmente, o exemplo não tem nenhum tipo de mídia, o que indica que o formato não foi alterado desde o exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="41d88-125">Usually, the sample has no media type, which indicates that the format has not changed since the previous sample.</span></span>

<span data-ttu-id="41d88-126">Embora um filtro esteja usando um buffer, ele mantém a contagem de referência no exemplo.</span><span class="sxs-lookup"><span data-stu-id="41d88-126">While a filter is using a buffer, it holds reference count on the sample.</span></span> <span data-ttu-id="41d88-127">O alocador usa a contagem de referência para determinar quando ele pode usar novamente o buffer.</span><span class="sxs-lookup"><span data-stu-id="41d88-127">The allocator uses the reference count to determine when it can re-use the buffer.</span></span> <span data-ttu-id="41d88-128">Isso impede que um filtro substitua um buffer que outro filtro ainda está usando.</span><span class="sxs-lookup"><span data-stu-id="41d88-128">This prevents a filter from overwriting a buffer that another filter is still using.</span></span> <span data-ttu-id="41d88-129">Um exemplo não retorna ao pool de exemplos disponíveis do alocador até que todos os filtros o tenham liberado.</span><span class="sxs-lookup"><span data-stu-id="41d88-129">A sample does not return to the allocator's pool of available samples until every filter has released it.</span></span>

<span data-ttu-id="41d88-130">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="41d88-130">For more information, see the following topics:</span></span>

-   <span data-ttu-id="41d88-131">O tópico [exemplos e alocadores](samples-and-allocators.md) fornece uma descrição mais detalhada de como os alocadores funcionam.</span><span class="sxs-lookup"><span data-stu-id="41d88-131">The topic [Samples and Allocators](samples-and-allocators.md) provides a more detailed description of how allocators work.</span></span>
-   <span data-ttu-id="41d88-132">O tópico [fluxo de dados no gráfico de filtro](data-flow-in-the-filter-graph.md) fornece uma visão geral do fluxo de dados no DirectShow.</span><span class="sxs-lookup"><span data-stu-id="41d88-132">The topic [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md) gives a general overview of data flow in DirectShow.</span></span>

<span data-ttu-id="41d88-133">Os tópicos a seguir destinam-se a desenvolvedores que estão escrevendo seus próprios filtros personalizados:</span><span class="sxs-lookup"><span data-stu-id="41d88-133">The following topics are intended for developers who are writing their own custom filters:</span></span>

-   [<span data-ttu-id="41d88-134">Fluxo de dados para os desenvolvedores de filtro</span><span class="sxs-lookup"><span data-stu-id="41d88-134">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
-   [<span data-ttu-id="41d88-135">Threads e seções críticas</span><span class="sxs-lookup"><span data-stu-id="41d88-135">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)

## <a name="related-topics"></a><span data-ttu-id="41d88-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="41d88-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41d88-137">O gráfico de filtro e seus componentes</span><span class="sxs-lookup"><span data-stu-id="41d88-137">The Filter Graph and Its Components</span></span>](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 



