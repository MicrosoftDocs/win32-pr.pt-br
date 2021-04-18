---
title: FontFace de edição
description: O atributo fontFace especifica ou recupera a fonte para texto no controle da caixa de edição.
ms.assetid: 5fb5e6d2-8535-402e-9ca1-d43e334e94e3
keywords:
- Admy. fontFace Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c5794da93821db840a48facbba45540da9249a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770503"
---
# <a name="editboxfontface"></a>FontFace de edição

O atributo **fontface** especifica ou recupera a fonte para texto no controle da caixa de edição.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Valores possíveis

Este atributo é uma **cadeia de caracteres** de leitura/gravação.

## <a name="remarks"></a>Comentários

Esse atributo pode ser o nome de qualquer fonte válida disponível no Windows. O Windows Media Player não oferecerá suporte à instalação de fontes, portanto, escolha uma fonte que você sabe que estará no sistema pretendido.

Se o **fontface** especificado não estiver disponível no sistema do usuário, o controle caixa de edição usa como padrão a fonte do sistema Windows. O valor padrão para sistemas de idioma inglês é "Tahoma". Para sistemas internacionais, o padrão é carregado a partir de um arquivo de recurso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------|
| Versão<br/> | Windows Media Player para Windows XP ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento admy**](editbox-element.md)
</dt> <dt>

[**Mythe. fontSize**](editbox-fontsize.md)
</dt> <dt>

[**FontStyle de edição**](editbox-fontstyle.md)
</dt> </dl>

 

 





