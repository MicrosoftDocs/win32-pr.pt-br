---
title: PLAYLIST. getNextSelectedItem
description: O método getNextSelectedItem recupera o índice do próximo item selecionado na lista de reprodução após o índice especificado.
ms.assetid: d46d3a65-8863-4a2f-9add-0701c8283a6b
keywords:
- Windows Media Player de PLAYLIST. getNextSelectedItem
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 872dd31694384dfa35d7ce98c2f26756ede14539f4e788cbb6f699d17ca78a8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467746"
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

 

 





