---
description: Esse filtro decodifica o vídeo MPEG-1, MPEG-2, H.264.
ms.assetid: d8195c3a-97ac-4ad1-a097-18878c8fda6f
title: Decodificador de vídeo do Microsoft MPEG-2 (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4afdd9609124ba1057f597c4b7a907654c62a321
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982189"
---
# <a name="microsoft-mpeg-2-video-decoder"></a>Decodificador de vídeo do Microsoft MPEG-2

Esse filtro decodifica o vídeo MPEG-1, MPEG-2, H.264.

> [!Note]  
> A decodificação do vídeo H.264 requer Windows 7.

 

> [!Note]  
> Não há suporte para esse filtro em plataformas baseadas em IA-64.

 

No Registro, o nome amigável desse filtro é "Decodificador de Vídeo DTV-DVD da Microsoft".



Informações de filtro

Interfaces de filtro

[**IAMDecoderCaps**](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps)<br/> [**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

Tipos de mídia de pino de entrada

Pino de entrada de vídeo:

-   MEDIATYPE \_ DVD \_ ENCRYPTED \_ PACK, MEDIASUBTYPE \_ MPEG2 \_ VIDEO
-   MEDIATYPE \_ MPEG2 \_ PES, MEDIASUBTYPE \_ MPEG2 \_ VIDEO
-   VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ MPEG1Packet
-   VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ MPEG1Payload
-   VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ MPEG2 \_ VIDEO

Pino de entrada da subpicture:<br/>

-   MEDIATYPE \_ DVD \_ ENCRYPTED \_ PACK, MEDIASUBTYPE \_ DVD \_ SUBPICTURE

A partir do Windows 7, o pin de entrada de vídeo também dá suporte aos seguintes tipos de entrada:<br/>

-   **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ AVC1**
-   **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ H264**
-   **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ h264**
-   **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ X264**
-   **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ x264**

Consulte [Tipos de vídeo H.264](h-264-video-types.md) para obter mais informações. O tipo de mídia de entrada pode mudar dinamicamente entre os tipos MPEG2 e H.264.<br/>

Interfaces de pino de entrada

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**Imeminputpin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IMFSampleProtection**](/windows/win32/api/mfidl/nn-mfidl-imfsampleprotection)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**Iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipos de mídia de pino de saída

Pino de saída de vídeo:

-   Vídeo \_ MEDIATYPE, modo DXVAMPEG2 \_ \_ A (DXVA 1.0)
-   Vídeo \_ MEDIATYPE, modo DXVAMPEG2 \_ \_ C (DXVA 1.0)
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ I420 (Decodificador de software ou DXVA2.0)
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ NV12 (Decodificar software ou DXVA2.0)
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ YUY2 (Decodificador de software ou DXVA2.0)
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ IMC3 (somente DXVA2.0)
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ IMC4 (somente DXVA2.0)
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ S340 (somente DXVA2.0)
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ YV12 (somente DXVA2.0)

Pino de saída da linha 21:<br/>

-   MEDIATYPE \_ AUXLine21Data, MEDIASUBTYPE \_ Line21 \_ GOPPacket

Pino de saída da subpicture:<br/>

-   VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ AI44
-   VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ ARGB32
-   VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ ARGB4444
-   VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ AYUV

Interfaces de pino de saída

[**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) (somente pin de saída de vídeo)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**Imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**Iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig)<br/>

Filtrar CLSID

**CLSID \_ CMPEG2VidDecoderDS** (definido em wmcodecdsp.h)

Executável

msmpeg2vdec.dll

[Mérito](merit.md)

**VALOR \_ NORMAL** – 1

