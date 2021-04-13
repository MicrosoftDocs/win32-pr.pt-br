---
description: Esse filtro decodifica o vídeo MPEG-1, MPEG-2, H. 264.
ms.assetid: d8195c3a-97ac-4ad1-a097-18878c8fda6f
title: Decodificador de vídeo do Microsoft MPEG-2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8460b5b554fffc8f0dd8679810e5ef3f42bcb004
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370105"
---
# <a name="microsoft-mpeg-2-video-decoder"></a>Decodificador de vídeo do Microsoft MPEG-2

Esse filtro decodifica o vídeo MPEG-1, MPEG-2, H. 264.

> [!Note]  
> A decodificação do vídeo H. 264 requer o Windows 7.

 

> [!Note]  
> Não há suporte para esse filtro em plataformas baseadas em IA-64.

 

No registro, o nome amigável desse filtro é "decodificador de vídeo Microsoft DTV-DVD".



Informações de filtro

Filtrar interfaces

[**IAMDecoderCaps**](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps)<br/> [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

Tipos de mídia de pino de entrada

Pino de entrada de vídeo:

-   \_ \_ Pacote de DVD criptografado \_ de MediaType, vídeo do MEDIASUBTYPE \_ MPEG2 \_
-   \_ \_ Vídeo de MediaType MPEG2 PES, MEDIASUBTYPE \_ MPEG2 \_
-   \_Vídeo de MediaType, MEDIASUBTYPE \_ MPEG1Packet
-   \_Vídeo de MediaType, MEDIASUBTYPE \_ MPEG1Payload
-   \_Vídeo de MediaType, vídeo do MEDIASUBTYPE \_ MPEG2 \_

Pino de entrada da subimagem:<br/>

-   \_ \_ pacote de DVD criptografado \_ de MediaType, \_ SUBimagem de DVD MEDIASUBTYPE \_

A partir do Windows 7, o PIN de entrada de vídeo também dá suporte aos seguintes tipos de entrada:<br/>

-   **MediaType \_ Vídeo**, **MEDIASUBTYPE \_ AVC1**
-   **MediaType \_ Vídeo**, **MEDIASUBTYPE \_ H264**
-   **MediaType \_ Vídeo**, **MEDIASUBTYPE \_ H264**
-   **MediaType \_ Vídeo**, **MEDIASUBTYPE \_ x264**
-   **MediaType \_ Vídeo**, **MEDIASUBTYPE \_ x264**

Consulte [tipos de vídeo H. 264](h-264-video-types.md) para obter mais informações. O tipo de mídia de entrada pode ser alterado dinamicamente entre os tipos MPEG2 e H. 264.<br/>

Interfaces de pino de entrada

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IMFSampleProtection**](/windows/win32/api/mfidl/nn-mfidl-imfsampleprotection)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipos de mídia do pino de saída

Pino de saída do vídeo:

-   Vídeo de MEDIATYPE \_ , DXVA \_ ModeMPEG2 \_ A (DXVA 1,0)
-   \_Vídeo de MediaType, DXVA \_ ModeMPEG2 \_ C (DXVA 1,0)
-   \_Vídeo de MediaType, MEDIASUBTYPE \_ I420 (decodificação de software ou DXVA 2.0)
-   \_Vídeo de MediaType, MEDIASUBTYPE \_ NV12 (decodificação de software ou DXVA 2.0)
-   \_Vídeo de MediaType, MEDIASUBTYPE \_ YUY2 (decodificação de software ou DXVA 2.0)
-   \_Vídeo de MediaType, MEDIASUBTYPE \_ IMC3 (somente DXVA 2.0)
-   \_Vídeo de MediaType, MEDIASUBTYPE \_ IMC4 (somente DXVA 2.0)
-   \_Vídeo de MediaType, MEDIASUBTYPE \_ S340 (somente DXVA 2.0)
-   \_Vídeo de MediaType, MEDIASUBTYPE \_ YV12 (somente DXVA 2.0)

Pino de saída de linha-21:<br/>

-   MEDIATYPE \_ AUXLine21Data, MEDIASUBTYPE \_ Line21 \_ GOPPacket

Pino de saída da subimagem:<br/>

-   \_Vídeo de MediaType, MEDIASUBTYPE \_ AI44
-   \_Vídeo de MediaType, MEDIASUBTYPE \_ ARGB32
-   \_Vídeo de MediaType, MEDIASUBTYPE \_ ARGB4444
-   \_Vídeo de MediaType, MEDIASUBTYPE \_ AYUV

Interfaces de pino de saída

[**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) (somente PIN de saída de vídeo)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig)<br/>

CLSID do filtro

**CLSID \_ do CMPEG2VidDecoderDS** (definido em wmcodecdsp. h)

Executável

msmpeg2vdec.dll

[Núcleo](merit.md)

**Mérito \_ NORMAL** -1

[Categoria do filtro](filter-categories.md)

**\_LEGACYAMFILTERCATEGORY CLSID**



 

## <a name="remarks"></a>Comentários

