---
description: Define a contagem de camadas temporais de vídeo para um codificador de vídeo.
ms.assetid: 36E1C86B-86D0-40CB-8F96-061FC653E9C3
title: Propriedade CODECAPI_AVEncVideoTemporalLayerCount (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a81ceaf82d9d202e97927e0e141aa03a4e8e27c49a28880509aa9bb3c24f9319
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743830"
---
# <a name="codecapi_avencvideotemporallayercount-property"></a>\_Propriedade CODECAPI AVEncVideoTemporalLayerCount

Define a contagem de camadas temporais de vídeo para um codificador de vídeo.

## <a name="data-type"></a>Tipo de dados

**ULONG (VT \_ UI4)**

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoTemporalLayerCount**

## <a name="remarks"></a>Comentários

Essa propriedade também é usada com [codificadores de câmera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).

CODECAPI \_ AVEncVideoTemporalLayerCount, [CODECAPI \_ AVEncVideoUsage](codecapi-avencvideousage.md)e [CODECAPI \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) são propriedades de codificador estáticos. Uma vez definido, eles só terão efeito depois que um tipo de mídia definido for chamado no pino de saída da câmera.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

