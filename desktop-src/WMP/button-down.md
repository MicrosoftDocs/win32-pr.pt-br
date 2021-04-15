---
title: BOTÃO. para baixo
description: O atributo down especifica ou recupera um valor que indica se o botão está na posição para cima ou para baixo.
ms.assetid: 75398e8c-b13e-4836-b487-ed880da753ea
keywords:
- BOTÃO. abaixar o Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a0e2c7f97f782b51c145f3974f1490d0286fbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761481"
---
# <a name="buttondown"></a>BOTÃO. para baixo

O atributo **down** especifica ou recupera um valor que indica se o **botão** está na posição para cima ou para baixo.

``` syntax
        elementID.down
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** de leitura/gravação.



| Valor | Descrição                                                   |
|-------|---------------------------------------------------------------|
| true  | Indica que o **botão** está na posição para baixo.        |
| false | Padrão. Indica que o **botão** está na posição para cima. |



 

## <a name="remarks"></a>Comentários

Para que um **botão** permaneça na posição inativa, **adesivo** deve ser definido como true. Por padrão, **adesivo** é false e qualquer tentativa **de definir como** true será ignorada.

Se um valor inválido for especificado, o estado anterior será mantido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BUTTON. downImage**](button-downimage.md)
</dt> <dt>

[**BUTTON. downToolTip**](button-downtooltip.md)
</dt> </dl>

 

 





