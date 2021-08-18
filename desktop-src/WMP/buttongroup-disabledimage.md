---
title: BUTTON. disabledImage
description: O atributo disabledImage especifica ou recupera o nome da imagem que representa o estado desabilitado dos botões no botão.
ms.assetid: 34d4e6a9-de73-4dfa-9c23-4f17b55298f6
keywords:
- Windows Media Player de BUTTON. disabledImage
topic_type:
- apiref
api_name:
- BUTTONGROUP.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eeef37bbc25185a64e767f00f9ce17934e8b445327606b552ad69d282e42e4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764346"
---
# <a name="buttongroupdisabledimage"></a>BUTTON. disabledImage

O atributo **disabledImage** especifica ou recupera o nome da imagem que representa o estado desabilitado dos botões no **botão**.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Valores possíveis

Este atributo é uma **cadeia de caracteres** de leitura/gravação.

## <a name="remarks"></a>Comentários

Os formatos de imagem com suporte são BMP, JPG, PNG e GIF. Se a imagem for um arquivo BMP de 8 bits, seus valores de matiz e de saturação poderão ser alterados dinamicamente usando os atributos **hueShift** e **saturação** .

Quando o atributo **Disabled** de um elemento **buttonelement** é definido como true, a região correspondente do **DisabledImage** para o grupo de **botões** é exibida. Se a imagem desabilitada for maior que a região definida, a imagem desabilitada será cortada.

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

[**BOTÃO. saturação**](buttongroup-saturation.md)
</dt> </dl>

 

 





