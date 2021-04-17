---
title: Exibir. backgroundImage
description: O atributo backgroundImage especifica ou recupera a imagem de plano de fundo da exibição ou da subexibição.
ms.assetid: 60ffb257-2f43-4ae3-869d-3eb981ef4ae7
keywords:
- EXIBIR o Windows Media Player. backgroundImage
topic_type:
- apiref
api_name:
- VIEW.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96f4a93882e02589d7f15b74ba5cb225f506d69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751581"
---
# <a name="viewbackgroundimage"></a>Exibir. backgroundImage

O atributo **backgroundImage** especifica ou recupera a imagem de plano de fundo da **exibição** ou da **subexibição**.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Valores possíveis

Este atributo é uma **cadeia de caracteres** de leitura/gravação.

## <a name="remarks"></a>Comentários

Os formatos com suporte são BMP, JPG, GIF e PNG. Se a imagem for um arquivo BMP de 8 bits, seus valores de matiz e de saturação poderão ser alterados dinamicamente usando os atributos **backgroundImageHueShift** e **backgroundImageSaturation** .

Em um pacote de download do Windows Media, se você especificar o atributo **backgroundImage** para um elemento **View** , também deverá especificar o atributo **backgroundColor** para esse elemento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento VIEW**](view-element.md)
</dt> <dt>

[**Exibir. backgroundImageHueShift**](view-backgroundimagehueshift.md)
</dt> <dt>

[**Exibir. backgroundImageSaturation**](view-backgroundimagesaturation.md)
</dt> </dl>

 

 





