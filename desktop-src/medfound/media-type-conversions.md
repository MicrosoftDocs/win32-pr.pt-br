---
description: Conversões de tipo de mídia
ms.assetid: 6aee18b8-79b1-47fb-816f-d1c2c77b3a03
title: Conversões de tipo de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5d91844a062d5d4a1aa98af1a2e77c9cabfadb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474342"
---
# <a name="media-type-conversions"></a>Conversões de tipo de mídia

ocasionalmente, é necessário converter entre Media Foundation tipos de mídia e as estruturas de tipo de mídia mais antigas de DirectShow ou o SDK do formato de mídia Windows.

### <a name="from-a-format-structure-to-a-media-foundation-type"></a>De uma estrutura de formato para um tipo de Media Foundation

As funções a seguir inicializam um tipo de mídia Media Foundation de uma estrutura de formato. Essas funções também serão úteis se um fluxo de dados ou um cabeçalho de arquivo contiver uma estrutura de formato. Por exemplo, o cabeçalho de arquivo para arquivos de áudio de som WAVE contém uma estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .




| Estrutura a ser convertida | Função | 
|----------------------|----------|
| <a href="/windows/win32/api/strmif/ns-strmif-am_media_type"><strong>AM_MEDIA_TYPE</strong></a> (DirectShow)<br /><a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type"><strong>DMO_MEDIA_TYPE</strong></a> (objetos de mídia do DirectX) <br /><a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type"><strong>WM_MEDIA_TYPE</strong></a> (SDK do formato de mídia do Windows) <br /><blockquote>[!Note]<br />Essas estruturas são equivalentes.</blockquote><br /><br /> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromammediatype"><strong>MFInitMediaTypeFromAMMediaType</strong></a> | 
| <a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader"><strong>BITMAPINFOHEADER</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatevideomediatypefrombitmapinfoheaderex"><strong>MFCreateVideoMediaTypeFromBitMapInfoHeaderEx</strong></a> | 
| <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat"><strong>MFVIDEOFORMAT</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommfvideoformat"><strong>MFInitMediaTypeFromMFVideoFormat</strong></a> | 
| <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo"><strong>MPEG1VIDEOINFO</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg1videoinfo"><strong>MFInitMediaTypeFromMPEG1VideoInfo</strong></a> | 
| <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo"><strong>MPEG2VIDEOINFO</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg2videoinfo"><strong>MFInitMediaTypeFromMPEG2VideoInfo</strong></a> | 
| <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2"><strong>VIDEOINFOHEADER2</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader2"><strong>MFInitMediaTypeFromVideoInfoHeader2</strong></a> | 
| <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader"><strong>VIDEOINFOHEADER</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader"><strong>MFInitMediaTypeFromVideoInfoHeader</strong></a> | 
| <a href="/previous-versions/dd757713(v=vs.85)"><strong>WAVEFORMATEX</strong></a> ou <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)"> <strong>WAVEFORMATEXTENSIBLE</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex"><strong>MFInitMediaTypeFromWaveFormatEx</strong></a> | 




 

### <a name="from-a-media-foundation-type-to-a-format-structure"></a>De um tipo de Media Foundation para uma estrutura de formato

As funções a seguir criam ou inicializam uma estrutura de formato de um tipo de mídia Media Foundation.



