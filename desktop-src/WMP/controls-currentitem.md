---
title: Controls.currentItem
description: A propriedade currentItem especifica ou recupera o item de mídia atual.
ms.assetid: 77e21585-3cc8-41f5-97b5-da6eb992c7bc
keywords:
- Controls.currentItem Windows Media Player
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
ms.openlocfilehash: 66dc0ad047213e0fbba7dbdd7336e67b8d015e39aba510ac37bd3701462413ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997546"
---
# <a name="controlscurrentitem"></a>Controls.currentItem

A **propriedade currentItem** especifica ou recupera o item de mídia atual.

``` syntax
player.controls.currentItem
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um objeto de mídia **de** leitura/gravação.

## <a name="remarks"></a>Comentários

Esse método funciona apenas com itens no *Player*. **currentPlaylist**. Não há suporte para chamar **currentItem** com uma referência a um item de mídia salvo.

## <a name="examples"></a>Exemplos

O exemplo JScript a seguir usa **currentItem** para definir o item de mídia atual do controle de player para o valor selecionado em um elemento HTML SELECT. A playlist atual foi especificada pela primeira vez usando *PlaylistCollection*. **getByName.** O **objeto** Player foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