Esse filtro tem dois Pins de entrada e três Pins de saída.

Pins de entrada:

-   Entrada de vídeo
-   Entrada de subimagem

Pins de saída:

-   Saída de vídeo
-   Saída de linha 21
-   Saída da subimagem

O filtro não criará o pino de saída da subimagem, a menos que o pino de entrada de vídeo esteja conectado a um tipo de mídia de **\_ \_ \_ pacote criptografado de DVD de MediaType** .

### <a name="mpeg-12-support"></a>Suporte a MPEG-1/2

Para MPEG-1 e MPEG-2, o decodificador dá suporte aos seguintes formatos:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Perfis/níveis</td>
<td>Qualquer combinação dos seguintes perfis e níveis:<br/>
<ul>
<li>Perfis: simples, principal</li>
<li>Níveis: baixo, principal, alto, alto 1440</li>
</ul></td>
</tr>
<tr class="even">
<td>Formatos de croma</td>
<td>4:2:0 croma</td>
</tr>
<tr class="odd">
<td>Resolução máxima</td>
<td>1920 × 1088 pixels</td>
</tr>
<tr class="even">
<td>DXVA</td>
<td>O decodificador dá suporte a DXVA (DirectX Video Acceleration) versão 1 e à versão 2.</td>
</tr>
</tbody>
</table>



 

O decodificador não dá suporte a fragmentado escalonáveis. A entrada deve ser um fluxo de vídeo elementar.

O decodificador não oferece suporte a formatos de 4:2:2 croma.

### <a name="h264-support"></a>Suporte a H. 264

Para H. 264, o decodificador dá suporte aos seguintes formatos:



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Perfis/níveis    | Perfis de linha de base, principal e alto, até o nível 5,1. (Consulte Especificação ITU-T H. 264 para obter detalhes.)                                                                                                                                                                          |
| Formatos de croma     | 4:2:0 croma ou monocromático                                                                                                                                                                                                                                                |
| Resolução mínima | 48 × 48 pixels                                                                                                                                                                                                                                                            |
| Resolução máxima | 1920 × 1088 pixels                                                                                                                                                                                                                                                        |
| DXVA               | O decodificador oferece suporte a DXVA versão 2, mas não a DXVA versão 1. A decodificação de DXVA tem suporte apenas para fragmentado de linha de base, principal e de perfil alto compatíveis com o principal. (Fragmentado de linha de base compatíveis principal são definidos como **perfil \_ idc**= 66 e **\_ \_ sinalizador conjunto1 restrito**= 1.) |



 

O decodificador não oferece suporte à tecnologia de refinamento de filmes.

Para obter informações sobre os tipos de mídia H. 264, consulte [tipos de vídeo h. 264](h-264-video-types.md).

### <a name="codec-properties"></a>Propriedades do codec

Os Pins de entrada dão suporte aos seguintes conjuntos de propriedades por meio de [**IKsPropertySet**](ikspropertyset.md):

-   [**Conjunto de propriedades da proteção contra cópia de DVD**](dvd-copy-protection-property-set.md)
-   [**Conjunto de propriedades de subimagem do DVD**](dvd-subpicture-property-set.md) (somente PIN da subimagem)

Os Pins de entrada dão suporte às seguintes propriedades por meio de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Propriedade                                                                  | Exige      |
|---------------------------------------------------------------------------|---------------|
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md)         | Windows Vista |
| [**AVDecVideoInputScanType**](avdecvideoinputscantype-property.md)       | Windows Vista |
| [**AVDecVideoPixelAspectRatio**](avdecvideopixelaspectratio-property.md) | Windows Vista |



 

O filtro oferece suporte às seguintes propriedades por meio de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Propriedade                                                                                | Exige      |
|-----------------------------------------------------------------------------------------|---------------|
| [**AVDecMmcssClass**](avdecmmcss-property.md)                                          | Windows Vista |
| [**AVDecVideoAcceleration \_ H264**](avdecvideoacceleration-h264-property.md)            | Windows 7     |
| [**AVDecVideoAcceleration \_ MPEG2**](avdecvideoacceleration-mpeg2-property.md)          | Windows 7     |
| [**AVDecVideoDropPicWithMissingRef**](avdecvideodroppicwithmissingref-property.md)     | Windows 7     |
| [**AVDecVideoFastDecodeMode**](avdecvideofastdecodemode.md)                            | Windows 7     |
| [**AVDecVideoImageSize**](avdecvideoimagesize.md)                                      | Windows 7     |
| [**AVDecVideoSoftwareDeinterlaceMode**](avdecvideosoftwaredeinterlacemode-property.md) | Windows 7     |
| [**AVDecVideoThumbnailGenerationMode**](avdecvideothumbnailgenerationmode-property.md) | Windows 7     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop apps\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                                                                     |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> <dt>

[**Tipos de mídia de DVD**](dvd-media-types.md)
</dt> <dt>

[Tipos de vídeo H. 264](h-264-video-types.md)
</dt> </dl>

 

 
