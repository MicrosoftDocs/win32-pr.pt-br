---
title: BOTÃO. saturação
description: O atributo saturação especifica ou recupera o valor de saturação das imagens de um botão.
ms.assetid: bfd957f0-8201-4a4f-9162-a397ed97c747
keywords:
- O Windows Media Player. saturação
topic_type:
- apiref
api_name:
- BUTTONGROUP.saturation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8de7dd39eb0b1a9e3f24031e24851eba22c6c6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780023"
---
# <a name="buttongroupsaturation"></a>BOTÃO. saturação

O atributo **saturação** especifica ou recupera o valor de saturação das imagens de um **botão** .

``` syntax
        elementID.saturation
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **número** de leitura/gravação (**float**) com um valor que varia de 0,0 a 2,0 com um valor padrão de 1,0.

## <a name="remarks"></a>Comentários

Esse atributo altera o valor de saturação das imagens especificadas pelos atributos **disabledImage**, **downImage**, **hoverDownImage**, **hoverImage** e **Image** se eles tiverem sido especificados e se referirem a imagens bmp de 8 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento de botão**](buttongroup-element.md)
</dt> <dt>

[**BUTTON. disabledImage**](buttongroup-disabledimage.md)
</dt> <dt>

[**BUTTON. downImage**](buttongroup-downimage.md)
</dt> <dt>

[**BUTTON. hoverDownImage**](buttongroup-hoverdownimage.md)
</dt> <dt>

[**BUTTON. hoverImage**](buttongroup-hoverimage.md)
</dt> <dt>

[**BUTTON. hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTON. Image**](buttongroup-image.md)
</dt> </dl>

 

 





