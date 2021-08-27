---
title: PLAYLIST.setSelectedState2
description: O método setSelectedState2 define o estado selecionado do item com o índice especificado no elemento PLAYLIST.
ms.assetid: 990b834a-f7ed-45b8-99e1-3efd7f4447f4
keywords:
- PLAYLIST.setSelectedState2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f952d00486fe2419ab48592c7624299ef466c5dfa2b96d53fefb308fc537488
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335808"
---
# <a name="playlistsetselectedstate2"></a>PLAYLIST.setSelectedState2

O **método setSelectedState2** define o estado selecionado do item com o índice especificado no elemento **PLAYLIST.**

``` syntax
        elementID.setSelectedState2(item, selected)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Item*
</dt> <dd>

**Número** (**longo**) que indica o índice de um item na playlist.

</dd> <dt>

<span id="selected"></span><span id="SELECTED"></span>*Selecionado*
</dt> <dd>

**Booliana** que indica se o item especificado deve ser selecionado (true) ou não selecionado (false).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método pode trabalhar com playlists aninhadas e substitui o **método setSelectedState** que não pode. Você pode definir todos os itens para o estado solicitado especificando 1 no parâmetro *item.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.setSelectedState**](playlist-setselectedstate.md)
</dt> </dl>

 

 





