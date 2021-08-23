---
title: attribute_onchange
description: Quando um atributo de capa altera o valor, ocorre um evento que pode ser manipulado por um manipulador de eventos. O nome do manipulador de eventos é o nome do atributo seguido por um sublinhado e \ 0034;onchange \ 0034;, como \ 0034;value \_ onchange \ 0034;.
ms.assetid: 783b686c-d56c-4036-9af4-97b9b246ef7e
keywords:
- attribute_onchange Windows Media Player
topic_type:
- apiref
api_name:
- attribute_onchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c707b04587b6e975f81c8a0d0918b14c8e193d303f82c61b5220796bb6975b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573756"
---
# <a name="attribute_onchange"></a>atributo \_ onchange

Quando um atributo de capa altera o valor, ocorre um evento que pode ser manipulado por um manipulador de eventos. O nome do manipulador de eventos é o nome do atributo seguido por um sublinhado e "onchange", como "value \_ onchange".

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

 

 





