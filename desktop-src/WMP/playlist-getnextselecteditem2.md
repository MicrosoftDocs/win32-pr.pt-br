---
title: PLAYLIST.getNextSelectedItem2
description: O método getNextSelectedItem2 recupera o índice do próximo item selecionado na playlist após o índice especificado.
ms.assetid: 18acf95c-ab79-4b5c-b904-e13ef9a034dc
keywords:
- PLAYLIST.getNextSelectedItem2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6d1f98a418da1d8b21345598999f847cbf2142e9ca575bcfdc7047e2f9fd524
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415276"
---
# <a name="playlistgetnextselecteditem2"></a>PLAYLIST.getNextSelectedItem2

O **método getNextSelectedItem2** recupera o índice do próximo item selecionado na playlist após o índice especificado.

``` syntax
        elementID.getNextSelectedItem2(item)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Item*
</dt> <dd>

**Número** (**longo**) que indica o índice do item a ser pesquisado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método retorna um **Número** (**long**).

## <a name="remarks"></a>Comentários

Esse método pode trabalhar com playlists aninhadas e substitui o **método getNextSelectedItem,** que não pode. Passe 1 no parâmetro *de item* para encontrar o primeiro item selecionado. Quando não houver mais itens selecionados, -1 será retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.getNextSelectedItem**](playlist-getnextselecteditem.md)
</dt> </dl>

 

 





