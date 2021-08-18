---
title: TEXT. scrollingAmount
description: O atributo scrollingAmount especifica ou recupera o número de pixels que o texto move durante cada movimento de rolagem.
ms.assetid: 46f74531-69dd-4505-8937-5b48b6e9be7b
keywords:
- Windows Media Player TEXT. scrollingAmount
topic_type:
- apiref
api_name:
- TEXT.scrollingAmount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a8d5b703c02c2d3049f98a934980f1dbf8b1c5beceaca4d97158ea68c13db9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119466956"
---
# <a name="textscrollingamount"></a>TEXT. scrollingAmount

O atributo **scrollingAmount** especifica ou recupera o número de pixels que o texto move durante cada movimento de rolagem.

``` syntax
        elementID.scrollingAmount
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **número** de leitura/gravação positivo (**int**) com um valor padrão de 6.

## <a name="remarks"></a>Comentários

Para uma rolagem suave, **scrollingAmount** deve ser pequeno. Para um desenho rápido com grandes intervalos, o **scrollingAmount** deve ser maior. Se **rolagem** = "false", **scrollingAmount** será ignorado.

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

 

 





