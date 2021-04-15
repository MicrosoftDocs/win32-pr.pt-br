---
description: Tipos de mídia de vídeo descompactados
ms.assetid: 50bf2947-27ee-4092-9d3a-a1c13ee80e95
title: Tipos de mídia de vídeo descompactados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c90a48aed62f22a492ac22dae93761c1046750a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104506339"
---
# <a name="uncompressed-video-media-types"></a><span data-ttu-id="0d580-103">Tipos de mídia de vídeo descompactados</span><span class="sxs-lookup"><span data-stu-id="0d580-103">Uncompressed Video Media Types</span></span>

<span data-ttu-id="0d580-104">Este tópico descreve como criar um tipo de mídia que descreve um formato de vídeo descompactado.</span><span class="sxs-lookup"><span data-stu-id="0d580-104">This topic describes how to create a media type that describes an uncompressed video format.</span></span> <span data-ttu-id="0d580-105">Para obter mais informações sobre tipos de mídia em geral, consulte [sobre tipos de mídia](about-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="0d580-105">For more information about media types generally, see [About Media Types](about-media-types.md).</span></span>

<span data-ttu-id="0d580-106">Para criar um tipo de vídeo descompactado completo, defina os atributos a seguir no ponteiro de interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="0d580-106">To create a complete uncompressed video type, set the following attributes on the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface pointer.</span></span>



| <span data-ttu-id="0d580-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="0d580-107">Attribute</span></span>                                                                            | <span data-ttu-id="0d580-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d580-108">Description</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d580-109">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="0d580-109">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                            | <span data-ttu-id="0d580-110">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="0d580-110">Major type.</span></span> <span data-ttu-id="0d580-111">Defina como **\_ vídeo MFMediaType**.</span><span class="sxs-lookup"><span data-stu-id="0d580-111">Set to **MFMediaType\_Video**.</span></span>                                                                                                                                                                                          |
| [<span data-ttu-id="0d580-112">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="0d580-112">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                   | <span data-ttu-id="0d580-113">Subtipo.</span><span class="sxs-lookup"><span data-stu-id="0d580-113">Subtype.</span></span> <span data-ttu-id="0d580-114">Consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="0d580-114">See [Video Subtype GUIDs](video-subtype-guids.md).</span></span>                                                                                                                                                                        |
| [<span data-ttu-id="0d580-115">**\_ \_ Stride padrão MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="0d580-115">**MF\_MT\_DEFAULT\_STRIDE**</span></span>](mf-mt-default-stride-attribute.md)                    | <span data-ttu-id="0d580-116">Stride da superfície.</span><span class="sxs-lookup"><span data-stu-id="0d580-116">Surface stride.</span></span> <span data-ttu-id="0d580-117">O *Stride* é o número de bytes necessários para passar de uma linha de pixels para a próxima.</span><span class="sxs-lookup"><span data-stu-id="0d580-117">The *stride* is the number of bytes needed to go from one row of pixels to the next.</span></span> <span data-ttu-id="0d580-118">Defina esse atributo se o stride em bytes não for igual à largura do vídeo em bytes.</span><span class="sxs-lookup"><span data-stu-id="0d580-118">Set this attribute if the stride in bytes is not the same as the video width in bytes.</span></span> <span data-ttu-id="0d580-119">Caso contrário, você pode omitir esse atributo.</span><span class="sxs-lookup"><span data-stu-id="0d580-119">Otherwise, you can omit this attribute.</span></span> |
| [<span data-ttu-id="0d580-120">**\_taxa de \_ quadros MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="0d580-120">**MF\_MT\_FRAME\_RATE**</span></span>](mf-mt-frame-rate-attribute.md)                            | <span data-ttu-id="0d580-121">Taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="0d580-121">Frame rate.</span></span>                                                                                                                                                                                                                         |
| [<span data-ttu-id="0d580-122">**\_tamanho do \_ quadro MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="0d580-122">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md)                            | <span data-ttu-id="0d580-123">Tamanho do quadro.</span><span class="sxs-lookup"><span data-stu-id="0d580-123">Frame size.</span></span>                                                                                                                                                                                                                         |
| [<span data-ttu-id="0d580-124">**\_modo de \_ entrelaçamento do MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="0d580-124">**MF\_MT\_INTERLACE\_MODE**</span></span>](mf-mt-interlace-mode-attribute.md)                    | <span data-ttu-id="0d580-125">Modo de entrelaçamento.</span><span class="sxs-lookup"><span data-stu-id="0d580-125">Interlacing mode.</span></span>                                                                                                                                                                                                                   |
| [<span data-ttu-id="0d580-126">**\_ \_ todos os exemplos do MF MT são \_ \_ independentes**</span><span class="sxs-lookup"><span data-stu-id="0d580-126">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md) | <span data-ttu-id="0d580-127">Especifica se cada amostra é independente.</span><span class="sxs-lookup"><span data-stu-id="0d580-127">Specifies whether each sample is independent.</span></span> <span data-ttu-id="0d580-128">Defina como **verdadeiro** para formatos não compactados.</span><span class="sxs-lookup"><span data-stu-id="0d580-128">Set to **TRUE** for uncompressed formats.</span></span>                                                                                                                                             |
| [<span data-ttu-id="0d580-129">**taxa de proporção de pixel do MF \_ MT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0d580-129">**MF\_MT\_PIXEL\_ASPECT\_RATIO**</span></span>](mf-mt-pixel-aspect-ratio-attribute.md)           | <span data-ttu-id="0d580-130">Taxa de proporção de pixel.</span><span class="sxs-lookup"><span data-stu-id="0d580-130">Pixel aspect ratio.</span></span>                                                                                                                                                                                                                 |



 

<span data-ttu-id="0d580-131">Além disso, defina os atributos a seguir se você souber os valores corretos.</span><span class="sxs-lookup"><span data-stu-id="0d580-131">In addition, set the following attributes if you know the correct values.</span></span> <span data-ttu-id="0d580-132">(Caso contrário, omita esses atributos.)</span><span class="sxs-lookup"><span data-stu-id="0d580-132">(Otherwise, omit these attributes.)</span></span>



| <span data-ttu-id="0d580-133">Atributo</span><span class="sxs-lookup"><span data-stu-id="0d580-133">Attribute</span></span>                                                                    | <span data-ttu-id="0d580-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d580-134">Description</span></span>        |
|------------------------------------------------------------------------------|--------------------|
| [<span data-ttu-id="0d580-135">**\_ \_ primários de vídeo MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="0d580-135">**MF\_MT\_VIDEO\_PRIMARIES**</span></span>](mf-mt-video-primaries-attribute.md)          | <span data-ttu-id="0d580-136">Primárias de cores.</span><span class="sxs-lookup"><span data-stu-id="0d580-136">Color primaries.</span></span>   |
| [<span data-ttu-id="0d580-137">**função de transferência do MF \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0d580-137">**MF\_MT\_TRANSFER\_FUNCTION**</span></span>](mf-mt-transfer-function-attribute.md)      | <span data-ttu-id="0d580-138">Função de transferência.</span><span class="sxs-lookup"><span data-stu-id="0d580-138">Transfer function.</span></span> |
| [<span data-ttu-id="0d580-139">**\_ \_ matriz YUV do MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="0d580-139">**MF\_MT\_YUV\_MATRIX**</span></span>](mf-mt-yuv-matrix-attribute.md)                    | <span data-ttu-id="0d580-140">Matriz de transferência.</span><span class="sxs-lookup"><span data-stu-id="0d580-140">Transfer matrix.</span></span>   |
| [<span data-ttu-id="0d580-141">**\_vídeo MF \_ MT \_ croma \_ localizando**</span><span class="sxs-lookup"><span data-stu-id="0d580-141">**MF\_MT\_VIDEO\_CHROMA\_SITING**</span></span>](mf-mt-video-chroma-siting-attribute.md) | <span data-ttu-id="0d580-142">Croma localizando.</span><span class="sxs-lookup"><span data-stu-id="0d580-142">Chroma siting.</span></span>     |
| [<span data-ttu-id="0d580-143">**\_ \_ intervalo nominal de vídeo MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0d580-143">**MF\_MT\_VIDEO\_NOMINAL\_RANGE**</span></span>](mf-mt-video-nominal-range-attribute.md) | <span data-ttu-id="0d580-144">Intervalo nominal.</span><span class="sxs-lookup"><span data-stu-id="0d580-144">Nominal range.</span></span>     |



 

<span data-ttu-id="0d580-145">Para obter mais informações, consulte [informações de cores estendidas](extended-color-information.md).</span><span class="sxs-lookup"><span data-stu-id="0d580-145">For more information, see [Extended Color Information](extended-color-information.md).</span></span> <span data-ttu-id="0d580-146">Por exemplo, se você criar um tipo de mídia que descreve um padrão de vídeo e o padrão definir croma localizando, adicione essas informações ao tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="0d580-146">For example, if you create a media type that describes a video standard, and the standard defines the chroma siting, add this information to the media type.</span></span> <span data-ttu-id="0d580-147">Isso ajuda a preservar a fidelidade de cores em todo o pipeline.</span><span class="sxs-lookup"><span data-stu-id="0d580-147">Doing so helps to preserve color fidelity throughout the pipeline.</span></span>

<span data-ttu-id="0d580-148">As funções a seguir podem ser úteis ao criar um tipo de mídia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0d580-148">The following functions might be useful when creating a video media type.</span></span>



| <span data-ttu-id="0d580-149">Função</span><span class="sxs-lookup"><span data-stu-id="0d580-149">Function</span></span>                                                                     | <span data-ttu-id="0d580-150">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d580-150">Description</span></span>                                                                                                                                                                          |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d580-151">**MFAverageTimePerFrameToFrameRate**</span><span class="sxs-lookup"><span data-stu-id="0d580-151">**MFAverageTimePerFrameToFrameRate**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | <span data-ttu-id="0d580-152">Calcula a taxa de quadros, de acordo com a duração média do quadro.</span><span class="sxs-lookup"><span data-stu-id="0d580-152">Calculates the frame rate, given the average frame duration.</span></span>                                                                                                                         |
| [<span data-ttu-id="0d580-153">**MFCalculateImageSize**</span><span class="sxs-lookup"><span data-stu-id="0d580-153">**MFCalculateImageSize**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | <span data-ttu-id="0d580-154">Calcula o tamanho da imagem para um formato de vídeo descompactado.</span><span class="sxs-lookup"><span data-stu-id="0d580-154">Calculates the image size for an uncompressed video format.</span></span>                                                                                                                          |
| [<span data-ttu-id="0d580-155">**MFFrameRateToAverageTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="0d580-155">**MFFrameRateToAverageTimePerFrame**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | <span data-ttu-id="0d580-156">Calcula a duração média de um quadro de vídeo, dada a taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="0d580-156">Calculates the average duration of a video frame, given the frame rate.</span></span>                                                                                                              |
| [<span data-ttu-id="0d580-157">**MFGetStrideForBitmapInfoHeader**</span><span class="sxs-lookup"><span data-stu-id="0d580-157">**MFGetStrideForBitmapInfoHeader**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | <span data-ttu-id="0d580-158">Retorna o stride de superfície mínimo para um formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0d580-158">Returns the minimum surface stride for a video format.</span></span> <span data-ttu-id="0d580-159">Para obter mais informações, consulte [Stride de imagem](image-stride.md).</span><span class="sxs-lookup"><span data-stu-id="0d580-159">For more information, see [Image Stride](image-stride.md).</span></span>                                                                   |
| [<span data-ttu-id="0d580-160">**MFInitVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="0d580-160">**MFInitVideoFormat**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfinitvideoformat)                               | <span data-ttu-id="0d580-161">Inicializa uma estrutura [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) para alguns formatos de vídeo padrão, como televisão NTSC.</span><span class="sxs-lookup"><span data-stu-id="0d580-161">Initializes an [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) structure for some standard video formats, such as NTSC television.</span></span> <span data-ttu-id="0d580-162">Em seguida, você pode usar a estrutura para inicializar um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="0d580-162">You can then use the structure to initialize a media type.</span></span> |
| [<span data-ttu-id="0d580-163">**MFIsFormatYUV**</span><span class="sxs-lookup"><span data-stu-id="0d580-163">**MFIsFormatYUV**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | <span data-ttu-id="0d580-164">Consulta se um formato de vídeo é um formato YUV.</span><span class="sxs-lookup"><span data-stu-id="0d580-164">Queries whether a video format is a YUV format.</span></span>                                                                                                                                      |



 

## <a name="examples"></a><span data-ttu-id="0d580-165">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0d580-165">Examples</span></span>

<span data-ttu-id="0d580-166">Este exemplo mostra uma função que preenche as informações mais comuns para um formato de vídeo descompactado.</span><span class="sxs-lookup"><span data-stu-id="0d580-166">This example shows a function that fills in the most common information for an uncompressed video format.</span></span> <span data-ttu-id="0d580-167">A função retorna um ponteiro de interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="0d580-167">The function returns an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface pointer.</span></span> <span data-ttu-id="0d580-168">Em seguida, você pode adicionar atributos adicionais ao tipo de mídia, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="0d580-168">You can then add additional attributes to the media type as needed.</span></span>


```C++
HRESULT CreateUncompressedVideoType(
    DWORD                fccFormat,  // FOURCC or D3DFORMAT value.     
    UINT32               width, 
    UINT32               height,
    MFVideoInterlaceMode interlaceMode,
    const MFRatio&       frameRate,
    const MFRatio&       par,
    IMFMediaType         **ppType
    )
{
    if (ppType == NULL)
    {
        return E_POINTER;
    }

    GUID    subtype = MFVideoFormat_Base;
    LONG    lStride = 0;
    UINT    cbImage = 0;

    IMFMediaType *pType = NULL;

    // Set the subtype GUID from the FOURCC or D3DFORMAT value.
    subtype.Data1 = fccFormat;

    HRESULT hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, subtype);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_INTERLACE_MODE, interlaceMode);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFSetAttributeSize(pType, MF_MT_FRAME_SIZE, width, height);
    if (FAILED(hr))
    {
        goto done;
    }

    // Calculate the default stride value.
    hr = pType->SetUINT32(MF_MT_DEFAULT_STRIDE, UINT32(lStride));
    if (FAILED(hr))
    {
        goto done;
    }

    // Calculate the image size in bytes.
    hr = MFCalculateImageSize(subtype, width, height, &cbImage);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_SAMPLE_SIZE, cbImage);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_FIXED_SIZE_SAMPLES, TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Frame rate
    hr = MFSetAttributeRatio(pType, MF_MT_FRAME_RATE, frameRate.Numerator, 
        frameRate.Denominator);
    if (FAILED(hr))
    {
        goto done;
    }

    // Pixel aspect ratio
    hr = MFSetAttributeRatio(pType, MF_MT_PIXEL_ASPECT_RATIO, par.Numerator, 
        par.Denominator);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppType = pType;
    (*ppType)->AddRef();

done:
    SafeRelease(&pType);
    return hr;
}
```



<span data-ttu-id="0d580-169">O exemplo a seguir usa um formato de vídeo codificado como entrada e cria um tipo de vídeo não compactado correspondente.</span><span class="sxs-lookup"><span data-stu-id="0d580-169">The next example takes an encoded video format as input, and creates a matching uncompressed video type.</span></span> <span data-ttu-id="0d580-170">Esse tipo seria adequado para ser definido em um codificador ou decodificador, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="0d580-170">This type would be suitable to set on an encoder or decoder, for example.</span></span>


```C++
HRESULT ConvertVideoTypeToUncompressedType(
    IMFMediaType *pType,    // Pointer to an encoded video type.
    const GUID& subtype,    // Uncompressed subtype (eg, RGB-32, AYUV)
    IMFMediaType **ppType   // Receives a matching uncompressed video type.
    )
{
    IMFMediaType *pTypeUncomp = NULL;

    HRESULT hr = S_OK;
    GUID majortype = { 0 };
    MFRatio par = { 0 };

    hr = pType->GetMajorType(&majortype);

    if (majortype != MFMediaType_Video)
    {
        return MF_E_INVALIDMEDIATYPE;
    }

    // Create a new media type and copy over all of the items.
    // This ensures that extended color information is retained.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pTypeUncomp);
    }

    if (SUCCEEDED(hr))
    {
        hr = pType->CopyAllItems(pTypeUncomp);
    }

    // Set the subtype.
    if (SUCCEEDED(hr))
    {
        hr = pTypeUncomp->SetGUID(MF_MT_SUBTYPE, subtype);
    }

    // Uncompressed means all samples are independent.
    if (SUCCEEDED(hr))
    {
        hr = pTypeUncomp->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
    }

    // Fix up PAR if not set on the original type.
    if (SUCCEEDED(hr))
    {
        hr = MFGetAttributeRatio(
            pTypeUncomp, 
            MF_MT_PIXEL_ASPECT_RATIO, 
            (UINT32*)&par.Numerator, 
            (UINT32*)&par.Denominator
            );

        // Default to square pixels.
        if (FAILED(hr))
        {
            hr = MFSetAttributeRatio(
                pTypeUncomp, 
                MF_MT_PIXEL_ASPECT_RATIO, 
                1, 1
                );
        }
    }

    if (SUCCEEDED(hr))
    {
        *ppType = pTypeUncomp;
        (*ppType)->AddRef();
    }

    SafeRelease(&pTypeUncomp);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="0d580-171">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d580-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d580-172">Informações de cores estendidas</span><span class="sxs-lookup"><span data-stu-id="0d580-172">Extended Color Information</span></span>](extended-color-information.md)
</dt> <dt>

[<span data-ttu-id="0d580-173">Stride da imagem</span><span class="sxs-lookup"><span data-stu-id="0d580-173">Image Stride</span></span>](image-stride.md)
</dt> <dt>

[<span data-ttu-id="0d580-174">Tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="0d580-174">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="0d580-175">Tipos de mídia de vídeo</span><span class="sxs-lookup"><span data-stu-id="0d580-175">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="0d580-176">GUIDs de subtipo de vídeo</span><span class="sxs-lookup"><span data-stu-id="0d580-176">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> </dl>

 

 



