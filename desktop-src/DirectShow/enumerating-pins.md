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
# <a name="enumerating-pins"></a><span data-ttu-id="f60e9-103">Enumerando Pins</span><span class="sxs-lookup"><span data-stu-id="f60e9-103">Enumerating Pins</span></span>

<span data-ttu-id="f60e9-104">Os filtros dão suporte ao método [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) , que enumera os Pins disponíveis no filtro.</span><span class="sxs-lookup"><span data-stu-id="f60e9-104">Filters support the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method, which enumerates the pins available on the filter.</span></span> <span data-ttu-id="f60e9-105">Ele retorna um ponteiro para a interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .</span><span class="sxs-lookup"><span data-stu-id="f60e9-105">It returns a pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface.</span></span> <span data-ttu-id="f60e9-106">O método [**IEnumPins:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) recupera ponteiros de interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="f60e9-106">The [**IEnumPins::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) method retrieves [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface pointers.</span></span>

<span data-ttu-id="f60e9-107">O exemplo a seguir mostra uma função que localiza um PIN com uma determinada direção (entrada ou saída) em um determinado filtro.</span><span class="sxs-lookup"><span data-stu-id="f60e9-107">The following example shows a function that locates a pin with a given direction (input or output) on a given filter.</span></span> <span data-ttu-id="f60e9-108">Ele usa a enumeração de [**\_ direção do PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) para especificar a direção do PIN e o método [**IPin:: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) para localizar a direção de cada PIN enumerado.</span><span class="sxs-lookup"><span data-stu-id="f60e9-108">It uses the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumeration to specify the pin direction, and the [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) method to find the direction of each enumerated pin.</span></span> <span data-ttu-id="f60e9-109">Se essa função encontrar um PIN correspondente, ela retornará um ponteiro de interface **IPin** com uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="f60e9-109">If this function finds a matching pin, it returns an **IPin** interface pointer with an outstanding reference count.</span></span> <span data-ttu-id="f60e9-110">O chamador é responsável por liberar a interface.</span><span class="sxs-lookup"><span data-stu-id="f60e9-110">The caller is responsible for releasing the interface.</span></span>


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



<span data-ttu-id="f60e9-111">Essa função pode ser facilmente modificada para retornar o enésimo PIN com a direção especificada ou o *n* º PIN não conectado.</span><span class="sxs-lookup"><span data-stu-id="f60e9-111">This function could easily be modified to return the nth pin with the specified direction, or the *n* th unconnected pin.</span></span> <span data-ttu-id="f60e9-112">(Para descobrir se um PIN está conectado a outro PIN, chame o método [**IPin:: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) .)</span><span class="sxs-lookup"><span data-stu-id="f60e9-112">(To find out if a pin is connected to another pin, call the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="f60e9-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f60e9-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f60e9-114">Enumerando objetos em um grafo de filtro</span><span class="sxs-lookup"><span data-stu-id="f60e9-114">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="f60e9-115">Localizar um PIN não conectado em um filtro</span><span class="sxs-lookup"><span data-stu-id="f60e9-115">Find an Unconnected Pin on a Filter</span></span>](find-an-unconnected-pin-on-a-filter.md)
</dt> <dt>

[<span data-ttu-id="f60e9-116">Técnicas de Graph-Building geral</span><span class="sxs-lookup"><span data-stu-id="f60e9-116">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="f60e9-117">Conjunto de propriedades de PIN</span><span class="sxs-lookup"><span data-stu-id="f60e9-117">Pin Property Set</span></span>](pin-property-set.md)
</dt> </dl>

 

 



