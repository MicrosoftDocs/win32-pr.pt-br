---
title: BUTTONGROUP.downImage
description: O atributo downImage especifica ou recupera o nome da imagem que representa o estado para baixo do BUTTONGROUP.
ms.assetid: 022e77e7-d3c0-41b5-984a-84d016a5a25a
keywords:
- BUTTONGROUP.downImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 233c56951ec88444ab58de901732517a4ced4c249f8a9b75f3461eb38e86c975
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997746"
---
# <a name="buttongroupdownimage"></a>BUTTONGROUP.downImage

O **atributo downImage** especifica ou recupera o nome da imagem que representa o estado para baixo do **BUTTONGROUP.**

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma cadeia de caracteres de **leitura/gravação.**

## <a name="remarks"></a>Comentários

Os formatos de imagem com suporte são BMP, JPG, PNG e GIF. Se a imagem for um arquivo BMP de 8 bits, seus valores de matiz e saturação poderão ser alterados dinamicamente usando os atributos **hueShift** **e saturação.**

A imagem padrão é a especificada no atributo **de** imagem.

Se a imagem para baixo for maior que a região definida, a imagem para baixo será cortada.

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

[**BUTTONGROUP.image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP.s saturação**](buttongroup-saturation.md)
</dt> </dl>

 

 





