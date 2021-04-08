---
description: Retorna o número de quadros de vídeo que foram codificados.
ms.assetid: ade9fe69-b3dd-44aa-856b-75d4a7e4c680
title: Propriedade AVEncStatVideoCodedFrames (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aed3ed0a06003807a6bd0db90b8978282042daf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087701"
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
| Cliente mínimo com suporte<br/> | Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




