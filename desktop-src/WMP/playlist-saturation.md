---
title: PLAYLIST. saturação
description: O atributo saturação especifica ou recupera o valor de saturação das imagens suspensas.
ms.assetid: 4c5dd3d9-828a-45c9-896a-9a702d354544
keywords:
- PLAYLIST. saturação do Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.saturation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82eb53afeafb0754f0e754f68fd5ff785eaade8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771523"
---
# <a name="playlistsaturation"></a>PLAYLIST. saturação

O atributo **saturação** especifica ou recupera o valor de saturação das imagens suspensas.

``` syntax
        elementID.saturation
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **número** de leitura/gravação (**float**) com um valor que varia de 0,0 a 2,0 com um valor padrão de 1,0.

## <a name="remarks"></a>Comentários

Esse atributo altera o valor de saturação das imagens especificadas pelos atributos **dropDownBackgroundImage** e **dropDownImage** se eles tiverem sido especificados e se referirem a imagens bmp de 8 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. dropDownBackgroundImage**](playlist-dropdownbackgroundimage.md)
</dt> <dt>

[**PLAYLIST. dropDownImage**](playlist-dropdownimage.md)
</dt> <dt>

[**PLAYLIST. hueShift**](playlist-hueshift.md)
</dt> </dl>

 

 





