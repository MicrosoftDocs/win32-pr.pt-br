---
description: Este tópico mostra algumas funções auxiliares para conectar filtros do DirectShow.
ms.assetid: cfd85944-7ae7-49e6-948f-9e190cdeed12
title: Conectar dois filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e70e607c510490e7ed841ea44303153a94e83f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087722"
---
# <a name="connect-two-filters"></a><span data-ttu-id="3dbc3-103">Conectar dois filtros</span><span class="sxs-lookup"><span data-stu-id="3dbc3-103">Connect Two Filters</span></span>

<span data-ttu-id="3dbc3-104">Este tópico mostra algumas funções auxiliares para conectar filtros do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3dbc3-104">This topic shows some helper functions for connecting DirectShow filters.</span></span>

<span data-ttu-id="3dbc3-105">Para conectar dois filtros, você deve encontrar um PIN de saída não conectado no filtro upstream e um PIN de entrada não conectado no filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="3dbc3-105">To connect two filters, you must find an unconnected output pin on the upstream filter, and an unconnected input pin on the downstream filter.</span></span>

<span data-ttu-id="3dbc3-106">Se você já tiver ponteiros para ambos os Pins, chame o método [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) para conectá-los.</span><span class="sxs-lookup"><span data-stu-id="3dbc3-106">If you already have pointers to both pins, call the [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) method to connect them.</span></span> <span data-ttu-id="3dbc3-107">Se os Pins não puderem se conectar diretamente entre si, o método **IGraphBuilder:: Connect** poderá inserir filtros adicionais para concluir a conexão.</span><span class="sxs-lookup"><span data-stu-id="3dbc3-107">If the pins cannot connect directly to each other, the **IGraphBuilder::Connect** method might insert additional filters, to complete the connection.</span></span> <span data-ttu-id="3dbc3-108">Para obter mais informações, consulte [conexão inteligente](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="3dbc3-108">For more information, see [Intelligent Connect](intelligent-connect.md).</span></span>

<span data-ttu-id="3dbc3-109">Se você tiver um ponteiro para os filtros, mas não os Pins, deverá usar o método [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) para localizar os Pins.</span><span class="sxs-lookup"><span data-stu-id="3dbc3-109">If you have a pointer to the filters but not the pins, you must use the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method to find the pins.</span></span> <span data-ttu-id="3dbc3-110">(Consulte [enumerando Pins](enumerating-pins.md).) As funções auxiliares neste tópico demonstram essa técnica.</span><span class="sxs-lookup"><span data-stu-id="3dbc3-110">(See [Enumerating Pins](enumerating-pins.md).) The helper functions in this topic demonstrate this technique.</span></span>

### <a name="output-pin-to-filter"></a><span data-ttu-id="3dbc3-111">Pino de saída para filtrar</span><span class="sxs-lookup"><span data-stu-id="3dbc3-111">Output Pin to Filter</span></span>

<span data-ttu-id="3dbc3-112">A função a seguir usa dois parâmetros: um ponteiro para um pino de saída e um ponteiro para um filtro.</span><span class="sxs-lookup"><span data-stu-id="3dbc3-112">The following function takes two parameters: A pointer to an output pin, and a pointer to a filter.</span></span> <span data-ttu-id="3dbc3-113">A função conecta o pino de saída ao primeiro PIN de entrada disponível no filtro.</span><span class="sxs-lookup"><span data-stu-id="3dbc3-113">The function connects the output pin to the first available input pin on the filter.</span></span>


```C++
// Connect output pin to filter.

HRESULT ConnectFilters(
    IGraphBuilder *pGraph, // Filter Graph Manager.
    IPin *pOut,            // Output pin on the upstream filter.
    IBaseFilter *pDest)    // Downstream filter.
{
    IPin *pIn = NULL;
        
    // Find an input pin on the downstream filter.
    HRESULT hr = FindUnconnectedPin(pDest, PINDIR_INPUT, &pIn);
    if (SUCCEEDED(hr))
    {
        // Try to connect them.
        hr = pGraph->Connect(pOut, pIn);
        pIn->Release();
    }
    return hr;
}
```



<span data-ttu-id="3dbc3-114">Essa função faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3dbc3-114">This function does the following:</span></span>

1.  <span data-ttu-id="3dbc3-115">Chama a `FindUnconnectedPin` função para obter um PIN de entrada não conectado.</span><span class="sxs-lookup"><span data-stu-id="3dbc3-115">Calls the `FindUnconnectedPin` function to get an unconnected input pin.</span></span> <span data-ttu-id="3dbc3-116">Essa função é mostrada no tópico [localizar um PIN não conectado em um filtro](find-an-unconnected-pin-on-a-filter.md).</span><span class="sxs-lookup"><span data-stu-id="3dbc3-116">This function is shown in the topic [Find an Unconnected Pin on a Filter](find-an-unconnected-pin-on-a-filter.md).</span></span>
2.  <span data-ttu-id="3dbc3-117">Chama [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) para conectar os dois Pins.</span><span class="sxs-lookup"><span data-stu-id="3dbc3-117">Calls [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) to connect the two pins.</span></span>

### <a name="filter-to-input-pin"></a><span data-ttu-id="3dbc3-118">Filtrar para o pino de entrada</span><span class="sxs-lookup"><span data-stu-id="3dbc3-118">Filter to Input Pin</span></span>

<span data-ttu-id="3dbc3-119">A próxima função usa um ponteiro para um filtro e um ponteiro para um pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="3dbc3-119">The next function takes a pointer to a filter and a pointer to an input pin.</span></span> <span data-ttu-id="3dbc3-120">Ele conecta o pino de entrada ao primeiro pino de saída disponível no filtro.</span><span class="sxs-lookup"><span data-stu-id="3dbc3-120">It connects the input pin to the first available output pin on the filter.</span></span>


```C++
// Connect filter to input pin.

HRESULT ConnectFilters(IGraphBuilder *pGraph, IBaseFilter *pSrc, IPin *pIn)
{
    IPin *pOut = NULL;
        
    // Find an output pin on the upstream filter.
    HRESULT hr = FindUnconnectedPin(pSrc, PINDIR_OUTPUT, &pOut);
    if (SUCCEEDED(hr))
    {
        // Try to connect them.
        hr = pGraph->Connect(pOut, pIn);
        pOut->Release();
    }
    return hr;
}
```



### <a name="filter-to-filter"></a><span data-ttu-id="3dbc3-121">Filtrar para filtrar</span><span class="sxs-lookup"><span data-stu-id="3dbc3-121">Filter to Filter</span></span>

<span data-ttu-id="3dbc3-122">A terceira função usa um ponteiro para um filtro upstream e um ponteiro para um filtro downstream e tenta conectar ambos os filtros.</span><span class="sxs-lookup"><span data-stu-id="3dbc3-122">The third function takes a pointer to an upstream filter and a pointer to a downstream filter, and tries to connect both filters.</span></span>


```C++
// Connect filter to filter

HRESULT ConnectFilters(IGraphBuilder *pGraph, IBaseFilter *pSrc, IBaseFilter *pDest)
{
    IPin *pOut = NULL;

    // Find an output pin on the first filter.
    HRESULT hr = FindUnconnectedPin(pSrc, PINDIR_OUTPUT, &pOut);
    if (SUCCEEDED(hr))
    {
        hr = ConnectFilters(pGraph, pOut, pDest);
        pOut->Release();
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="3dbc3-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3dbc3-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dbc3-124">Técnicas de Graph-Building geral</span><span class="sxs-lookup"><span data-stu-id="3dbc3-124">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="3dbc3-125">**ICaptureGraphBuilder2::RenderStream**</span><span class="sxs-lookup"><span data-stu-id="3dbc3-125">**ICaptureGraphBuilder2::RenderStream**</span></span>](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)
</dt> </dl>

 

 



