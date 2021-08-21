---
title: PLAYLIST.setCheckedState2
description: O método setCheckedState2 define o estado verificado do item com o índice especificado no elemento PLAYLIST.
ms.assetid: 241221a3-810b-422d-8f73-25c5b5c82c70
keywords:
- PLAYLIST.setCheckedState2 Windows Media Player
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
# <a name="playlistsetcheckedstate2"></a>PLAYLIST.setCheckedState2

O **método setCheckedState2** define o estado verificado do item com o índice especificado no elemento **PLAYLIST.**

``` syntax
        elementID.setCheckedState(item, checked)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Item*
</dt> <dd>

**Número** (**longo**) que indica o índice do item de playlist a ser verificado ou desmarcado.

</dd> <dt>

<span id="checked"></span><span id="CHECKED"></span>*Verificado*
</dt> <dd>

**Booliana** que indica se o item especificado deve ser verificado (true) ou desmarcado (false).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método retorna um **booliana.**

## <a name="remarks"></a>Comentários

Esse método pode trabalhar com playlists aninhadas e substitui o **método setCheckedState,** que não pode. Você pode definir todos os itens para o estado solicitado especificando 1 no parâmetro *item.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.setCheckedState**](playlist-setcheckedstate.md)
</dt> </dl>

 

 





