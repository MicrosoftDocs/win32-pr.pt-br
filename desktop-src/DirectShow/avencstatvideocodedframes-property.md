---
description: Retorna o número de quadros de vídeo que foram codificados.
ms.assetid: ade9fe69-b3dd-44aa-856b-75d4a7e4c680
title: Propriedade AVEncStatVideoCodedFrames (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34f8858aba7a36d79096eccad40990e1859d4073695aaf80910587bac4005d6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119342556"
---
# <a name="avencstatvideocodedframes-property"></a>Propriedade AVEncStatVideoCodedFrames

Retorna o número de quadros de vídeo que foram codificados.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncStatVideoCodedFrames**

## <a name="remarks"></a>Comentários

Essa propriedade estará disponível após a conclusão da codificação.

O valor dessa propriedade é igual à propriedade [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md) menos o número de quadros descartados. O codificador pode descartar quadros para permanecer dentro das restrições de taxa de bits especificadas. Ele também pode descartar quadros no final do fluxo (consulte a propriedade [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md) ).

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

 

 




