---
description: Etapa 3A.
ms.assetid: 774fcb12-8928-4667-8ef6-dce86717cc29
title: Etapa 3A. Implementar o método CheckInputType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5eb6ff440838d7a4b65b586e5dba963ff254eef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770062"
---
# <a name="step-3a-implement-the-checkinputtype-method"></a><span data-ttu-id="4be95-104">Etapa 3A.</span><span class="sxs-lookup"><span data-stu-id="4be95-104">Step 3A.</span></span> <span data-ttu-id="4be95-105">Implementar o método CheckInputType</span><span class="sxs-lookup"><span data-stu-id="4be95-105">Implement the CheckInputType Method</span></span>

<span data-ttu-id="4be95-106">Esta é a etapa 3A do tutorial [escrevendo filtros de transformação](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="4be95-106">This is step 3A of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="4be95-107">O método [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) é chamado quando o filtro upstream propõe um tipo de mídia para o filtro de transformação.</span><span class="sxs-lookup"><span data-stu-id="4be95-107">The [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method is called when the upstream filter proposes a media type to the transform filter.</span></span> <span data-ttu-id="4be95-108">Esse método usa um ponteiro para um objeto [**CMediaType**](cmediatype.md) , que é um wrapper fino para a estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="4be95-108">This method takes a pointer to a [**CMediaType**](cmediatype.md) object, which is a thin wrapper for the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="4be95-109">Nesse método, você deve examinar todos os campos relevantes da estrutura **do \_ \_ tipo de mídia am** , incluindo os campos no bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="4be95-109">In this method, you should examine every relevant field of the **AM\_MEDIA\_TYPE** structure, including the fields in the format block.</span></span> <span data-ttu-id="4be95-110">Você pode usar os métodos de acessadores definidos em **CMediaType** ou fazer referência diretamente aos membros da estrutura.</span><span class="sxs-lookup"><span data-stu-id="4be95-110">You can use the accessor methods defined in **CMediaType**, or reference the structure members directly.</span></span> <span data-ttu-id="4be95-111">Se qualquer campo não for válido, retornará VFW \_ E \_ tipo \_ não \_ aceito.</span><span class="sxs-lookup"><span data-stu-id="4be95-111">If any field is not valid, return VFW\_E\_TYPE\_NOT\_ACCEPTED.</span></span> <span data-ttu-id="4be95-112">Se o tipo de mídia inteiro for válido, retorne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4be95-112">If the entire media type is valid, return S\_OK.</span></span>

<span data-ttu-id="4be95-113">Por exemplo, no filtro do codificador RLE, o tipo de entrada deve ser vídeo RGB descompactado de 8 ou 4 bits.</span><span class="sxs-lookup"><span data-stu-id="4be95-113">For example, in the RLE encoder filter, the input type must be 8-bit or 4-bit uncompressed RGB video.</span></span> <span data-ttu-id="4be95-114">Não há motivo para dar suporte a outros formatos de entrada, como o RGB de 16 ou 24 bits, porque o filtro teria que convertê-los em uma profundidade de bits inferior, e o DirectShow já fornece um filtro de [conversor de espaço de cor](color-space-converter-filter.md) para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="4be95-114">There is no reason to support other input formats, such as 16- or 24-bit RGB, because the filter would have to convert them to a lower bit depth, and DirectShow already provides a [Color Space Converter](color-space-converter-filter.md) filter for that purpose.</span></span> <span data-ttu-id="4be95-115">O exemplo a seguir pressupõe que o codificador dá suporte a vídeo de 8 bits, mas não vídeo de 4 bits:</span><span class="sxs-lookup"><span data-stu-id="4be95-115">The following example assumes that the encoder supports 8-bit video but not 4-bit video:</span></span>


```C++
HRESULT CRleFilter::CheckInputType(const CMediaType *mtIn)
{
    if ((mtIn->majortype != MEDIATYPE_Video) ||
        (mtIn->subtype != MEDIASUBTYPE_RGB8) ||
        (mtIn->formattype != FORMAT_VideoInfo) || 
        (mtIn->cbFormat < sizeof(VIDEOINFOHEADER)))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    VIDEOINFOHEADER *pVih = 
        reinterpret_cast<VIDEOINFOHEADER*>(mtIn->pbFormat);
    if ((pVih->bmiHeader.biBitCount != 8) ||
        (pVih->bmiHeader.biCompression != BI_RGB))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Check the palette table.
    if (pVih->bmiHeader.biClrUsed > PALETTE_ENTRIES(pVih))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    DWORD cbPalette = pVih->bmiHeader.biClrUsed * sizeof(RGBQUAD);
    if (mtIn->cbFormat < sizeof(VIDEOINFOHEADER) + cbPalette)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Everything is good.
    return S_OK;
}
```



<span data-ttu-id="4be95-116">Neste exemplo, o método primeiro verifica o tipo principal e subtipo.</span><span class="sxs-lookup"><span data-stu-id="4be95-116">In this example, the method first checks the major type and subtype.</span></span> <span data-ttu-id="4be95-117">Em seguida, ele verifica o tipo de formato para verificar se o bloco de formato é uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="4be95-117">Then it checks the format type, to make sure the format block is a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span> <span data-ttu-id="4be95-118">O filtro também pode dar suporte a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2), mas, nesse caso, não haveria nenhum benefício real.</span><span class="sxs-lookup"><span data-stu-id="4be95-118">The filter could also support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2), but in this case there would be no real benefit.</span></span> <span data-ttu-id="4be95-119">A estrutura **VIDEOINFOHEADER2** adiciona suporte para entrelaçamento e pixels não quadrados, que provavelmente não serão relevantes no vídeo de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="4be95-119">The **VIDEOINFOHEADER2** structure adds support for interlacing and non-square pixels, which are not likely to be relevant in 8-bit video.</span></span>

