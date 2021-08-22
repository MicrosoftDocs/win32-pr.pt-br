---
title: BUTTON.down
description: O atributo down especifica ou recupera um valor que indica se o BUTTON está na posição para cima ou para baixo.
ms.assetid: 75398e8c-b13e-4836-b487-ed880da753ea
keywords:
- BUTTON.down Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c169def4940af3c3123e9f211a404c2926192a4d6676f3233a23bceb664e5521
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118840628"
---
# <a name="buttondown"></a>BUTTON.down

O **atributo down** especifica ou recupera um valor que indica se o **BUTTON** está na posição para cima ou para baixo.

``` syntax
        elementID.down
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um booliana **de leitura/gravação.**



| Valor | Descrição                                                   |
|-------|---------------------------------------------------------------|
| true  | Indica que o **BUTTON** está na posição para baixo.        |
| false | Padrão. Indica que o **BUTTON** está na posição para cima. |



 

## <a name="remarks"></a>Comentários

Para que **um BUTTON** permaneça na posição para baixo, **sticky** deve ser definido como true. Por padrão, **sticky** é false e qualquer tentativa de **definir como** true será ignorada.

Se um valor inválido for especificado, o estado anterior será mantido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BUTTON.downImage**](button-downimage.md)
</dt> <dt>

[**BUTTON.downToolTip**](button-downtooltip.md)
</dt> </dl>

 

 





