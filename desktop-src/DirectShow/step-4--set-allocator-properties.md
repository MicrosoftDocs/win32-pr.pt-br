---
description: Etapa 4.
ms.assetid: c2fd6d8b-b239-45e4-9c02-41edafa58762
title: Etapa 4. Definir propriedades de alocador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32d5e3affba32b96dc93cb97e1886322bc6f2c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787132"
---
# <a name="step-4-set-allocator-properties"></a><span data-ttu-id="3f230-104">Etapa 4.</span><span class="sxs-lookup"><span data-stu-id="3f230-104">Step 4.</span></span> <span data-ttu-id="3f230-105">Definir propriedades de alocador</span><span class="sxs-lookup"><span data-stu-id="3f230-105">Set Allocator Properties</span></span>

<span data-ttu-id="3f230-106">Esta é a etapa 4 do tutorial [escrevendo filtros de transformação](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="3f230-106">This is step 4 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="3f230-107">Esta etapa não é necessária para filtros que derivam de **CTransInPlaceFilter**.</span><span class="sxs-lookup"><span data-stu-id="3f230-107">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="3f230-108">Depois que dois Pins concordam em um tipo de mídia, eles selecionam um alocador para a conexão e negociam as propriedades do alocador, como o tamanho do buffer e o número de buffers.</span><span class="sxs-lookup"><span data-stu-id="3f230-108">After two pins agree on a media type, they select an allocator for the connection and negotiate allocator properties, such as the buffer size and the number of buffers.</span></span>

<span data-ttu-id="3f230-109">Na classe **CTransformFilter** , há dois alocadores, um para a conexão de PIN upstream e outro para a conexão de PIN de downstream.</span><span class="sxs-lookup"><span data-stu-id="3f230-109">In the **CTransformFilter** class, there are two allocators, one for the upstream pin connection and one for the downstream pin connection.</span></span> <span data-ttu-id="3f230-110">O filtro upstream seleciona o alocador upstream e também escolhe as propriedades do alocador.</span><span class="sxs-lookup"><span data-stu-id="3f230-110">The upstream filter selects the upstream allocator and also chooses the allocator properties.</span></span> <span data-ttu-id="3f230-111">O PIN de entrada aceita tudo o que o filtro upstream decide.</span><span class="sxs-lookup"><span data-stu-id="3f230-111">The input pin accepts whatever the upstream filter decides.</span></span> <span data-ttu-id="3f230-112">Se você precisar modificar esse comportamento, substitua o método [**CBaseInputPin:: NotifyAllocator**](cbaseinputpin-notifyallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="3f230-112">If you need to modify this behavior, override the [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md) method.</span></span>

<span data-ttu-id="3f230-113">O pino de saída do filtro de transformação seleciona o alocador downstream.</span><span class="sxs-lookup"><span data-stu-id="3f230-113">The transform filter's output pin selects the downstream allocator.</span></span> <span data-ttu-id="3f230-114">Ele executa as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="3f230-114">It performs the following steps:</span></span>

1.  <span data-ttu-id="3f230-115">Se o filtro downstream puder fornecer um alocador, o PIN de saída usará aquele.</span><span class="sxs-lookup"><span data-stu-id="3f230-115">If the downstream filter can provide an allocator, the output pin uses that one.</span></span> <span data-ttu-id="3f230-116">Caso contrário, o pino de saída criará um novo alocador.</span><span class="sxs-lookup"><span data-stu-id="3f230-116">Otherwise, the output pin creates a new allocator.</span></span>
2.  <span data-ttu-id="3f230-117">O pino de saída Obtém os requisitos de alocador do filtro downstream (se houver) chamando [**IMemInputPin:: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).</span><span class="sxs-lookup"><span data-stu-id="3f230-117">The output pin gets the downstream filter's allocator requirements (if any) by calling [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).</span></span>
3.  <span data-ttu-id="3f230-118">O pino de saída chama o método [**CTransformFilter::D ecidebuffersize**](ctransformfilter-decidebuffersize.md) do filtro de transformação, que é virtual puro.</span><span class="sxs-lookup"><span data-stu-id="3f230-118">The output pin calls the transform filter's [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which is pure virtual.</span></span> <span data-ttu-id="3f230-119">Os parâmetros para esse método são um ponteiro para o alocador e uma estrutura de [**\_ Propriedades de alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) com os requisitos do filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="3f230-119">The parameters to this method are a pointer to the allocator and an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure with the downstream filter's requirements.</span></span> <span data-ttu-id="3f230-120">Se o filtro downstream não tiver requisitos de alocador, a estrutura será zerada.</span><span class="sxs-lookup"><span data-stu-id="3f230-120">If the downstream filter has no allocator requirements, the structure is zeroed out.</span></span>
4.  <span data-ttu-id="3f230-121">No método **DecideBufferSize** , a classe derivada define as propriedades do alocador chamando [**IMemAllocator:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).</span><span class="sxs-lookup"><span data-stu-id="3f230-121">In the **DecideBufferSize** method, the derived class sets the allocator properties by calling [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).</span></span>

<span data-ttu-id="3f230-122">Em geral, a classe derivada selecionará as propriedades do alocador com base no formato de saída, os requisitos do filtro downstream e os requisitos próprios do filtro.</span><span class="sxs-lookup"><span data-stu-id="3f230-122">Generally, the derived class will select allocator properties based on the output format, the downstream filter's requirements, and the filter's own requirements.</span></span> <span data-ttu-id="3f230-123">Tente selecionar as propriedades que são compatíveis com a solicitação do filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="3f230-123">Try to select properties that are compatible with the downstream filter's request.</span></span> <span data-ttu-id="3f230-124">Caso contrário, o filtro downstream poderá rejeitar a conexão.</span><span class="sxs-lookup"><span data-stu-id="3f230-124">Otherwise, the downstream filter might reject the connection.</span></span>

<span data-ttu-id="3f230-125">No exemplo a seguir, o codificador RLE define valores mínimos para o tamanho do buffer, o alinhamento do buffer e a contagem de buffers.</span><span class="sxs-lookup"><span data-stu-id="3f230-125">In the following example, the RLE encoder sets minimum values for the buffer size, buffer alignment, and buffer count.</span></span> <span data-ttu-id="3f230-126">Para o prefixo, ele usa qualquer valor que o filtro downstream solicitou.</span><span class="sxs-lookup"><span data-stu-id="3f230-126">For the prefix, it uses whatever value the downstream filter requested.</span></span> <span data-ttu-id="3f230-127">O prefixo geralmente é zero bytes, mas alguns filtros exigem isso.</span><span class="sxs-lookup"><span data-stu-id="3f230-127">The prefix is typically zero bytes, but some filters require it.</span></span> <span data-ttu-id="3f230-128">Por exemplo, o filtro [AVI Mux](avi-mux-filter.md) usa o prefixo para gravar cabeçalhos riff.</span><span class="sxs-lookup"><span data-stu-id="3f230-128">For example, the [AVI Mux](avi-mux-filter.md) filter uses the prefix to write RIFF headers.</span></span>


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



<span data-ttu-id="3f230-129">O alocador pode não ser capaz de corresponder exatamente à sua solicitação.</span><span class="sxs-lookup"><span data-stu-id="3f230-129">The allocator may not be able to match your request exactly.</span></span> <span data-ttu-id="3f230-130">Portanto, o método **SetProperties** retorna o resultado real em uma estrutura **de \_ Propriedades de alocador** separada (o parâmetro *real* , no exemplo anterior).</span><span class="sxs-lookup"><span data-stu-id="3f230-130">Therefore, the **SetProperties** method returns the actual result in a separate **ALLOCATOR\_PROPERTIES** structure (the *Actual* parameter, in the previous example).</span></span> <span data-ttu-id="3f230-131">Mesmo quando **SetProperties** é executado com sucesso, você deve verificar o resultado para garantir que eles atendam aos requisitos mínimos do seu filtro.</span><span class="sxs-lookup"><span data-stu-id="3f230-131">Even when **SetProperties** succeeds, you should check the result to make sure they meet your filter's minimum requirements.</span></span>

<span data-ttu-id="3f230-132">**Alocadores personalizados**</span><span class="sxs-lookup"><span data-stu-id="3f230-132">**Custom Allocators**</span></span>

<span data-ttu-id="3f230-133">Por padrão, todas as classes de filtro usam a classe [**CMemAllocator**](cmemallocator.md) para seus alocadores.</span><span class="sxs-lookup"><span data-stu-id="3f230-133">By default, all of the filter classes use the [**CMemAllocator**](cmemallocator.md) class for their allocators.</span></span> <span data-ttu-id="3f230-134">Essa classe aloca memória do espaço de endereço virtual do processo do cliente (usando o **VirtualAlloc**).</span><span class="sxs-lookup"><span data-stu-id="3f230-134">This class allocates memory from the virtual address space of the client process (using **VirtualAlloc**).</span></span> <span data-ttu-id="3f230-135">Se o filtro precisar usar algum outro tipo de memória, como as superfícies do DirectDraw, você poderá implementar um alocador personalizado.</span><span class="sxs-lookup"><span data-stu-id="3f230-135">If your filter needs to use some other kind of memory, such as DirectDraw surfaces, you can implement a custom allocator.</span></span> <span data-ttu-id="3f230-136">Você pode usar a classe [**CBaseAllocator**](cbaseallocator.md) ou escrever uma classe de alocador totalmente nova.</span><span class="sxs-lookup"><span data-stu-id="3f230-136">You can use the [**CBaseAllocator**](cbaseallocator.md) class or write an entirely new allocator class.</span></span> <span data-ttu-id="3f230-137">Se o filtro tiver um alocador personalizado, substitua os seguintes métodos, dependendo de qual PIN usa o alocador:</span><span class="sxs-lookup"><span data-stu-id="3f230-137">If your filter has a custom allocator, override the following methods, depending on which pin uses the allocator:</span></span>

-   <span data-ttu-id="3f230-138">Pino de entrada: [**CBaseInputPin:: Getalocator**](cbaseinputpin-getallocator.md) e [**CBaseInputPin:: NotifyAllocator**](cbaseinputpin-notifyallocator.md).</span><span class="sxs-lookup"><span data-stu-id="3f230-138">Input pin: [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) and [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md).</span></span>
-   <span data-ttu-id="3f230-139">Pino de saída: [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md).</span><span class="sxs-lookup"><span data-stu-id="3f230-139">Output pin: [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md).</span></span>

<span data-ttu-id="3f230-140">Se o outro filtro se recusar a se conectar usando seu alocador personalizado, o filtro poderá falhar na conexão ou conectar-se com o alocador do outro filtro.</span><span class="sxs-lookup"><span data-stu-id="3f230-140">If the other filter refuses to connect using your custom allocator, your filter can either fail the connection, or else connect with the other filter's allocator.</span></span> <span data-ttu-id="3f230-141">No último caso, talvez seja necessário definir um sinalizador interno que indique o tipo de alocador.</span><span class="sxs-lookup"><span data-stu-id="3f230-141">In the latter case, you might need to set an internal flag indicating the type of allocator.</span></span> <span data-ttu-id="3f230-142">Para obter um exemplo dessa abordagem, consulte [**classe CDrawImage**](cdrawimage.md).</span><span class="sxs-lookup"><span data-stu-id="3f230-142">For an example of this approach, see [**CDrawImage Class**](cdrawimage.md).</span></span>

<span data-ttu-id="3f230-143">Em seguida: [etapa 5. Transforme a imagem](step-5--transform-the-image.md).</span><span class="sxs-lookup"><span data-stu-id="3f230-143">Next: [Step 5. Transform the Image](step-5--transform-the-image.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f230-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3f230-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f230-145">Gravando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="3f230-145">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



