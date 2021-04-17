---
title: Controle deslizante. slide
description: O atributo de slide especifica ou recupera um valor que indica se a imagem em primeiro plano desliza sobre a imagem de plano de fundo ou é revelada gradualmente em uma posição estática na imagem de plano de fundo.
ms.assetid: dc68c2a0-d3fe-4984-9607-12703a27edbd
keywords:
- Controle deslizante. Deslize o Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.slide
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9f79b5016b323380c5a4d06c8af7ab5fb0b8a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749398"
---
# <a name="sliderslide"></a>Controle deslizante. slide

O atributo de **Slide** especifica ou recupera um valor que indica se a imagem em primeiro plano desliza sobre a imagem de plano de fundo ou é revelada gradualmente em uma posição estática na imagem de plano de fundo.

``` syntax
        elementID.slide
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** de leitura/gravação.



| Valor | Descrição                                                          |
|-------|----------------------------------------------------------------------|
| true  | Padrão. A imagem em primeiro plano desliza sobre a imagem de plano de fundo.      |
| false | A imagem em primeiro plano é revelada no lugar da imagem de plano de fundo. |



 

## <a name="remarks"></a>Comentários

Quando o controle deslizante **thumbImage** for movido com o mouse, se o **Slide** estiver definido como true, a imagem em primeiro plano deslizará como se fosse puxada pelo controle deslizante para cobrir a imagem de plano de fundo. Se o **Slide** for definido como false, a imagem em primeiro plano não se moverá, mas será revelada no lugar, como se o controle deslizante estiver movendo a imagem de plano de fundo para a imagem em primeiro plano.

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

[**SLIDER. foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





