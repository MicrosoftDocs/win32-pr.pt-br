---
title: TEXT.foregroundColor
description: O atributo foregroundColor especifica ou recupera a cor do texto para o controle Text.
ms.assetid: 1ddbad93-fbff-4be6-9797-6594b5f09a1e
keywords:
- TEXT.foregroundColor Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b134058fdc39b653982f752f2623c6cd69b192e24e417ac012a02813a38334a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467066"
---
# <a name="textforegroundcolor"></a>TEXT.foregroundColor

O **atributo foregroundColor** especifica ou recupera a cor do texto para o controle Text.

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma Cadeia de **caracteres** de leitura/gravação que contém qualquer valor de Internet Explorer da Microsoft. O valor padrão é "preto".

Consulte o [atributo value](text-value.md) para um exemplo que ilustra como os atributos do **elemento TEXT** são usados.

Quando você usa **alphaBlend** ou **alphaBlendTo** com um elemento **TEXT** que não tem a **backgroundColor** especificada, uma cor da tela de fundo preta será usada. Se a cor de primeiro plano também for preta (que é o valor padrão para o atributo **foregroundColor),** o texto poderá se tornar ilegível. Para evitar isso, sempre especifique o **atributo backgroundColor** ou de definir **foregroundColor** como uma cor diferente de preto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AmbientAttributes.alphaBlend**](ambientattributes-alphablend.md)
</dt> <dt>

[**AmbientAttributes.alphaBlendTo**](ambientattributes-alphablendto.md)
</dt> <dt>

[**Referência de cores**](color-reference.md)
</dt> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.backgroundColor**](text-backgroundcolor.md)
</dt> </dl>

 

 





