---
description: Definir propriedades do alocador como parte da escrita de um filtro de transformação. O pino de saída do filtro de transformação seleciona o alocador downstream.
ms.assetid: c2fd6d8b-b239-45e4-9c02-41edafa58762
title: Etapa 4. Definir propriedades do alocador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ee7d9ecdc85b63ec6bd774a3a47e0e9399dcf3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406819"
---
# <a name="step-4-set-allocator-properties"></a><span data-ttu-id="ca607-105">Etapa 4.</span><span class="sxs-lookup"><span data-stu-id="ca607-105">Step 4.</span></span> <span data-ttu-id="ca607-106">Definir propriedades do alocador</span><span class="sxs-lookup"><span data-stu-id="ca607-106">Set Allocator Properties</span></span>

<span data-ttu-id="ca607-107">Esta é a etapa 4 do tutorial Escrevendo [filtros de transformação.](writing-transform-filters.md)</span><span class="sxs-lookup"><span data-stu-id="ca607-107">This is step 4 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="ca607-108">Esta etapa não é necessária para filtros que derivam de **CTransInPlaceFilter.**</span><span class="sxs-lookup"><span data-stu-id="ca607-108">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="ca607-109">Depois que dois pinos concordarem com um tipo de mídia, eles selecionarão um alocador para a conexão e negociarão as propriedades do alocador, como o tamanho do buffer e o número de buffers.</span><span class="sxs-lookup"><span data-stu-id="ca607-109">After two pins agree on a media type, they select an allocator for the connection and negotiate allocator properties, such as the buffer size and the number of buffers.</span></span>

<span data-ttu-id="ca607-110">Na classe **CTransformFilter,** há dois alocadores, um para a conexão de pino upstream e outro para a conexão de pino downstream.</span><span class="sxs-lookup"><span data-stu-id="ca607-110">In the **CTransformFilter** class, there are two allocators, one for the upstream pin connection and one for the downstream pin connection.</span></span> <span data-ttu-id="ca607-111">O filtro upstream seleciona o alocador upstream e também escolhe as propriedades do alocador.</span><span class="sxs-lookup"><span data-stu-id="ca607-111">The upstream filter selects the upstream allocator and also chooses the allocator properties.</span></span> <span data-ttu-id="ca607-112">O pino de entrada aceita qualquer decisão do filtro upstream.</span><span class="sxs-lookup"><span data-stu-id="ca607-112">The input pin accepts whatever the upstream filter decides.</span></span> <span data-ttu-id="ca607-113">Se você precisar modificar esse comportamento, substitua o [**método CBaseInputPin::NotifyAllocator.**](cbaseinputpin-notifyallocator.md)</span><span class="sxs-lookup"><span data-stu-id="ca607-113">If you need to modify this behavior, override the [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md) method.</span></span>

<span data-ttu-id="ca607-114">O pino de saída do filtro de transformação seleciona o alocador downstream.</span><span class="sxs-lookup"><span data-stu-id="ca607-114">The transform filter's output pin selects the downstream allocator.</span></span> <span data-ttu-id="ca607-115">Ele executa as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="ca607-115">It performs the following steps:</span></span>

1.  <span data-ttu-id="ca607-116">Se o filtro downstream puder fornecer um alocador, o pino de saída usará esse.</span><span class="sxs-lookup"><span data-stu-id="ca607-116">If the downstream filter can provide an allocator, the output pin uses that one.</span></span> <span data-ttu-id="ca607-117">Caso contrário, o pino de saída criará um novo alocador.</span><span class="sxs-lookup"><span data-stu-id="ca607-117">Otherwise, the output pin creates a new allocator.</span></span>
2.  <span data-ttu-id="ca607-118">O pino de saída obtém os requisitos de alocador do filtro downstream (se algum) chamando [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).</span><span class="sxs-lookup"><span data-stu-id="ca607-118">The output pin gets the downstream filter's allocator requirements (if any) by calling [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).</span></span>
3.  <span data-ttu-id="ca607-119">O pino de saída chama o método [**CTransformFilter::D eformBufferSize**](ctransformfilter-decidebuffersize.md) do filtro de transformação, que é virtual puro.</span><span class="sxs-lookup"><span data-stu-id="ca607-119">The output pin calls the transform filter's [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which is pure virtual.</span></span> <span data-ttu-id="ca607-120">Os parâmetros para esse método são um ponteiro para o alocador e uma estrutura [**ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) com os requisitos do filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="ca607-120">The parameters to this method are a pointer to the allocator and an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure with the downstream filter's requirements.</span></span> <span data-ttu-id="ca607-121">Se o filtro downstream não tiver requisitos de alocador, a estrutura será zerada.</span><span class="sxs-lookup"><span data-stu-id="ca607-121">If the downstream filter has no allocator requirements, the structure is zeroed out.</span></span>
4.  <span data-ttu-id="ca607-122">No método **DecideBufferSize,** a classe derivada define as propriedades do alocador chamando [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).</span><span class="sxs-lookup"><span data-stu-id="ca607-122">In the **DecideBufferSize** method, the derived class sets the allocator properties by calling [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).</span></span>

