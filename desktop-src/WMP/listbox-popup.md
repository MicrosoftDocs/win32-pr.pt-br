---
title: LISTBOX. popUp
description: O atributo popUp especifica um valor que indica se o elemento representa um controle de caixa de listagem ou pop-up.
ms.assetid: b0ade23a-6164-4dd4-b599-43ea1fcd44e4
keywords:
- LISTBOX. popUp do Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.popUp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d197adbdf2ec27ea6ef7bf04c5c71d15ae923d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813368"
---
# <a name="listboxpopup"></a>LISTBOX. popUp

O atributo **popUp** especifica um valor que indica se o elemento representa um controle de caixa de listagem ou pop-up.

``` syntax
<ELEMENT popUp="value">
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** especificado somente no momento do design.



| Valor | Descrição                                |
|-------|--------------------------------------------|
| true  | O elemento representa um controle Popup.    |
| false | O elemento representa um controle de caixa de listagem. |



 

## <a name="remarks"></a>Comentários

O elemento **Popup** representa um controle de caixa de listagem que é exibido somente quando necessário. É idêntico ao elemento **ListBox** , exceto pelo valor padrão desse atributo, que altera o comportamento de exibição. Para elementos **ListBox** , o valor padrão é false. Para elementos **Popup** , o valor padrão é true. Em vez de especificar esse atributo, o elemento **ListBox** ou **Popup** deve ser usado de acordo com o comportamento desejado.

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

 

 





