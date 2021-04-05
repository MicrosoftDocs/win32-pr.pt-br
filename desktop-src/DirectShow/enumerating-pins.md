---
description: Enumerando Pins
ms.assetid: 231f10c1-46b4-4b66-b0ce-06a191237dfb
title: Enumerando Pins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322f1764c46c146d1b899c869d1708eac1f0427d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825749"
---
# <a name="enumerating-pins"></a>Enumerando Pins

Os filtros dão suporte ao método [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) , que enumera os Pins disponíveis no filtro. Ele retorna um ponteiro para a interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) . O método [**IEnumPins:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) recupera ponteiros de interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .

O exemplo a seguir mostra uma função que localiza um PIN com uma determinada direção (entrada ou saída) em um determinado filtro. Ele usa a enumeração de [**\_ direção do PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) para especificar a direção do PIN e o método [**IPin:: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) para localizar a direção de cada PIN enumerado. Se essa função encontrar um PIN correspondente, ela retornará um ponteiro de interface **IPin** com uma contagem de referência pendente. O chamador é responsável por liberar a interface.


```C++
HRESULT GetPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin **ppPin)
{
    IEnumPins  *pEnum = NULL;
    IPin       *pPin = NULL;
    HRESULT    hr;

    if (ppPin == NULL)
    {
        return E_POINTER;
    }

    hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        return hr;
    }
    while(pEnum->Next(1, &pPin, 0) == S_OK)
    {
        PIN_DIRECTION PinDirThis;
        hr = pPin->QueryDirection(&PinDirThis);
        if (FAILED(hr))
        {
            pPin->Release();
            pEnum->Release();
            return hr;
        }
        if (PinDir == PinDirThis)
        {
            // Found a match. Return the IPin pointer to the caller.
            *ppPin = pPin;
            pEnum->Release();
            return S_OK;
        }
        // Release the pin for the next time through the loop.
        pPin->Release();
    }
    // No more pins. We did not find a match.
    pEnum->Release();
    return E_FAIL;  
}
```



Essa função pode ser facilmente modificada para retornar o enésimo PIN com a direção especificada ou o *n* º PIN não conectado. (Para descobrir se um PIN está conectado a outro PIN, chame o método [**IPin:: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) .)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Enumerando objetos em um grafo de filtro](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Localizar um PIN não conectado em um filtro](find-an-unconnected-pin-on-a-filter.md)
</dt> <dt>

[Técnicas de Graph-Building geral](general-graph-building-techniques.md)
</dt> <dt>

[Conjunto de propriedades de PIN](pin-property-set.md)
</dt> </dl>

 

 



