---
title: BUTTON. hoverImage
description: O atributo hoverImage especifica ou recupera a imagem exibida quando o botão está no estado ativo e o usuário passa sobre ele com o ponteiro do mouse.
ms.assetid: 6704e63d-1def-4e8e-808f-131c3cc1c0de
keywords:
- BUTTON. hoverImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8488fb599a958a96ef7b5aaa5afbf4c219110f0da5be7016a8190efe2004475d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003716"
---
# <a name="buttonhoverimage"></a>BUTTON. hoverImage

O atributo **hoverImage** especifica ou recupera a imagem exibida quando o **botão** está no estado ativo e o usuário passa sobre ele com o ponteiro do mouse.

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome do arquivo de imagem.

## <a name="remarks"></a>Comentários

Os formatos de imagem com suporte são BMP, JPG, PNG e GIF.

A imagem padrão é aquela especificada no atributo **Image** ou seu padrão.

Se a imagem em foco for maior do que a região definida no atributo ambiente, a imagem em foco será cortada.

Se a imagem não puder ser recuperada, uma imagem padrão (a imagem vermelha-x) será exibida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BOTÃO. imagem**](button-image.md)
</dt> </dl>

 

 





