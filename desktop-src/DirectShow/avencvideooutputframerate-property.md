---
description: Especifica a taxa de quadros no fluxo de saída do codificador, em quadros por segundo.
ms.assetid: 72e16c7d-977e-4269-9576-afc789e31826
title: Propriedade AVEncVideoOutputFrameRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f1e1105ad98564b8d837f35e574be25bcd6cb9506a2adddbc115129fcb65564
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540666"
---
# <a name="avencvideooutputframerate-property"></a>Propriedade AVEncVideoOutputFrameRate

Especifica a taxa de quadros no fluxo de saída do codificador, em quadros por segundo.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT64** (**VT \_ UI8**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoOutputFrameRate**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade é uma razão que define a taxa de quadros. Os bits superiores de 32 contêm o numerador e os bits inferiores de 32 contêm o denominador. A tabela a seguir mostra as taxas de quadros comuns, em quadros por segundo.



| Taxa de quadros | Proporção      |
|------------|------------|
| 23,97      | 24000/1001 |
| 24         | 24/1       |
| 25         | 25/1       |
| 29,97      | 30000/1001 |
| 30         | 30/1       |
| 50         | 50/1       |
| 59,94      | 60000/1001 |
| 60         | 60/1       |



 

## <a name="remarks"></a>Comentários

Os aplicativos podem definir essa propriedade para especificar a taxa de quadros de saída. Os codificadores também podem retornar essa propriedade como um recurso. Dependendo do codificador, o valor pode ser restrito à taxa de quadros de entrada. Caso contrário, o codificador será capaz de converter a taxa de quadros internamente. Consulte a [**Propriedade AVEncVideoOutputFrameRateConversion**](avencvideooutputframerateconversion-property.md).

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

 