[Categoria de filtro](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Comentários

Esse filtro tem dois pinos de entrada e três pinos de saída.

Pinos de entrada:

-   Entrada de vídeo
-   Entrada de subtípico

Pinos de saída:

-   Saída de vídeo
-   Saída da linha 21
-   Saída da subpicture

O filtro não cria o pino de saída da subpicture, a menos que o pino de entrada de vídeo esteja conectado a um tipo de mídia **MEDIATYPE \_ DVD \_ ENCRYPTED \_ PACK.**

### <a name="mpeg-12-support"></a>Suporte a MPEG-1/2

Para MPEG-1 e MPEG-2, o decodificador dá suporte aos seguintes formatos:




| Rótulo | Valor |
|--------|-------|
| Perfis/Níveis | Qualquer combinação dos seguintes perfis e níveis:<br /><ul><li>Perfis: Simples, Principal</li><li>Níveis: Baixo, Principal, Alto, Alto 1440</li></ul> | 
| Formatos Chroma | 4:2:0 chroma | 
| Resolução máxima | 1920 × 1088 pixels | 
| DXVA | O decodificador dá suporte à DXVA (Aceleração de Vídeo DirectX) versão 1 e versão 2. | 




 

O decodificador não dá suporte a bitstreams escalonáveis. A entrada deve ser um fluxo de vídeo elementar.

O decodificador não dá suporte a formatos chroma 4:2:2.

### <a name="h264-support"></a>Suporte a H.264

Para H.264, o decodificador dá suporte aos seguintes formatos:



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Perfis/Níveis    | Perfis de Linha de Base, Principal e Alto, até o nível 5.1. (Confira Especificação de ITU-T H.264 para obter detalhes.)                                                                                                                                                                          |
| Formatos Chroma     | 4:2:0 chroma ou monocromático                                                                                                                                                                                                                                                |
| Resolução mínima | 48 × 48 pixels                                                                                                                                                                                                                                                            |
| Resolução máxima | 1920 × 1088 pixels                                                                                                                                                                                                                                                        |
| DXVA               | O decodificador dá suporte ao DXVA versão 2, mas não à DXVA versão 1. A decodificação DXVA tem suporte apenas para bitstreams de Linha de Base, Principal e Alto perfil compatíveis com main. (Os bitstreams de linha de base compatíveis com a principal são definidos como **perfil \_ idc**=66 e sinalizador **\_ set1 \_ restrito**=1.) |



 

O decodificador não dá suporte à tecnologia Decodificador Decodificador.

Para obter informações sobre os tipos de mídia H.264, consulte [Tipos de vídeo H.264](h-264-video-types.md).

### <a name="codec-properties"></a>Propriedades do Codec

Os pinos de entrada suportam os seguintes conjuntos de propriedades por [**meio de IKsPropertySet**](ikspropertyset.md):

-   [**Conjunto de propriedades de proteção de cópia de DVD**](dvd-copy-protection-property-set.md)
-   [**Conjunto de propriedades da Subpicture dvd**](dvd-subpicture-property-set.md) (somente pin de subpicture)

Os pinos de entrada suportam as seguintes propriedades por [**meio de ICodecAPI:**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)



| Propriedade                                                                  | Exige      |
|---------------------------------------------------------------------------|---------------|
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md)         | Windows Vista |
| [**AVDecVideoInputScanType**](avdecvideoinputscantype-property.md)       | Windows Vista |
| [**AVDecVideoPixelAspectRatio**](avdecvideopixelaspectratio-property.md) | Windows Vista |



 

O filtro dá suporte às seguintes propriedades por [**meio de ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Propriedade                                                                                | Exige      |
|-----------------------------------------------------------------------------------------|---------------|
| [**AVDecMmcssClass**](avdecmmcss-property.md)                                          | Windows Vista |
| [**AVDecVideoAcceleration \_ H264**](avdecvideoacceleration-h264-property.md)            | Windows 7     |
| [**AVDecVideoAcceleration \_ MPEG2**](avdecvideoacceleration-mpeg2-property.md)          | Windows 7     |
| [**AVDecVideoDropPicWithMissingRef**](avdecvideodroppicwithmissingref-property.md)     | Windows 7     |
| [**AVDecVideoFastDecodeMode**](avdecvideofastdecodemode.md)                            | Windows 7     |
| [**AVDecVideoImageSize**](avdecvideoimagesize.md)                                      | Windows 7     |
| [**AVDecVideoSoftwareDeintermodMode**](avdecvideosoftwaredeinterlacemode-property.md) | Windows 7     |
| [**AVDecVideoThumbnailGenerationMode**](avdecvideothumbnailgenerationmode-property.md) | Windows 7     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Aplicativos de área de trabalho \[ ultimate\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[**Tipos de mídia de DVD**](dvd-media-types.md)
</dt> <dt>

[Tipos de vídeo H.264](h-264-video-types.md)
</dt> </dl>

 

 
