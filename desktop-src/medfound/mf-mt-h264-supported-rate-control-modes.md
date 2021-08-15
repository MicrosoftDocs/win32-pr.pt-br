---
description: Especifica os modos de controle de taxa com suporte para um fluxo de vídeo H. 264.
ms.assetid: DAA62ECD-AFA2-40C2-9B52-F2D581F4D894
title: Atributo MF_MT_H264_SUPPORTED_RATE_CONTROL_MODES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9665fd99635749e2400437e77cb89e74d2cb8675689f6f4b867a20ac82fadaec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692278"
---
# <a name="mf_mt_h264_supported_rate_control_modes-attribute"></a>\_Atributo de \_ \_ modos de \_ controle de taxa com suporte do \_ MF MT H264 \_

Especifica os modos de controle de taxa com suporte para um fluxo de vídeo H. 264.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Comentários

Esse atributo se aplica aos tipos de mídia para os fluxos H. 264 transmitidos por USB. O valor corresponde ao campo **bmSupportedRateControlModes** no descritor de formato de vídeo UVC 1,5 H. 264.

Esse atributo também é usado com [codificadores de câmera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 




