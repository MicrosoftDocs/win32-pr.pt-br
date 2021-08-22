---
description: Define a taxa máxima de entrada em tempo real dos quadros de vídeo sendo alimentados no codificador.
ms.assetid: ACBE8799-A81C-44C3-B985-88ADFB1E51B4
title: Propriedade CODECAPI_AVEncMaxFrameRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb4202dd2079cc013560947ef11581cdb24b92ad0aaaf544e12923d5e46b319
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974925"
---
# <a name="codecapi_avencmaxframerate-property"></a>\_Propriedade CODECAPI AVEncMaxFrameRate

Define a taxa máxima de entrada em tempo real dos quadros de vídeo sendo alimentados no codificador.

## <a name="data-type"></a>Tipo de dados

**ULONGULONG** (VT \_ UI8)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncMaxFrameRate**

## <a name="remarks"></a>Comentários

Essa propriedade permite que o chamador especifique a taxa máxima de entrada em tempo real dos quadros de vídeo sendo alimentados no codificador. Isso dá ao codificador uma indicação da taxa de que precisará processar os quadros de entrada. Isso é útil para codificadores que se definem em uma configuração de estado de energia específica com base na resolução e na taxa de quadros do vídeo de origem.

A taxa de quadros é expressa como uma taxa. Os bits superiores de 32 do valor do atributo contêm o numerador e os bits inferiores de 32 contêm o denominador. Por exemplo, se a taxa de quadros for de 30 quadros por segundo (FPS), a taxa será 30/1. Se a taxa de quadros for de 29,97 fps, a taxa será 30.000/1001.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server 2016 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

