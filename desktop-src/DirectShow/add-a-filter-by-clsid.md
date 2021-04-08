---
description: Adicionar um filtro por CLSID
ms.assetid: b15cf324-5b9b-41da-a8cf-87071aaf3b60
title: Adicionar um filtro por CLSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f880ab1cb3b88fbe6d889acdd192bba341ce2acf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087874"
---
# <a name="add-a-filter-by-clsid"></a><span data-ttu-id="6b079-103">Adicionar um filtro por CLSID</span><span class="sxs-lookup"><span data-stu-id="6b079-103">Add a Filter by CLSID</span></span>

<span data-ttu-id="6b079-104">A função a seguir cria um filtro com um identificador de classe especificado (CLSID) e o adiciona ao gráfico de filtro:</span><span class="sxs-lookup"><span data-stu-id="6b079-104">The following function creates a filter with a specified class identifier (CLSID) and adds it to the filter graph:</span></span>


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
> <span data-ttu-id="6b079-105">Este exemplo usa a função [SafeRelease](/windows/desktop/medfound/saferelease) para liberar o ponteiro [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="6b079-105">This example uses the [SafeRelease](/windows/desktop/medfound/saferelease) function to release the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span>

 

<span data-ttu-id="6b079-106">A função chama [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar o filtro e, em seguida, chama [**IFilterGraph:: addfiltro**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para adicionar o filtro ao grafo.</span><span class="sxs-lookup"><span data-stu-id="6b079-106">The function calls [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the filter, and then calls [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the graph.</span></span> <span data-ttu-id="6b079-107">O exemplo de código a seguir usa essa função para adicionar o filtro [AVI Mux](avi-mux-filter.md) ao grafo:</span><span class="sxs-lookup"><span data-stu-id="6b079-107">The following code example uses this function to add the [AVI Mux](avi-mux-filter.md) filter to the graph:</span></span>


```C++
IBaseFilter *pMux;
hr = AddFilterByCLSID(pGraph, CLSID_AviDest, L"AVI Mux", &pMux, NULL); 
if (SUCCEEDED(hr))
{
    /* ... */
   pMux->Release();
}
```



<span data-ttu-id="6b079-108">Observe que alguns filtros não podem ser criados com [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="6b079-108">Note that some filters cannot be created with [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="6b079-109">Esse é geralmente o caso com filtros que gerenciam outros componentes de software.</span><span class="sxs-lookup"><span data-stu-id="6b079-109">This is often the case with filters that manage other software components.</span></span> <span data-ttu-id="6b079-110">Por exemplo, o filtro de [compressor AVI](avi-compressor-filter.md) é um wrapper para codecs de vídeo e o filtro de [captura de vídeo WDM](wdm-video-capture-filter.md) é um wrapper para drivers de captura WDM.</span><span class="sxs-lookup"><span data-stu-id="6b079-110">For example, the [AVI Compressor](avi-compressor-filter.md) filter is a wrapper for video codecs, and the [WDM Video Capture](wdm-video-capture-filter.md) filter is a wrapper for WDM capture drivers.</span></span> <span data-ttu-id="6b079-111">Esses filtros devem ser criados usando o [enumerador de dispositivo do sistema](system-device-enumerator.md) ou o [mapeador de filtro](filter-mapper.md).</span><span class="sxs-lookup"><span data-stu-id="6b079-111">These filters must be created using either the [System Device Enumerator](system-device-enumerator.md) or the [Filter Mapper](filter-mapper.md).</span></span> <span data-ttu-id="6b079-112">Para obter mais informações, consulte [enumerando dispositivos e filtros](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="6b079-112">For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b079-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6b079-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b079-114">Técnicas de Graph-Building geral</span><span class="sxs-lookup"><span data-stu-id="6b079-114">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> </dl>

 

 
