---
title: PLAYLIST. setCheckedState2
description: O método setCheckedState2 define o estado de ativação do item com o índice especificado no elemento PLAYLIST.
ms.assetid: 241221a3-810b-422d-8f73-25c5b5c82c70
keywords:
- PLAYLIST. setCheckedState2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 37cc9c821ae783e79d327e93b0c2f297fb75eab1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762374"
---
# <a name="playlistsetcheckedstate2"></a>PLAYLIST. setCheckedState2

O método **setCheckedState2** define o estado de ativação do item com o índice especificado no elemento **playlist** .

``` syntax
        elementID.setCheckedState(item, checked)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*item*
</dt> <dd>

**Número** (**longo**) que indica o índice do item da playlist a ser marcado ou desmarcado.

</dd> <dt>

<span id="checked"></span><span id="CHECKED"></span>*check*
</dt> <dd>

**Booliano** que indica se o item especificado deve ser marcado (true) ou desmarcado (false).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método retorna um **valor booleano**.

## <a name="remarks"></a>Comentários

Esse método pode trabalhar com listas de reprodução aninhadas e substituir o método **Setcheckstate** , que não pode. Você pode definir todos os itens para o estado solicitado especificando 1 no parâmetro *Item* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. setcheckstate**](playlist-setcheckedstate.md)
</dt> </dl>

 

 





