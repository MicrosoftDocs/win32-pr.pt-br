---
description: Especifica os cantos esquerdo e superior do retângulo de recorte, se o vídeo for cortado.
ms.assetid: 8ce8b3b8-dd91-41e1-a4ba-b0c2d9d0edd2
title: Propriedade AVEncVideoEncodeOffsetOrigin (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fdc4ffd1f168fa98ce71937b5ddc22d429c573481575432e94964fdfc5205b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119275756"
---
# <a name="avencvideoencodeoffsetorigin-property"></a>Propriedade AVEncVideoEncodeOffsetOrigin

Especifica os cantos esquerdo e superior do retângulo de recorte, se o vídeo for cortado.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoEncodeOffsetOrigin**

## <a name="property-value"></a>Valor da propriedade

Os 16 bits superiores do valor contêm o deslocamento da borda esquerda do quadro de entrada, em pixels. Os 16 bits inferiores contêm o deslocamento da borda superior do quadro de entrada, em pixels.

## <a name="remarks"></a>Comentários

Os aplicativos podem definir essa propriedade para cortar o vídeo de entrada. Use a propriedade [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md) para especificar a largura e a altura do retângulo de recorte.

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

 

 




