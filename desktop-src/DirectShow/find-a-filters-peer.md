---
description: Localizar um par de filtros
ms.assetid: 74d9fe65-f7f4-4971-9550-27884ac4146b
title: Localizar um par de filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1717f6ad61ad7310fdaa11ea5baaab4dcb7f8011
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009878"
---
# <a name="find-a-filters-peer"></a><span data-ttu-id="89cb1-103">Localizar um par de filtros</span><span class="sxs-lookup"><span data-stu-id="89cb1-103">Find a Filters Peer</span></span>

<span data-ttu-id="89cb1-104">Dado um filtro, você pode percorrer o grafo localizando os filtros aos quais ele está conectado.</span><span class="sxs-lookup"><span data-stu-id="89cb1-104">Given a filter, you can traverse the graph by finding the filters to which it is connected.</span></span> <span data-ttu-id="89cb1-105">Comece enumerando os Pins do filtro.</span><span class="sxs-lookup"><span data-stu-id="89cb1-105">Start by enumerating the filter's pins.</span></span> <span data-ttu-id="89cb1-106">Para cada PIN, verifique se esse PIN está conectado a outro PIN.</span><span class="sxs-lookup"><span data-stu-id="89cb1-106">For each pin, check whether that pin is connected to another pin.</span></span> <span data-ttu-id="89cb1-107">Nesse caso, consulte o outro PIN para seu filtro proprietário.</span><span class="sxs-lookup"><span data-stu-id="89cb1-107">If so, query the other pin for it's owning filter.</span></span> <span data-ttu-id="89cb1-108">Você pode percorrer o grafo na direção de upstream enumerando os Pins de entrada do filtro ou na direção do downstream enumerando os Pins de saída.</span><span class="sxs-lookup"><span data-stu-id="89cb1-108">You can walk the graph in the upstream direction by enumerating the filter's input pins, or in the downstream direction by enumerating the output pins.</span></span>

<span data-ttu-id="89cb1-109">A função a seguir pesquisa upstream ou downstream em busca de um filtro conectado.</span><span class="sxs-lookup"><span data-stu-id="89cb1-109">The following function searches upstream or downstream for a connected filter.</span></span> <span data-ttu-id="89cb1-110">Ele retorna o primeiro filtro de correspondência que ele encontra:</span><span class="sxs-lookup"><span data-stu-id="89cb1-110">It returns the first matching filter that it finds:</span></span>


```C++
// Get the first upstream or downstream filter
HRESULT GetNextFilter(
    IBaseFilter *pFilter, // Pointer to the starting filter
    PIN_DIRECTION Dir,    // Direction to search (upstream or downstream)
    IBaseFilter **ppNext) // Receives a pointer to the next filter.
{
    if (!pFilter || !ppNext) return E_POINTER;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;
    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr)) return hr;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        // See if this pin matches the specified direction.
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            // Something strange happened.
            hr = E_UNEXPECTED;
            pPin->Release();
            break;
        }
        if (ThisPinDir == Dir)
        {
            // Check if the pin is connected to another pin.
            IPin *pPinNext = 0;
            hr = pPin->ConnectedTo(&pPinNext);
            if (SUCCEEDED(hr))
            {
                // Get the filter that owns that pin.
                PIN_INFO PinInfo;
                hr = pPinNext->QueryPinInfo(&PinInfo);
                pPinNext->Release();
                pPin->Release();
                pEnum->Release();
                if (FAILED(hr) || (PinInfo.pFilter == NULL))
                {
                    // Something strange happened.
                    return E_UNEXPECTED;
                }
                // This is the filter we're looking for.
                *ppNext = PinInfo.pFilter; // Client must release.
                return S_OK;
            }
        }
        pPin->Release();
    }
    pEnum->Release();
    // Did not find a matching filter.
    return E_FAIL;
}
```



