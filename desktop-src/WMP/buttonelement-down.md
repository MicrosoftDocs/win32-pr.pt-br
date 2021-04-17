---
title: BOTÃO. para baixo
description: O atributo down especifica ou recupera um valor que indica se o elemento Button está na posição para cima ou para baixo.
ms.assetid: 6b3633c5-84c1-48a0-bd2f-94660890d9a6
keywords:
- BUTTONelement. inoperante do Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23f48b0e2ac0f4bf02f87d90bb0bd504478beb52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762097"
---
# <a name="buttonelementdown"></a>BOTÃO. para baixo

O atributo **down** especifica ou recupera um valor que indica se o elemento Button está na posição para cima ou para baixo.

``` syntax
        elementID.down
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** de leitura/gravação.



| Valor | Descrição                                                     |
|-------|-----------------------------------------------------------------|
| true  | Indica que o **buttonelement** está na posição para baixo.        |
| false | Padrão. Indica que o **buttonelement** está na posição para cima. |



 

## <a name="remarks"></a>Comentários

Para que um elemento de botão permaneça na posição inativa, **adesivo** deve ser definido como true. Por padrão, **adesivo** é false e qualquer tentativa **de definir como** true será ignorada.

Se um valor inválido for especificado, o estado anterior será mantido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento BUTTONelement**](buttonelement-element.md)
</dt> <dt>

[**BUTTONelement. downToolTip**](buttonelement-downtooltip.md)
</dt> </dl>

 

 





