---
title: PLAYLIST. getNextSelectedItem
description: O método getNextSelectedItem recupera o índice do próximo item selecionado na lista de reprodução após o índice especificado.
ms.assetid: d46d3a65-8863-4a2f-9add-0701c8283a6b
keywords:
- PLAYLIST. getNextSelectedItem Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c5e37ad5109066a11cf28a593ed69f8c86b8b639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105798388"
---
# <a name="playlistgetnextselecteditem"></a>PLAYLIST. getNextSelectedItem

O método **getNextSelectedItem** recupera o índice do próximo item selecionado na lista de reprodução após o índice especificado.

``` syntax
        elementID.getNextSelectedItem(item)
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

Quando não há nenhum outro item selecionado, esse método retorna 1.

Esse método foi substituído por **getNextSelectedItem2**, que dá suporte a listas de reprodução aninhadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. getNextSelectedItem2**](playlist-getnextselecteditem2.md)
</dt> </dl>

 

 





