---
description: O número máximo de quadros que o codificador H.264 leva para responder a um comando.
ms.assetid: C856B2B0-4A06-436D-B589-B01DA86DB53D
title: MF_MT_H264_MAX_CODEC_CONFIG_DELAY atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efc3610f9fce8201e3381b9684e3ea5b76578d8a22f751821dd16b0d9742ffff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035194"
---
# <a name="mf_mt_h264_max_codec_config_delay-attribute"></a>Atributo \_ MF MT \_ H264 \_ MAX \_ CODEC \_ CONFIG \_ DELAY

O número máximo de quadros que o codificador H.264 leva para responder a um comando.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Comentários

Esse atributo se aplica a tipos de mídia para fluxos H.264 transmitidos por USB. O valor corresponde ao **campo bMaxCodecConfigDelay** no descritor de formato de vídeo UVC 1.2 H.264.

Esse atributo também é usado com codificadores de câmera [UVC 1.5 H.264](camera-encoder-h264-uvc-1-5.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 




