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
# <a name="using-the-filter-mapper"></a><span data-ttu-id="4e287-103">Usando o mapeador de filtro</span><span class="sxs-lookup"><span data-stu-id="4e287-103">Using the Filter Mapper</span></span>

<span data-ttu-id="4e287-104">O [mapeador de filtro](filter-mapper.md) é um objeto com que enumera filtros do DirectShow com base em vários critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="4e287-104">The [Filter Mapper](filter-mapper.md) is a COM object that enumerates DirectShow filters based on various search criteria.</span></span> <span data-ttu-id="4e287-105">O mapeador de filtro pode ser menos eficiente do que o enumerador de dispositivo do sistema, portanto, se você precisar de filtros de uma determinada categoria, deverá usar o enumerador de dispositivo do sistema.</span><span class="sxs-lookup"><span data-stu-id="4e287-105">The Filter Mapper can be less efficient than the System Device Enumerator, so if you need filters from a particular category, you should use the System Device Enumerator.</span></span> <span data-ttu-id="4e287-106">Mas se você precisar localizar um filtro que ofereça suporte a uma determinada combinação de tipos de mídia, mas não se enquadrar em uma categoria de corte claro, talvez seja necessário usar o mapeador de filtro.</span><span class="sxs-lookup"><span data-stu-id="4e287-106">But if you need to locate a filter that supports a certain combination of media types, but does not fall into a clear-cut category, you might need to use the Filter Mapper.</span></span> <span data-ttu-id="4e287-107">(Um exemplo seria um filtro de processador ou um filtro de decodificador.)</span><span class="sxs-lookup"><span data-stu-id="4e287-107">(An example would be a renderer filter or a decoder filter.)</span></span>

<span data-ttu-id="4e287-108">O mapeador de filtro expõe a interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .</span><span class="sxs-lookup"><span data-stu-id="4e287-108">The Filter Mapper exposes the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface.</span></span> <span data-ttu-id="4e287-109">Para procurar um filtro, chame o método [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) .</span><span class="sxs-lookup"><span data-stu-id="4e287-109">To search for a filter, call the [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method.</span></span> <span data-ttu-id="4e287-110">Esse método usa vários parâmetros que definem os critérios de pesquisa e retorna um enumerador para os filtros correspondentes.</span><span class="sxs-lookup"><span data-stu-id="4e287-110">This method takes several parameters that define the search criteria, and returns an enumerator for the matching filters.</span></span> <span data-ttu-id="4e287-111">O enumerador dá suporte à interface [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) e fornece um moniker exclusivo para cada filtro correspondente.</span><span class="sxs-lookup"><span data-stu-id="4e287-111">The enumerator supports the [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) interface, and supplies a unique moniker for each matching filter.</span></span>

<span data-ttu-id="4e287-112">O exemplo a seguir enumera filtros que aceitam entrada de vídeo digital (DV) e têm pelo menos um pino de saída, de qualquer tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="4e287-112">The following example enumerates filters that accept digital video (DV) input and have at least one output pin, of any media type.</span></span> <span data-ttu-id="4e287-113">(O filtro do [decodificador de vídeo DV](dv-video-decoder-filter.md) corresponde a esses critérios.)</span><span class="sxs-lookup"><span data-stu-id="4e287-113">(The [DV Video Decoder](dv-video-decoder-filter.md) filter matches these criteria.)</span></span>


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



<span data-ttu-id="4e287-114">O método [**EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) tem um número muito grande de parâmetros, que são comentados no exemplo.</span><span class="sxs-lookup"><span data-stu-id="4e287-114">The [**EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method has a fairly large number of parameters, which are commented in the example.</span></span> <span data-ttu-id="4e287-115">As partes significativas para esse exemplo incluem:</span><span class="sxs-lookup"><span data-stu-id="4e287-115">The significant ones for this example include:</span></span>

-   <span data-ttu-id="4e287-116">Valor de mérito mínimo: o filtro deve ter um valor de mérito acima do mérito não \_ \_ \_ usar.</span><span class="sxs-lookup"><span data-stu-id="4e287-116">Minimum merit value: The filter must have a merit value above MERIT\_DO\_NOT\_USE.</span></span>
-   <span data-ttu-id="4e287-117">Tipos de entrada: o chamador passa uma matriz que contém pares de tipos e subtipos principais.</span><span class="sxs-lookup"><span data-stu-id="4e287-117">Input types: The caller passes an array containing pairs of major types and subtypes.</span></span> <span data-ttu-id="4e287-118">Somente filtros que dão suporte a pelo menos um desses pares serão correspondentes.</span><span class="sxs-lookup"><span data-stu-id="4e287-118">Only filters that support at least one of these pairs will match.</span></span>
-   <span data-ttu-id="4e287-119">Correspondência exata: um filtro pode registrar valores **nulos** para tipo principal, subtipo, categoria de PIN ou médio.</span><span class="sxs-lookup"><span data-stu-id="4e287-119">Exact match: A filter can register **NULL** values for major type, subtype, pin category, or medium.</span></span> <span data-ttu-id="4e287-120">A menos que você especifique a correspondência exata, um valor **nulo** atua como um caractere curinga, correspondendo a qualquer valor que você especificar.</span><span class="sxs-lookup"><span data-stu-id="4e287-120">Unless you specify exact matching, a **NULL** value acts as a wildcard, matching any value that you specify.</span></span> <span data-ttu-id="4e287-121">Com correspondência exata, o filtro deve corresponder exatamente aos seus critérios.</span><span class="sxs-lookup"><span data-stu-id="4e287-121">With exact matching, the filter must exactly match your criteria.</span></span> <span data-ttu-id="4e287-122">No entanto, se você fornecer um parâmetro **nulo** nos critérios de pesquisa, ele sempre funcionará como um valor curinga ou "não importa", correspondendo a qualquer filtro.</span><span class="sxs-lookup"><span data-stu-id="4e287-122">However, if you give a **NULL** parameter in the search criteria, it always acts as a wildcard or "don't care" value, matching any filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e287-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e287-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e287-124">Enumerando dispositivos e filtros</span><span class="sxs-lookup"><span data-stu-id="4e287-124">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="4e287-125">Conexão inteligente</span><span class="sxs-lookup"><span data-stu-id="4e287-125">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> </dl>

 

 
