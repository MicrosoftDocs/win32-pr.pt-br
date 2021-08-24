---
description: Enumerando pinos
ms.assetid: 231f10c1-46b4-4b66-b0ce-06a191237dfb
title: Enumerando pinos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d772903321c71ab2c6d66f7cc46b7ca61b11f96a4bc17b13b8b2f8931d8eac5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748706"
---
# <a name="enumerating-pins"></a>Enumerando pinos

Os filtros são suportados pelo método [**IBaseFilter::EnumPins,**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) que enumera os pinos disponíveis no filtro. Ele retorna um ponteiro para a interface [**IEnumPins.**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) O [**método IEnumPins::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) recupera ponteiros de interface [**IPin.**](/windows/desktop/api/Strmif/nn-strmif-ipin)

O exemplo a seguir mostra uma função que localiza um pino com uma determinada direção (entrada ou saída) em um determinado filtro. Ele usa a [**enumeração PIN \_ DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) para especificar a direção do pino e o método [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) para encontrar a direção de cada pino enumerado. Se essa função encontrar um pin correspondente, ela retornará um ponteiro de interface **IPin** com uma contagem de referência pendente. O chamador é responsável por liberar a interface.


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



Essa função pode ser facilmente modificada para retornar o nº pino com a direção especificada ou o *n* o pino não conectado. (Para descobrir se um pino está conectado a outro pino, chame o método [**IPin::ConnectedTo.)**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Enumerando objetos em um filtro Graph](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Encontrar um pino não conectado em um filtro](find-an-unconnected-pin-on-a-filter.md)
</dt> <dt>

[Técnicas Graph-Building geral](general-graph-building-techniques.md)
</dt> <dt>

[Fixar conjunto de propriedades](pin-property-set.md)
</dt> </dl>

 

 



