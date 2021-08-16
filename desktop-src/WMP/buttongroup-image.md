---
title: BUTTONGROUP.image
description: O atributo de imagem especifica ou recupera o nome da imagem que representa os botões de um BUTTONGROUP.
ms.assetid: dad50a1e-d147-4e0f-b5d6-8cbfeef32438
keywords:
- BUTTONGROUP.image Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2fcd8d76bd217087b6b948cec3216efc2bbc6c9845e9c18b5a7619d292232b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342629"
---
# <a name="buttongroupimage"></a>BUTTONGROUP.image

O **atributo** de imagem especifica ou recupera o nome da imagem que representa os botões de um **BUTTONGROUP.**

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma cadeia de caracteres de **leitura/gravação.**

## <a name="remarks"></a>Comentários

Os formatos de imagem com suporte são BMP, JPG, PNG e GIF. Se a imagem for um arquivo BMP de 8 bits, seus valores de matiz e saturação poderão ser alterados dinamicamente usando os atributos **hueShift** **e saturação.**

Se a imagem do controle for maior que a região definida, a imagem será cortada.

Se a imagem não puder ser recuperada, uma imagem padrão (a imagem x vermelha) será exibida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP.hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP.s saturação**](buttongroup-saturation.md)
</dt> </dl>

 

 





