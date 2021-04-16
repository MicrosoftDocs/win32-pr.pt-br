---
title: PLAYLIST. setcheckstate
description: O método setcheckstate especifica que o item indexado na playlist está marcado.
ms.assetid: ce5de21b-6354-485e-b6f7-f4d090c149f7
keywords:
- PLAYLIST. setcheckstate do Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a8c86459dcf590b1ff1e884a8aa671dc1bba78a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105773047"
---
# <a name="playlistsetcheckedstate"></a>PLAYLIST. setcheckstate

O método **Setcheckstate** especifica que o item indexado na playlist está marcado.

``` syntax
        elementID.setCheckedState(item)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*item*
</dt> <dd>

**Número** (**longo**) indicando o índice do item da playlist a ser verificado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método retorna um **valor booleano**.

## <a name="remarks"></a>Comentários

Você pode definir todos os itens para o estado Checked especificando 1 no parâmetro *Item* .

Esse método foi substituído por **setCheckedState2**, que dá suporte a listas de reprodução aninhadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. setCheckedState2**](playlist-setcheckedstate2.md)
</dt> </dl>

 

 





