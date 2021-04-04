---
description: Declarando informações de filtro
ms.assetid: ed3c1d44-ccef-4dde-819b-f5d4d3be6d1e
title: Declarando informações de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8975217f1b7746b26dc5dd16ce9f4e7f694f44bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646127"
---
# <a name="declaring-filter-information"></a><span data-ttu-id="7c870-103">Declarando informações de filtro</span><span class="sxs-lookup"><span data-stu-id="7c870-103">Declaring Filter Information</span></span>

<span data-ttu-id="7c870-104">A primeira etapa é declarar as informações de filtro, se necessário.</span><span class="sxs-lookup"><span data-stu-id="7c870-104">The first step is to declare the filter information, if needed.</span></span> <span data-ttu-id="7c870-105">O DirectShow define as seguintes estruturas para descrever filtros, pins e tipos de mídia:</span><span class="sxs-lookup"><span data-stu-id="7c870-105">DirectShow defines the following structures for describing filters, pins, and media types:</span></span>



| <span data-ttu-id="7c870-106">Estrutura</span><span class="sxs-lookup"><span data-stu-id="7c870-106">Structure</span></span>                                               | <span data-ttu-id="7c870-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7c870-107">Description</span></span>             |
|---------------------------------------------------------|-------------------------|
| [<span data-ttu-id="7c870-108">**filtro de AMOVIESETUP \_**</span><span class="sxs-lookup"><span data-stu-id="7c870-108">**AMOVIESETUP\_FILTER**</span></span>](amoviesetup-filter.md)       | <span data-ttu-id="7c870-109">Descreve um filtro.</span><span class="sxs-lookup"><span data-stu-id="7c870-109">Describes a filter.</span></span>     |
| [<span data-ttu-id="7c870-110">**AMOVIESETUP \_ PIN**</span><span class="sxs-lookup"><span data-stu-id="7c870-110">**AMOVIESETUP\_PIN**</span></span>](amoviesetup-pin.md)             | <span data-ttu-id="7c870-111">Descreve um PIN.</span><span class="sxs-lookup"><span data-stu-id="7c870-111">Describes a pin.</span></span>        |
| [<span data-ttu-id="7c870-112">**\_MediaType AMOVIESETUP**</span><span class="sxs-lookup"><span data-stu-id="7c870-112">**AMOVIESETUP\_MEDIATYPE**</span></span>](amoviesetup-mediatype.md) | <span data-ttu-id="7c870-113">Descreve um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="7c870-113">Describes a media type.</span></span> |



 

<span data-ttu-id="7c870-114">Essas estruturas são aninhadas.</span><span class="sxs-lookup"><span data-stu-id="7c870-114">These structures are nested.</span></span> <span data-ttu-id="7c870-115">A estrutura do **\_ filtro AMOVEIESETUP** tem um ponteiro para uma matriz de estruturas de **\_ PIN AMOVIESETUP** , e cada uma delas tem um ponteiro para uma matriz de estruturas **AMOVEIESETUP \_ MediaType** .</span><span class="sxs-lookup"><span data-stu-id="7c870-115">The **AMOVEIESETUP\_FILTER** structure has a pointer to an array of **AMOVIESETUP\_PIN** structures, and each of these has a pointer to an array of **AMOVEIESETUP\_MEDIATYPE** structures.</span></span> <span data-ttu-id="7c870-116">Juntas, essas estruturas fornecem informações suficientes para a interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) localizar um filtro.</span><span class="sxs-lookup"><span data-stu-id="7c870-116">Taken together, these structures provide enough information for the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface to locate a filter.</span></span> <span data-ttu-id="7c870-117">Elas não são uma descrição completa de um filtro.</span><span class="sxs-lookup"><span data-stu-id="7c870-117">They are not a complete description of a filter.</span></span> <span data-ttu-id="7c870-118">Por exemplo, se o filtro criar várias instâncias do mesmo PIN, você deverá declarar apenas uma estrutura [**de \_ PIN AMOVIESETUP**](amoviesetup-pin.md) para esse PIN.</span><span class="sxs-lookup"><span data-stu-id="7c870-118">For example, if the filter creates multiple instances of the same pin, you should declare only one [**AMOVIESETUP\_PIN**](amoviesetup-pin.md) structure for that pin.</span></span> <span data-ttu-id="7c870-119">Além disso, um filtro não é necessário para dar suporte a todas as combinações de tipos de mídia que ele registra; Nem é necessário registrar todos os tipos de mídia aos quais ele dá suporte.</span><span class="sxs-lookup"><span data-stu-id="7c870-119">Also, a filter is not required to support every combination of media types that it registers; nor is required to register every media type that it supports.</span></span>

<span data-ttu-id="7c870-120">Declare as estruturas de configuração como variáveis globais dentro de sua DLL.</span><span class="sxs-lookup"><span data-stu-id="7c870-120">Declare the set-up structures as global variables within your DLL.</span></span> <span data-ttu-id="7c870-121">O exemplo a seguir mostra um filtro com um pino de saída:</span><span class="sxs-lookup"><span data-stu-id="7c870-121">The following example shows a filter with one output pin:</span></span>


```C++
static const WCHAR g_wszName[] = L"Some Filter";

AMOVIESETUP_MEDIATYPE sudMediaTypes[] = {
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB24 },
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB32 },
};

AMOVIESETUP_PIN sudOutputPin = {
    L"",            // Obsolete, not used.
    FALSE,          // Is this pin rendered?
    TRUE,           // Is it an output pin?
    FALSE,          // Can the filter create zero instances?
    FALSE,          // Does the filter create multiple instances?
    &GUID_NULL,     // Obsolete.
    NULL,           // Obsolete.
    2,              // Number of media types.
    sudMediaTypes   // Pointer to media types.
};

AMOVIESETUP_FILTER sudFilterReg = {
    &CLSID_SomeFilter,      // Filter CLSID.
    g_wszName,              // Filter name.
    MERIT_NORMAL,           // Merit.
    1,                      // Number of pin types.
    &sudOutputPin           // Pointer to pin information.
};
```



<span data-ttu-id="7c870-122">O nome do filtro é declarado como uma variável global estática, pois ele será usado novamente em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="7c870-122">The filter name is declared as a static global variable, because it will be used again elsewhere.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c870-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7c870-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c870-124">Como registrar filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="7c870-124">How to Register DirectShow Filters</span></span>](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