<span data-ttu-id="4be95-120">Se o tipo de formato estiver correto, o exemplo verificará os membros **biBitCount** e **biCompression** da estrutura **VIDEOINFOHEADER** , para verificar se o formato é RGB não compactado de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="4be95-120">If the format type is correct, the example checks the **biBitCount** and **biCompression** members of the **VIDEOINFOHEADER** structure, to verify that the format is 8-bit uncompressed RGB.</span></span> <span data-ttu-id="4be95-121">Como mostra este exemplo, você deve forçar o</span><span class="sxs-lookup"><span data-stu-id="4be95-121">As this example shows, you must coerce the</span></span>


```C++
pbFormat
```



<span data-ttu-id="4be95-122">Ponteiro para a estrutura correta, com base no tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="4be95-122">pointer to the correct structure, based on the format type.</span></span> <span data-ttu-id="4be95-123">Sempre verifique o tipo de formato GUID (**formatType**) e o tamanho do bloco de formato (**cbFormat**) antes de converter o ponteiro.</span><span class="sxs-lookup"><span data-stu-id="4be95-123">Always check the format type GUID (**formattype**) and the size of the format block (**cbFormat**) before casting the pointer.</span></span>

<span data-ttu-id="4be95-124">O exemplo também verifica se o número de entradas da paleta é compatível com a profundidade de bits e o bloco de formato é grande o suficiente para manter as entradas da paleta.</span><span class="sxs-lookup"><span data-stu-id="4be95-124">The example also verifies that the number of palette entries is compatible with the bit depth and the format block is large enough to hold the palette entries.</span></span> <span data-ttu-id="4be95-125">Se todas essas informações estiverem corretas, o método retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4be95-125">If all of this information is correct, the method returns S\_OK.</span></span>

<span data-ttu-id="4be95-126">Em seguida: [etapa 3B. implemente o método GetMediaType](step-3b--implement-the-getmediatype-method.md).</span><span class="sxs-lookup"><span data-stu-id="4be95-126">Next: [Step 3B. Implement the GetMediaType Method](step-3b--implement-the-getmediatype-method.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4be95-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4be95-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4be95-128">Gravando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="4be95-128">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



