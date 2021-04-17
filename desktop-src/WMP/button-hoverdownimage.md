---
title: BUTTON. hoverDownImage
description: O atributo hoverDownImage especifica ou recupera a imagem exibida quando o botão está no estado inoperante e o usuário passa sobre ele com o ponteiro do mouse.
ms.assetid: 06645307-50f1-400d-aa73-c48d0fba3ee1
keywords:
- BUTTON. hoverDownImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bc8221875656c38a35eb6539dce25f58133984f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760893"
---
# <a name="buttonhoverdownimage"></a>BUTTON. hoverDownImage

O atributo **hoverDownImage** especifica ou recupera a imagem exibida quando o **botão** está no estado inoperante e o usuário passa sobre ele com o ponteiro do mouse.

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome do arquivo de imagem.

## <a name="remarks"></a>Comentários

Os formatos de imagem com suporte são BMP, JPG, PNG e GIF.

A imagem padrão é aquela especificada no atributo **downImage** ou seu padrão.

Se a imagem focalizada for maior do que a região definida no atributo ambiente, a imagem focalizada será cortada.

Se a imagem não puder ser recuperada, uma imagem padrão (a imagem vermelha-x) será exibida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BUTTON. downImage**](button-downimage.md)
</dt> </dl>

 

 





