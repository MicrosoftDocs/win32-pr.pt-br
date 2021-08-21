---
title: SLIDER. backgroundImage
description: O atributo backgroundImage especifica ou recupera a imagem de plano de fundo do controle deslizante.
ms.assetid: 73757635-4d1c-4ed0-8721-0608cd85859c
keywords:
- SLIDER. backgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2c4f6d31e3f870541310b23544a15c7b9af0043014a9013310cea7dd4ee072
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118832993"
---
# <a name="sliderbackgroundimage"></a>SLIDER. backgroundImage

O atributo **backgroundImage** especifica ou recupera a imagem de plano de fundo do controle deslizante.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome de um arquivo de imagem.

## <a name="remarks"></a>Comentários

Esse atributo é opcional. Ao usar imagens para construir um controle deslizante, o **backgroundImage** é usado para a imagem principal do controle deslizante. O **thumbImage** representa o controle deslizante real e pode ser movido usando o mouse. No controle deslizante **thumbImage** , há uma linha invisível em que a imagem de plano de fundo é exibida em um lado da linha e a imagem em primeiro plano é exibida no outro lado.

Quando o controle deslizante **thumbImage** for movido com o mouse, se o **Slide** estiver definido como true, a imagem em primeiro plano deslizará como se fosse puxada pelo controle deslizante para cobrir a imagem de plano de fundo. Se o **Slide** for definido como false, a imagem em primeiro plano não se moverá, mas será revelada no lugar, como se o controle deslizante estiver movendo a imagem de plano de fundo para a imagem em primeiro plano.

Se o **atributo de** subbarra for definido como true e a imagem de plano de fundo for menor do que o controle deslizante, a imagem será colocada na horizontal ou verticalmente, dependendo do atributo **Direction** . Se o atributo **borderize** for definido como um valor maior que zero, o número especificado será o número de pixels da esquerda e da direita ou da parte superior e inferior da imagem (novamente, dependendo do atributo **Direction** ) que será reservado para as bordas do controle deslizante. Nesse caso, somente a parte central da imagem é usada para sublado o restante do controle.

Os formatos com suporte são BMP, JPG, PNG e GIF (não incluindo GIFs animados).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER. foregroundImage**](slider-foregroundimage.md)
</dt> <dt>

[**Controle deslizante. slide**](slider-slide.md)
</dt> <dt>

[**SLIDER. thumbImage**](slider-thumbimage.md)
</dt> </dl>

 

 