| Função                                                                             | Estrutura de Destino                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFMediaType:: getrepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation)            | [**Am \_ \_Tipo de mídia**](/windows/win32/api/strmif/ns-strmif-am_media_type), [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat), [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)ou [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) |
| [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype)     | [**\_tipo de mídia am \_**](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |
| [**MFCreateMFVideoFormatFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemfvideoformatfrommfmediatype) | [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat)                                                                                                                                              |
| [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype)   | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) ou [ **WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))                                                                                    |
| [**MFInitAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype)         | [**\_tipo de mídia am \_**](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |



 

## <a name="format-mappings"></a>Mapeamentos de formato

As tabelas a seguir listam os atributos de Media Foundation que correspondem a várias estruturas de formato. Nem todos esses atributos podem ser convertidos diretamente. Para executar conversões, você deve usar as funções listadas na seção anterior; essas tabelas são fornecidas principalmente para referência.

### <a name="am_media_type"></a>\_tipo de mídia am \_



| Membro                   | Atributo                                                                            |
|--------------------------|--------------------------------------------------------------------------------------|
| **bTemporalCompression** | [**\_ \_ todos os exemplos do MF MT são \_ \_ independentes**](mf-mt-all-samples-independent-attribute.md) |
| **bFixedSizeSamples**    | [**\_amostras de \_ \_ tamanho fixo MF MT \_**](mf-mt-fixed-size-samples-attribute.md)           |
| **lSampleSize**          | [**tamanho de amostra do MF \_ MT \_ \_**](mf-mt-sample-size-attribute.md)                          |



 

### <a name="waveformatex-waveformatextensible"></a>WAVEFORMATEX, WAVEFORMATEXTENSIBLE



| Membro                  | Atributo                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **wFormatTag**          | [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)<br/> Se **wFormatTag** for \_ \_ extensível de formato Wave, o subtipo será encontrado no membro **subformate** .<br/> |
| **nChannels**           | [**\_canais de \_ número de áudio MF MT \_ \_**](mf-mt-audio-num-channels-attribute.md)                                                                                                |
| **nSamplesPerSec**      | [**\_amostras de áudio MF MT \_ \_ \_ por \_ segundo**](mf-mt-audio-samples-per-second-attribute.md)                                                                                   |
| **nAvgBytesPerSec**     | [**áudio do MF \_ MT \_ média de \_ \_ bytes \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md)                                                                              |
| **nBlockAlign**         | [**\_alinhamento de \_ bloco de áudio MF MT \_ \_**](mf-mt-audio-block-alignment-attribute.md)                                                                                          |
| **wBitsPerSample**      | [**\_bits de áudio MF MT \_ \_ \_ por \_ amostra**](mf-mt-audio-bits-per-sample-attribute.md)                                                                                         |
| **wValidBitsPerSample** | [**\_áudio MF \_ MT \_ \_ bits válidos \_ por \_ amostra**](mf-mt-audio-valid-bits-per-sample-attribute.md)                                                                            |
| **wSamplesPerBlock**    | [**\_amostras de áudio MF MT \_ \_ \_ por \_ bloco**](mf-mt-audio-samples-per-block-attribute.md)                                                                                     |
| **dwChannelMask**       | [**\_máscara de \_ canal de áudio MF MT \_ \_**](mf-mt-audio-channel-mask-attribute.md)                                                                                                |
| **SubFormat**           | [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)                                                                                                                        |
| Dados extras              | [**dados de usuário do MF \_ MT \_ \_**](mf-mt-user-data-attribute.md)                                                                                                                   |



 

### <a name="videoinfoheader-videoinfoheader2"></a>VIDEOINFOHEADER, VIDEOINFOHEADER2



| Membro                                         | Atributo                                                                                                                                                                                                                                        |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwBitRate**                                  | [**\_taxa de \_ \_ bits média de MF MT**](mf-mt-avg-bitrate-attribute.md)                                                                                                                                                                                      |
| **dwBitErrorRate**                             | [**\_taxa de \_ \_ erros de \_ bit \_ do MF MT**](mf-mt-avg-bit-error-rate-attribute.md)                                                                                                                                                                      |
| **AvgTimePerFrame**                            | [**MF \_ \_ \_ Taxa de quadros MT**](mf-mt-frame-rate-attribute.md); use [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) para calcular esse valor.                                                                             |
| **dwInterlaceFlags**                           | [**\_modo de \_ entrelaçamento do MF MT \_**](mf-mt-interlace-mode-attribute.md)                                                                                                                                                                                |
| **dwCopyProtectFlags**                         | Nenhum equivalente definido                                                                                                                                                                                                                            |
| **dwPictAspectRatioX**, **dwPictAspectRatioY** | [**MF \_ \_ \_ \_ Taxa**](mf-mt-pixel-aspect-ratio-attribute.md)de proporção de pixel MT; deve converter da taxa de proporção da imagem para a taxa de proporção da imagem.                                                                                                      |
| **dwControlFlags**                             | [**MF \_ \_sinalizadores de \_ controle \_ do pad MT**](mf-mt-pad-control-flags-attribute.md). Se o sinalizador **AMCONTROL \_ COLORINFO \_ presente** estiver presente, defina os atributos de cores estendidos descritos em [informações de cores estendidas](extended-color-information.md). |
| **bmiHeader. bilargura**, **BmiHeader. biHeight**  | [**\_tamanho do \_ quadro MF MT \_**](mf-mt-frame-size-attribute.md)                                                                                                                                                                                        |
| **bmiHeader.biBitCount**                       | Implícito no subtipo ([**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md)).                                                                                                                                                                    |
| **bmiHeader. biCompression**                    | Implícito no subtipo.                                                                                                                                                                                                                         |
| **bmiHeader.biSizeImage**                      | [**tamanho de amostra do MF \_ MT \_ \_**](mf-mt-sample-size-attribute.md)                                                                                                                                                                                      |
| Informações da paleta                            | [**\_paleta MF MT \_**](mf-mt-palette-attribute.md)                                                                                                                                                                                               |



 

Os atributos a seguir podem ser inferidos da estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) ou [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , mas também exigem algum conhecimento dos detalhes do formato. Por exemplo, diferentes formatos YUV têm requisitos de Stride diferentes.

-   [**\_ \_ Stride padrão MF \_ MT**](mf-mt-default-stride-attribute.md)
-   [**\_abertura de \_ \_ exibição mínima \_ de MF MT**](mf-mt-minimum-display-aperture-attribute.md)
-   [**\_abertura de \_ digitalização de Pan MT \_ MF \_**](mf-mt-pan-scan-aperture-attribute.md)

### <a name="mpeg1videoinfo"></a>MPEG1VIDEOINFO



| Membro                                   | Atributo                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------|
| **dwStartTimeCode**                      | [**código de hora de início do MF \_ MT \_ MPEG \_ \_ \_**](mf-mt-mpeg-start-time-code-attribute.md) |
| **bSequenceHeader**                      | [**cabeçalho de sequência do MF \_ MT \_ MPEG \_ \_**](mf-mt-mpeg-sequence-header-attribute.md)  |
| **biXPelsPerMeter**, **biYPelsPerMeter** | [**taxa de proporção de pixel do MF \_ MT \_ \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md)      |



 

### <a name="mpeg2videoinfo"></a>MPEG2VIDEOINFO



| Membro               | Atributo                                                                       |
|----------------------|---------------------------------------------------------------------------------|
| **dwStartTimeCode**  | [**código de hora de início do MF \_ MT \_ MPEG \_ \_ \_**](mf-mt-mpeg-start-time-code-attribute.md) |
| **dwSequenceHeader** | [**cabeçalho de sequência do MF \_ MT \_ MPEG \_ \_**](mf-mt-mpeg-sequence-header-attribute.md)  |
| **dwProfile**        | [**\_Perfil MF \_ MT \_**](mf-mt-mpeg2-profile-attribute.md)                 |
| **dwLevel**          | [**Nível de MPEG2 do MF \_ MT \_ \_**](mf-mt-mpeg2-level-attribute.md)                     |
| **dwFlags**          | [**Sinalizadores de MPEG2 do MF \_ MT \_ \_**](mf-mt-mpeg2-flags-attribute.md)                     |



 

## <a name="examples"></a>Exemplos

O código a seguir preenche uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) de um tipo de mídia de vídeo. Observe que essas conversões perdem algumas das informações de formato (entrelaçamento, taxa de quadros, dados de cores estendidos). No entanto, pode ser útil ao salvar um bitmap de um quadro de vídeo, por exemplo.


