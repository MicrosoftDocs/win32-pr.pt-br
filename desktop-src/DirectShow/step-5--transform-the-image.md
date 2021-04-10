---
description: Etapa 5.
ms.assetid: b7d878ab-523f-4b52-b98d-c9d4fa18ce8a
title: Etapa 5. Transformar a imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 609acb626d00dbceea8b6f5bca6af012d8158b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170968"
---
# <a name="step-5-transform-the-image"></a><span data-ttu-id="12336-104">Etapa 5.</span><span class="sxs-lookup"><span data-stu-id="12336-104">Step 5.</span></span> <span data-ttu-id="12336-105">Transformar a imagem</span><span class="sxs-lookup"><span data-stu-id="12336-105">Transform the Image</span></span>

<span data-ttu-id="12336-106">Esta é a etapa 5 do tutorial [escrevendo filtros de transformação](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="12336-106">This is step 5 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="12336-107">O filtro upstream fornece amostras de mídia para o filtro de transformação chamando o método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) no pino de entrada do filtro de transformação.</span><span class="sxs-lookup"><span data-stu-id="12336-107">The upstream filter delivers media samples to the transform filter by calling the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the transform filter's input pin.</span></span> <span data-ttu-id="12336-108">Para processar os dados, o filtro de transformação chama o método **Transform** , que é virtual puro.</span><span class="sxs-lookup"><span data-stu-id="12336-108">To process the data, the transform filter calls the **Transform** method, which is pure virtual.</span></span> <span data-ttu-id="12336-109">As classes **CTransformFilter** e **CTransInPlaceFilter** usam duas versões diferentes desse método:</span><span class="sxs-lookup"><span data-stu-id="12336-109">The **CTransformFilter** and **CTransInPlaceFilter** classes use two different versions of this method:</span></span>

-   <span data-ttu-id="12336-110">[**CTransformFilter:: Transform**](ctransformfilter-transform.md) usa um ponteiro para o exemplo de entrada e um ponteiro para o exemplo de saída.</span><span class="sxs-lookup"><span data-stu-id="12336-110">[**CTransformFilter::Transform**](ctransformfilter-transform.md) takes a pointer to the input sample and a pointer to the output sample.</span></span> <span data-ttu-id="12336-111">Antes que o filtro chame o método, ele copia as propriedades de exemplo do exemplo de entrada para o exemplo de saída, incluindo os carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="12336-111">Before the filter calls the method, it copies the sample properties from the input sample to the output sample, including the time stamps.</span></span>
-   <span data-ttu-id="12336-112">[**CTransInPlaceFilter:: Transform**](ctransinplacefilter-transform.md) usa um ponteiro para o exemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="12336-112">[**CTransInPlaceFilter::Transform**](ctransinplacefilter-transform.md) takes a pointer to the input sample.</span></span> <span data-ttu-id="12336-113">O filtro modifica os dados no local.</span><span class="sxs-lookup"><span data-stu-id="12336-113">The filter modifies the data in place.</span></span>

<span data-ttu-id="12336-114">Se o método **Transform** retornar S \_ OK, o filtro entregará o exemplo downstream.</span><span class="sxs-lookup"><span data-stu-id="12336-114">If the **Transform** method returns S\_OK, the filter delivers the sample downstream.</span></span> <span data-ttu-id="12336-115">Para ignorar um quadro, retorne S \_ false.</span><span class="sxs-lookup"><span data-stu-id="12336-115">To skip a frame, return S\_FALSE.</span></span> <span data-ttu-id="12336-116">Se houver um erro de streaming, retorne um código de falha.</span><span class="sxs-lookup"><span data-stu-id="12336-116">If there is a streaming error, return a failure code.</span></span>

<span data-ttu-id="12336-117">O exemplo a seguir mostra como o codificador RLE pode implementar esse método.</span><span class="sxs-lookup"><span data-stu-id="12336-117">The following example shows how the RLE encoder might implement this method.</span></span> <span data-ttu-id="12336-118">Sua própria implementação pode diferir consideravelmente, dependendo do que o filtro faz.</span><span class="sxs-lookup"><span data-stu-id="12336-118">Your own implementation might differ considerably, depending on what your filter does.</span></span>


