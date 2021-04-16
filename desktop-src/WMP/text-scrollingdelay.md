---
title: TEXT. scrollingDelay
description: O atributo scrollingDelay especifica ou recupera o intervalo de tempo entre movimentos de rolagem.
ms.assetid: b965fe8f-c809-431f-b8fe-f7c3060068ac
keywords:
- TEXT. scrollingDelay Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.scrollingDelay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e81259ca84c62327bea67ae70d3f9ec3363450fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758718"
---
# <a name="textscrollingdelay"></a>TEXT. scrollingDelay

O atributo **scrollingDelay** especifica ou recupera o intervalo de tempo entre movimentos de rolagem.

``` syntax
        elementID.scrollingDelay
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **número** de leitura/gravação (**int**) que especifica o atraso em milissegundos. Ele tem um valor mínimo de 30 e um valor padrão de 85. Se um valor menor que o mínimo for especificado, o padrão será usado.

## <a name="remarks"></a>Comentários

Se a **rolagem** for definida como false, **scrollingDelay** será ignorado.

Consulte o atributo [Value](text-value.md) para ver um exemplo ilustrando como os atributos do elemento **Text** são usados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento de texto**](text-element.md)
</dt> <dt>

[**TEXTO. rolagem**](text-scrolling.md)
</dt> </dl>

 

 





