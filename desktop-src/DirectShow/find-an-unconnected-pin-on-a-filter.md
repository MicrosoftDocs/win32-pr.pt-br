---
description: Este tópico descreve como localizar um PIN não conectado em um filtro. Encontrar um PIN não conectado é útil quando você está conectando filtros.
ms.assetid: d0a906a8-bae4-43b3-8b02-ee5b97c9323d
title: Localizar um PIN não conectado em um filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee47b811c027161b70769cb04063d0e8214934a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009877"
---
# <a name="find-an-unconnected-pin-on-a-filter"></a>Localizar um PIN não conectado em um filtro

Este tópico descreve como localizar um PIN não conectado em um filtro. Encontrar um PIN não conectado é útil quando você está conectando filtros.

Em um cenário típico de construção de grafo do DirectShow, você precisa de um PIN não conectado que corresponda a uma direção de PIN específica (entrada ou saída). Por exemplo, ao conectar dois filtros, você conecta um pino de saída de um filtro a um PIN de entrada do outro filtro. Ambos os Pins devem ser desconectados antes de você conectá-los.

Primeiro, precisamos de uma função que teste se um PIN está conectado a outro PIN. Essa função chama o método [**IPin:: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) para testar se o PIN está conectado a outro PIN.


```C++
// Query whether a pin is connected to another pin.
//
// Note: This function does not return a pointer to the connected pin.

HRESULT IsPinConnected(IPin *pPin, BOOL *pResult)
{
    IPin *pTmp = NULL;
    HRESULT hr = pPin->ConnectedTo(&pTmp);
    if (SUCCEEDED(hr))
    {
        *pResult = TRUE;
    }
    else if (hr == VFW_E_NOT_CONNECTED)
    {
        // The pin is not connected. This is not an error for our purposes.
        *pResult = FALSE;
        hr = S_OK;
    }

    SafeRelease(&pTmp);
    return hr;
}
```



> [!Note]  
> Este exemplo usa a função [SafeRelease](/windows/desktop/medfound/saferelease) para liberar ponteiros de interface.

 

Em seguida, precisamos de uma função que teste se um PIN corresponde a uma direção de PIN especificada. Essa função chama o método [**IPin:: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) para obter a direção do PIN.


```C++
// Query whether a pin has a specified direction (input / output)
HRESULT IsPinDirection(IPin *pPin, PIN_DIRECTION dir, BOOL *pResult)
{
    PIN_DIRECTION pinDir;
    HRESULT hr = pPin->QueryDirection(&pinDir);
    if (SUCCEEDED(hr))
    {
        *pResult = (pinDir == dir);
    }
    return hr;
}
```



A próxima função corresponde a um PIN por ambos os critérios (direção do PIN e status da conexão).


```C++
// Match a pin by pin direction and connection state.
HRESULT MatchPin(IPin *pPin, PIN_DIRECTION direction, BOOL bShouldBeConnected, BOOL *pResult)
{
    assert(pResult != NULL);

    BOOL bMatch = FALSE;
    BOOL bIsConnected = FALSE;

    HRESULT hr = IsPinConnected(pPin, &bIsConnected);
    if (SUCCEEDED(hr))
    {
        if (bIsConnected == bShouldBeConnected)
        {
            hr = IsPinDirection(pPin, direction, &bMatch);
        }
    }

    if (SUCCEEDED(hr))
    {
        *pResult = bMatch;
    }
    return hr;
}
```



Por fim, a função a seguir usa a interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) para executar um loop pelos Pins no filtro. O chamador especifica a direção do PIN desejado. Para cada PIN, a função chama `MatchPin` para testar se o PIN é uma correspondência. Se a direção corresponder e o PIN não estiver conectado, a função retornará um ponteiro para o PIN correspondente no parâmetro *ppPin* .


```C++
// Return the first unconnected input pin or output pin.
HRESULT FindUnconnectedPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin **ppPin)
{
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;
    BOOL bFound = FALSE;

    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = MatchPin(pPin, PinDir, FALSE, &bFound);
        if (FAILED(hr))
        {
            goto done;
        }
        if (bFound)
        {
            *ppPin = pPin;
            (*ppPin)->AddRef();
            break;
        }
        SafeRelease(&pPin);
    }

    if (!bFound)
    {
        hr = VFW_E_NOT_FOUND;
    }

done:
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    return hr;
}
```



Para obter um exemplo de como essa função pode ser usada, consulte [conectar dois filtros](connect-two-filters.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Enumerando Pins](enumerating-pins.md)
</dt> <dt>

[Técnicas de Graph-Building geral](general-graph-building-techniques.md)
</dt> <dt>

[**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin)
</dt> </dl>

 

 
