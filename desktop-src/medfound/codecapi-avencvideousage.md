---
description: Define o uso de vídeo para um codificador de vídeo.
ms.assetid: 2A6941A3-CCA0-467C-AC8A-DADC2CD1D405
title: CODECAPI_AVEncVideoUsage propriedade (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b6d3ee174fbc22ca7b1ab4e309d87112463740a075b497cc35033f8c96bbe8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777706"
---
# <a name="codecapi_avencvideousage-property"></a>Propriedade CODECAPI \_ AVEncVideoUsage

Define o uso de vídeo para um codificador de vídeo.

## <a name="data-type"></a>Tipo de dados

**ULONG (VT \_ UI4)**

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoUsage**

## <a name="remarks"></a>Comentários

Essa propriedade também é usada com codificadores de câmera [UVC 1.5 H.264](camera-encoder-h264-uvc-1-5.md).

[CODECAPI \_ AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md), \_ CODECAPI AVEncVideoUsage e [CODECAPI \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) são propriedades do codificador estático. Depois de definidas, elas só terão efeito depois que um tipo de mídia definido for chamado no pino de saída da câmera.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

