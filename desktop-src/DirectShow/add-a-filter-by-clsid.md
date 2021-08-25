---
description: Adicionar um filtro por CLSID
ms.assetid: b15cf324-5b9b-41da-a8cf-87071aaf3b60
title: Adicionar um filtro por CLSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed8306613e5a73ad863b3c16b04529e3e0def12b76fb4e27685db9cb442b6c80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873426"
---
# <a name="add-a-filter-by-clsid"></a>Adicionar um filtro por CLSID

A função a seguir cria um filtro com um identificador de classe especificado (CLSID) e o adiciona ao gráfico de filtro:


```C++
// Create a filter by CLSID and add it to the graph.

HRESULT AddFilterByCLSID(
    IGraphBuilder *pGraph,      // Pointer to the Filter Graph Manager.
    REFGUID clsid,              // CLSID of the filter to create.
    IBaseFilter **ppF,          // Receives a pointer to the filter.
    LPCWSTR wszName             // A name for the filter (can be NULL).
    )
{
    *ppF = 0;

    IBaseFilter *pFilter = NULL;
    
    HRESULT hr = CoCreateInstance(clsid, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pFilter, wszName);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppF = pFilter;
    (*ppF)->AddRef();

done:
    SafeRelease(&pFilter);
    return hr;
}
```



> [!Note]  
> Este exemplo usa a função [SafeRelease](/windows/desktop/medfound/saferelease) para liberar o ponteiro [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .

 

A função chama [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar o filtro e, em seguida, chama [**IFilterGraph:: addfiltro**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para adicionar o filtro ao grafo. O exemplo de código a seguir usa essa função para adicionar o filtro [AVI Mux](avi-mux-filter.md) ao grafo:


```C++
IBaseFilter *pMux;
hr = AddFilterByCLSID(pGraph, CLSID_AviDest, L"AVI Mux", &pMux, NULL); 
if (SUCCEEDED(hr))
{
    /* ... */
   pMux->Release();
}
```



Observe que alguns filtros não podem ser criados com [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Esse é geralmente o caso com filtros que gerenciam outros componentes de software. Por exemplo, o filtro de [compressor AVI](avi-compressor-filter.md) é um wrapper para codecs de vídeo e o filtro de [captura de vídeo WDM](wdm-video-capture-filter.md) é um wrapper para drivers de captura WDM. Esses filtros devem ser criados usando o [enumerador de dispositivo do sistema](system-device-enumerator.md) ou o [mapeador de filtro](filter-mapper.md). Para obter mais informações, consulte [enumerando dispositivos e filtros](enumerating-devices-and-filters.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Técnicas de Graph-Building geral](general-graph-building-techniques.md)
</dt> </dl>

 

 
