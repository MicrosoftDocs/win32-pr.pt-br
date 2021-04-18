---
title: PLAYLIST. getNextCheckedItem
description: O método getNextCheckedItem recupera o índice do próximo item selecionado na lista de reprodução após o índice especificado.
ms.assetid: 474a497d-5efe-4c95-8eb5-2ba71bd29057
keywords:
- PLAYLIST. getNextCheckedItem Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b4a85fdccc5de227ab8aea3d0ee4f93d46eed50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784606"
---
# <a name="playlistgetnextcheckeditem"></a>PLAYLIST. getNextCheckedItem

O método **getNextCheckedItem** recupera o índice do próximo item selecionado na lista de reprodução após o índice especificado.

``` syntax
        elementID.getNextCheckedItem(item)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*item*
</dt> <dd>

**Número** (**longo**) indicando o índice do item a ser pesquisado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método retorna um **número** (**longo**).

## <a name="remarks"></a>Comentários

Quando não há itens marcados adicionais, esse método retorna 1.

Esse método foi substituído por **getNextCheckedItem2**, que dá suporte a listas de reprodução aninhadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. getNextCheckedItem2**](playlist-getnextcheckeditem2.md)
</dt> </dl>

 

 





