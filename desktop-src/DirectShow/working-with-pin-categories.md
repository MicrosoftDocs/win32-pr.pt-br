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
# <a name="working-with-pin-categories"></a><span data-ttu-id="4034b-103">Trabalhando com categorias de PIN</span><span class="sxs-lookup"><span data-stu-id="4034b-103">Working with Pin Categories</span></span>

<span data-ttu-id="4034b-104">Para pesquisar em um filtro o para um PIN com uma determinada categoria de PIN, você pode usar o método [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) .</span><span class="sxs-lookup"><span data-stu-id="4034b-104">To search on a filter the the for a pin with a given pin category, you can use the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method.</span></span> <span data-ttu-id="4034b-105">O exemplo a seguir pesquisa um pino de visualização de vídeo:</span><span class="sxs-lookup"><span data-stu-id="4034b-105">The following example searches for a video preview pin:</span></span>


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



<span data-ttu-id="4034b-106">O primeiro parâmetro é um ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do filtro.</span><span class="sxs-lookup"><span data-stu-id="4034b-106">The first parameter is a pointer to the filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="4034b-107">Os próximos três parâmetros especificam a direção, a categoria do PIN e o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="4034b-107">The next three parameters specify the direction, pin category, and media type.</span></span> <span data-ttu-id="4034b-108">O valor **false** no quinto parâmetro indica que o PIN pode ser conectado ou desconectado.</span><span class="sxs-lookup"><span data-stu-id="4034b-108">The value **FALSE** in the fifth parameter indicates that the pin can be either connected or unconnected.</span></span> <span data-ttu-id="4034b-109">(Para obter as definições exatas desses parâmetros, consulte a documentação do método.) Se o método encontrar um PIN correspondente, ele retornará um ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) no parâmetro *pPin* .</span><span class="sxs-lookup"><span data-stu-id="4034b-109">(For the exact definitions of these parameters, refer to the documentation for the method.) If the method finds a matching pin, it returns a pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface in the *pPin* parameter.</span></span>

<span data-ttu-id="4034b-110">Embora o método [**FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) seja conveniente, você também pode escrever suas próprias funções auxiliares, se preferir.</span><span class="sxs-lookup"><span data-stu-id="4034b-110">Although the [**FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method is convenient, you can also write your own helper functions if you prefer.</span></span> <span data-ttu-id="4034b-111">Para determinar a categoria de um PIN, chame o método [**IKsPropertySet:: Get**](ikspropertyset-get.md) conforme descrito no tópico [conjunto de propriedades de PIN](pin-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="4034b-111">To determine a pin's category, call the [**IKsPropertySet::Get**](ikspropertyset-get.md) method as described in the topic [Pin Property Set](pin-property-set.md).</span></span>

<span data-ttu-id="4034b-112">O código a seguir mostra uma função auxiliar que verifica se um PIN corresponde a uma categoria especificada:</span><span class="sxs-lookup"><span data-stu-id="4034b-112">The following code shows a helper function that checks whether a pin matches a specified category:</span></span>


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



<span data-ttu-id="4034b-113">O exemplo a seguir é uma função que procura um PIN por categoria, semelhante ao método [**FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) :</span><span class="sxs-lookup"><span data-stu-id="4034b-113">The next example is a function that searches for a pin by category, similar to the [**FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method:</span></span>


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



<span data-ttu-id="4034b-114">O código a seguir usa a função Previous para procurar um PIN de porta de vídeo em um filtro:</span><span class="sxs-lookup"><span data-stu-id="4034b-114">The following code uses the previous function to search for a video port pin on a filter:</span></span>


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



<span data-ttu-id="4034b-115">Para obter mais informações sobre conjuntos de propriedades, consulte a documentação do [Windows Driver Kit (WDK)](/windows-hardware/drivers/gettingstarted/) .</span><span class="sxs-lookup"><span data-stu-id="4034b-115">For more information about property sets, refer to the [Windows Driver Kit (WDK)](/windows-hardware/drivers/gettingstarted/) documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4034b-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4034b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4034b-117">Tópicos de captura avançada</span><span class="sxs-lookup"><span data-stu-id="4034b-117">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="4034b-118">Conjunto de propriedades de PIN</span><span class="sxs-lookup"><span data-stu-id="4034b-118">Pin Property Set</span></span>](pin-property-set.md)
</dt> <dt>

[<span data-ttu-id="4034b-119">Filtros de captura de vídeo do DirectShow</span><span class="sxs-lookup"><span data-stu-id="4034b-119">DirectShow Video Capture Filters</span></span>](directshow-video-capture-filters.md)
</dt> </dl>

 

 
