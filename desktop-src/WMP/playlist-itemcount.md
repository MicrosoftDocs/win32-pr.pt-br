---
title: PLAYLIST. itemCount
description: O atributo itemCount recupera o número de itens atualmente exibidos no elemento PLAYLIST.
ms.assetid: d090d95c-e3c3-41bc-951e-ffeb0a314a0c
keywords:
- PLAYLIST. itemCount Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbde81ee6c2849a19c6400fee4ef7fa6514eaefe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811207"
---
# <a name="playlistitemcount"></a>PLAYLIST. itemCount

O atributo **ItemCount** recupera o número de itens atualmente exibidos no elemento **playlist** .

``` syntax
        elementID.itemCount
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **número** somente leitura (**Long**).

## <a name="remarks"></a>Comentários

A propriedade **ItemCount** contará o número total de itens expandidos. Por exemplo, se houver duas listas de reprodução que contenham três itens de mídia cada, **ItemCount** retornará 2 se as listas de reprodução não forem expandidas. Se apenas a primeira playlist for expandida, **ItemCount** retornará 4. Se ambas as listas de reprodução forem expandidas, **ItemCount** retornará 6.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





