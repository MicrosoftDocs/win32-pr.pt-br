---
title: SLIDER. backgroundColor
description: O atributo backgroundColor especifica ou recupera a cor do plano de fundo do controle deslizante.
ms.assetid: 8f2c48ec-29f5-4fbe-aa62-c7cfb8a8678c
keywords:
- Controle deslizante. backgroundColor Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06cc595af13b28541fcc570e130da4e804fdeafe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753675"
---
# <a name="sliderbackgroundcolor"></a>SLIDER. backgroundColor

O atributo **backgroundColor** especifica ou recupera a cor do plano de fundo do controle deslizante.

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém qualquer valor de cor do Microsoft Internet Explorer. Não tem nenhum valor padrão.

## <a name="remarks"></a>Comentários

Um controle Slider básico pode ser construído especificando **backgroundColor** ou **BackgroundImage**, e **foregroundColor** ou **foregroundImage**.

Ao usar as cores, as dimensões do controle deslizante definem a área preenchida pela cor da tela de fundo. A cor do primeiro plano cobre a cor do plano de fundo conforme a posição do controle deslizante aumenta.

Para fazer um preenchimento gradual da área ocupada pela cor do plano de fundo ou do primeiro plano, especifique os atributos **backgroundEndColor** ou **foregroundEndColor** .

Consulte o *CUSTOMSLIDER*. atributo [positionImage](customslider-positionimage.md) para um exemplo que ilustra como os atributos do elemento **Slider** são usados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de cor**](color-reference.md)
</dt> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER. backgroundEndColor**](slider-backgroundendcolor.md)
</dt> <dt>

[**SLIDER. backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**SLIDER. foregroundColor**](slider-foregroundcolor.md)
</dt> <dt>

[**SLIDER. foregroundEndColor**](slider-foregroundendcolor.md)
</dt> <dt>

[**SLIDER. foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





