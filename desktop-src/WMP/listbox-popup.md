---
title: LISTBOX.popUp
description: O atributo popUp especifica um valor que indica se o elemento representa um controle pop-up ou de caixa de listagem.
ms.assetid: b0ade23a-6164-4dd4-b599-43ea1fcd44e4
keywords:
- LISTBOX.popUp Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.popUp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a755a4fc8f5e1451ee118f718a9b6618e75875789faef7318164f7f2add2069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996436"
---
# <a name="listboxpopup"></a>LISTBOX.popUp

O **atributo popUp** especifica um valor que indica se o elemento representa um controle pop-up ou de caixa de listagem.

``` syntax
<ELEMENT popUp="value">
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliana** especificado somente em tempo de design.



| Valor | Descrição                                |
|-------|--------------------------------------------|
| true  | O elemento representa um controle pop-up.    |
| false | O elemento representa um controle de caixa de listagem. |



 

## <a name="remarks"></a>Comentários

O **elemento POPUP** representa um controle de caixa de listagem que é exibido somente quando necessário. Ele é idêntico ao elemento **LISTBOX,** exceto pelo valor padrão desse atributo, que altera o comportamento de exibição. Para **elementos LISTBOX,** o valor padrão é false. Para **elementos POPUP,** o valor padrão é true. Em vez de especificar esse atributo, o **elemento LISTBOX** ou **POPUP** deve ser usado de acordo com o comportamento desejado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------|
| Versão<br/> | Windows Media Player para Windows XP ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento LISTBOX**](listbox-element.md)
</dt> <dt>

[**Elemento POPUP**](popup-element.md)
</dt> </dl>

 

 