```C++
#include <dshow.h>
#include <dvdmedia.h>

// Converts a video type to a BITMAPINFO structure.
// The caller must free the structure by calling CoTaskMemFree.

// Note that this conversion loses some format information, including 
// interlacing, and frame rate.

HRESULT GetBitmapInfoHeaderFromMFMediaType(
    IMFMediaType *pType,            // Pointer to the media type.
    BITMAPINFOHEADER **ppBmih,      // Receives a pointer to the structure. 
    DWORD *pcbSize)                 // Receives the size of the structure.
{
    *ppBmih = NULL;
    *pcbSize = 0;

    GUID majorType = GUID_NULL;
    AM_MEDIA_TYPE *pmt = NULL;
    DWORD cbSize = 0;
    DWORD cbOffset = 0;
    BITMAPINFOHEADER *pBMIH = NULL;

    // Verify that this is a video type.
    HRESULT hr = pType->GetMajorType(&majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    if (majorType != MFMediaType_Video)
    {
        hr = MF_E_INVALIDMEDIATYPE;
        goto done;
    }

    hr = pType->GetRepresentation(AM_MEDIA_TYPE_REPRESENTATION, (void**)&pmt);
    if (FAILED(hr))
    {
        goto done;
    }

    if (pmt->formattype == FORMAT_VideoInfo)
    {
        cbOffset = (FIELD_OFFSET(VIDEOINFOHEADER,bmiHeader));
    }
    else if (pmt->formattype == FORMAT_VideoInfo2)
    {
        cbOffset = (FIELD_OFFSET(VIDEOINFOHEADER2,bmiHeader));
    }
    else
    {
        hr = MF_E_INVALIDMEDIATYPE; // Unsupported format type.
        goto done;
    }

    if (pmt->cbFormat - cbOffset < sizeof(BITMAPINFOHEADER))
    {
        hr = E_UNEXPECTED; // Bad format size. 
        goto done;
    }

    cbSize = pmt->cbFormat - cbOffset;

    pBMIH = (BITMAPINFOHEADER*)CoTaskMemAlloc(cbSize);
    if (pBMIH == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }
    
    CopyMemory(pBMIH, pmt->pbFormat + cbOffset, cbSize);
    
    *ppBmih = pBMIH;
    *pcbSize = cbSize;

done:
    if (pmt)
    {
        pType->FreeRepresentation(AM_MEDIA_TYPE_REPRESENTATION, pmt);
    }
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de mídia](media-types.md)
</dt> </dl>

 

 
