---
title: TEXT.toolTip
description: O atributo toolTip especifica ou recupera o texto da Dica de Ferramenta para o controle de texto.
ms.assetid: 3e275607-e7ff-4424-8310-c628ede22629
keywords:
- Text.toolTip Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.toolTip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 726337ffb31b86d4eaa3a20a1d922fc622110b647fe9be747e8ae239c4548276
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118831814"
---
# <a name="texttooltip"></a>TEXT.toolTip

O **atributo toolTip** especifica ou recupera o texto da Dica de Ferramenta para o controle de texto.

``` syntax
        elementID.toolTip
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma cadeia de **caracteres** de leitura/gravação com um comprimento máximo de 1024 caracteres. Não tem nenhum valor padrão.

## <a name="remarks"></a>Comentários

Se esse atributo não for especificado e  o texto no atributo value for truncado no controle Texto ou **wordWrap** estiver definido como true, a Dica de Ferramenta exibirá o texto completo do atributo **de** valor.

Quando esse atributo é definido como "" (cadeia de caracteres vazia), nenhuma Dica de Ferramenta é exibida.

Consulte o [atributo value](text-value.md) para um exemplo que ilustra como os atributos do **elemento TEXT** são usados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.value**](text-value.md)
</dt> <dt>

[**TEXT.wordWrap**](text-wordwrap.md)
</dt> </dl>

 

 





