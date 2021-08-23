---
title: SLIDER.foregroundImage
description: O atributo foregroundImage especifica ou recupera a imagem de primeiro plano do controle deslizante.
ms.assetid: f713fba8-e965-4fed-b323-8a513d1f13e6
keywords:
- SLIDER.foregroundImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7fad50a6e33ca4de5890dfca340e36aa2fdc0af0c0b938793eac4edc1dfb71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119735706"
---
# <a name="sliderforegroundimage"></a>SLIDER.foregroundImage

O **atributo foregroundImage** especifica ou recupera a imagem de primeiro plano do controle deslizante.

``` syntax
        elementID.foregroundImage
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma cadeia de caracteres **de** leitura/gravação que contém o nome de um arquivo de imagem.

## <a name="remarks"></a>Comentários

Esse atributo é opcional. Ao usar imagens para construir um controle deslizante, **backgroundImage** é usado para a imagem do controle deslizante principal. O **thumbImage representa** o controle deslizante real e pode ser movido usando o mouse. No controle **deslizante thumbImage,** há uma linha invisível em que a imagem da tela de fundo é exibida em um lado da linha e a imagem de primeiro plano é exibida no outro lado.

Quando o controle deslizante **thumbImage** é  movido com o mouse, se slide estiver definido como true, a imagem de primeiro plano deslizará como se estivesse sendo esbosada pelo controle deslizante para cobrir a imagem de plano de fundo. Se **slide** for definido como false, a imagem de primeiro plano não se move, mas será revelada no local, como se o controle deslizante estivesse movendo a imagem de plano de fundo da imagem de primeiro plano.

Se  o atributo lado a lado for definido como true e a imagem de primeiro plano for menor que a área de primeiro  plano do controle deslizante, a imagem será lado a lado horizontal ou verticalmente, dependendo do atributo de direção, para preencher o espaço disponível.

Os formatos com suporte são BMP, JPG, PNG e GIF (não incluindo GIFs animados).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER.backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**SLIDER.slide**](slider-slide.md)
</dt> <dt>

[**SLIDER.thumbImage**](slider-thumbimage.md)
</dt> <dt>

[**SLIDER.value**](slider-value.md)
</dt> </dl>

 

 





