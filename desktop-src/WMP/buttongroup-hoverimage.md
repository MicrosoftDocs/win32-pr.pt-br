---
title: BUTTON. hoverImage
description: O atributo hoverImage especifica ou recupera o nome da imagem que representa o estado de foco de um botão no botão. O estado de foco ocorre quando o botão está no estado ativo e o usuário passa o mouse sobre ele.
ms.assetid: 319b8770-8c4a-441a-ad03-9ff895958cf2
keywords:
- Windows Media Player de BUTTON. hoverImage
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ee872c06d405d0f9cf5c09f59a86ba1962d0a5b349460c978e37fb5022f1d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135899"
---
# <a name="buttongrouphoverimage"></a>BUTTON. hoverImage

O atributo **hoverImage** especifica ou recupera o nome da imagem que representa o estado de foco de um botão no **botão**. O estado de foco ocorre quando o botão está no estado ativo e o usuário passa o mouse sobre ele.

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>Valores possíveis

Este atributo é uma **cadeia de caracteres** de leitura/gravação.

## <a name="remarks"></a>Comentários

Os formatos de imagem com suporte são BMP, JPG, PNG e GIF. Se a imagem for um arquivo BMP de 8 bits, seus valores de matiz e de saturação poderão ser alterados dinamicamente usando os atributos **hueShift** e **saturação** .

A imagem padrão é aquela especificada no atributo **Image** ou seu padrão.

Se a imagem em foco for maior que a região definida, a imagem em foco será cortada.

Se a imagem não puder ser recuperada, uma imagem padrão (a imagem vermelha-x) será exibida.

## <a name="examples"></a>Exemplos

Consulte o *botãoelement*. atributo [mappingColor](buttonelement-mappingcolor.md) para um exemplo que ilustra o uso desse atributo.

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

 

 





