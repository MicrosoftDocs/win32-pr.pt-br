---
description: Especifica o parâmetro de quantificação (QP) para codificação de vídeo.
ms.assetid: 9E3B5E2D-3583-4C89-BC2A-4AC3C5545673
title: Propriedade CODECAPI_AVEncVideoEncodeQP (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ed7ba8e3cf522c1e3cfa07d22cf5e37639717c230ca571ffd89d9e1d513a0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974885"
---
# <a name="codecapi_avencvideoencodeqp-property"></a>\_Propriedade CODECAPI AVEncVideoEncodeQP

Especifica o parâmetro de quantificação (QP) para codificação de vídeo.

## <a name="data-type"></a>Tipo de dados

**ULONGLONG** (VT \_ UI8)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoEncodeQP**

## <a name="property-value"></a>Valor da propriedade

Um conjunto de campos de 4 16 bits usado para especificar o quadro QPs na codificação de QP fixa.

Os campos são:

-   Bits 0-15: QP padrão
-   Bits 16-31: QP usado para quadros I
-   Bits 32-47: QP usado para quadros P
-   Bits 48-63: QP usado para quadros B

## <a name="remarks"></a>Comentários

Essa propriedade também é usada com [codificadores de câmera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).

Para garantir o uso consistente em codificadores diferentes, você deve assumir que os codificadores só verão a QP padrão e podem ignorar valores de QP para imagens I/P/B.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

