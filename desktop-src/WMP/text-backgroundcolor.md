---
title: TEXT. backgroundColor
description: O atributo backgroundColor especifica ou recupera a cor do plano de fundo do controle de texto.
ms.assetid: 0c16318f-bf57-4c5f-85c1-46641124d431
keywords:
- TEXT. backgroundColor Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff833fad0b5ad60b49479c57dc51cbe82f48dbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771308"
---
# <a name="textbackgroundcolor"></a>TEXT. backgroundColor

O atributo **backgroundColor** especifica ou recupera a cor do plano de fundo do controle de texto.

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém qualquer valor de cor do Microsoft Internet Explorer ou o valor "None". Ele tem um valor padrão de "None", o que significa que o plano de fundo é transparente.

## <a name="remarks"></a>Comentários

A cor do plano de fundo é definida para a altura e a largura do controle. Se a altura e a largura não forem definidas, a cor do plano de fundo será definida com a altura e a largura do texto.

Quando você usa **alphaBlend** ou **alphaBlendTo** com um elemento de **texto** que não tem o **backgroundColor** especificado, uma cor de plano de fundo de preto será usada. Se a cor de primeiro plano também for preta (que é o valor padrão para o atributo **foregroundColor** ), seu texto poderá ficar ilegível. Para evitar isso, sempre especifique o atributo **backgroundColor** ou defina **foregroundColor** como uma cor diferente de preto.

Consulte o atributo [Value](text-value.md) para ver um exemplo ilustrando como os atributos do elemento **Text** são usados.

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

[**TEXT. foregroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





