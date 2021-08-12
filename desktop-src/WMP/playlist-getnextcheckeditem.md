---
title: PLAYLIST.getNextCheckedItem
description: O método getNextCheckedItem recupera o índice do próximo item verificado na playlist após o índice especificado.
ms.assetid: 474a497d-5efe-4c95-8eb5-2ba71bd29057
keywords:
- PLAYLIST.getNextCheckedItem Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 54b6e598737d1aac09754b15c037c27a435deb5fff34c729aa48c51019e12982
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571446"
---
# <a name="playlistgetnextcheckeditem"></a>PLAYLIST.getNextCheckedItem

O **método getNextCheckedItem** recupera o índice do próximo item verificado na playlist após o índice especificado.

``` syntax
        elementID.getNextCheckedItem(item)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Item*
</dt> <dd>

**Número** (**longo**) que indica o índice do item a ser pesquisado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método retorna um **Número** (**long**).

## <a name="remarks"></a>Comentários

Quando não há mais itens verificados, esse método retorna 1.

Esse método foi substituído por **getNextCheckedItem2**, que dá suporte a playlists aninhadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.getNextCheckedItem2**](playlist-getnextcheckeditem2.md)
</dt> </dl>

 

 