```C++
HRESULT CRleFilter::Transform(IMediaSample *pSource, IMediaSample *pDest)
{
    // Get pointers to the underlying buffers.
    BYTE *pBufferIn, *pBufferOut;
    hr = pSource->GetPointer(&pBufferIn);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pDest->GetPointer(&pBufferOut);
    if (FAILED(hr))
    {
        return hr;
    }
    // Process the data.
    DWORD cbDest = EncodeFrame(pBufferIn, pBufferOut);
    KASSERT((long)cbDest <= pDest->GetSize());

    pDest->SetActualDataLength(cbDest);
    pDest->SetSyncPoint(TRUE);
    return S_OK;
}
```



<span data-ttu-id="12336-119">Este exemplo pressupõe que EncodeFrame é um método particular que implementa a codificação RLE.</span><span class="sxs-lookup"><span data-stu-id="12336-119">This example assumes that EncodeFrame is a private method that implements the RLE encoding.</span></span> <span data-ttu-id="12336-120">O próprio algoritmo de codificação não é descrito aqui; para obter detalhes, consulte o tópico "compactação de bitmap" na documentação do Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="12336-120">The encoding algorithm itself is not described here; for details, see the topic "Bitmap Compression" in the Platform SDK documentation.</span></span>

<span data-ttu-id="12336-121">Primeiro, o exemplo chama [**IMediaSample:: Getapontarr**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) para recuperar os endereços dos buffers subjacentes.</span><span class="sxs-lookup"><span data-stu-id="12336-121">First, the example calls [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) to retrieve the addresses of the underlying buffers.</span></span> <span data-ttu-id="12336-122">Ele passa esses para o método EncoderFrame privado.</span><span class="sxs-lookup"><span data-stu-id="12336-122">It passes these to the private EncoderFrame method.</span></span> <span data-ttu-id="12336-123">Em seguida, ele chama [**IMediaSample:: SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) para especificar o comprimento dos dados codificados.</span><span class="sxs-lookup"><span data-stu-id="12336-123">Then it calls [**IMediaSample::SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) to specify the length of the encoded data.</span></span> <span data-ttu-id="12336-124">O filtro downstream precisa dessas informações para que possa gerenciar o buffer corretamente.</span><span class="sxs-lookup"><span data-stu-id="12336-124">The downstream filter needs this information so that it can manage the buffer properly.</span></span> <span data-ttu-id="12336-125">Por fim, o método chama [**IMediaSample:: SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) para definir o sinalizador de quadro de chave como **true**.</span><span class="sxs-lookup"><span data-stu-id="12336-125">Finally, the method calls [**IMediaSample::SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) to set the key frame flag to **TRUE**.</span></span> <span data-ttu-id="12336-126">A codificação de comprimento de execução não usa quadros Delta, portanto, cada quadro é um quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="12336-126">Run-length encoding does not use any delta frames, so every frame is a key frame.</span></span> <span data-ttu-id="12336-127">Para quadros Delta, defina o valor como **false**.</span><span class="sxs-lookup"><span data-stu-id="12336-127">For delta frames, set the value to **FALSE**.</span></span>

<span data-ttu-id="12336-128">Outros problemas que você deve considerar incluem:</span><span class="sxs-lookup"><span data-stu-id="12336-128">Other issues that you must consider include:</span></span>

