---
title: TEXT. textlargura
description: O atributo TextWidth recupera a largura em pixels do texto contido no atributo Value.
ms.assetid: 46c34659-f441-467c-8846-45785f7a2736
keywords:
- TEXT. textlargura do Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.textWidth
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17ce93517837aecf737336137df3cf5d8bf292dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811701"
---
# <a name="texttextwidth"></a>TEXT. textlargura

O atributo **TextWidth** recupera a largura em pixels do texto contido no atributo **Value** .

``` syntax
        elementID.textWidth
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **número** somente leitura (**int**).

## <a name="remarks"></a>Comentários

O valor retornado é baseado nos atributos **fontface**, **FontSize** e **FontStyle** , bem como nos caracteres reais na cadeia de caracteres do atributo **Value** .

Consulte o atributo [Value](text-value.md) para ver um exemplo ilustrando como os atributos do elemento **Text** são usados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento de texto**](text-element.md)
</dt> <dt>

[**TEXT. fontFace**](text-fontface.md)
</dt> <dt>

[**TEXT. fontSize**](text-fontsize.md)
</dt> <dt>

[**TEXT. fontStyle**](text-fontstyle.md)
</dt> <dt>

[**TEXT. Value**](text-value.md)
</dt> </dl>

 

 





