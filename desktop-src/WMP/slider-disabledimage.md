---
title: SLIDER. disabledImage
description: O atributo disabledImage especifica ou recupera a imagem do controle deslizante que é usado quando o controle deslizante está desabilitado.
ms.assetid: b6c4237d-8eb0-44ce-a23f-9bdc5c21aca8
keywords:
- Controle deslizante. disabledImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1b90dcbd551ca0f8bb332f858eac0b69c46733
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755507"
---
# <a name="sliderdisabledimage"></a>SLIDER. disabledImage

O atributo **disabledImage** especifica ou recupera a imagem do controle deslizante que é usado quando o controle deslizante está desabilitado.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome de um arquivo de imagem.

## <a name="remarks"></a>Comentários

O **disabledImage** é opcional. Se não for fornecido, o **backgroundImage** será usado para todos os Estados desabilitados. Quando um controle deslizante está desabilitado, nenhuma imagem de primeiro plano é visível.

Os formatos com suporte são BMP, JPG, PNG e GIF (não incluindo GIFs animados).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER. backgroundImage**](slider-backgroundimage.md)
</dt> </dl>

 

 





