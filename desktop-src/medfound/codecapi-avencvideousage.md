---
description: Define o uso de vídeo para um codificador de vídeo.
ms.assetid: 2A6941A3-CCA0-467C-AC8A-DADC2CD1D405
title: Propriedade CODECAPI_AVEncVideoUsage (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27568412613702846e99d0ca556cc59cdc4fc77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749548"
---
# <a name="codecapi_avencvideousage-property"></a>\_Propriedade CODECAPI AVEncVideoUsage

Define o uso de vídeo para um codificador de vídeo.

## <a name="data-type"></a>Tipo de dados

**ULONG (VT \_ UI4)**

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoUsage**

## <a name="remarks"></a>Comentários

Essa propriedade também é usada com [codificadores de câmera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).

[CODECAPI \_ AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md), CODECAPI \_ AVEncVideoUsage e [CODECAPI \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) são propriedades de codificador estáticos. Uma vez definido, eles só terão efeito depois que um tipo de mídia definido for chamado no pino de saída da câmera.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

