---
title: TEXTO. rolagem
description: O atributo de rolagem especifica ou recupera um valor que indica se o texto rola.
ms.assetid: 1cd5cb4e-673f-4273-91ff-50165c2b08fa
keywords:
- TEXT. rolando o Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.scrolling
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fdbb80b2033d542da4894172d58451ed5da224f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768298"
---
# <a name="textscrolling"></a>TEXTO. rolagem

O atributo de **rolagem** especifica ou recupera um valor que indica se o texto rola.

``` syntax
        elementID.scrolling
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** de leitura/gravação.



| Valor | Descrição                     |
|-------|---------------------------------|
| true  | A rolagem está habilitada.           |
| false | Padrão. A rolagem está desabilitada. |



 

## <a name="remarks"></a>Comentários

O recurso de rolagem fornece um buffer de dois espaços entre o fim do texto e o início da linha repetida.

O atributo de **justificativa** especifica onde o texto aparece primeiro antes do início da rolagem.

Consulte o atributo [Value](text-value.md) para ver um exemplo ilustrando como os atributos do elemento **Text** são usados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento de texto**](text-element.md)
</dt> <dt>

[**TEXTO. justificativa**](text-justification.md)
</dt> <dt>

[**TEXT. scrollingAmount**](text-scrollingamount.md)
</dt> <dt>

[**TEXT. scrollingDelay**](text-scrollingdelay.md)
</dt> <dt>

[**TEXT. scrollingDirection**](text-scrollingdirection.md)
</dt> </dl>

 

 





