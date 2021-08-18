---
title: BUTTONGROUP.hoverDownImage
description: O atributo hoverDownImage especifica ou recupera o nome da imagem que representa o estado de foco para baixo de um botão no BUTTONGROUP. O estado de passar o mouse para baixo ocorre quando o botão está no estado para baixo e o usuário fica sobre ele com o mouse.
ms.assetid: dc048303-21d1-40ba-99bb-8d1c2f46628b
keywords:
- BUTTONGROUP.hoverDownImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c84d907a9b3fd1fc1a2eaf2dcf30337d016ae0732b147f435f49343d791b65c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119875"
---
# <a name="buttongrouphoverdownimage"></a>BUTTONGROUP.hoverDownImage

O **atributo hoverDownImage** especifica ou recupera o nome da imagem que representa o estado de foco para baixo de um botão no **BUTTONGROUP.** O estado de passar o mouse para baixo ocorre quando o botão está no estado para baixo e o usuário fica sobre ele com o mouse.

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma cadeia de caracteres de **leitura/gravação.**

## <a name="remarks"></a>Comentários

Os formatos de imagem com suporte são BMP, JPG, PNG e GIF. Se a imagem for um arquivo BMP de 8 bits, seus valores de matiz e saturação poderão ser alterados dinamicamente usando os atributos **hueShift** **e saturação.**

A imagem padrão é a especificada no atributo **downImage** ou seu padrão.

Se a imagem de passar o mouse para baixo for maior que a região definida, a imagem de foco para baixo será cortada.

Se a imagem não puder ser recuperada, uma imagem padrão (a imagem x vermelha) será exibida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP.downImage**](buttongroup-downimage.md)
</dt> <dt>

[**BUTTONGROUP.hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP.s saturação**](buttongroup-saturation.md)
</dt> </dl>

 

 





