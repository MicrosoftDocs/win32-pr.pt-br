---
description: Usando o mapeador de filtro
ms.assetid: 3f774350-4508-437f-98d1-cca91220f339
title: Usando o mapeador de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2d7acf85a7b415fc161cd21e17d069b46c3f40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829056"
---
# <a name="using-the-filter-mapper"></a>Usando o mapeador de filtro

O [mapeador de filtro](filter-mapper.md) é um objeto com que enumera filtros do DirectShow com base em vários critérios de pesquisa. O mapeador de filtro pode ser menos eficiente do que o enumerador de dispositivo do sistema, portanto, se você precisar de filtros de uma determinada categoria, deverá usar o enumerador de dispositivo do sistema. Mas se você precisar localizar um filtro que ofereça suporte a uma determinada combinação de tipos de mídia, mas não se enquadrar em uma categoria de corte claro, talvez seja necessário usar o mapeador de filtro. (Um exemplo seria um filtro de processador ou um filtro de decodificador.)

O mapeador de filtro expõe a interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) . Para procurar um filtro, chame o método [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) . Esse método usa vários parâmetros que definem os critérios de pesquisa e retorna um enumerador para os filtros correspondentes. O enumerador dá suporte à interface [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) e fornece um moniker exclusivo para cada filtro correspondente.

O exemplo a seguir enumera filtros que aceitam entrada de vídeo digital (DV) e têm pelo menos um pino de saída, de qualquer tipo de mídia. (O filtro do [decodificador de vídeo DV](dv-video-decoder-filter.md) corresponde a esses critérios.)


```C++
IFilterMapper2 *pMapper = NULL;
IEnumMoniker *pEnum = NULL;

hr = CoCreateInstance(CLSID_FilterMapper2, 
    NULL, CLSCTX_INPROC, IID_IFilterMapper2, 
    (void **) &pMapper);

if (FAILED(hr))
{
    // Error handling omitted for clarity.
}

GUID arrayInTypes[2];
arrayInTypes[0] = MEDIATYPE_Video;
arrayInTypes[1] = MEDIASUBTYPE_dvsd;

hr = pMapper->EnumMatchingFilters(
        &pEnum,
        0,                  // Reserved.
        TRUE,               // Use exact match?
        MERIT_DO_NOT_USE+1, // Minimum merit.
        TRUE,               // At least one input pin?
        1,                  // Number of major type/subtype pairs for input.
        arrayInTypes,       // Array of major type/subtype pairs for input.
        NULL,               // Input medium.
        NULL,               // Input pin category.
        FALSE,              // Must be a renderer?
        TRUE,               // At least one output pin?
        0,                  // Number of major type/subtype pairs for output.
        NULL,               // Array of major type/subtype pairs for output.
        NULL,               // Output medium.
        NULL);              // Output pin category.

// Enumerate the monikers.
IMoniker *pMoniker;
ULONG cFetched;
while (pEnum->Next(1, &pMoniker, &cFetched) == S_OK)
{
    IPropertyBag *pPropBag = NULL;
    hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
       (void **)&pPropBag);

    if (SUCCEEDED(hr))
    {
        // To retrieve the friendly name of the filter, do the following:
        VARIANT varName;
        VariantInit(&varName);
        hr = pPropBag->Read(L"FriendlyName", &varName, 0);
        if (SUCCEEDED(hr))
        {
            // Display the name in your UI somehow.
        }
        VariantClear(&varName);

        // To create an instance of the filter, do the following:
        IBaseFilter *pFilter;
        hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, (void**)&pFilter);
        // Now add the filter to the graph. Remember to release pFilter later.
    
        // Clean up.
        pPropBag->Release();
    }
    pMoniker->Release();
}

// Clean up.
pMapper->Release();
pEnum->Release();
```



O método [**EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) tem um número muito grande de parâmetros, que são comentados no exemplo. As partes significativas para esse exemplo incluem:

-   Valor de mérito mínimo: o filtro deve ter um valor de mérito acima do mérito não \_ \_ \_ usar.
-   Tipos de entrada: o chamador passa uma matriz que contém pares de tipos e subtipos principais. Somente filtros que dão suporte a pelo menos um desses pares serão correspondentes.
-   Correspondência exata: um filtro pode registrar valores **nulos** para tipo principal, subtipo, categoria de PIN ou médio. A menos que você especifique a correspondência exata, um valor **nulo** atua como um caractere curinga, correspondendo a qualquer valor que você especificar. Com correspondência exata, o filtro deve corresponder exatamente aos seus critérios. No entanto, se você fornecer um parâmetro **nulo** nos critérios de pesquisa, ele sempre funcionará como um valor curinga ou "não importa", correspondendo a qualquer filtro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Enumerando dispositivos e filtros](enumerating-devices-and-filters.md)
</dt> <dt>

[Conexão inteligente](intelligent-connect.md)
</dt> </dl>

 

 
