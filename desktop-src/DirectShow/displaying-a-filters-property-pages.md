---
description: Exibindo páginas de propriedades de um filtro
ms.assetid: 4a5f6938-7b33-4350-b8fa-cf78c5c44bcd
title: Exibindo páginas de propriedades de um filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0845a12b73363dc6ed93654439fd31826bf9cfc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370073"
---
# <a name="displaying-a-filters-property-pages"></a><span data-ttu-id="e31b7-103">Exibindo páginas de propriedades de um filtro</span><span class="sxs-lookup"><span data-stu-id="e31b7-103">Displaying a Filter's Property Pages</span></span>

<span data-ttu-id="e31b7-104">Uma página de propriedades é uma maneira de um filtro oferecer suporte a propriedades que o usuário pode definir.</span><span class="sxs-lookup"><span data-stu-id="e31b7-104">A property page is one way for a filter to support properties that the user can set.</span></span> <span data-ttu-id="e31b7-105">Este artigo descreve como exibir as páginas de propriedades de um filtro em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e31b7-105">This article describes how to display a filter's property pages in an application.</span></span> <span data-ttu-id="e31b7-106">Para obter mais informações sobre páginas de propriedades, consulte a documentação do Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="e31b7-106">For more information about property pages, see the Platform SDK documentation.</span></span>

> [!Note]  
> <span data-ttu-id="e31b7-107">Embora muitos dos filtros fornecidos com as páginas de propriedades de suporte do DirectShow, eles destinam-se a fins de depuração e não são recomendados para uso do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e31b7-107">Although many of the filters provided with DirectShow support property pages, they are intended for debugging purposes, and are not recommended for application use.</span></span> <span data-ttu-id="e31b7-108">Na maioria dos casos, a funcionalidade equivalente é fornecida por meio de uma interface personalizada no filtro.</span><span class="sxs-lookup"><span data-stu-id="e31b7-108">In most cases the equivalent functionality is provided through a custom interface on the filter.</span></span> <span data-ttu-id="e31b7-109">Um aplicativo deve controlar esses filtros programaticamente, em vez de expor suas páginas de propriedades aos usuários.</span><span class="sxs-lookup"><span data-stu-id="e31b7-109">An application should control these filters programmatically, rather than expose their property pages to users.</span></span>

 

<span data-ttu-id="e31b7-110">Filtros com páginas de propriedades expõem a interface **ISpecifyPropertyPages** .</span><span class="sxs-lookup"><span data-stu-id="e31b7-110">Filters with property pages expose the **ISpecifyPropertyPages** interface.</span></span> <span data-ttu-id="e31b7-111">Para determinar se um filtro define uma página de propriedades, consulte o filtro para essa interface usando **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="e31b7-111">To determine whether a filter defines a property page, query the filter for this interface using **QueryInterface**.</span></span>

<span data-ttu-id="e31b7-112">Se você criou diretamente uma instância de um filtro (chamando **CoCreateInstance**), você já tem um ponteiro para o filtro.</span><span class="sxs-lookup"><span data-stu-id="e31b7-112">If you directly created an instance of a filter (by calling **CoCreateInstance**), you already have a pointer to the filter.</span></span> <span data-ttu-id="e31b7-113">Caso contrário, você pode enumerar os filtros no grafo, usando o método [**IFilterGraph:: EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) .</span><span class="sxs-lookup"><span data-stu-id="e31b7-113">If not, you can enumerate the filters in the graph, using the [**IFilterGraph::EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) method.</span></span> <span data-ttu-id="e31b7-114">Para obter detalhes, consulte [Enumerando objetos em um grafo de filtro](enumerating-objects-in-a-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="e31b7-114">For details, see [Enumerating Objects in a Filter Graph](enumerating-objects-in-a-filter-graph.md).</span></span>

<span data-ttu-id="e31b7-115">Quando você tiver o ponteiro de interface **ISpecifyPropertyPages** , recupere as páginas de propriedades do filtro chamando o método **ISpecifyPropertyPages:: GetPages** .</span><span class="sxs-lookup"><span data-stu-id="e31b7-115">Once you have the **ISpecifyPropertyPages** interface pointer, retrieve the filter's property pages by calling the **ISpecifyPropertyPages::GetPages** method.</span></span> <span data-ttu-id="e31b7-116">Esse método preenche uma matriz contada de identificadores globalmente exclusivos (GUIDs) com o identificador de classe (CLSID) de cada página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="e31b7-116">This method fills a counted array of globally unique identifiers (GUIDs) with the class identifier (CLSID) of each property page.</span></span> <span data-ttu-id="e31b7-117">Uma matriz contada é definida por uma estrutura **CAUUID** , que você deve alocar, mas não precisa inicializar.</span><span class="sxs-lookup"><span data-stu-id="e31b7-117">A counted array is defined by a **CAUUID** structure, which you must allocate but do not have to initialize.</span></span> <span data-ttu-id="e31b7-118">O método **GetPages** aloca a matriz, que está contida no membro **PElems** da estrutura **CAUUID** .</span><span class="sxs-lookup"><span data-stu-id="e31b7-118">The **GetPages** method allocates the array, which is contained in the **pElems** member of the **CAUUID** structure.</span></span> <span data-ttu-id="e31b7-119">Quando terminar, libere a matriz chamando a função **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="e31b7-119">When you are done, free the array by calling the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="e31b7-120">A função **OleCreatePropertyFrame** fornece uma maneira simples de exibir as páginas de propriedades dentro de uma caixa de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="e31b7-120">The **OleCreatePropertyFrame** function provides a simple way to display the property pages inside a modal dialog box.</span></span>


```C++
IBaseFilter *pFilter;
/* Obtain the filter's IBaseFilter interface. (Not shown) */
ISpecifyPropertyPages *pProp;
HRESULT hr = pFilter->QueryInterface(IID_ISpecifyPropertyPages, (void **)&pProp);
if (SUCCEEDED(hr)) 
{
    // Get the filter's name and IUnknown pointer.
    FILTER_INFO FilterInfo;
    hr = pFilter->QueryFilterInfo(&FilterInfo); 
    IUnknown *pFilterUnk;
    pFilter->QueryInterface(IID_IUnknown, (void **)&pFilterUnk);

    // Show the page. 
    CAUUID caGUID;
    pProp->GetPages(&caGUID);
    pProp->Release();
    OleCreatePropertyFrame(
        hWnd,                   // Parent window
        0, 0,                   // Reserved
        FilterInfo.achName,     // Caption for the dialog box
        1,                      // Number of objects (just the filter)
        &pFilterUnk,            // Array of object pointers. 
        caGUID.cElems,          // Number of property pages
        caGUID.pElems,          // Array of property page CLSIDs
        0,                      // Locale identifier
        0, NULL                 // Reserved
    );

    // Clean up.
    pFilterUnk->Release();
    FilterInfo.pGraph->Release(); 
    CoTaskMemFree(caGUID.pElems);
}
```



## <a name="related-topics"></a><span data-ttu-id="e31b7-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e31b7-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e31b7-122">Tarefas básicas do DirectShow</span><span class="sxs-lookup"><span data-stu-id="e31b7-122">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 



