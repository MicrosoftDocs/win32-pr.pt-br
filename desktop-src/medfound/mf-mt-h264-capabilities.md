---
description: Especifica os sinalizadores de recursos para um fluxo de vídeo H. 264.
ms.assetid: 59EF18D6-6063-4EF3-BBFB-51A966CFF09E
title: Atributo MF_MT_H264_CAPABILITIES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 138cfa32fc50ebb02ca4d399a178b338e58016c64ae3486d7f7b4a76f3e47afe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741758"
---
# <a name="mf_mt_h264_capabilities-attribute"></a>Atributo de recursos do MF \_ MT \_ H264 \_

Especifica os sinalizadores de recursos para um fluxo de vídeo H. 264.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Comentários

Esse atributo se aplica aos tipos de mídia para os fluxos H. 264 transmitidos por USB. O valor corresponde ao campo **bmCapabilities** no descritor de quadro de vídeo UVC 1,5 H. 264.

Esse atributo também é usado com [codificadores de câmera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 




