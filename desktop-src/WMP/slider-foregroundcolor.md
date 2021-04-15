---
title: SLIDER. foregroundColor
description: O atributo foregroundColor especifica ou recupera a cor de primeiro plano do controle deslizante.
ms.assetid: 8c8de4a9-0021-41ed-aeb8-75653855b6f1
keywords:
- Controle deslizante. foregroundColor Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d334dff4d9b7d90582e44018bf8f56c04fa784a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753886"
---
# <a name="sliderforegroundcolor"></a>SLIDER. foregroundColor

O atributo **foregroundColor** especifica ou recupera a cor de primeiro plano do controle deslizante.

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém qualquer valor de cor do Microsoft Internet Explorer. O valor padrão é "White".

## <a name="remarks"></a>Comentários

Um controle Slider básico pode ser construído especificando um dos dois pares de atributos: **backgroundColor** e **ForegroundColor**, ou **backgroundImage** e **foregroundImage**.

Quando você constrói um controle deslizante usando os atributos de cor, as dimensões do controle deslizante definem a área preenchida pela cor da tela de fundo. A cor do primeiro plano cobre a cor do plano de fundo conforme a posição do controle deslizante aumenta.

Para fazer um preenchimento gradual na área ocupada pelo plano de fundo ou pela cor de primeiro plano, especifique os atributos **backgroundEndColor** ou **foregroundEndColor** .

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

[**SLIDER. backgroundColor**](slider-backgroundcolor.md)
</dt> <dt>

[**SLIDER. backgroundEndColor**](slider-backgroundendcolor.md)
</dt> <dt>

[**SLIDER. foregroundEndColor**](slider-foregroundendcolor.md)
</dt> <dt>

[**SLIDER. foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





