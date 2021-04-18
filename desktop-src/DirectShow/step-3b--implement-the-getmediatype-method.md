---
description: Etapa 3B.
ms.assetid: 0ec57083-b192-404a-938f-bc6bb1cf0ddb
title: Etapa 3B. Implementar o método GetMediaType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab3ee41c6740fc2914f943784c0d51116f90428
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104506343"
---
# <a name="step-3b-implement-the-getmediatype-method"></a><span data-ttu-id="94abc-104">Etapa 3B.</span><span class="sxs-lookup"><span data-stu-id="94abc-104">Step 3B.</span></span> <span data-ttu-id="94abc-105">Implementar o método GetMediaType</span><span class="sxs-lookup"><span data-stu-id="94abc-105">Implement the GetMediaType Method</span></span>

<span data-ttu-id="94abc-106">Esta é a etapa 3B do tutorial [escrevendo filtros de transformação](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="94abc-106">This is step 3B of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="94abc-107">Esta etapa não é necessária para filtros que derivam de **CTransInPlaceFilter**.</span><span class="sxs-lookup"><span data-stu-id="94abc-107">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="94abc-108">O método [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) retorna um dos tipos de saída preferenciais do filtro, referenciado pelo número de índice.</span><span class="sxs-lookup"><span data-stu-id="94abc-108">The [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method returns one of the filter's preferred output types, referenced by index number.</span></span> <span data-ttu-id="94abc-109">Esse método nunca é chamado a menos que o PIN de entrada do filtro já esteja conectado.</span><span class="sxs-lookup"><span data-stu-id="94abc-109">This method is never called unless the filter's input pin is already connected.</span></span> <span data-ttu-id="94abc-110">Portanto, você pode usar o tipo de mídia da conexão upstream para determinar os tipos de saída preferenciais.</span><span class="sxs-lookup"><span data-stu-id="94abc-110">Therefore, you can use the media type from the upstream connection to determine the preferred output types.</span></span>

<span data-ttu-id="94abc-111">Um codificador normalmente oferece um único tipo preferencial, representando o formato de destino.</span><span class="sxs-lookup"><span data-stu-id="94abc-111">An encoder typically offers a single preferred type, representing the target format.</span></span> <span data-ttu-id="94abc-112">Os decodificadores geralmente dão suporte a uma variedade de formatos de saída e os oferecem em ordem de qualidade ou eficiência decrescente.</span><span class="sxs-lookup"><span data-stu-id="94abc-112">Decoders generally support a range of output formats, and offer them in order of descending quality or efficiency.</span></span> <span data-ttu-id="94abc-113">Por exemplo, a lista pode ser UYVY, Y211, RGB-24, RGB-565, RGB-555 e RGB-8, nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="94abc-113">For example, the list might be UYVY, Y211, RGB-24, RGB-565, RGB-555, and RGB-8, in that order.</span></span> <span data-ttu-id="94abc-114">Filtros de efeito podem exigir uma correspondência exata entre o formato de saída e o formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="94abc-114">Effect filters may require an exact match between the output format and the input format.</span></span>

<span data-ttu-id="94abc-115">O exemplo a seguir retorna um único tipo de saída, que é construído modificando o tipo de entrada para especificar a compactação RLE8:</span><span class="sxs-lookup"><span data-stu-id="94abc-115">The following example returns a single output type, which is constructed by modifying the input type to specify RLE8 compression:</span></span>


```C++
HRESULT CRleFilter::GetMediaType(int iPosition, CMediaType *pMediaType)
{
    ASSERT(m_pInput->IsConnected());
    if (iPosition < 0)
    {
        return E_INVALIDARG;
    }
    if (iPosition == 0)
    {
        HRESULT hr = m_pInput->ConnectionMediaType(pMediaType);
        if (FAILED(hr))
        {
            return hr;
        }
        FOURCCMap fccMap = FCC('MRLE'); 
        pMediaType->subtype = static_cast<GUID>(fccMap);
        pMediaType->SetVariableSize();
        pMediaType->SetTemporalCompression(FALSE);

        ASSERT(pMediaType->formattype == FORMAT_VideoInfo);
        VIDEOINFOHEADER *pVih =
            reinterpret_cast<VIDEOINFOHEADER*>(pMediaType->pbFormat);
        pVih->bmiHeader.biCompression = BI_RLE8;
        pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader); 
        return S_OK;
    }
    // else
    return VFW_S_NO_MORE_ITEMS;
}
```



<span data-ttu-id="94abc-116">Neste exemplo, o método chama [**IPin:: ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) para obter o tipo de entrada do pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="94abc-116">In this example, the method calls [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) to get the input type from the input pin.</span></span> <span data-ttu-id="94abc-117">Em seguida, ele altera alguns dos campos para indicar o formato de compactação, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="94abc-117">Then it changes some of the fields to indicate the compression format, as follows:</span></span>

-   <span data-ttu-id="94abc-118">Ele atribui um novo GUID de subtipo, que é construído a partir do código FOURCC ' MRLE ', usando a classe [**FOURCCMap**](fourccmap.md) .</span><span class="sxs-lookup"><span data-stu-id="94abc-118">It assigns a new subtype GUID, which is constructed from the FOURCC code 'MRLE', using the [**FOURCCMap**](fourccmap.md) class.</span></span>
-   <span data-ttu-id="94abc-119">Ele chama o método [**CMediaType:: Setvariables**](cmediatype-setvariablesize.md) , que define o sinalizador **bFixedSizeSamples** como **false** e o membro **lSampleSize** como zero, indicando exemplos de tamanho variável.</span><span class="sxs-lookup"><span data-stu-id="94abc-119">It calls the [**CMediaType::SetVariableSize**](cmediatype-setvariablesize.md) method, which sets the **bFixedSizeSamples** flag to **FALSE** and the **lSampleSize** member to zero, indicating variable-sized samples.</span></span>
-   <span data-ttu-id="94abc-120">Ele chama o método [**CMediaType:: SetTemporalCompression**](cmediatype-settemporalcompression.md) com o valor **false**, indicando que cada quadro é um quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="94abc-120">It calls the [**CMediaType::SetTemporalCompression**](cmediatype-settemporalcompression.md) method with the value **FALSE**, indicating that every frame is a key frame.</span></span> <span data-ttu-id="94abc-121">(Esse campo é apenas informativo, portanto, você pode ignorá-lo com segurança.)</span><span class="sxs-lookup"><span data-stu-id="94abc-121">(This field is informational only, so you could safely ignore it.)</span></span>
-   <span data-ttu-id="94abc-122">Ele define o campo de **Bicompactação** como bi \_ RLE8.</span><span class="sxs-lookup"><span data-stu-id="94abc-122">It sets the **biCompression** field to BI\_RLE8.</span></span>
-   <span data-ttu-id="94abc-123">Ele define o campo **biSizeImage** para o tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="94abc-123">It sets the **biSizeImage** field to the image size.</span></span>

<span data-ttu-id="94abc-124">Em seguida: [etapa 3C. implemente o método CheckTransform](step-3c--implement-the-checktransform-method.md).</span><span class="sxs-lookup"><span data-stu-id="94abc-124">Next: [Step 3C. Implement the CheckTransform Method](step-3c--implement-the-checktransform-method.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="94abc-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="94abc-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94abc-126">Gravando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="94abc-126">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



