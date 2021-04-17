---
title: PLAYLIST. setselecionostate
description: O método setselecionostate especifica que o item indexado na lista de reprodução está selecionado.
ms.assetid: 61770053-733f-40b5-8b1f-92b6975d3ad3
keywords:
- PLAYLIST. setselecionou Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 09a7bb545330710ae4fe2c39eae4556207061203
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791476"
---
# <a name="playlistsetselectedstate"></a>PLAYLIST. setselecionostate

O método **Setselecionostate** especifica que o item indexado na lista de reprodução está selecionado.

``` syntax
        elementID.setSelectedState(item)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*item*
</dt> <dd>

**Número** (**longo**) indicando o índice de um item na lista de reprodução.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Você pode definir todos os itens para o estado selecionado especificando 1 no parâmetro *Item* .

Esse método foi substituído por **setSelectedState2**, que dá suporte a listas de reprodução aninhadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. setSelectedState2**](playlist-setselectedstate2.md)
</dt> </dl>

 

 





