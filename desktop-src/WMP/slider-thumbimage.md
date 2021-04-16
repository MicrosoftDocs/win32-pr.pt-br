---
title: SLIDER. thumbImage
description: O atributo thumbImage especifica ou recupera a imagem que será usada para representar a posição atual do controle deslizante.
ms.assetid: 3aa69188-3443-483c-81a9-bf22832509d8
keywords:
- Controle deslizante. thumbImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.thumbImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b798dfbae24fe2cef3669d2fb372966e47254026
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761185"
---
# <a name="sliderthumbimage"></a>SLIDER. thumbImage

O atributo **thumbImage** especifica ou recupera a imagem que será usada para representar a posição atual do controle deslizante.

``` syntax
        elementID.thumbImage
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome de um arquivo de imagem.

## <a name="remarks"></a>Comentários

O **thumbImage** especifica a imagem que será usada para representar a posição atual, bem como indicar que o usuário pode executar uma ação com o controle. Se nenhuma imagem Thumb for especificada, o controle deslizante será não interativo.

A imagem em miniatura é centralizada na dimensão estreita do controle Slider. Se a imagem em miniatura for mais estreita do que o controle, a imagem aparecerá no meio do plano de fundo. Se a imagem em miniatura for maior que o controle, as extremidades da imagem serão cortadas.

A posição do controle deslizante é especificada pelo centro da imagem do polegar. Se **Bordere** for zero, apenas metade da imagem Thumb ficará visível nas posições do controle deslizante inicial e final. Para evitar isso, defina **borderize** como um valor maior ou igual à metade da largura da imagem Thumb (ou metade da altura se a **direção** for definida como "vertical").

Os formatos com suporte são BMP, JPG, PNG e GIF (não incluindo GIFs animados).

Consulte o **CUSTOMSLIDER**. atributo [positionImage](customslider-positionimage.md) para um exemplo que ilustra como os atributos do elemento **Slider** são usados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**Controle deslizante. Borderize**](slider-bordersize.md)
</dt> <dt>

[**Controle deslizante. direção**](slider-direction.md)
</dt> </dl>

 

 





