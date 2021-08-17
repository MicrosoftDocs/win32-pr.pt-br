---
description: Este tópico mostra algumas funções auxiliares para se conectar DirectShow filtros.
ms.assetid: cfd85944-7ae7-49e6-948f-9e190cdeed12
title: Conexão Dois filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab83e8608c088fde6d06c0a44621f1c066f177ecf76cbc8ba3f55d31218b49ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954205"
---
# <a name="connect-two-filters"></a>Conexão Dois filtros

Este tópico mostra algumas funções auxiliares para se conectar DirectShow filtros.

Para conectar dois filtros, você deve encontrar um pino de saída não conectado no filtro upstream e um pino de entrada não conectado no filtro downstream.

Se você já tiver ponteiros para ambos os pinos, chame o [**método IGraphBuilder::Conexão**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) para conectá-los. Se os pinos não puderem se conectar diretamente entre si, o método **IGraphBuilder::Conexão** poderá inserir filtros adicionais para concluir a conexão. Para obter mais informações, consulte [Intelligent Conexão](intelligent-connect.md).

Se você tiver um ponteiro para os filtros, mas não os pinos, deverá usar o método [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) para encontrar os pinos. (Consulte [Enumerando pinos](enumerating-pins.md).) As funções auxiliares neste tópico demonstram essa técnica.

### <a name="output-pin-to-filter"></a>Pino de saída para filtrar

A função a seguir leva dois parâmetros: um ponteiro para um pino de saída e um ponteiro para um filtro. A função conecta o pino de saída ao primeiro pino de entrada disponível no filtro.


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

1.  Chama a `FindUnconnectedPin` função para obter um pino de entrada não conectado. Essa função é mostrada no tópico [Find an Unconnected Pin on a Filter](find-an-unconnected-pin-on-a-filter.md).
2.  Chama [**IGraphBuilder::Conexão**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) para conectar os dois pinos.

### <a name="filter-to-input-pin"></a>Filtrar para o pino de entrada

A próxima função leva um ponteiro para um filtro e um ponteiro para um pino de entrada. Ele conecta o pino de entrada ao primeiro pino de saída disponível no filtro.


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

A terceira função leva um ponteiro para um filtro upstream e um ponteiro para um filtro downstream e tenta conectar os dois filtros.


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

[Técnicas Graph-Building geral](general-graph-building-techniques.md)
</dt> <dt>

[**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)
</dt> </dl>

 

 



