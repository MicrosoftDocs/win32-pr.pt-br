---
description: Enumerando filtros
ms.assetid: 57bcaa4d-37bf-457d-937e-f9d24fb5784f
title: Enumerando filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d584ddf74a13b06e99d9a7e0a34ac802c6da881d87cb163411100ea7772e1df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819659"
---
# <a name="enumerating-filters"></a>Enumerando filtros

O Gerenciador Graph Filtro dá suporte ao método [**IFilterGraph::EnumFilters,**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) que enumera todos os filtros no grafo de filtro. Ele retorna um ponteiro para a interface [**IEnumFilters.**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) O [**método IEnumFilters::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) recupera ponteiros de interface [**IBaseFilter.**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)

O exemplo a seguir mostra uma função que enumera os filtros em um grafo e exibe uma caixa de mensagem com o nome de cada filtro. Ele usa o [**método IBaseFilter::QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) para recuperar o nome do filtro. Observe os locais em que a função **chama Release** em uma interface para decrementar a contagem de referência.


```C++
HRESULT EnumFilters (IFilterGraph *pGraph) 
{
    IEnumFilters *pEnum = NULL;
    IBaseFilter *pFilter;
    ULONG cFetched;

    HRESULT hr = pGraph->EnumFilters(&pEnum);
    if (FAILED(hr)) return hr;

    while(pEnum->Next(1, &pFilter, &cFetched) == S_OK)
    {
        FILTER_INFO FilterInfo;
        hr = pFilter->QueryFilterInfo(&FilterInfo);
        if (FAILED(hr))
        {
            MessageBox(NULL, TEXT("Could not get the filter info"),
                TEXT("Error"), MB_OK | MB_ICONERROR);
            continue;  // Maybe the next one will work.
        }

#ifdef UNICODE
        MessageBox(NULL, FilterInfo.achName, TEXT("Filter Name"), MB_OK);
#else
        char szName[MAX_FILTER_NAME];
        int cch = WideCharToMultiByte(CP_ACP, 0, FilterInfo.achName,
            MAX_FILTER_NAME, szName, MAX_FILTER_NAME, 0, 0);
        if (cch > 0)
            MessageBox(NULL, szName, TEXT("Filter Name"), MB_OK);
#endif

        // The FILTER_INFO structure holds a pointer to the Filter Graph
        // Manager, with a reference count that must be released.
        if (FilterInfo.pGraph != NULL)
        {
            FilterInfo.pGraph->Release();
        }
        pFilter->Release();
    }

    pEnum->Release();
    return S_OK;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Enumerando objetos em um filtro Graph](enumerating-objects-in-a-filter-graph.md)
</dt> </dl>

 

 



