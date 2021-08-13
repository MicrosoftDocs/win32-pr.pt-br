---
description: Define o limite no qual o codificador considera um campo de vídeo redundante.
ms.assetid: db6c2f0e-f451-4d2d-984f-b507083e8358
title: Propriedade AVEncVideoInverseTeleariaThreshold (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 297dae601c5112714272a2d1c2e0b1a7ebeee5faa3aa2fabebc32e79c1745c9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119275175"
---
# <a name="avencvideoinversetelecinethreshold-property"></a>Propriedade AVEncVideoInverseTeleariaThreshold

Define o limite no qual o codificador considera um campo de vídeo redundante.

Essa propriedade é leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoInverseTeleariaThreshold**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade tem o intervalo a seguir.



| Valor | Descrição                                                    |
|-------|----------------------------------------------------------------|
| 0     | O codificador tem menos probabilidade de considerar campos de vídeo redundantes. |
| 100   | É mais provável que o codificador considere campos de vídeo redundantes. |



 

## <a name="remarks"></a>Comentários

De definir essa propriedade se o codificador estiver executando teletravas inversas com uma fonte de vídeo análoga.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[ aplicativos UWP da área de \| trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows aplicativos da área de trabalho do servidor 2000 \[ \| aplicativos UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do Codec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI Interface**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




