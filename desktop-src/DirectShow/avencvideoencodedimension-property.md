---
description: Especifica a largura e a altura do vídeo codificado, se o vídeo for cortado.
ms.assetid: d6217250-63ff-4dff-a357-ff4aaa764695
title: Propriedade AVEncVideoEncodeDimension (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d99a0c14cbb3f67f7aa1c634a59c5f4cb9184dcd861bc8f14023c4afcebcefa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159315"
---
# <a name="avencvideoencodedimension-property"></a>Propriedade AVEncVideoEncodeDimension

Especifica a largura e a altura do vídeo codificado, se o vídeo for cortado.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoEncodeDimension**

## <a name="property-value"></a>Valor da propriedade

Os 16 bits superiores do valor contêm a largura em pixels e os 16 bits inferiores contêm a altura em pixels.

## <a name="remarks"></a>Comentários

Os aplicativos podem definir essa propriedade para cortar o vídeo de entrada. O tamanho especificado deve ser menor que o tamanho dos quadros de vídeo de entrada. Use a propriedade [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md) para especificar os cantos esquerdo e superior do retângulo de recorte.

Os codificadores podem retornar essa propriedade como um recurso.

Essa propriedade também é usada com [codificadores de câmera H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).

Para codificadores de câmera UVC 1,5, não há suporte para [AVEncVideoEncodeOffsetOrigin](avencvideoencodeoffsetorigin-property.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | aplicativos Windows 2000 Professional \[ desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows \[ aplicativos da área de trabalho do servidor 2000 \| aplicativo UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

