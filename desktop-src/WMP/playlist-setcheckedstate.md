---
title: PLAYLIST.setCheckedState
description: O método setCheckedState especifica que o item indexado na playlist está marcado.
ms.assetid: ce5de21b-6354-485e-b6f7-f4d090c149f7
keywords:
- PLAYLIST.setCheckedState Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 93e143f738197524e1555f18aedf84aa606626de645a98149c65507b71291cde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336243"
---
# <a name="playlistsetcheckedstate"></a>PLAYLIST.setCheckedState

O **método setCheckedState** especifica que o item indexado na playlist está marcado.

``` syntax
        elementID.setCheckedState(item)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Item*
</dt> <dd>

**Número** (**longo**) que indica o índice do item de playlist a ser verificado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método retorna um **booliana.**

## <a name="remarks"></a>Comentários

Você pode definir todos os itens para o estado verificado especificando 1 no parâmetro *item.*

Esse método foi substituído por **setCheckedState2**, que dá suporte a playlists aninhadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.setCheckedState2**](playlist-setcheckedstate2.md)
</dt> </dl>

 

 





