---
description: Localizar uma interface em um filtro ou PIN
ms.assetid: 546f5b7d-3bcd-4e97-a012-daca6ae7bca1
title: Localizar uma interface em um filtro ou PIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d264a35e0c33ba53f6a8df7f69113f3358a9737
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163694"
---
# <a name="find-an-interface-on-a-filter-or-pin"></a><span data-ttu-id="395d0-103">Localizar uma interface em um filtro ou PIN</span><span class="sxs-lookup"><span data-stu-id="395d0-103">Find an Interface on a Filter or Pin</span></span>

<span data-ttu-id="395d0-104">Para muitas operações no DirectShow, o aplicativo chama métodos no Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="395d0-104">For many operations in DirectShow, the application calls methods on the Filter Graph Manager.</span></span> <span data-ttu-id="395d0-105">Em algumas situações, no entanto, o aplicativo deve chamar um método diretamente em um filtro ou PIN.</span><span class="sxs-lookup"><span data-stu-id="395d0-105">In some situations, however, the application must call a method directly on a filter or pin.</span></span> <span data-ttu-id="395d0-106">Por exemplo, muitos filtros expõem interfaces especializadas que são usadas para configurar o filtro.</span><span class="sxs-lookup"><span data-stu-id="395d0-106">For example, many filters expose specialized interfaces that are used to configure the filter.</span></span>

<span data-ttu-id="395d0-107">No caso de uma interface de filtro, talvez você já tenha um ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do filtro.</span><span class="sxs-lookup"><span data-stu-id="395d0-107">In the case of a filter interface, you might already have a pointer to the filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="395d0-108">Nesse caso, basta usar **QueryInterface** para obter a outra interface.</span><span class="sxs-lookup"><span data-stu-id="395d0-108">In that case, simply use **QueryInterface** to get the other interface.</span></span> <span data-ttu-id="395d0-109">Mas alguns filtros podem ser adicionados ao grafo pelo Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="395d0-109">But some filters might be added to the graph by the Filter Graph Manager.</span></span> <span data-ttu-id="395d0-110">(Para obter detalhes, consulte [conexão inteligente](intelligent-connect.md).) Nesse caso, use a interface [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) para executar um loop por todos os filtros no grafo e consulte cada um deles por vez.</span><span class="sxs-lookup"><span data-stu-id="395d0-110">(For details, see [Intelligent Connect](intelligent-connect.md).) In that case, use the [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) interface to loop through all the filters in the graph, and query each one in turn.</span></span> <span data-ttu-id="395d0-111">A função a seguir demonstra isso:</span><span class="sxs-lookup"><span data-stu-id="395d0-111">The following function demonstrates this:</span></span>


```C++
HRESULT FindFilterInterface(
    IGraphBuilder *pGraph, // Pointer to the Filter Graph Manager.
    REFGUID iid,           // IID of the interface to retrieve.
    void **ppUnk)          // Receives the interface pointer.
{
    if (!pGraph || !ppUnk) return E_POINTER;

    HRESULT hr = E_FAIL;
    IEnumFilters *pEnum = NULL;
    IBaseFilter *pF = NULL;
    if (FAILED(pGraph->EnumFilters(&pEnum)))
    {
        return E_FAIL;
    }
    // Query every filter for the interface.
    while (S_OK == pEnum->Next(1, &pF, 0))
    {
        hr = pF->QueryInterface(iid, ppUnk);
        pF->Release();
        if (SUCCEEDED(hr))
        {
            break;
        }
    }
    pEnum->Release();
    return hr;
}
```



<span data-ttu-id="395d0-112">Para localizar uma interface em um PIN, use a interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) para executar um loop pelos Pins em um filtro.</span><span class="sxs-lookup"><span data-stu-id="395d0-112">To find an interface on a pin, use the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface to loop through the pins on a filter.</span></span> <span data-ttu-id="395d0-113">A função a seguir mostra como fazer isso:</span><span class="sxs-lookup"><span data-stu-id="395d0-113">The following function shows how to do this:</span></span>


```C++
HRESULT FindPinInterface(
    IBaseFilter *pFilter,  // Pointer to the filter to search.
    REFGUID iid,           // IID of the interface.
    void **ppUnk)          // Receives the interface pointer.
{
    if (!pFilter || !ppUnk) return E_POINTER;

    HRESULT hr = E_FAIL;
    IEnumPins *pEnum = 0;
    if (FAILED(pFilter->EnumPins(&pEnum)))
    {
        return E_FAIL;
    }
    // Query every pin for the interface.
    IPin *pPin = 0;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        hr = pPin->QueryInterface(iid, ppUnk);
        pPin->Release();
        if (SUCCEEDED(hr))
        {
            break;
        }
    }
    pEnum->Release();
    return hr;
}
```



<span data-ttu-id="395d0-114">A próxima função pesquisa uma interface em um filtro ou um PIN:</span><span class="sxs-lookup"><span data-stu-id="395d0-114">The next function searches for an interface on a filter or a pin:</span></span>


```C++
HRESULT FindInterfaceAnywhere(
    IGraphBuilder *pGraph, 
    REFGUID iid, 
    void **ppUnk)
{
    if (!pGraph || !ppUnk) return E_POINTER;
    HRESULT hr = E_FAIL;
    IEnumFilters *pEnum = 0;
    if (FAILED(pGraph->EnumFilters(&pEnum)))
    {
        return E_FAIL;
    }
    // Loop through every filter in the graph.
    IBaseFilter *pF = 0;
    while (S_OK == pEnum->Next(1, &pF, 0))
    {
        hr = pF->QueryInterface(iid, ppUnk);
        if (FAILED(hr))
        {
            // The filter does not expose the interface, but maybe
            // one of its pins does.
            hr = FindPinInterface(pF, iid, ppUnk);
        }
        pF->Release();
        if (SUCCEEDED(hr))
        {
            break;
        }
    }
    pEnum->Release();
    return hr;
}
```



<span data-ttu-id="395d0-115">Observe que todas as funções mostradas aqui são interrompidas no primeiro **QueryInterface** bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="395d0-115">Note that all of the functions shown here stop at the first successful **QueryInterface**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="395d0-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="395d0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="395d0-117">Enumerando filtros</span><span class="sxs-lookup"><span data-stu-id="395d0-117">Enumerating Filters</span></span>](enumerating-filters.md)
</dt> <dt>

[<span data-ttu-id="395d0-118">Enumerando Pins</span><span class="sxs-lookup"><span data-stu-id="395d0-118">Enumerating Pins</span></span>](enumerating-pins.md)
</dt> <dt>

[<span data-ttu-id="395d0-119">**ICaptureGraphBuilder2::FindInterface**</span><span class="sxs-lookup"><span data-stu-id="395d0-119">**ICaptureGraphBuilder2::FindInterface**</span></span>](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)
</dt> </dl>

 

 



