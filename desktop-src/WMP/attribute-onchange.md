---
title: attribute_onchange
description: Quando um atributo de aparência muda de valor, ocorre um evento que pode ser manipulado por um manipulador de eventos. O nome do manipulador de eventos é o nome do atributo seguido por um sublinhado e \ 0034; OnChange \ 0034;, como \ 0034; valor \_ onChange \ 0034;.
ms.assetid: 783b686c-d56c-4036-9af4-97b9b246ef7e
keywords:
- attribute_onchange o Windows Media Player
topic_type:
- apiref
api_name:
- attribute_onchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c4955193507e258d055a3399fc565c569fd291
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761489"
---
# <a name="attribute_onchange"></a>atributo \_ onChange

Quando um atributo de aparência muda de valor, ocorre um evento que pode ser manipulado por um manipulador de eventos. O nome do manipulador de eventos é o nome do atributo seguido por um sublinhado e "OnChange", como "valor \_ onChange".

``` syntax
        attribute_onchange
```

## <a name="examples"></a>Exemplos


```JScript
<SLIDER 
  thumbImage = "thumb.gif"
  value_onchange = "JScript: if (value == 100) backgroundColor = 'green';"
/>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------|
| Versão<br/> | Windows Media Player versão 70 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Manipuladores de eventos de ambiente**](ambient-event-handlers.md)
</dt> </dl>

 

 





