---
description: Remover todos os filtros no Graph
ms.assetid: a11af581-c331-4607-be8b-5f65961bd422
title: Remover todos os filtros no Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f10b76bb5f5bc3cff2bfb989c422f177ef0d2ee4d09acff3c2f895ef9984b7c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072730"
---
# <a name="remove-all-the-filters-in-the-graph"></a>Remover todos os filtros no Graph

a maneira mais fácil de remover todos os filtros em um grafo de filtro é simplesmente liberar o filtro Graph Manager e criar um novo. certifique-se de liberar todos os ponteiros que seu aplicativo tem para qualquer interface no filtro Graph gerenciadores, bem como ponteiros para objetos no grafo, incluindo filtros, pins, o relógio de referência e assim por diante.

Como alternativa, você pode remover os filtros um de cada vez, usando o método [**IFilterGraph:: RemoveFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-removefilter) :


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



Este exemplo usa o método [**IFilterGraph:: EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) para enumerar os filtros no grafo. A remoção de um filtro faz com que o objeto enumerador fique fora de sincronia com o grafo. Use o método [**IEnumFilters:: Reset**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-reset) para redefinir o enumerador. Caso contrário, qualquer chamada subsequente para [**IEnumFilters:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) falhará.

 

 



