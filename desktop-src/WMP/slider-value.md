---
title: Controle deslizante. valor
description: O atributo Value especifica ou recupera a posição atual do controle deslizante. | Controle deslizante. valor
ms.assetid: 2cd2f8b2-d3f1-4897-98b0-af551d6693e6
keywords:
- Controle deslizante. valor Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87aeff5c97808efb812f530236227b07f463855
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751031"
---
# <a name="slidervalue"></a>Controle deslizante. valor

O atributo **Value** especifica ou recupera a posição atual do controle deslizante.

``` syntax
        elementID.value
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **número** de leitura/gravação (**float**) com um valor padrão de **mín**.

## <a name="remarks"></a>Comentários

O **valor** deve ser sempre maior ou igual a **mín** e menor ou igual ao **máximo**. Se você especificar um valor fora desse intervalo, o **valor** e a posição do controle deslizante não serão alterados.

Consulte o **CUSTOMSLIDER**. atributo [positionImage](customslider-positionimage.md) para um exemplo que ilustra como os atributos do elemento **Slider** são usados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER. min**](slider-min.md)
</dt> </dl>

 

 