<span data-ttu-id="89cb1-111">A função chama [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) para enumerar os Pins do primeiro filtro.</span><span class="sxs-lookup"><span data-stu-id="89cb1-111">The function calls [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) to enumerate the first filter's pins.</span></span> <span data-ttu-id="89cb1-112">Para cada PIN, ele chama [**IPin:: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) para verificar se o PIN corresponde à direção especificada (entrada ou saída).</span><span class="sxs-lookup"><span data-stu-id="89cb1-112">For each pin, it calls [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) to check whether the pin matches the specified direction (input or output).</span></span> <span data-ttu-id="89cb1-113">Nesse caso, a função determina se o PIN está conectado a outro PIN, chamando o método [**IPin:: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) .</span><span class="sxs-lookup"><span data-stu-id="89cb1-113">If so, the function determines whether that pin is connected to another pin, by calling the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method.</span></span> <span data-ttu-id="89cb1-114">Por fim, ele chama [**IPin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) no PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="89cb1-114">Finally, it calls [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) on the connected pin.</span></span> <span data-ttu-id="89cb1-115">Esse método retorna uma estrutura que contém, entre outras coisas, um ponteiro para o filtro proprietário do PIN.</span><span class="sxs-lookup"><span data-stu-id="89cb1-115">This method returns a structure that contains, among other things, a pointer to that pin's owning filter.</span></span> <span data-ttu-id="89cb1-116">Esse ponteiro é retornado para o chamador no parâmetro *ppNext* .</span><span class="sxs-lookup"><span data-stu-id="89cb1-116">This pointer is returned to the caller in the *ppNext* parameter.</span></span> <span data-ttu-id="89cb1-117">O chamador deve liberar o ponteiro.</span><span class="sxs-lookup"><span data-stu-id="89cb1-117">The caller must release the pointer.</span></span>

<span data-ttu-id="89cb1-118">O código a seguir mostra como chamar essa função:</span><span class="sxs-lookup"><span data-stu-id="89cb1-118">The following code shows how to call this function:</span></span>


```C++
IBaseFilter *pF; // Pointer to some filter.
IBaseFilter *pUpstream = NULL;
if (SUCCEEDED(GetNextFilter(pF, PINDIR_INPUT, &pUpstream)))
{
    // Use pUpstream ...
    pUpstream->Release();
}
```



<span data-ttu-id="89cb1-119">Um filtro pode estar conectado a dois ou mais filtros em qualquer direção.</span><span class="sxs-lookup"><span data-stu-id="89cb1-119">A filter might be connected to two or more filters in either direction.</span></span> <span data-ttu-id="89cb1-120">Por exemplo, pode ser um filtro de divisão, com vários filtros downstream.</span><span class="sxs-lookup"><span data-stu-id="89cb1-120">For example, it might be a splitter filter, with several filters downstream from it.</span></span> <span data-ttu-id="89cb1-121">Ou pode ser um filtro Mux, com vários filtros upstream a partir dele.</span><span class="sxs-lookup"><span data-stu-id="89cb1-121">Or it might be a mux filter, with several filters upstream from it.</span></span> <span data-ttu-id="89cb1-122">Portanto, talvez você queira coletar todos eles em uma lista.</span><span class="sxs-lookup"><span data-stu-id="89cb1-122">Therefore, you might want to collect all of them into a list.</span></span>

<span data-ttu-id="89cb1-123">O código a seguir mostra uma maneira possível de implementar tal função.</span><span class="sxs-lookup"><span data-stu-id="89cb1-123">The following code shows one possible way to implement such a function.</span></span> <span data-ttu-id="89cb1-124">Ele usa a classe [**CGenericList**](cgenericlist.md) do DirectShow; Você poderia escrever uma função equivalente usando alguma outra estrutura de dados.</span><span class="sxs-lookup"><span data-stu-id="89cb1-124">It uses the DirectShow [**CGenericList**](cgenericlist.md) class; you could write an equivalent function using some other data structure.</span></span>


