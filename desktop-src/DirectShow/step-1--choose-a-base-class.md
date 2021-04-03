---
description: Etapa 1.
ms.assetid: 4b2d3add-0430-480b-ad5f-bb1aa19fef21
title: Etapa 1. Escolher uma classe base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4679873e78e75b350335b5294db63579fd41f36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829068"
---
# <a name="step-1-choose-a-base-class"></a><span data-ttu-id="70aca-104">Etapa 1.</span><span class="sxs-lookup"><span data-stu-id="70aca-104">Step 1.</span></span> <span data-ttu-id="70aca-105">Escolher uma classe base</span><span class="sxs-lookup"><span data-stu-id="70aca-105">Choose a Base Class</span></span>

<span data-ttu-id="70aca-106">Esta é a etapa 1 do tutorial [escrevendo filtros de transformação](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="70aca-106">This is step 1 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="70aca-107">Supondo que você decida escrever um filtro e não um DMO, a primeira etapa é escolher qual classe base usar.</span><span class="sxs-lookup"><span data-stu-id="70aca-107">Assuming that you decide to write a filter and not a DMO, the first step is choosing which base class to use.</span></span> <span data-ttu-id="70aca-108">As classes a seguir são apropriadas para filtros de transformação:</span><span class="sxs-lookup"><span data-stu-id="70aca-108">The following classes are appropriate for transform filters:</span></span>

-   <span data-ttu-id="70aca-109">O [**CTransformFilter**](ctransformfilter.md) foi projetado para filtros de transformação que usam buffers de entrada e saída separados.</span><span class="sxs-lookup"><span data-stu-id="70aca-109">[**CTransformFilter**](ctransformfilter.md) is designed for transform filters that use separate input and output buffers.</span></span> <span data-ttu-id="70aca-110">Esse tipo de filtro, às vezes, é chamado de filtro de cópia/transformação.</span><span class="sxs-lookup"><span data-stu-id="70aca-110">This kind of filter is sometimes called a copy-transform filter.</span></span> <span data-ttu-id="70aca-111">Quando um filtro de cópia/transformação recebe um exemplo de entrada, ele grava novos dados em um exemplo de saída e entrega o exemplo de saída para o próximo filtro.</span><span class="sxs-lookup"><span data-stu-id="70aca-111">When a copy-transform filter receives an input sample, it writes new data to an output sample and delivers the output sample to the next filter.</span></span>
-   <span data-ttu-id="70aca-112">O [**CTransInPlaceFilter**](ctransinplacefilter.md) é projetado para filtros que modificam dados no buffer original, também chamados de filtros de trans-in-Place.</span><span class="sxs-lookup"><span data-stu-id="70aca-112">[**CTransInPlaceFilter**](ctransinplacefilter.md) is designed for filters that modify data in the original buffer, also called trans-in-place filters.</span></span> <span data-ttu-id="70aca-113">Quando um filtro de trans-in-Place recebe um exemplo, ele altera os dados dentro desse exemplo e entrega o mesmo exemplo downstream.</span><span class="sxs-lookup"><span data-stu-id="70aca-113">When a trans-in-place filter receives a sample, it changes the data inside that sample and delivers the same sample downstream.</span></span> <span data-ttu-id="70aca-114">O PIN de entrada do filtro e o PIN de saída sempre se conectam com os tipos de mídia correspondentes.</span><span class="sxs-lookup"><span data-stu-id="70aca-114">The filter's input pin and output pin always connect with matching media types.</span></span>
-   <span data-ttu-id="70aca-115">O [**CVideoTransformFilter**](cvideotransformfilter.md) é projetado principalmente para decodificadores de vídeo.</span><span class="sxs-lookup"><span data-stu-id="70aca-115">[**CVideoTransformFilter**](cvideotransformfilter.md) is designed primarily for video decoders.</span></span> <span data-ttu-id="70aca-116">Ele deriva de **CTransformFilter**, mas inclui a funcionalidade para descartar quadros se o renderizador downstream estiver para trás.</span><span class="sxs-lookup"><span data-stu-id="70aca-116">It derives from **CTransformFilter**, but includes functionality for dropping frames if the downstream renderer falls behind.</span></span>
-   <span data-ttu-id="70aca-117">[**CBaseFilter**](cbasefilter.md) é uma classe de filtro genérica.</span><span class="sxs-lookup"><span data-stu-id="70aca-117">[**CBaseFilter**](cbasefilter.md) is a generic filter class.</span></span> <span data-ttu-id="70aca-118">Todas as outras classes nessa lista derivam de **CBaseFilter**.</span><span class="sxs-lookup"><span data-stu-id="70aca-118">The other classes in this list all derive from **CBaseFilter**.</span></span> <span data-ttu-id="70aca-119">Se nenhuma delas for adequada, você poderá fazer fallback nessa classe.</span><span class="sxs-lookup"><span data-stu-id="70aca-119">If none of them is suitable, you can fall back on this class.</span></span> <span data-ttu-id="70aca-120">No entanto, essa classe também requer a maioria dos trabalhos de sua parte.</span><span class="sxs-lookup"><span data-stu-id="70aca-120">However, this class also requires the most work on your part.</span></span>
-   <span data-ttu-id="70aca-121">\[! Fundamental\]</span><span class="sxs-lookup"><span data-stu-id="70aca-121">\[!Important\]</span></span>  
    > <span data-ttu-id="70aca-122">As transformações de vídeo in-loco podem ter um impacto sério no desempenho da renderização.</span><span class="sxs-lookup"><span data-stu-id="70aca-122">In-place video transforms can have a serious impact on rendering performance.</span></span> <span data-ttu-id="70aca-123">As transformações in-loco exigem operações de leitura/modificação/gravação no buffer.</span><span class="sxs-lookup"><span data-stu-id="70aca-123">In-place transforms require read-modify-write operations on the buffer.</span></span> <span data-ttu-id="70aca-124">Se a memória residir em uma placa gráfica, as operações de leitura serão significativamente mais lentas.</span><span class="sxs-lookup"><span data-stu-id="70aca-124">If the memory resides on a graphics card, read operations are significantly slower.</span></span> <span data-ttu-id="70aca-125">Além disso, até mesmo uma transformação de cópia poderá causar operações de leitura não intencionais se você não a implementar com cuidado.</span><span class="sxs-lookup"><span data-stu-id="70aca-125">Moreover, even a copy transform can cause unintended read operations if you do not implement it carefully.</span></span> <span data-ttu-id="70aca-126">Portanto, você deve sempre fazer testes de desempenho se escrever uma transformação de vídeo.</span><span class="sxs-lookup"><span data-stu-id="70aca-126">Therefore, you should always do performance testing if you write a video transform.</span></span>

     

<span data-ttu-id="70aca-127">Para o codificador RLE de exemplo, a melhor opção é **CTransformFilter** ou **CVideoTransformFilter**.</span><span class="sxs-lookup"><span data-stu-id="70aca-127">For the example RLE encoder, the best choice is either **CTransformFilter** or **CVideoTransformFilter**.</span></span> <span data-ttu-id="70aca-128">Na verdade, as diferenças entre eles são amplamente internas, portanto, é fácil converter de um para o outro.</span><span class="sxs-lookup"><span data-stu-id="70aca-128">In fact, the differences between them are largely internal, so it is easy to convert from one to the other.</span></span> <span data-ttu-id="70aca-129">Como os tipos de mídia devem ser diferentes nos dois Pins, a classe **CTransInPlaceFilter** não é apropriada para esse filtro.</span><span class="sxs-lookup"><span data-stu-id="70aca-129">Because the media types must be different on the two pins, the **CTransInPlaceFilter** class is not appropriate for this filter.</span></span> <span data-ttu-id="70aca-130">Este exemplo usará **CTransformFilter**.</span><span class="sxs-lookup"><span data-stu-id="70aca-130">This example will use **CTransformFilter**.</span></span>

<span data-ttu-id="70aca-131">Em seguida: [etapa 2. Declare a classe de filtro](step-2--declare-the-filter-class.md).</span><span class="sxs-lookup"><span data-stu-id="70aca-131">Next: [Step 2. Declare the Filter Class](step-2--declare-the-filter-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="70aca-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="70aca-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70aca-133">Gravando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="70aca-133">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



