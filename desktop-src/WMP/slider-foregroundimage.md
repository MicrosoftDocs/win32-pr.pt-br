---
title: SLIDER. foregroundImage
description: O atributo foregroundImage especifica ou recupera a imagem em primeiro plano do controle deslizante.
ms.assetid: f713fba8-e965-4fed-b323-8a513d1f13e6
keywords:
- Controle deslizante. foregroundImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a286d3b73a2647160a0bd23357703f4fcb88d267
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756098"
---
# <a name="sliderforegroundimage"></a>SLIDER. foregroundImage

O atributo **foregroundImage** especifica ou recupera a imagem em primeiro plano do controle deslizante.

``` syntax
        elementID.foregroundImage
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome de um arquivo de imagem.

## <a name="remarks"></a>Comentários

Esse atributo é opcional. Ao usar imagens para construir um controle deslizante, o **backgroundImage** é usado para a imagem principal do controle deslizante. O **thumbImage** representa o controle deslizante real e pode ser movido usando o mouse. No controle deslizante **thumbImage** , há uma linha invisível em que a imagem de plano de fundo é exibida em um lado da linha e a imagem em primeiro plano é exibida no outro lado.

Quando o controle deslizante **thumbImage** for movido com o mouse, se o **Slide** estiver definido como true, a imagem em primeiro plano deslizará como se fosse puxada pelo controle deslizante para cobrir a imagem de plano de fundo. Se o **Slide** for definido como false, a imagem em primeiro plano não se moverá, mas será revelada no lugar, como se o controle deslizante estiver movendo a imagem de plano de fundo para a imagem em primeiro plano.

Se o **atributo de** subbarra for definido como true e a imagem em primeiro plano for menor do que a área de primeiro plano do controle deslizante, a imagem será colocada lado-a-horizontal ou verticalmente, dependendo do atributo **Direction** , para preencher o espaço disponível.

Os formatos com suporte são BMP, JPG, PNG e GIF (não incluindo GIFs animados).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER. backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**Controle deslizante. slide**](slider-slide.md)
</dt> <dt>

[**SLIDER. thumbImage**](slider-thumbimage.md)
</dt> <dt>

[**Controle deslizante. valor**](slider-value.md)
</dt> </dl>

 

 





