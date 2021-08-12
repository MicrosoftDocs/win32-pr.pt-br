---
title: BOTÃO. saturação
description: O atributo saturação especifica ou recupera o valor de saturação das imagens de um botão.
ms.assetid: bfd957f0-8201-4a4f-9162-a397ed97c747
keywords:
- Windows Media Player de botão. saturação
topic_type:
- apiref
api_name:
- BUTTONGROUP.saturation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d3579ac8109cb56e56c78a07a8f53e4cd7c017a695b6018f6a2ad41f703035
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581298"
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

 

 





