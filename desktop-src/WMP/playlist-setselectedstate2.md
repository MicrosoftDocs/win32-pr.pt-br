---
title: PLAYLIST. setSelectedState2
description: O método setSelectedState2 define o estado selecionado do item com o índice especificado no elemento PLAYLIST.
ms.assetid: 990b834a-f7ed-45b8-99e1-3efd7f4447f4
keywords:
- PLAYLIST. setSelectedState2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1a4e317543765fb24755516a0637b16958ad679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771767"
---
# <a name="playlistsetselectedstate2"></a>PLAYLIST. setSelectedState2

O método **setSelectedState2** define o estado selecionado do item com o índice especificado no elemento **playlist** .

``` syntax
        elementID.setSelectedState2(item, selected)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*item*
</dt> <dd>

**Número** (**longo**) indicando o índice de um item na lista de reprodução.

</dd> <dt>

<span id="selected"></span><span id="SELECTED"></span>*Selecione*
</dt> <dd>

**Booliano** que indica se o item especificado deve ser selecionado (true) ou não selecionado (false).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método pode trabalhar com listas de reprodução aninhadas e substituir o método **Setselecionostate** que não pode. Você pode definir todos os itens para o estado solicitado especificando 1 no parâmetro *Item* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. setselecionostate**](playlist-setselectedstate.md)
</dt> </dl>

 

 





