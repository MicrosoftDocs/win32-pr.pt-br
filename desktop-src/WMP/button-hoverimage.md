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
ms.openlocfilehash: 80b17a461ffde4b9f6777f3ce360c6b3f1747235
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781275"
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

 

 





