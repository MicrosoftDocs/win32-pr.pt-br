---
description: Remover todos os filtros no grafo
ms.assetid: a11af581-c331-4607-be8b-5f65961bd422
title: Remover todos os filtros no grafo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d414ef7e532eaf5df9143a6b601a57e4a8bd45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645850"
---
# <a name="remove-all-the-filters-in-the-graph"></a><span data-ttu-id="c4830-103">Remover todos os filtros no grafo</span><span class="sxs-lookup"><span data-stu-id="c4830-103">Remove All the Filters in the Graph</span></span>

<span data-ttu-id="c4830-104">A maneira mais fácil de remover todos os filtros em um grafo de filtro é simplesmente liberar o Gerenciador de gráfico de filtro e criar um novo.</span><span class="sxs-lookup"><span data-stu-id="c4830-104">The easiest way to remove all of the filters in a filter graph is simply to release the Filter Graph Manager and create a new one.</span></span> <span data-ttu-id="c4830-105">Certifique-se de liberar todos os ponteiros que seu aplicativo tem para qualquer interface nos gerenciadores de gráfico de filtro, bem como ponteiros para objetos no grafo, incluindo filtros, Pins, o relógio de referência e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c4830-105">Make sure to release every pointer that your application has to any interfaces on the Filter Graph Managers, as well as pointers to objects in the graph, including filters, pins, the reference clock, and so forth.</span></span>

<span data-ttu-id="c4830-106">Como alternativa, você pode remover os filtros um de cada vez, usando o método [**IFilterGraph:: RemoveFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-removefilter) :</span><span class="sxs-lookup"><span data-stu-id="c4830-106">Alternatively, you can remove the filters one at a time, using the [**IFilterGraph::RemoveFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-removefilter) method:</span></span>


```C++
// Stop the graph.
pControl->Stop();

// Enumerate the filters in the graph.
IEnumFilters *pEnum = NULL;
HRESULT hr = pGraph->EnumFilters(&pEnum);
if (SUCCEEDED(hr))
{
    IBaseFilter *pFilter = NULL;
    while (S_OK == pEnum->Next(1, &pFilter, NULL))
     {
         // Remove the filter.
         pGraph->RemoveFilter(pFilter);
         // Reset the enumerator.
         pEnum->Reset();
         pFilter->Release();
    }
    pEnum->Release();
}
```



<span data-ttu-id="c4830-107">Este exemplo usa o método [**IFilterGraph:: EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) para enumerar os filtros no grafo.</span><span class="sxs-lookup"><span data-stu-id="c4830-107">This example uses the [**IFilterGraph::EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) method to enumerate the filters in the graph.</span></span> <span data-ttu-id="c4830-108">A remoção de um filtro faz com que o objeto enumerador fique fora de sincronia com o grafo.</span><span class="sxs-lookup"><span data-stu-id="c4830-108">Removing a filter causes the enumerator object to become out of sync with the graph.</span></span> <span data-ttu-id="c4830-109">Use o método [**IEnumFilters:: Reset**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-reset) para redefinir o enumerador.</span><span class="sxs-lookup"><span data-stu-id="c4830-109">Use the [**IEnumFilters::Reset**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-reset) method to reset the enumerator.</span></span> <span data-ttu-id="c4830-110">Caso contrário, qualquer chamada subsequente para [**IEnumFilters:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) falhará.</span><span class="sxs-lookup"><span data-stu-id="c4830-110">Otherwise, any subsequent call to [**IEnumFilters::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) will fail.</span></span>

 

 



