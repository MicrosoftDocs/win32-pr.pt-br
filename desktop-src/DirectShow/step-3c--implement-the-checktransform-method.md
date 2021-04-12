---
description: Etapa 3C.
ms.assetid: e780df46-bf47-4334-b788-05ad8179f051
title: Etapa 3C. Implementar o método CheckTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78148701fc54e73a6970d45fde95d70f4cf0df3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171507"
---
# <a name="step-3c-implement-the-checktransform-method"></a><span data-ttu-id="13a81-104">Etapa 3C.</span><span class="sxs-lookup"><span data-stu-id="13a81-104">Step 3C.</span></span> <span data-ttu-id="13a81-105">Implementar o método CheckTransform</span><span class="sxs-lookup"><span data-stu-id="13a81-105">Implement the CheckTransform Method</span></span>

<span data-ttu-id="13a81-106">Esta é a etapa 3C do tutorial [escrevendo filtros de transformação](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="13a81-106">This is step 3C of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="13a81-107">Esta etapa não é necessária para filtros que derivam de **CTransInPlaceFilter**.</span><span class="sxs-lookup"><span data-stu-id="13a81-107">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="13a81-108">O método [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) verifica se um tipo de saída proposto é compatível com o tipo de entrada atual.</span><span class="sxs-lookup"><span data-stu-id="13a81-108">The [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method checks if a proposed output type is compatible with the current input type.</span></span> <span data-ttu-id="13a81-109">O método também será chamado se o PIN de entrada se reconectar após a conexão do pino de saída.</span><span class="sxs-lookup"><span data-stu-id="13a81-109">The method is also called if the input pin reconnects after the output pin connects.</span></span>

<span data-ttu-id="13a81-110">O exemplo a seguir verifica se o formato é RLE8 vídeo; as dimensões da imagem correspondem ao formato de entrada; e as entradas da paleta são as mesmas.</span><span class="sxs-lookup"><span data-stu-id="13a81-110">The following example verifies whether the format is RLE8 video; the image dimensions match the input format; and the palette entries are the same.</span></span> <span data-ttu-id="13a81-111">Ele também rejeita os retângulos de origem e destino que não correspondem ao tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="13a81-111">It also rejects source and target rectangles that do not match the image size.</span></span>


```C++
HRESULT CRleFilter::CheckTransform(
    const CMediaType *mtIn, const CMediaType *mtOut)
{
    // Check the major type.
    if (mtOut->majortype != MEDIATYPE_Video)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Check the subtype and format type.
    FOURCCMap fccMap = FCC('MRLE'); 
    if (mtOut->subtype != static_cast<GUID>(fccMap))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    if ((mtOut->formattype != FORMAT_VideoInfo) || 
        (mtOut->cbFormat < sizeof(VIDEOINFOHEADER)))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Compare the bitmap information against the input type.
    ASSERT(mtIn->formattype == FORMAT_VideoInfo);
    BITMAPINFOHEADER *pBmiOut = HEADER(mtOut->pbFormat);
    BITMAPINFOHEADER *pBmiIn = HEADER(mtIn->pbFormat);
    if ((pBmiOut->biPlanes != 1) ||
        (pBmiOut->biBitCount != 8) ||
        (pBmiOut->biCompression != BI_RLE8) ||
        (pBmiOut->biWidth != pBmiIn->biWidth) ||
        (pBmiOut->biHeight != pBmiIn->biHeight))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Compare source and target rectangles.
    RECT rcImg;
    SetRect(&rcImg, 0, 0, pBmiIn->biWidth, pBmiIn->biHeight);
    RECT *prcSrc = &((VIDEOINFOHEADER*)(mtIn->pbFormat))->rcSource;
    RECT *prcTarget = &((VIDEOINFOHEADER*)(mtOut->pbFormat))->rcTarget;
    if (!IsRectEmpty(prcSrc) && !EqualRect(prcSrc, &rcImg))
    {
        return VFW_E_INVALIDMEDIATYPE;
    }
    if (!IsRectEmpty(prcTarget) && !EqualRect(prcTarget, &rcImg))
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the palette table.
    if (pBmiOut->biClrUsed != pBmiIn->biClrUsed)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    DWORD cbPalette = pBmiOut->biClrUsed * sizeof(RGBQUAD);
    if (mtOut->cbFormat < sizeof(VIDEOINFOHEADER) + cbPalette)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    if (0 != memcmp(pBmiOut + 1, pBmiIn + 1, cbPalette))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Everything is good.
    return S_OK;
}
```



<span data-ttu-id="13a81-112">**Fixar reconexões**</span><span class="sxs-lookup"><span data-stu-id="13a81-112">**Pin Reconnections**</span></span>

<span data-ttu-id="13a81-113">Os aplicativos podem se desconectar e reconectar Pins.</span><span class="sxs-lookup"><span data-stu-id="13a81-113">Applications can disconnect and reconnect pins.</span></span> <span data-ttu-id="13a81-114">Suponha que um aplicativo conecte ambos os Pins, desconecte o PIN de entrada e, em seguida, reconecte o PIN de entrada usando um novo tamanho de imagem.</span><span class="sxs-lookup"><span data-stu-id="13a81-114">Suppose an application connects both pins, disconnects the input pin, and then reconnects the input pin using a new image size.</span></span> <span data-ttu-id="13a81-115">Nesse caso, **CheckTransform** falhará porque as dimensões da imagem não correspondem mais.</span><span class="sxs-lookup"><span data-stu-id="13a81-115">In that case, **CheckTransform** fails because the dimensions of the image no longer match.</span></span> <span data-ttu-id="13a81-116">Esse comportamento é razoável, embora o filtro também possa tentar reconectar o pino de saída com um novo tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="13a81-116">This behavior is reasonable, although the filter could also try reconnecting the output pin with a new media type.</span></span>

<span data-ttu-id="13a81-117">Em seguida: [etapa 4. Definir propriedades de alocador](step-4--set-allocator-properties.md).</span><span class="sxs-lookup"><span data-stu-id="13a81-117">Next: [Step 4. Set Allocator Properties](step-4--set-allocator-properties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="13a81-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="13a81-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13a81-119">Reconectando Pins</span><span class="sxs-lookup"><span data-stu-id="13a81-119">Reconnecting Pins</span></span>](reconnecting-pins.md)
</dt> <dt>

[<span data-ttu-id="13a81-120">Retângulos de origem e de destino em renderizadores de vídeo</span><span class="sxs-lookup"><span data-stu-id="13a81-120">Source and Target Rectangles in Video Renderers</span></span>](source-and-target-rectangles-in-video-renderers.md)
</dt> <dt>

[<span data-ttu-id="13a81-121">Gravando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="13a81-121">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



