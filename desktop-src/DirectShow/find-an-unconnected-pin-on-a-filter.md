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
# <a name="find-an-unconnected-pin-on-a-filter"></a><span data-ttu-id="4f594-104">Localizar um PIN não conectado em um filtro</span><span class="sxs-lookup"><span data-stu-id="4f594-104">Find an Unconnected Pin on a Filter</span></span>

<span data-ttu-id="4f594-105">Este tópico descreve como localizar um PIN não conectado em um filtro.</span><span class="sxs-lookup"><span data-stu-id="4f594-105">This topic describes how to find an unconnected pin on a filter.</span></span> <span data-ttu-id="4f594-106">Encontrar um PIN não conectado é útil quando você está conectando filtros.</span><span class="sxs-lookup"><span data-stu-id="4f594-106">Finding an unconnected pin is useful when you are connecting filters.</span></span>

<span data-ttu-id="4f594-107">Em um cenário típico de construção de grafo do DirectShow, você precisa de um PIN não conectado que corresponda a uma direção de PIN específica (entrada ou saída).</span><span class="sxs-lookup"><span data-stu-id="4f594-107">In a typical DirectShow graph-building scenario, you need an unconnected pin that matches a particular pin direction (input or output).</span></span> <span data-ttu-id="4f594-108">Por exemplo, ao conectar dois filtros, você conecta um pino de saída de um filtro a um PIN de entrada do outro filtro.</span><span class="sxs-lookup"><span data-stu-id="4f594-108">For example, when you connect two filters, you connect an output pin from one filter to an input pin from the other filter.</span></span> <span data-ttu-id="4f594-109">Ambos os Pins devem ser desconectados antes de você conectá-los.</span><span class="sxs-lookup"><span data-stu-id="4f594-109">Both pins must be unconnected before you connect them.</span></span>

<span data-ttu-id="4f594-110">Primeiro, precisamos de uma função que teste se um PIN está conectado a outro PIN.</span><span class="sxs-lookup"><span data-stu-id="4f594-110">First, we need a function that tests whether a pin is connected to another pin.</span></span> <span data-ttu-id="4f594-111">Essa função chama o método [**IPin:: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) para testar se o PIN está conectado a outro PIN.</span><span class="sxs-lookup"><span data-stu-id="4f594-111">This function calls the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method to test whether the pin is connected to another pin.</span></span>


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
> <span data-ttu-id="4f594-112">Este exemplo usa a função [SafeRelease](/windows/desktop/medfound/saferelease) para liberar ponteiros de interface.</span><span class="sxs-lookup"><span data-stu-id="4f594-112">This example uses the [SafeRelease](/windows/desktop/medfound/saferelease) function to release interface pointers.</span></span>

 

<span data-ttu-id="4f594-113">Em seguida, precisamos de uma função que teste se um PIN corresponde a uma direção de PIN especificada.</span><span class="sxs-lookup"><span data-stu-id="4f594-113">Next, we need a function that tests whether a pin matches a specified pin direction.</span></span> <span data-ttu-id="4f594-114">Essa função chama o método [**IPin:: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) para obter a direção do PIN.</span><span class="sxs-lookup"><span data-stu-id="4f594-114">This function calls the [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) method to get the pin direction.</span></span>


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



<span data-ttu-id="4f594-115">A próxima função corresponde a um PIN por ambos os critérios (direção do PIN e status da conexão).</span><span class="sxs-lookup"><span data-stu-id="4f594-115">The next function matches a pin by both criteria (pin direction and connection status).</span></span>


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



<span data-ttu-id="4f594-116">Por fim, a função a seguir usa a interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) para executar um loop pelos Pins no filtro.</span><span class="sxs-lookup"><span data-stu-id="4f594-116">Finally, the following function uses the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface to loop through the pins on the filter.</span></span> <span data-ttu-id="4f594-117">O chamador especifica a direção do PIN desejado.</span><span class="sxs-lookup"><span data-stu-id="4f594-117">The caller specifies the desired pin direction.</span></span> <span data-ttu-id="4f594-118">Para cada PIN, a função chama `MatchPin` para testar se o PIN é uma correspondência.</span><span class="sxs-lookup"><span data-stu-id="4f594-118">For each pin, the function calls `MatchPin` to test whether the pin is a match.</span></span> <span data-ttu-id="4f594-119">Se a direção corresponder e o PIN não estiver conectado, a função retornará um ponteiro para o PIN correspondente no parâmetro *ppPin* .</span><span class="sxs-lookup"><span data-stu-id="4f594-119">If the direction matches and the pin is unconnected, the function returns a pointer to the matching pin in the *ppPin* parameter.</span></span>


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



<span data-ttu-id="4f594-120">Para obter um exemplo de como essa função pode ser usada, consulte [conectar dois filtros](connect-two-filters.md).</span><span class="sxs-lookup"><span data-stu-id="4f594-120">For an example of how this function can be used, see [Connect Two Filters](connect-two-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f594-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4f594-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f594-122">Enumerando Pins</span><span class="sxs-lookup"><span data-stu-id="4f594-122">Enumerating Pins</span></span>](enumerating-pins.md)
</dt> <dt>

[<span data-ttu-id="4f594-123">Técnicas de Graph-Building geral</span><span class="sxs-lookup"><span data-stu-id="4f594-123">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="4f594-124">**ICaptureGraphBuilder2::FindPin**</span><span class="sxs-lookup"><span data-stu-id="4f594-124">**ICaptureGraphBuilder2::FindPin**</span></span>](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin)
</dt> </dl>

 

 
