---
title: TEXT. fontFace
description: O atributo fontFace especifica ou recupera o tipo de fonte para o controle de texto.
ms.assetid: 3b39e245-139a-4361-b678-0f9e962996b7
keywords:
- Windows Media Player TEXT. fontFace
topic_type:
- apiref
api_name:
- TEXT.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3b1044d01ac3ca6a8cc4f1212232bfcc630eb73831f90eb7fd5f423f5dc38d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118348"
---
# <a name="textfontface"></a>TEXT. fontFace

O atributo **fontface** especifica ou recupera o tipo de fonte para o controle de texto.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Valores possíveis

Este atributo é uma **cadeia de caracteres** de leitura/gravação.

## <a name="remarks"></a>Comentários

Esse atributo pode ser o nome de qualquer fonte válida disponível em Windows. Windows Media Player não dará suporte à instalação de fontes, portanto, escolha uma fonte que você sabe que estará no sistema pretendido.

se o **fontFace** especificado não estiver disponível no sistema do usuário, o controle de texto usa como padrão a fonte do sistema Windows.

Consulte o atributo [Value](text-value.md) para ver um exemplo ilustrando como os atributos do elemento **Text** são usados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento de texto**](text-element.md)
</dt> <dt>

[**TEXT. fontSize**](text-fontsize.md)
</dt> </dl>

 

 





