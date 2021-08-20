---
description: Este tópico descreve como encontrar um pino não conectado em um filtro. Encontrar um pino não conectado é útil quando você está conectando filtros.
ms.assetid: d0a906a8-bae4-43b3-8b02-ee5b97c9323d
title: Encontrar um pino não conectado em um filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a76100622f0398c58eb10f2dda041ba074f4610efbd1c649d48199ea2c676eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401750"
---
# <a name="find-an-unconnected-pin-on-a-filter"></a>Encontrar um pino não conectado em um filtro

Este tópico descreve como encontrar um pino não conectado em um filtro. Encontrar um pino não conectado é útil quando você está conectando filtros.

Em um cenário DirectShow de criação de grafo típico, você precisa de um pino desconectado que corresponde a uma direção de pino específica (entrada ou saída). Por exemplo, quando você conecta dois filtros, conecta um pino de saída de um filtro a um pino de entrada do outro filtro. Ambos os pinos devem ser desconectados antes de conectá-los.

Primeiro, precisamos de uma função que teste se um pino está conectado a outro pino. Essa função chama o [**método IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) para testar se o pino está conectado a outro pino.


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
> Este exemplo usa a [função SafeRelease](/windows/desktop/medfound/saferelease) para liberar ponteiros de interface.

 

Em seguida, precisamos de uma função que teste se um pino corresponde a uma direção de pino especificada. Essa função chama o [**método IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) para obter a direção do pino.


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



A próxima função corresponde a um pino por ambos os critérios (direção do pino e status da conexão).


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



Por fim, a função a seguir usa a interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) para fazer um loop pelos pinos no filtro. O chamador especifica a direção do pino desejado. Para cada pino, a função chama `MatchPin` para testar se o pino é uma combinação. Se a direção corresponder e o pino estiver desconectado, a função retornará um ponteiro para o pino correspondente no *parâmetro ppPin.*


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



Para ver um exemplo de como essa função pode ser usada, [consulte Conexão Dois Filtros](connect-two-filters.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Enumerando pinos](enumerating-pins.md)
</dt> <dt>

[Técnicas Graph-Building geral](general-graph-building-techniques.md)
</dt> <dt>

[**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin)
</dt> </dl>

 

 
