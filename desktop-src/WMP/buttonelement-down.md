---
title: BOTÃO. para baixo
description: O atributo down especifica ou recupera um valor que indica se o elemento Button está na posição para cima ou para baixo.
ms.assetid: 6b3633c5-84c1-48a0-bd2f-94660890d9a6
keywords:
- BOTÃO. Down Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff20aebda01b24dc14eb7d5298ee0d663d903bedcb7ef6ef8b05b6211af8b567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764466"
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

 

 





