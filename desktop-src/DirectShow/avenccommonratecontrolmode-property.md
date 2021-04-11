---
description: Especifica o modo de controle de taxa.
ms.assetid: 4a0d49b1-30da-4ebe-abff-3fceef6dd94a
title: Propriedade AVEncCommonRateControlMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d18d0d7cb68936326fb4c4ba08188e362fdc91d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163862"
---
# <a name="avenccommonratecontrolmode-property"></a>Propriedade AVEncCommonRateControlMode

Especifica o modo de controle de taxa.

Os aplicativos podem definir essa propriedade para especificar o modo de controle de taxa. Os codificadores também podem retornar essa propriedade como um recurso.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncCommonRateControlMode**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade é um membro da enumeração [**eAVEncCommonRateControlMode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode) .

## <a name="remarks"></a>Comentários

Essa propriedade também é usada com [codificadores de câmera H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).

[CODECAPI \_ AVEncVideoTemporalLayerCount](/windows/desktop/medfound/codecapi-avencvideotemporallayercount), [CODECAPI \_ AVEncVideoUsage](/windows/desktop/medfound/codecapi-avencvideousage)e CODECAPI \_ AVEncCommonRateControlMode são propriedades de codificador estáticos. Uma vez definido, eles só terão efeito depois que um tipo de mídia definido for chamado no pino de saída da câmera.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

