---
description: Especifica se o codec deve usar a otimização de perceptiva conservadora durante a codificação.
ms.assetid: f44fd932-d8f8-46c7-b17c-27e6141408ab
title: Propriedade MFPKEY_PERCEPTUALOPTLEVEL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f9eb74ae025dbddbdea7f76c2af8b15e912cf80ebd06e810a5214bf9798d1bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953846"
---
# <a name="mfpkey_perceptualoptlevel-property"></a>\_Propriedade MFPKEY PERCEPTUALOPTLEVEL

Especifica se o codec deve usar a otimização de perceptiva conservadora durante a codificação.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCPerceptualOptLevel

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

0

## <a name="remarks"></a>Comentários

A otimização de perceptiva conservadora é um processo pelo qual o codec tenta identificar regiões "importantes" e "não importantes" no quadro de vídeo. Depois de identificar essas regiões do quadro, o codec dará uma prioridade mais alta à qualidade das regiões importantes, às custas da qualidade de regiões não importantes.

A otimização de perceptiva enfatiza a aparência da imagem correta para o olho humano, em vez de insistir na precisão matemática estrita.

Os resultados da otimização irão variar consideravelmente dependendo do tipo de vídeo que está sendo codificado. Esse recurso pode ser adequado para a baixa taxa de bits e a codificação de baixa resolução (por exemplo, web streaming), mas provavelmente deve ser evitado ao mirar a qualidade do vídeo de arquivamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




