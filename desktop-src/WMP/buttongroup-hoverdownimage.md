---
title: BUTTON. hoverDownImage
description: O atributo hoverDownImage especifica ou recupera o nome da imagem que representa o estado de focalização de um botão no botão. O estado de focalização ocorre quando o botão está no estado inativo e o usuário passa o mouse sobre ele.
ms.assetid: dc048303-21d1-40ba-99bb-8d1c2f46628b
keywords:
- HoverDownImage Windows Media Player.
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a40788fafffd6eb4626bc834a941f7330c988fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810577"
---
# <a name="buttongrouphoverdownimage"></a>BUTTON. hoverDownImage

O atributo **hoverDownImage** especifica ou recupera o nome da imagem que representa o estado de focalização de um botão no **botão**. O estado de focalização ocorre quando o botão está no estado inativo e o usuário passa o mouse sobre ele.

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a>Valores possíveis

Este atributo é uma **cadeia de caracteres** de leitura/gravação.

## <a name="remarks"></a>Comentários

Os formatos de imagem com suporte são BMP, JPG, PNG e GIF. Se a imagem for um arquivo BMP de 8 bits, seus valores de matiz e de saturação poderão ser alterados dinamicamente usando os atributos **hueShift** e **saturação** .

A imagem padrão é aquela especificada no atributo **downImage** ou seu padrão.

Se a imagem focalizada for maior que a região definida, a imagem focalizada será cortada.

Se a imagem não puder ser recuperada, uma imagem padrão (a imagem vermelha-x) será exibida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento de botão**](buttongroup-element.md)
</dt> <dt>

[**BUTTON. downImage**](buttongroup-downimage.md)
</dt> <dt>

[**BUTTON. hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BOTÃO. saturação**](buttongroup-saturation.md)
</dt> </dl>

 

 





