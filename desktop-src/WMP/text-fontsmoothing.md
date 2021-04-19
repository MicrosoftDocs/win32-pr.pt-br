---
title: TEXT. fontSmoothing
description: O atributo fontSmoothing especifica ou recupera um valor que indica se a suavização de fontes está habilitada.
ms.assetid: bd6f0468-285e-44b3-a5e8-361744c5ce4a
keywords:
- TEXT. fontSmoothing Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.fontSmoothing
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcdf285572b4edda0f514cb3519b6953f9e94677
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813548"
---
# <a name="textfontsmoothing"></a>TEXT. fontSmoothing

O atributo **fontSmoothing** especifica ou recupera um valor que indica se a suavização de fontes está habilitada.

``` syntax
        elementID.fontSmoothing
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** de leitura/gravação.



| Valor | Descrição                          |
|-------|--------------------------------------|
| true  | A suavização de fontes está habilitada.           |
| false | Padrão. A suavização de fontes está desabilitada. |



 

## <a name="remarks"></a>Comentários

A suavização de fontes usa o recurso de suavização de serrilhado do sistema operacional. Se a suavização de fontes estiver habilitada e o sistema operacional oferecer suporte a suavização de serrilhado, o Windows Media Player tentará suavizar o texto. Nem todas as fontes dão suporte à suavização de serrilhado. O Windows Media Player 10 usa o método de suavização de serrilhado Windows XP ClearType.

-   **Aviso** A suavização de fontes em uma cor transparente pode fazer com que a cor transparente seja mesclada nos caracteres. Não é recomendável que você use **fontSmoothing** se o texto for exibido em uma transparência.

Consulte o atributo [Value](text-value.md) para ver um exemplo ilustrando como os atributos do elemento **Text** são usados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento de texto**](text-element.md)
</dt> </dl>

 

 