<span data-ttu-id="ca607-123">Em geral, a classe derivada selecionará as propriedades do alocador com base no formato de saída, nos requisitos do filtro downstream e nos próprios requisitos do filtro.</span><span class="sxs-lookup"><span data-stu-id="ca607-123">Generally, the derived class will select allocator properties based on the output format, the downstream filter's requirements, and the filter's own requirements.</span></span> <span data-ttu-id="ca607-124">Tente selecionar propriedades compatíveis com a solicitação do filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="ca607-124">Try to select properties that are compatible with the downstream filter's request.</span></span> <span data-ttu-id="ca607-125">Caso contrário, o filtro downstream poderá rejeitar a conexão.</span><span class="sxs-lookup"><span data-stu-id="ca607-125">Otherwise, the downstream filter might reject the connection.</span></span>

<span data-ttu-id="ca607-126">No exemplo a seguir, o codificador RLE define valores mínimos para o tamanho do buffer, o alinhamento do buffer e a contagem de buffers.</span><span class="sxs-lookup"><span data-stu-id="ca607-126">In the following example, the RLE encoder sets minimum values for the buffer size, buffer alignment, and buffer count.</span></span> <span data-ttu-id="ca607-127">Para o prefixo, ele usa qualquer valor que o filtro downstream solicitou.</span><span class="sxs-lookup"><span data-stu-id="ca607-127">For the prefix, it uses whatever value the downstream filter requested.</span></span> <span data-ttu-id="ca607-128">O prefixo normalmente é zero bytes, mas alguns filtros o exigem.</span><span class="sxs-lookup"><span data-stu-id="ca607-128">The prefix is typically zero bytes, but some filters require it.</span></span> <span data-ttu-id="ca607-129">Por exemplo, o [filtro AVI Mux](avi-mux-filter.md) usa o prefixo para gravar os títulos DEIS.</span><span class="sxs-lookup"><span data-stu-id="ca607-129">For example, the [AVI Mux](avi-mux-filter.md) filter uses the prefix to write RIFF headers.</span></span>


```C++
HRESULT CRleFilter::DecideBufferSize(
    IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp)
{
    AM_MEDIA_TYPE mt;
    HRESULT hr = m_pOutput->ConnectionMediaType(&mt);
    if (FAILED(hr))
    {
        return hr;
    }

    ASSERT(mt.formattype == FORMAT_VideoInfo);
    BITMAPINFOHEADER *pbmi = HEADER(mt.pbFormat);
    pProp->cbBuffer = DIBSIZE(*pbmi) * 2; 
    if (pProp->cbAlign == 0)
    {
        pProp->cbAlign = 1;
    }
    if (pProp->cBuffers == 0)
    {
        pProp->cBuffers = 1;
    }
    // Release the format block.
    FreeMediaType(mt);

    // Set allocator properties.
    ALLOCATOR_PROPERTIES Actual;
    hr = pAlloc->SetProperties(pProp, &Actual);
    if (FAILED(hr)) 
    {
        return hr;
    }
    // Even when it succeeds, check the actual result.
    if (pProp->cbBuffer > Actual.cbBuffer) 
    {
        return E_FAIL;
    }
    return S_OK;
}
```



