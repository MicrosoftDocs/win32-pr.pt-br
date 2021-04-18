---
title: LISTBOX. fontFace
description: O atributo fontFace especifica ou recupera a fonte do controle de caixa de listagem.
ms.assetid: 15e3180a-6e1e-4654-a0bb-164d66a86a26
keywords:
- LISTBOX. fontFace Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c03c367001b307dd8bd5059ec7e3f4a0b364e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796135"
---
# <a name="listboxfontface"></a>LISTBOX. fontFace

O atributo **fontface** especifica ou recupera a fonte do controle de caixa de listagem.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Valores possíveis

Este atributo é uma **cadeia de caracteres** de leitura/gravação.

## <a name="remarks"></a>Comentários

Esse atributo pode ser o nome de qualquer fonte válida disponível no Windows. O Windows Media Player não oferecerá suporte à instalação de fontes, portanto, escolha uma fonte que você sabe que estará no sistema pretendido.

Se o **fontface** especificado não estiver disponível no sistema do usuário, o controle caixa de listagem usa como padrão a fonte do sistema Windows. O valor padrão para sistemas de idioma inglês é "Tahoma". Para sistemas internacionais, o padrão é carregado a partir de um arquivo de recurso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------|
| Versão<br/> | Windows Media Player para Windows XP ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento LISTBOX**](listbox-element.md)
</dt> <dt>

[**Caixa de listagem. fontSize**](listbox-fontsize.md)
</dt> <dt>

[**LISTBOX. fontStyle**](listbox-fontstyle.md)
</dt> </dl>

 

 





