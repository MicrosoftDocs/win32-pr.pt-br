---
title: VIEW.resizable
description: O atributo resizável recupera um valor que indica se o VIEW pode ser reessado.
ms.assetid: 4f0e4f31-cf16-498f-823f-da43566043b1
keywords:
- VIEW.resizable Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.resizable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 622c732ce6a1218fa16bbe70c1ef18d53ba4211abfde9d39fc794ec862348033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332904"
---
# <a name="viewresizable"></a>VIEW.resizable

O **atributo resizável** recupera um valor que indica se **o VIEW** pode ser reessado.

``` syntax
        elementID.resizable
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um booliana somente **leitura** com um valor padrão igual ao **atributo da barra de** título.



| Valores | Descrição             |
|--------|-------------------------|
| true   | A exibição pode ser resized.    |
| false  | A exibição não pode ser ressada. |



 

## <a name="remarks"></a>Comentários

Se não houver nenhuma **barra de título** e, portanto, nenhuma janela ou borda, você deverá usar o método **size** para reessar o **elemento VIEW.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento VIEW**](view-element.md)
</dt> </dl>

 

 





