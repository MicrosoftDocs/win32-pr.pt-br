---
title: PLAYLIST. getNextSelectedItem2
description: O método getNextSelectedItem2 recupera o índice do próximo item selecionado na lista de reprodução após o índice especificado.
ms.assetid: 18acf95c-ab79-4b5c-b904-e13ef9a034dc
keywords:
- PLAYLIST. getNextSelectedItem2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 27d166887bb2fa98e184e1f64f4aaceb89930d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764525"
---
# <a name="playlistgetnextselecteditem2"></a>PLAYLIST. getNextSelectedItem2

O método **getNextSelectedItem2** recupera o índice do próximo item selecionado na lista de reprodução após o índice especificado.

``` syntax
        elementID.getNextSelectedItem2(item)
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

Esse método pode trabalhar com listas de reprodução aninhadas e substituir o método **getNextSelectedItem** , que não pode. Passe 1 no parâmetro *Item* para localizar o primeiro item selecionado. Quando não há mais itens selecionados,-1 é retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. getNextSelectedItem**](playlist-getnextselecteditem.md)
</dt> </dl>

 

 