-   <span data-ttu-id="12336-129">Carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="12336-129">Time stamps.</span></span> <span data-ttu-id="12336-130">A classe **CTransformFilter** carimbo de data/hora o exemplo de saída antes de chamar o método **Transform** .</span><span class="sxs-lookup"><span data-stu-id="12336-130">The **CTransformFilter** class timestamps the output sample before calling the **Transform** method.</span></span> <span data-ttu-id="12336-131">Ele copia os valores de carimbo de data/hora do exemplo de entrada, sem modificá-los.</span><span class="sxs-lookup"><span data-stu-id="12336-131">It copies the time stamp values from the input sample, without modifying them.</span></span> <span data-ttu-id="12336-132">Se o filtro precisar alterar os carimbos de data/hora, chame [**IMediaSample:: SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) no exemplo de saída.</span><span class="sxs-lookup"><span data-stu-id="12336-132">If your filter needs to change the time stamps, call [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) on the output sample.</span></span>
-   <span data-ttu-id="12336-133">Formatar alterações.</span><span class="sxs-lookup"><span data-stu-id="12336-133">Format changes.</span></span> <span data-ttu-id="12336-134">O filtro upstream pode alterar formatos MID-Stream anexando um tipo de mídia ao exemplo.</span><span class="sxs-lookup"><span data-stu-id="12336-134">The upstream filter can change formats mid-stream by attaching a media type to the sample.</span></span> <span data-ttu-id="12336-135">Antes de fazer isso, ele chama [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) no PIN de entrada do seu filtro.</span><span class="sxs-lookup"><span data-stu-id="12336-135">Before doing so, it calls [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) on your filter's input pin.</span></span> <span data-ttu-id="12336-136">Na classe **CTransformFilter** , isso resulta em uma chamada para **CheckInputType** seguida por **CheckTransform**.</span><span class="sxs-lookup"><span data-stu-id="12336-136">In the **CTransformFilter** class, this results in a call to **CheckInputType** followed by **CheckTransform**.</span></span> <span data-ttu-id="12336-137">O filtro downstream também pode alterar os tipos de mídia, usando o mesmo mecanismo.</span><span class="sxs-lookup"><span data-stu-id="12336-137">The downstream filter can also change media types, using the same mechanism.</span></span> <span data-ttu-id="12336-138">Em seu próprio filtro, há duas coisas a serem observadas:</span><span class="sxs-lookup"><span data-stu-id="12336-138">In your own filter, there are two things to watch for:</span></span>

    -   <span data-ttu-id="12336-139">Certifique-se de que **QueryAccept** não retorna falsos aceitações.</span><span class="sxs-lookup"><span data-stu-id="12336-139">Make sure that **QueryAccept** does not return false acceptances.</span></span>
    -   <span data-ttu-id="12336-140">Se o filtro aceitar alterações de formato, verifique-as dentro do método **Transform** chamando [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="12336-140">If your filter does accept format changes, check for them inside the **Transform** method by calling [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span></span> <span data-ttu-id="12336-141">Se esse método retornar S \_ OK, o filtro deverá responder à alteração de formato.</span><span class="sxs-lookup"><span data-stu-id="12336-141">If that method returns S\_OK, your filter must respond to the format change.</span></span>

    <span data-ttu-id="12336-142">Para obter mais informações, consulte [Dynamic Format Changes](dynamic-format-changes.md).</span><span class="sxs-lookup"><span data-stu-id="12336-142">For more information, see [Dynamic Format Changes](dynamic-format-changes.md).</span></span>

-   <span data-ttu-id="12336-143">Threads.</span><span class="sxs-lookup"><span data-stu-id="12336-143">Threads.</span></span> <span data-ttu-id="12336-144">Em **CTransformFilter** e **CTransInPlaceFilter**, o filtro de transformação fornece amostras de saída de forma síncrona dentro do método **Receive** .</span><span class="sxs-lookup"><span data-stu-id="12336-144">In both **CTransformFilter** and **CTransInPlaceFilter**, the transform filter delivers output samples synchronously inside the **Receive** method.</span></span> <span data-ttu-id="12336-145">O filtro não cria nenhum thread de trabalho para processar os dados.</span><span class="sxs-lookup"><span data-stu-id="12336-145">The filter does not create any worker threads to process the data.</span></span> <span data-ttu-id="12336-146">Normalmente, não há motivo para um filtro de transformação criar threads de trabalho.</span><span class="sxs-lookup"><span data-stu-id="12336-146">Typically, there is no reason for a transform filter to create worker threads.</span></span>

<span data-ttu-id="12336-147">Em seguida: [etapa 6. Adicione suporte para COM](step-6--add-support-for-com.md).</span><span class="sxs-lookup"><span data-stu-id="12336-147">Next: [Step 6. Add Support for COM](step-6--add-support-for-com.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="12336-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12336-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12336-149">Gravando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="12336-149">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



