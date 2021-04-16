---
title: PLAYLIST. getNextCheckedItem2
description: O método getNextCheckedItem2 recupera o índice do próximo item selecionado na lista de reprodução após o índice especificado.
ms.assetid: 64e51fd1-eb0f-47e5-8684-96824f4f3194
keywords:
- PLAYLIST. getNextCheckedItem2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50bb2fd6ed6e3328df29a59381571204ebd28369
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765233"
---
# <a name="playlistgetnextcheckeditem2"></a>PLAYLIST. getNextCheckedItem2

O método **getNextCheckedItem2** recupera o índice do próximo item selecionado na lista de reprodução após o índice especificado.

``` syntax
        elementID.getNextCheckedItem2(item)
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

Esse método pode trabalhar com listas de reprodução aninhadas e substituir o método **getNextCheckedItem** , que não pode. Passe 1 no parâmetro *Item* para localizar o primeiro item selecionado. Quando não há itens marcados adicionais, esse método retorna 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. getNextCheckedItem**](playlist-getnextcheckeditem.md)
</dt> </dl>

 

 





