---
title: SLIDER.foregroundColor
description: O atributo foregroundColor especifica ou recupera a cor de primeiro plano do controle deslizante.
ms.assetid: 8c8de4a9-0021-41ed-aeb8-75653855b6f1
keywords:
- CONTROLE DESLIZANTE.foregroundColor Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a111dca131351dedaf2080d16bffa4db1344e9993cabcfe8ca44f149fd97eb3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569080"
---
# <a name="sliderforegroundcolor"></a>SLIDER.foregroundColor

O **atributo foregroundColor** especifica ou recupera a cor de primeiro plano do controle deslizante.

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma Cadeia de **caracteres** de leitura/gravação que contém qualquer valor de Internet Explorer da Microsoft. O valor padrão é "white".

## <a name="remarks"></a>Comentários

Um controle deslizante básico pode ser construído especificando um dos dois pares de atributos: **backgroundColor** e **foregroundColor** ou **backgroundImage** e **foregroundImage.**

Quando você constrói um controle deslizante usando os atributos de cor, as dimensões do controle deslizante definem a área preenchida pela cor da tela de fundo. A cor de primeiro plano cobre a cor da tela de fundo conforme a posição do controle deslizante aumenta.

Para fazer um preenchimento de gradiente na área ocupada pela cor da tela de fundo ou primeiro plano, especifique os atributos **backgroundEndColor** **ou foregroundEndColor.**

Consulte *o DELIDER.* [atributo positionImage](customslider-positionimage.md) para um exemplo que ilustra como os atributos do **elemento SLIDER** são usados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de cores**](color-reference.md)
</dt> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER.backgroundColor**](slider-backgroundcolor.md)
</dt> <dt>

[**SLIDER.backgroundEndColor**](slider-backgroundendcolor.md)
</dt> <dt>

[**SLIDER.foregroundEndColor**](slider-foregroundendcolor.md)
</dt> <dt>

[**SLIDER.foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





