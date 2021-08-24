---
description: Localizar uma interface em um filtro ou PIN
ms.assetid: 546f5b7d-3bcd-4e97-a012-daca6ae7bca1
title: Localizar uma interface em um filtro ou PIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17314f7e44e4b2c4f412dd0d152e038203268c29d585cd684ddde9eb34992a2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819558"
---
# <a name="find-an-interface-on-a-filter-or-pin"></a>Localizar uma interface em um filtro ou PIN

para muitas operações no DirectShow, o aplicativo chama métodos no gerenciador de Graph de filtro. Em algumas situações, no entanto, o aplicativo deve chamar um método diretamente em um filtro ou PIN. Por exemplo, muitos filtros expõem interfaces especializadas que são usadas para configurar o filtro.

No caso de uma interface de filtro, talvez você já tenha um ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do filtro. Nesse caso, basta usar **QueryInterface** para obter a outra interface. mas alguns filtros podem ser adicionados ao grafo pelo filtro Graph Manager. (para obter detalhes, consulte [Conexão inteligentes](intelligent-connect.md).) Nesse caso, use a interface [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) para executar um loop por todos os filtros no grafo e consulte cada um deles por vez. A função a seguir demonstra isso:


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



Para localizar uma interface em um PIN, use a interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) para executar um loop pelos Pins em um filtro. A função a seguir mostra como fazer isso:


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



A próxima função pesquisa uma interface em um filtro ou um PIN:


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



Observe que todas as funções mostradas aqui são interrompidas no primeiro **QueryInterface** bem-sucedido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Enumerando filtros](enumerating-filters.md)
</dt> <dt>

[Enumerando Pins](enumerating-pins.md)
</dt> <dt>

[**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)
</dt> </dl>

 

 



