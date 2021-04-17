---
description: Trabalhando com categorias de PIN
ms.assetid: 1ee648b3-8370-4e4d-b513-d998131512ee
title: Trabalhando com categorias de PIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ac58fff91821477cca51e0613772e3e5763d4d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759006"
---
# <a name="working-with-pin-categories"></a>Trabalhando com categorias de PIN

Para pesquisar em um filtro o para um PIN com uma determinada categoria de PIN, você pode usar o método [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) . O exemplo a seguir pesquisa um pino de visualização de vídeo:


```C++
int i = 0;
hr = pBuild->FindPin(
    pFilter,               // Pointer to a filter to search.
    PINDIR_OUTPUT,         // Which pin direction?
    &PIN_CATEGORY_PREVIEW, // Which category? (NULL means "any category")
    &MEDIATYPE_Video,      // What media type? (NULL means "any type")
    FALSE,                 // Must be connected?
    i,                     // Get the i'th matching pin (0 = first match)
    &pPin                  // Receives a pointer to the pin.
);
```



O primeiro parâmetro é um ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do filtro. Os próximos três parâmetros especificam a direção, a categoria do PIN e o tipo de mídia. O valor **false** no quinto parâmetro indica que o PIN pode ser conectado ou desconectado. (Para obter as definições exatas desses parâmetros, consulte a documentação do método.) Se o método encontrar um PIN correspondente, ele retornará um ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) no parâmetro *pPin* .

Embora o método [**FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) seja conveniente, você também pode escrever suas próprias funções auxiliares, se preferir. Para determinar a categoria de um PIN, chame o método [**IKsPropertySet:: Get**](ikspropertyset-get.md) conforme descrito no tópico [conjunto de propriedades de PIN](pin-property-set.md).

O código a seguir mostra uma função auxiliar que verifica se um PIN corresponde a uma categoria especificada:


```C++
// Returns TRUE if a pin matches the specified pin category.

BOOL PinMatchesCategory(IPin *pPin, REFGUID Category)
{
    BOOL bFound = FALSE;

    IKsPropertySet *pKs = NULL;
    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (SUCCEEDED(hr))
    {
        GUID PinCategory;
        DWORD cbReturned;
        hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
            &PinCategory, sizeof(GUID), &cbReturned);
        if (SUCCEEDED(hr) && (cbReturned == sizeof(GUID)))
        {
            bFound = (PinCategory == Category);
        }
        pKs->Release();
    }
    return bFound;
}
```



O exemplo a seguir é uma função que procura um PIN por categoria, semelhante ao método [**FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) :


```C++
// Finds the first pin that matches a specified pin category and direction.

HRESULT FindPinByCategory(
    IBaseFilter *pFilter, // Pointer to the filter to search.
    PIN_DIRECTION PinDir, // Direction of the pin.
    REFGUID Category,     // Pin category.
    IPin **ppPin)         // Receives a pointer to the pin.
{
    *ppPin = 0;

    HRESULT hr = S_OK;
    BOOL bFound = FALSE;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;

    hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (hr = pEnum->Next(1, &pPin, 0), hr == S_OK)
    {
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            goto done;
        }
        if ((ThisPinDir == PinDir) && 
            PinMatchesCategory(pPin, Category))
        {
            *ppPin = pPin;
            (*ppPin)->AddRef();   // The caller must release the interface.
            bFound = TRUE;
            break;
        }
        SafeRelease(&pPin);
    }

done:
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    if (SUCCEEDED(hr) && !bFound)
    {
        hr = E_FAIL;
    }
    return hr;
}
```



O código a seguir usa a função Previous para procurar um PIN de porta de vídeo em um filtro:


```C++
IPin *pVP; 
hr = FindPinByCategory(pFilter, PINDIR_OUTPUT, 
    PIN_CATEGORY_VIDEOPORT, &pVP);
if (SUCCEEDED(hr))
{
    // Use pVP ... 
    // Release when you are done.
    pVP->Release();
}
```



Para obter mais informações sobre conjuntos de propriedades, consulte a documentação do [Windows Driver Kit (WDK)](/windows-hardware/drivers/gettingstarted/) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tópicos de captura avançada](advanced-capture-topics.md)
</dt> <dt>

[Conjunto de propriedades de PIN](pin-property-set.md)
</dt> <dt>

[Filtros de captura de vídeo do DirectShow](directshow-video-capture-filters.md)
</dt> </dl>

 

 
