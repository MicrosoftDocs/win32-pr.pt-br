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
# <a name="uncompressed-video-media-types"></a>Tipos de mídia de vídeo descompactados

Este tópico descreve como criar um tipo de mídia que descreve um formato de vídeo descompactado. Para obter mais informações sobre tipos de mídia em geral, consulte [sobre tipos de mídia](about-media-types.md).

Para criar um tipo de vídeo descompactado completo, defina os atributos a seguir no ponteiro de interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .



| Atributo                                                                            | Descrição                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md)                            | Tipo principal. Defina como **\_ vídeo MFMediaType**.                                                                                                                                                                                          |
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)                                   | Subtipo. Consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).                                                                                                                                                                        |
| [**\_ \_ Stride padrão MF \_ MT**](mf-mt-default-stride-attribute.md)                    | Stride da superfície. O *Stride* é o número de bytes necessários para passar de uma linha de pixels para a próxima. Defina esse atributo se o stride em bytes não for igual à largura do vídeo em bytes. Caso contrário, você pode omitir esse atributo. |
| [**\_taxa de \_ quadros MF MT \_**](mf-mt-frame-rate-attribute.md)                            | Taxa de quadros.                                                                                                                                                                                                                         |
| [**\_tamanho do \_ quadro MF MT \_**](mf-mt-frame-size-attribute.md)                            | Tamanho do quadro.                                                                                                                                                                                                                         |
| [**\_modo de \_ entrelaçamento do MF MT \_**](mf-mt-interlace-mode-attribute.md)                    | Modo de entrelaçamento.                                                                                                                                                                                                                   |
| [**\_ \_ todos os exemplos do MF MT são \_ \_ independentes**](mf-mt-all-samples-independent-attribute.md) | Especifica se cada amostra é independente. Defina como **verdadeiro** para formatos não compactados.                                                                                                                                             |
| [**taxa de proporção de pixel do MF \_ MT \_ \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md)           | Taxa de proporção de pixel.                                                                                                                                                                                                                 |



 

Além disso, defina os atributos a seguir se você souber os valores corretos. (Caso contrário, omita esses atributos.)



| Atributo                                                                    | Descrição        |
|------------------------------------------------------------------------------|--------------------|
| [**\_ \_ primários de vídeo MF MT \_**](mf-mt-video-primaries-attribute.md)          | Primárias de cores.   |
| [**função de transferência do MF \_ MT \_ \_**](mf-mt-transfer-function-attribute.md)      | Função de transferência. |
| [**\_ \_ matriz YUV do MF MT \_**](mf-mt-yuv-matrix-attribute.md)                    | Matriz de transferência.   |
| [**\_vídeo MF \_ MT \_ croma \_ localizando**](mf-mt-video-chroma-siting-attribute.md) | Croma localizando.     |
| [**\_ \_ intervalo nominal de vídeo MF MT \_ \_**](mf-mt-video-nominal-range-attribute.md) | Intervalo nominal.     |



 

Para obter mais informações, consulte [informações de cores estendidas](extended-color-information.md). Por exemplo, se você criar um tipo de mídia que descreve um padrão de vídeo e o padrão definir croma localizando, adicione essas informações ao tipo de mídia. Isso ajuda a preservar a fidelidade de cores em todo o pipeline.

As funções a seguir podem ser úteis ao criar um tipo de mídia de vídeo.



| Função                                                                     | Descrição                                                                                                                                                                          |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | Calcula a taxa de quadros, de acordo com a duração média do quadro.                                                                                                                         |
| [**MFCalculateImageSize**](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | Calcula o tamanho da imagem para um formato de vídeo descompactado.                                                                                                                          |
| [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | Calcula a duração média de um quadro de vídeo, dada a taxa de quadros.                                                                                                              |
| [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | Retorna o stride de superfície mínimo para um formato de vídeo. Para obter mais informações, consulte [Stride de imagem](image-stride.md).                                                                   |
| [**MFInitVideoFormat**](/windows/desktop/api/mfapi/nf-mfapi-mfinitvideoformat)                               | Inicializa uma estrutura [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) para alguns formatos de vídeo padrão, como televisão NTSC. Em seguida, você pode usar a estrutura para inicializar um tipo de mídia. |
| [**MFIsFormatYUV**](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | Consulta se um formato de vídeo é um formato YUV.                                                                                                                                      |



 

## <a name="examples"></a>Exemplos

Este exemplo mostra uma função que preenche as informações mais comuns para um formato de vídeo descompactado. A função retorna um ponteiro de interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Em seguida, você pode adicionar atributos adicionais ao tipo de mídia, conforme necessário.


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



O exemplo a seguir usa um formato de vídeo codificado como entrada e cria um tipo de vídeo não compactado correspondente. Esse tipo seria adequado para ser definido em um codificador ou decodificador, por exemplo.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Informações de cores estendidas](extended-color-information.md)
</dt> <dt>

[Stride da imagem](image-stride.md)
</dt> <dt>

[Tipos de mídia](media-types.md)
</dt> <dt>

[Tipos de mídia de vídeo](video-media-types.md)
</dt> <dt>

[GUIDs de subtipo de vídeo](video-subtype-guids.md)
</dt> </dl>

 

 



