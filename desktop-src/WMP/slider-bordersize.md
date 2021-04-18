---
title: Controle deslizante. Borderize
description: O atributo Borderize especifica ou recupera a largura da borda em pixels.
ms.assetid: ca766b45-1be3-4207-8cd0-ad50c33d52be
keywords:
- Controle deslizante. Bordasize o Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.borderSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c3ebc95e3ecf04ae78fa78c4b46f38fdd910004
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756321"
---
# <a name="sliderbordersize"></a>Controle deslizante. Borderize

O atributo **borderize** especifica ou recupera a largura da borda em pixels.

``` syntax
        elementID.borderSize
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **número** de leitura/gravação (**longo**) que representa a largura da borda em pixels. O valor padrão é zero.

## <a name="remarks"></a>Comentários

Esse atributo define um deslocamento do início e do fim do controle deslizante que é, da esquerda e direita, se o atributo **Direction** estiver definido como "horizontal", e da parte superior e inferior se for definido como "vertical". Essas posições de deslocamento determinam as posições mínima e máxima do controle deslizante, além dos quais a cor ou a imagem de primeiro plano não será aplicada.

Se uma imagem de plano de fundo for usada **com o atributo** de sublinhado definido como true, o deslocamento será aplicado à imagem, ditando a quantidade da imagem (da esquerda e da direita ou da parte superior e inferior) a ser usada nas bordas inicial e final do controle deslizante, com a parte central da imagem que está sendo colocada ao lado do restante. Dessa forma, uma pequena imagem de fundo pode ser usada para cobrir todo o comprimento de um controle deslizante maior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER. foregroundColor**](slider-foregroundcolor.md)
</dt> <dt>

[**SLIDER. foregroundImage**](slider-foregroundimage.md)
</dt> <dt>

[**SLIDER. thumbImage**](slider-thumbimage.md)
</dt> <dt>

[**Controle deslizante. xadrez**](slider-tiled.md)
</dt> </dl>

 

 





