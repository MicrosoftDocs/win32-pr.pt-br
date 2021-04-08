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
# <a name="connect-two-filters"></a>Conectar dois filtros

Este tópico mostra algumas funções auxiliares para conectar filtros do DirectShow.

Para conectar dois filtros, você deve encontrar um PIN de saída não conectado no filtro upstream e um PIN de entrada não conectado no filtro downstream.

Se você já tiver ponteiros para ambos os Pins, chame o método [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) para conectá-los. Se os Pins não puderem se conectar diretamente entre si, o método **IGraphBuilder:: Connect** poderá inserir filtros adicionais para concluir a conexão. Para obter mais informações, consulte [conexão inteligente](intelligent-connect.md).

Se você tiver um ponteiro para os filtros, mas não os Pins, deverá usar o método [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) para localizar os Pins. (Consulte [enumerando Pins](enumerating-pins.md).) As funções auxiliares neste tópico demonstram essa técnica.

### <a name="output-pin-to-filter"></a>Pino de saída para filtrar

A função a seguir usa dois parâmetros: um ponteiro para um pino de saída e um ponteiro para um filtro. A função conecta o pino de saída ao primeiro PIN de entrada disponível no filtro.


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



Essa função faz o seguinte:

1.  Chama a `FindUnconnectedPin` função para obter um PIN de entrada não conectado. Essa função é mostrada no tópico [localizar um PIN não conectado em um filtro](find-an-unconnected-pin-on-a-filter.md).
2.  Chama [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) para conectar os dois Pins.

### <a name="filter-to-input-pin"></a>Filtrar para o pino de entrada

A próxima função usa um ponteiro para um filtro e um ponteiro para um pino de entrada. Ele conecta o pino de entrada ao primeiro pino de saída disponível no filtro.


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



### <a name="filter-to-filter"></a>Filtrar para filtrar

A terceira função usa um ponteiro para um filtro upstream e um ponteiro para um filtro downstream e tenta conectar ambos os filtros.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Técnicas de Graph-Building geral](general-graph-building-techniques.md)
</dt> <dt>

[**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)
</dt> </dl>

 

 



