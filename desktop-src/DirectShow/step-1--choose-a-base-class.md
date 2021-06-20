---
description: Escolha uma classe base como parte da gravação de um filtro de transformação. Saiba quais classes são apropriadas para filtros de transformação.
ms.assetid: 4b2d3add-0430-480b-ad5f-bb1aa19fef21
title: Etapa 1. Escolher uma classe base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1a2bbf704bb2247034bc2ba3a6f35812f46aaaa
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406459"
---
# <a name="step-1-choose-a-base-class"></a><span data-ttu-id="11d10-105">Etapa 1.</span><span class="sxs-lookup"><span data-stu-id="11d10-105">Step 1.</span></span> <span data-ttu-id="11d10-106">Escolher uma classe base</span><span class="sxs-lookup"><span data-stu-id="11d10-106">Choose a Base Class</span></span>

<span data-ttu-id="11d10-107">Esta é a etapa 1 do tutorial [escrevendo filtros de transformação](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="11d10-107">This is step 1 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="11d10-108">Supondo que você decida escrever um filtro e não um DMO, a primeira etapa é escolher qual classe base usar.</span><span class="sxs-lookup"><span data-stu-id="11d10-108">Assuming that you decide to write a filter and not a DMO, the first step is choosing which base class to use.</span></span> <span data-ttu-id="11d10-109">As classes a seguir são apropriadas para filtros de transformação:</span><span class="sxs-lookup"><span data-stu-id="11d10-109">The following classes are appropriate for transform filters:</span></span>

-   <span data-ttu-id="11d10-110">O [**CTransformFilter**](ctransformfilter.md) foi projetado para filtros de transformação que usam buffers de entrada e saída separados.</span><span class="sxs-lookup"><span data-stu-id="11d10-110">[**CTransformFilter**](ctransformfilter.md) is designed for transform filters that use separate input and output buffers.</span></span> <span data-ttu-id="11d10-111">Esse tipo de filtro, às vezes, é chamado de filtro de cópia/transformação.</span><span class="sxs-lookup"><span data-stu-id="11d10-111">This kind of filter is sometimes called a copy-transform filter.</span></span> <span data-ttu-id="11d10-112">Quando um filtro de cópia/transformação recebe um exemplo de entrada, ele grava novos dados em um exemplo de saída e entrega o exemplo de saída para o próximo filtro.</span><span class="sxs-lookup"><span data-stu-id="11d10-112">When a copy-transform filter receives an input sample, it writes new data to an output sample and delivers the output sample to the next filter.</span></span>
-   <span data-ttu-id="11d10-113">O [**CTransInPlaceFilter**](ctransinplacefilter.md) é projetado para filtros que modificam dados no buffer original, também chamados de filtros de trans-in-Place.</span><span class="sxs-lookup"><span data-stu-id="11d10-113">[**CTransInPlaceFilter**](ctransinplacefilter.md) is designed for filters that modify data in the original buffer, also called trans-in-place filters.</span></span> <span data-ttu-id="11d10-114">Quando um filtro de trans-in-Place recebe um exemplo, ele altera os dados dentro desse exemplo e entrega o mesmo exemplo downstream.</span><span class="sxs-lookup"><span data-stu-id="11d10-114">When a trans-in-place filter receives a sample, it changes the data inside that sample and delivers the same sample downstream.</span></span> <span data-ttu-id="11d10-115">O PIN de entrada do filtro e o PIN de saída sempre se conectam com os tipos de mídia correspondentes.</span><span class="sxs-lookup"><span data-stu-id="11d10-115">The filter's input pin and output pin always connect with matching media types.</span></span>
-   <span data-ttu-id="11d10-116">O [**CVideoTransformFilter**](cvideotransformfilter.md) é projetado principalmente para decodificadores de vídeo.</span><span class="sxs-lookup"><span data-stu-id="11d10-116">[**CVideoTransformFilter**](cvideotransformfilter.md) is designed primarily for video decoders.</span></span> <span data-ttu-id="11d10-117">Ele deriva de **CTransformFilter**, mas inclui a funcionalidade para descartar quadros se o renderizador downstream estiver para trás.</span><span class="sxs-lookup"><span data-stu-id="11d10-117">It derives from **CTransformFilter**, but includes functionality for dropping frames if the downstream renderer falls behind.</span></span>
-   <span data-ttu-id="11d10-118">[**CBaseFilter**](cbasefilter.md) é uma classe de filtro genérica.</span><span class="sxs-lookup"><span data-stu-id="11d10-118">[**CBaseFilter**](cbasefilter.md) is a generic filter class.</span></span> <span data-ttu-id="11d10-119">Todas as outras classes nessa lista derivam de **CBaseFilter**.</span><span class="sxs-lookup"><span data-stu-id="11d10-119">The other classes in this list all derive from **CBaseFilter**.</span></span> <span data-ttu-id="11d10-120">Se nenhuma delas for adequada, você poderá fazer fallback nessa classe.</span><span class="sxs-lookup"><span data-stu-id="11d10-120">If none of them is suitable, you can fall back on this class.</span></span> <span data-ttu-id="11d10-121">No entanto, essa classe também requer a maioria dos trabalhos de sua parte.</span><span class="sxs-lookup"><span data-stu-id="11d10-121">However, this class also requires the most work on your part.</span></span>
-   <span data-ttu-id="11d10-122">\[! Fundamental\]</span><span class="sxs-lookup"><span data-stu-id="11d10-122">\[!Important\]</span></span>  
    > <span data-ttu-id="11d10-123">As transformações de vídeo in-loco podem ter um impacto sério no desempenho da renderização.</span><span class="sxs-lookup"><span data-stu-id="11d10-123">In-place video transforms can have a serious impact on rendering performance.</span></span> <span data-ttu-id="11d10-124">As transformações in-loco exigem operações de leitura/modificação/gravação no buffer.</span><span class="sxs-lookup"><span data-stu-id="11d10-124">In-place transforms require read-modify-write operations on the buffer.</span></span> <span data-ttu-id="11d10-125">Se a memória residir em uma placa gráfica, as operações de leitura serão significativamente mais lentas.</span><span class="sxs-lookup"><span data-stu-id="11d10-125">If the memory resides on a graphics card, read operations are significantly slower.</span></span> <span data-ttu-id="11d10-126">Além disso, até mesmo uma transformação de cópia poderá causar operações de leitura não intencionais se você não a implementar com cuidado.</span><span class="sxs-lookup"><span data-stu-id="11d10-126">Moreover, even a copy transform can cause unintended read operations if you do not implement it carefully.</span></span> <span data-ttu-id="11d10-127">Portanto, você deve sempre fazer testes de desempenho se escrever uma transformação de vídeo.</span><span class="sxs-lookup"><span data-stu-id="11d10-127">Therefore, you should always do performance testing if you write a video transform.</span></span>

     

<span data-ttu-id="11d10-128">Para o codificador RLE de exemplo, a melhor opção é **CTransformFilter** ou **CVideoTransformFilter**.</span><span class="sxs-lookup"><span data-stu-id="11d10-128">For the example RLE encoder, the best choice is either **CTransformFilter** or **CVideoTransformFilter**.</span></span> <span data-ttu-id="11d10-129">Na verdade, as diferenças entre eles são amplamente internas, portanto, é fácil converter de um para o outro.</span><span class="sxs-lookup"><span data-stu-id="11d10-129">In fact, the differences between them are largely internal, so it is easy to convert from one to the other.</span></span> <span data-ttu-id="11d10-130">Como os tipos de mídia devem ser diferentes nos dois Pins, a classe **CTransInPlaceFilter** não é apropriada para esse filtro.</span><span class="sxs-lookup"><span data-stu-id="11d10-130">Because the media types must be different on the two pins, the **CTransInPlaceFilter** class is not appropriate for this filter.</span></span> <span data-ttu-id="11d10-131">Este exemplo usará **CTransformFilter**.</span><span class="sxs-lookup"><span data-stu-id="11d10-131">This example will use **CTransformFilter**.</span></span>

<span data-ttu-id="11d10-132">Em seguida: [etapa 2. Declare a classe de filtro](step-2--declare-the-filter-class.md).</span><span class="sxs-lookup"><span data-stu-id="11d10-132">Next: [Step 2. Declare the Filter Class](step-2--declare-the-filter-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="11d10-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="11d10-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11d10-134">Gravando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="11d10-134">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