```C++
#include <streams.h>  // Link to the DirectShow base class library
// Define a typedef for a list of filters.
typedef CGenericList<IBaseFilter> CFilterList;

// Forward declaration. Adds a filter to the list unless it's a duplicate.
void AddFilterUnique(CFilterList &FilterList, IBaseFilter *pNew);

// Find all the immediate upstream or downstream peers of a filter.
HRESULT GetPeerFilters(
    IBaseFilter *pFilter, // Pointer to the starting filter
    PIN_DIRECTION Dir,    // Direction to search (upstream or downstream)
    CFilterList &FilterList)  // Collect the results in this list.
{
    if (!pFilter) return E_POINTER;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;
    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr)) return hr;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        // See if this pin matches the specified direction.
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            // Something strange happened.
            hr = E_UNEXPECTED;
            pPin->Release();
            break;
        }
        if (ThisPinDir == Dir)
        {
            // Check if the pin is connected to another pin.
            IPin *pPinNext = 0;
            hr = pPin->ConnectedTo(&pPinNext);
            if (SUCCEEDED(hr))
            {
                // Get the filter that owns that pin.
                PIN_INFO PinInfo;
                hr = pPinNext->QueryPinInfo(&PinInfo);
                pPinNext->Release();
                if (FAILED(hr) || (PinInfo.pFilter == NULL))
                {
                    // Something strange happened.
                    pPin->Release();
                    pEnum->Release();
                    return E_UNEXPECTED;
                }
                // Insert the filter into the list.
                AddFilterUnique(FilterList, PinInfo.pFilter);
                PinInfo.pFilter->Release();
            }
        }
        pPin->Release();
    }
    pEnum->Release();
    return S_OK;
}
void AddFilterUnique(CFilterList &FilterList, IBaseFilter *pNew)
{
    if (pNew == NULL) return;

    POSITION pos = FilterList.GetHeadPosition();
    while (pos)
    {
        IBaseFilter *pF = FilterList.GetNext(pos);
        if (IsEqualObject(pF, pNew))
        {
            return;
        }
    }
    pNew->AddRef();  // The caller must release everything in the list.
    FilterList.AddTail(pNew);
}
```



<span data-ttu-id="89cb1-125">Para complicar as coisas de certa forma, um filtro pode ter várias conexões de PIN com o mesmo filtro.</span><span class="sxs-lookup"><span data-stu-id="89cb1-125">To complicate matters somewhat, a filter can have multiple pin connections to the same filter.</span></span> <span data-ttu-id="89cb1-126">Para evitar colocar duplicatas na lista, consulte cada ponteiro **IBaseFilter** para **IUnknown** e compare os ponteiros **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="89cb1-126">To avoid putting duplicates into the list, query each **IBaseFilter** pointer for **IUnknown** and compare the **IUnknown** pointers.</span></span> <span data-ttu-id="89cb1-127">Pelas regras de COM, dois ponteiros de interface se referem ao mesmo objeto se e somente se retornarem ponteiros **IUnknown** idênticos.</span><span class="sxs-lookup"><span data-stu-id="89cb1-127">By the rules of COM, two interface pointers refer to the same object if and only if they return identical **IUnknown** pointers.</span></span> <span data-ttu-id="89cb1-128">No exemplo anterior, a função AddFilterUnique lida com esse detalhe.</span><span class="sxs-lookup"><span data-stu-id="89cb1-128">In the previous example, the AddFilterUnique function handles this detail.</span></span>

<span data-ttu-id="89cb1-129">O exemplo a seguir mostra como usar a função GetPeerFilters:</span><span class="sxs-lookup"><span data-stu-id="89cb1-129">The following example shows how to use the GetPeerFilters function:</span></span>


```C++
IBaseFilter *pF; // Pointer to some filter.
CFilterList FList(NAME("MyList"));  // List to hold the downstream peers.
hr = GetPeerFilters(pF, PINDIR_OUTPUT, FList);
if (SUCCEEDED(hr))
{
    POSITION pos = FList.GetHeadPosition();
    while (pos)
    {
        IBaseFilter *pDownstream = FList.GetNext(pos);
        pDownstream->Release();
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="89cb1-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="89cb1-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89cb1-131">Técnicas de Graph-Building geral</span><span class="sxs-lookup"><span data-stu-id="89cb1-131">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> </dl>

 

 



