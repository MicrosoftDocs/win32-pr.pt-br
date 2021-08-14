---
description: Localizar um par de filtros
ms.assetid: 74d9fe65-f7f4-4971-9550-27884ac4146b
title: Localizar um par de filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d2f20a7145d2365e7ee1ec261ea861ddc5fa1eb01d0c3b2503f6f53fa25815
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401760"
---
# <a name="find-a-filters-peer"></a>Localizar um par de filtros

Dado um filtro, você pode percorrer o grafo localizando os filtros aos quais ele está conectado. Comece enumerando os Pins do filtro. Para cada PIN, verifique se esse PIN está conectado a outro PIN. Nesse caso, consulte o outro PIN para seu filtro proprietário. Você pode percorrer o grafo na direção de upstream enumerando os Pins de entrada do filtro ou na direção do downstream enumerando os Pins de saída.

A função a seguir pesquisa upstream ou downstream em busca de um filtro conectado. Ele retorna o primeiro filtro de correspondência que ele encontra:


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



A função chama [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) para enumerar os Pins do primeiro filtro. Para cada PIN, ele chama [**IPin:: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) para verificar se o PIN corresponde à direção especificada (entrada ou saída). Nesse caso, a função determina se o PIN está conectado a outro PIN, chamando o método [**IPin:: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) . Por fim, ele chama [**IPin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) no PIN conectado. Esse método retorna uma estrutura que contém, entre outras coisas, um ponteiro para o filtro proprietário do PIN. Esse ponteiro é retornado para o chamador no parâmetro *ppNext* . O chamador deve liberar o ponteiro.

O código a seguir mostra como chamar essa função:


```C++
IBaseFilter *pF; // Pointer to some filter.
IBaseFilter *pUpstream = NULL;
if (SUCCEEDED(GetNextFilter(pF, PINDIR_INPUT, &pUpstream)))
{
    // Use pUpstream ...
    pUpstream->Release();
}
```



Um filtro pode estar conectado a dois ou mais filtros em qualquer direção. Por exemplo, pode ser um filtro de divisão, com vários filtros downstream. Ou pode ser um filtro Mux, com vários filtros upstream a partir dele. Portanto, talvez você queira coletar todos eles em uma lista.

O código a seguir mostra uma maneira possível de implementar tal função. ele usa a classe DirectShow [**CGenericList**](cgenericlist.md) ; Você poderia escrever uma função equivalente usando alguma outra estrutura de dados.


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



Para complicar as coisas de certa forma, um filtro pode ter várias conexões de PIN com o mesmo filtro. Para evitar colocar duplicatas na lista, consulte cada ponteiro **IBaseFilter** para **IUnknown** e compare os ponteiros **IUnknown** . Pelas regras de COM, dois ponteiros de interface se referem ao mesmo objeto se e somente se retornarem ponteiros **IUnknown** idênticos. No exemplo anterior, a função AddFilterUnique lida com esse detalhe.

O exemplo a seguir mostra como usar a função GetPeerFilters:


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Técnicas de Graph-Building geral](general-graph-building-techniques.md)
</dt> </dl>

 

 



