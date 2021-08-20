---
title: SLIDER.slide
description: O atributo slide especifica ou recupera um valor que indica se a imagem de primeiro plano desliza sobre a imagem de plano de fundo ou é gradualmente revelada em uma posição estática sobre a imagem de plano de fundo.
ms.assetid: dc68c2a0-d3fe-4984-9607-12703a27edbd
keywords:
- CONTROLE DESLIZANTE.slide Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.slide
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5d1a9480a171372ff5c90990d07bd583bd880570472b25af8d1ada945b31a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117933504"
---
# <a name="sliderslide"></a>SLIDER.slide

O **atributo slide** especifica ou recupera um valor que indica se a imagem de primeiro plano desliza sobre a imagem de plano de fundo ou é gradualmente revelada em uma posição estática sobre a imagem de plano de fundo.

``` syntax
        elementID.slide
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um booliana **de leitura/gravação.**



| Valor | Descrição                                                          |
|-------|----------------------------------------------------------------------|
| true  | Padrão. A imagem de primeiro plano desliza sobre a imagem de plano de fundo.      |
| false | A imagem de primeiro plano é revelada no local sobre a imagem de plano de fundo. |



 

## <a name="remarks"></a>Comentários

Quando o controle deslizante **thumbImage** é  movido com o mouse, se slide estiver definido como true, a imagem de primeiro plano deslizará como se estivesse sendo esbosada pelo controle deslizante para cobrir a imagem de plano de fundo. Se **slide** for definido como false, a imagem de primeiro plano não se move, mas será revelada no local, como se o controle deslizante estivesse movendo a imagem de plano de fundo da imagem de primeiro plano.

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

[**SLIDER.foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





