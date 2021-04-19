---
title: TEXT. toolTip
description: O atributo toolTip especifica ou recupera o texto da dica de ferramenta para o controle de texto.
ms.assetid: 3e275607-e7ff-4424-8310-c628ede22629
keywords:
- TEXT. toolTip Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.toolTip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b064f2abefd07ec65a82069196b1012561699b62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770124"
---
# <a name="texttooltip"></a>TEXT. toolTip

O atributo **ToolTip** especifica ou recupera o texto da dica de ferramenta para o controle de texto.

``` syntax
        elementID.toolTip
```

## <a name="possible-values"></a>Valores possíveis

Este atributo é uma **cadeia de caracteres** de leitura/gravação com um comprimento máximo de 1024 caracteres. Não tem nenhum valor padrão.

## <a name="remarks"></a>Comentários

Se esse atributo não for especificado e o texto no atributo de **valor** estiver truncado no controle de texto, ou se **WordWrap** for definido como true, a dica de ferramenta exibirá o texto completo do atributo **Value** .

Quando esse atributo é definido como "" (cadeia de caracteres vazia), nenhuma dica de ferramenta é exibida.

Consulte o atributo [Value](text-value.md) para ver um exemplo ilustrando como os atributos do elemento **Text** são usados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento de texto**](text-element.md)
</dt> <dt>

[**TEXT. Value**](text-value.md)
</dt> <dt>

[**TEXT. wordWrap**](text-wordwrap.md)
</dt> </dl>

 

 





