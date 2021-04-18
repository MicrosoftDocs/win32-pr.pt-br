---
title: TEXT. foregroundColor
description: O atributo foregroundColor especifica ou recupera a cor do texto para o controle de texto.
ms.assetid: 1ddbad93-fbff-4be6-9797-6594b5f09a1e
keywords:
- TEXT. foregroundColor Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e452a18a085337e8cbf0ec88567d6a57a0a498a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810751"
---
# <a name="textforegroundcolor"></a>TEXT. foregroundColor

O atributo **foregroundColor** especifica ou recupera a cor do texto para o controle de texto.

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém qualquer valor de cor do Microsoft Internet Explorer. O valor padrão é "Black".

Consulte o atributo [Value](text-value.md) para ver um exemplo ilustrando como os atributos do elemento **Text** são usados.

Quando você usa **alphaBlend** ou **alphaBlendTo** com um elemento de **texto** que não tem o **backgroundColor** especificado, uma cor de plano de fundo de preto será usada. Se a cor de primeiro plano também for preta (que é o valor padrão para o atributo **foregroundColor** ), seu texto poderá ficar ilegível. Para evitar isso, sempre especifique o atributo **backgroundColor** ou defina **foregroundColor** como uma cor diferente de preto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Ambienteattributes. alphaBlend**](ambientattributes-alphablend.md)
</dt> <dt>

[**Ambienteattributes. alphaBlendTo**](ambientattributes-alphablendto.md)
</dt> <dt>

[**Referência de cor**](color-reference.md)
</dt> <dt>

[**Elemento de texto**](text-element.md)
</dt> <dt>

[**TEXT. backgroundColor**](text-backgroundcolor.md)
</dt> </dl>

 

 





