---
title: Controls. currentItem
description: A propriedade currentItem especifica ou recupera o item de mídia atual.
ms.assetid: 77e21585-3cc8-41f5-97b5-da6eb992c7bc
keywords:
- Controls. currentItem Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentItem
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81658665cb6f31acd327f5050a733a2fc3c70371
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788182"
---
# <a name="controlscurrentitem"></a>Controls. currentItem

A propriedade **currentItem** especifica ou recupera o item de mídia atual.

``` syntax
player.controls.currentItem
      
```

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é um objeto de **mídia** de leitura/gravação.

## <a name="remarks"></a>Comentários

Esse método funciona apenas com itens no *Player*. **currentPlaylist**. Não há suporte para chamar **currentItem** com uma referência a um item de mídia salvo.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa **currentItem** para definir o item de mídia atual do controle Player para o valor selecionado em um elemento HTML SELECT. A playlist atual foi especificada pela primeira vez usando *playlistcollection*. **getByName**. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<SELECT ID = playItem  NAME = "playItem"  LANGUAGE = "JScript"

    /* Specify the current item when the selected list value changes. */
    onChange = "Player.controls.currentItem = Player.currentPlaylist.item(playItem.value);">

    /* Fill the SELECT element list with three items that match
       the songs in the playlist. */
    <OPTION VALUE = 0 >Laure
    <OPTION VALUE = 1 >Jeanne
    <OPTION VALUE = 2 >House
</SELECT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Playlistcollection. getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





