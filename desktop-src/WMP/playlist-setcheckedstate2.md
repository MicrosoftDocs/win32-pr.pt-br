---
title: PLAYLIST. setCheckedState2
description: O método setCheckedState2 define o estado de ativação do item com o índice especificado no elemento PLAYLIST.
ms.assetid: 241221a3-810b-422d-8f73-25c5b5c82c70
keywords:
- Windows Media Player de PLAYLIST. setCheckedState2
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b6b95cb332c5f5a9d86e6f49484b27c1ab5802f28b18195f610395a1c732e369
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336215"
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

 

 





