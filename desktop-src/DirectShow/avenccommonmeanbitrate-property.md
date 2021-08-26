---
description: Especifica a taxa média de bits codificada, em bits por segundo. Essa propriedade só se aplica a constantes de taxa de bits constante (CBR) e a taxa de bits variável (VBR).
ms.assetid: 8519685a-4f5b-44af-ad46-09eba7a198c6
title: Propriedade AVEncCommonMeanBitRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05c1db672b09e257959a409182288cdfbfd271d0679335c9d9e14048c1e31781
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983776"
---
# <a name="avenccommonmeanbitrate-property"></a>Propriedade AVEncCommonMeanBitRate

Especifica a taxa média de bits codificada, em bits por segundo. Essa propriedade só se aplica a constantes de taxa de bits constante (CBR) e a taxa de bits variável (VBR).

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncCommonMeanBitRate**

## <a name="property-value"></a>Valor da propriedade

Os codificadores podem implementar essa propriedade como um conjunto enumerado ou como um intervalo linear.

## <a name="remarks"></a>Comentários

Essa propriedade também é usada com [codificadores de câmera H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).

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

 

