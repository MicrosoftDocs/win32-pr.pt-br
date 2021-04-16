---
description: Configurando o relógio do grafo
ms.assetid: 23deab26-6c9a-4f94-b750-11c9b1a14ce3
title: Configurando o relógio do grafo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe98c8dce1ab5f94664fbe1406c682e5d4e50b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105779230"
---
# <a name="setting-the-graph-clock"></a><span data-ttu-id="fc0dd-103">Configurando o relógio do grafo</span><span class="sxs-lookup"><span data-stu-id="fc0dd-103">Setting the Graph Clock</span></span>

<span data-ttu-id="fc0dd-104">Quando você cria um gráfico de filtro, o Gerenciador do grafo de filtro escolhe automaticamente um relógio de referência para o grafo.</span><span class="sxs-lookup"><span data-stu-id="fc0dd-104">When you build a filter graph, the Filter Graph Manager automatically chooses a reference clock for the graph.</span></span> <span data-ttu-id="fc0dd-105">Todos os filtros no grafo são sincronizados com o relógio de referência.</span><span class="sxs-lookup"><span data-stu-id="fc0dd-105">All filters in the graph are synchronized to the reference clock.</span></span> <span data-ttu-id="fc0dd-106">Em particular, os filtros de renderização usam o relógio de referência para determinar o tempo de apresentação de cada exemplo.</span><span class="sxs-lookup"><span data-stu-id="fc0dd-106">In particular, renderer filters use the reference clock to determine the presentation time of each sample.</span></span>

<span data-ttu-id="fc0dd-107">Normalmente, não há motivo para um aplicativo substituir a opção do relógio de referência do Gerenciador de grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="fc0dd-107">There is usually no reason for an application to override the Filter Graph Manager's choice of reference clock.</span></span> <span data-ttu-id="fc0dd-108">No entanto, você pode fazer isso chamando o método [**IMediaFilter:: Setsincronizate**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) no Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="fc0dd-108">However, you can do so by calling the [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method on the Filter Graph Manager.</span></span> <span data-ttu-id="fc0dd-109">Esse método usa um ponteiro para a interface **IReferenceClock** do relógio.</span><span class="sxs-lookup"><span data-stu-id="fc0dd-109">This method takes a pointer to the clock's **IReferenceClock** interface.</span></span> <span data-ttu-id="fc0dd-110">Chame o método enquanto o grafo estiver parado.</span><span class="sxs-lookup"><span data-stu-id="fc0dd-110">Call the method while the graph is stopped.</span></span>

<span data-ttu-id="fc0dd-111">Se um filtro fornecer um relógio, você poderá obter o ponteiro **IReferenceClock** chamando **QueryInterface** no filtro.</span><span class="sxs-lookup"><span data-stu-id="fc0dd-111">If a filter provides a clock, you can get the **IReferenceClock** pointer by calling **QueryInterface** on the filter.</span></span> <span data-ttu-id="fc0dd-112">Como alternativa, você pode implementar um relógio de referência externa que não é fornecido por um filtro, desde que o relógio externo implemente **IReferenceClock**.</span><span class="sxs-lookup"><span data-stu-id="fc0dd-112">Alternatively, you can implement an external reference clock that is not provided by a filter, as long as your external clock implements **IReferenceClock**.</span></span> <span data-ttu-id="fc0dd-113">O exemplo a seguir mostra como especificar um relógio:</span><span class="sxs-lookup"><span data-stu-id="fc0dd-113">The following example shows how to specify a clock:</span></span>


```C++
IGraphBuilder *pGraph = 0;
IReferenceClock *pClock = 0;

CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
    IID_IGraphBuilder, (void **)&pGraph);

// Build the graph.
pGraph->RenderFile(L"C:\\Example.avi", 0);

// Create your clock.
hr = CreateMyPrivateClock(&pClock);
if (SUCCEEDED(hr))
{
    // Set the graph clock.
    IMediaFilter *pMediaFilter = 0;
    pGraph->QueryInterface(IID_IMediaFilter, (void**)&pMediaFilter);
    pMediaFilter->SetSyncSource(pClock);
    pClock->Release();
    pMediaFilter->Release();
}
```



<span data-ttu-id="fc0dd-114">Este exemplo pressupõe que CreateMyPrivateClock é uma função definida pelo aplicativo que cria um relógio e retorna um ponteiro **IReferenceClock** .</span><span class="sxs-lookup"><span data-stu-id="fc0dd-114">This example assumes that CreateMyPrivateClock is an application-defined function that creates a clock and returns an **IReferenceClock** pointer.</span></span>

<span data-ttu-id="fc0dd-115">Você também pode definir o grafo de filtro para ser executado sem nenhum relógio, chamando **Setsincronizate** com o valor **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fc0dd-115">You can also set the filter graph to run with no clock, by calling **SetSyncSource** with the value **NULL**.</span></span> <span data-ttu-id="fc0dd-116">Se não houver nenhum relógio, o grafo será executado o mais rápido possível.</span><span class="sxs-lookup"><span data-stu-id="fc0dd-116">If there is no clock, the graph runs as quickly as possible.</span></span> <span data-ttu-id="fc0dd-117">Sem nenhum relógio, os filtros de processador não aguardam o tempo de apresentação de um exemplo.</span><span class="sxs-lookup"><span data-stu-id="fc0dd-117">With no clock, renderer filters do not wait for a sample's presentation time.</span></span> <span data-ttu-id="fc0dd-118">Em vez disso, eles renderizam cada exemplo assim que chega.</span><span class="sxs-lookup"><span data-stu-id="fc0dd-118">Instead, they render each sample as soon as it arrives.</span></span> <span data-ttu-id="fc0dd-119">Definir o grafo para ser executado sem um relógio será útil se você quiser processar dados rapidamente, em vez de visualizá-los em tempo real.</span><span class="sxs-lookup"><span data-stu-id="fc0dd-119">Setting the graph to run without a clock is useful if you want to process data quickly, rather than previewing it in real time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc0dd-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc0dd-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc0dd-121">Tarefas básicas do DirectShow</span><span class="sxs-lookup"><span data-stu-id="fc0dd-121">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> <dt>

[<span data-ttu-id="fc0dd-122">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="fc0dd-122">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> <dt>

[<span data-ttu-id="fc0dd-123">Tempo e relógios no DirectShow</span><span class="sxs-lookup"><span data-stu-id="fc0dd-123">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