<span data-ttu-id="ca607-130">O alocador pode não ser capaz de corresponder exatamente à sua solicitação.</span><span class="sxs-lookup"><span data-stu-id="ca607-130">The allocator may not be able to match your request exactly.</span></span> <span data-ttu-id="ca607-131">Portanto, o **método SetProperties** retorna o resultado real em uma estrutura **ALLOCATOR \_ PROPERTIES** separada (o parâmetro *Real,* no exemplo anterior).</span><span class="sxs-lookup"><span data-stu-id="ca607-131">Therefore, the **SetProperties** method returns the actual result in a separate **ALLOCATOR\_PROPERTIES** structure (the *Actual* parameter, in the previous example).</span></span> <span data-ttu-id="ca607-132">Mesmo quando **SetProperties for** bem-sucedido, você deverá verificar o resultado para garantir que eles atendem aos requisitos mínimos do filtro.</span><span class="sxs-lookup"><span data-stu-id="ca607-132">Even when **SetProperties** succeeds, you should check the result to make sure they meet your filter's minimum requirements.</span></span>

<span data-ttu-id="ca607-133">**Alocadores personalizados**</span><span class="sxs-lookup"><span data-stu-id="ca607-133">**Custom Allocators**</span></span>

<span data-ttu-id="ca607-134">Por padrão, todas as classes de filtro usam a [**classe CMemAllocator**](cmemallocator.md) para seus alocadores.</span><span class="sxs-lookup"><span data-stu-id="ca607-134">By default, all of the filter classes use the [**CMemAllocator**](cmemallocator.md) class for their allocators.</span></span> <span data-ttu-id="ca607-135">Essa classe aloca memória do espaço de endereço virtual do processo do cliente (usando **VirtualAlloc**).</span><span class="sxs-lookup"><span data-stu-id="ca607-135">This class allocates memory from the virtual address space of the client process (using **VirtualAlloc**).</span></span> <span data-ttu-id="ca607-136">Se o filtro precisar usar algum outro tipo de memória, como superfícies directDraw, você poderá implementar um alocador personalizado.</span><span class="sxs-lookup"><span data-stu-id="ca607-136">If your filter needs to use some other kind of memory, such as DirectDraw surfaces, you can implement a custom allocator.</span></span> <span data-ttu-id="ca607-137">Você pode usar a [**classe CBaseAllocator**](cbaseallocator.md) ou escrever uma classe de alocador totalmente nova.</span><span class="sxs-lookup"><span data-stu-id="ca607-137">You can use the [**CBaseAllocator**](cbaseallocator.md) class or write an entirely new allocator class.</span></span> <span data-ttu-id="ca607-138">Se o filtro tiver um alocador personalizado, substitua os seguintes métodos, dependendo de qual pino usa o alocador:</span><span class="sxs-lookup"><span data-stu-id="ca607-138">If your filter has a custom allocator, override the following methods, depending on which pin uses the allocator:</span></span>

-   <span data-ttu-id="ca607-139">Pino de entrada: [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) e [**CBaseInputPin::NotifyAllocator.**](cbaseinputpin-notifyallocator.md)</span><span class="sxs-lookup"><span data-stu-id="ca607-139">Input pin: [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) and [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md).</span></span>
-   <span data-ttu-id="ca607-140">Pino de saída: [**CBaseOutputPin::D eputaçãoAllocator**](cbaseoutputpin-decideallocator.md).</span><span class="sxs-lookup"><span data-stu-id="ca607-140">Output pin: [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md).</span></span>

<span data-ttu-id="ca607-141">Se o outro filtro se recusar a se conectar usando seu alocador personalizado, o filtro poderá falhar na conexão ou conectar-se ao alocador do outro filtro.</span><span class="sxs-lookup"><span data-stu-id="ca607-141">If the other filter refuses to connect using your custom allocator, your filter can either fail the connection, or else connect with the other filter's allocator.</span></span> <span data-ttu-id="ca607-142">No último caso, talvez seja necessário definir um sinalizador interno indicando o tipo de alocador.</span><span class="sxs-lookup"><span data-stu-id="ca607-142">In the latter case, you might need to set an internal flag indicating the type of allocator.</span></span> <span data-ttu-id="ca607-143">Para ver um exemplo dessa abordagem, consulte [**Classe CDrawImage**](cdrawimage.md).</span><span class="sxs-lookup"><span data-stu-id="ca607-143">For an example of this approach, see [**CDrawImage Class**](cdrawimage.md).</span></span>

<span data-ttu-id="ca607-144">Próximo: [Etapa 5. Transforme a Imagem](step-5--transform-the-image.md).</span><span class="sxs-lookup"><span data-stu-id="ca607-144">Next: [Step 5. Transform the Image](step-5--transform-the-image.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca607-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ca607-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca607-146">Escrevendo filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="ca607-146">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



