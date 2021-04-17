---
description: Define a taxa máxima de entrada em tempo real dos quadros de vídeo sendo alimentados no codificador.
ms.assetid: ACBE8799-A81C-44C3-B985-88ADFB1E51B4
title: Propriedade CODECAPI_AVEncMaxFrameRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c04d1fd1297f299db133cd98bd493c968fcc29c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748112"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

