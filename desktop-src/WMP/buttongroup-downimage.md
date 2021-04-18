---
title: BUTTON. downImage
description: O atributo downImage especifica ou recupera o nome da imagem que representa o estado inoperante do botão.
ms.assetid: 022e77e7-d3c0-41b5-984a-84d016a5a25a
keywords:
- DownImage Windows Media Player.
topic_type:
- apiref
api_name:
- BUTTONGROUP.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82b8a1d5bc2f4c68894a3bba1ad8ce9f2b3aa28a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781270"
---
# <a name="buttongroupdownimage"></a>BUTTON. downImage

O atributo **downImage** especifica ou recupera o nome da imagem que representa o estado inoperante do **botão**.

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a>Valores possíveis

Este atributo é uma **cadeia de caracteres** de leitura/gravação.

## <a name="remarks"></a>Comentários

Os formatos de imagem com suporte são BMP, JPG, PNG e GIF. Se a imagem for um arquivo BMP de 8 bits, seus valores de matiz e de saturação poderão ser alterados dinamicamente usando os atributos **hueShift** e **saturação** .

A imagem padrão é aquela especificada no atributo **Image** .

Se a imagem inoperante for maior que a região definida, a imagem abaixo será cortada.

Se a imagem não puder ser recuperada, uma imagem padrão (a imagem vermelha-x) será exibida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento de botão**](buttongroup-element.md)
</dt> <dt>

[**BUTTON. hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTON. Image**](buttongroup-image.md)
</dt> <dt>

[**BOTÃO. saturação**](buttongroup-saturation.md)
</dt> </dl>

 

 





