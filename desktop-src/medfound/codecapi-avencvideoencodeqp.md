---
description: Especifica o parâmetro de quantificação (QP) para codificação de vídeo.
ms.assetid: 9E3B5E2D-3583-4C89-BC2A-4AC3C5545673
title: Propriedade CODECAPI_AVEncVideoEncodeQP (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec6c746f2f3c902ca416097571abaf5953956cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814126"
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
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

