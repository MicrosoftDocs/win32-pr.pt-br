---
title: VIEW.backgroundImage
description: O atributo backgroundImage especifica ou recupera a imagem de plano de fundo do VIEW ou SUBVIEW.
ms.assetid: 60ffb257-2f43-4ae3-869d-3eb981ef4ae7
keywords:
- VIEW.backgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1de8bcbd0eb47f03aaff46b4292a8afe226ca8a221ec570537351af8e509801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761736"
---
# <a name="viewbackgroundimage"></a>VIEW.backgroundImage

O **atributo backgroundImage** especifica ou recupera a imagem de plano de fundo do **VIEW** ou **SUBVIEW.**

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma cadeia de caracteres de **leitura/gravação.**

## <a name="remarks"></a>Comentários

Os formatos com suporte são BMP, JPG, GIF e PNG. Se a imagem for um arquivo BMP de 8 bits, seus valores de matiz e saturação poderão ser alterados dinamicamente usando os atributos **backgroundImageShift** e **backgroundImageSaturation.**

Em um Windows de Download de Mídia, se você especificar o atributo **backgroundImage** para um elemento **VIEW,** também deverá especificar o atributo **backgroundColor** para esse elemento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento VIEW**](view-element.md)
</dt> <dt>

[**VIEW.backgroundImageShift**](view-backgroundimagehueshift.md)
</dt> <dt>

[**VIEW.backgroundImageS saturação**](view-backgroundimagesaturation.md)
</dt> </dl>

 

 





