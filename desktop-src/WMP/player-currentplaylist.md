---
title: Player. currentPlaylist
description: A propriedade currentPlaylist especifica ou recupera o objeto de playlist atual.
ms.assetid: fabfb927-5f64-4fc4-8ee5-e2449082dfbc
keywords:
- Windows Media Player Player. currentPlaylist
topic_type:
- apiref
api_name:
- Player.currentPlaylist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7139c567eab5fbb3c324916dec260d34f57429cb50bb99d199f35be8aee7a1c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118573211"
---
# <a name="playercurrentplaylist"></a>Player. currentPlaylist

A propriedade currentPlaylist especifica ou recupera o objeto de **playlist** atual.

## <a name="syntax"></a>Sintaxe

*Player* . **currentPlaylist**

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é um objeto de **lista de reprodução** de leitura/gravação.

## <a name="remarks"></a>Comentários

se o *Configurações*. a propriedade **AutoStart** é true, a reprodução é iniciada automaticamente sempre que você definir **currentPlaylist**.

Essa propriedade usa um objeto playlist, que pode ser adquirido de várias maneiras, como ao chamar *PlaylistArray*. **Item** ou *playlistcollection*. **newPlaylist**. Para carregar um item da **playlist** usando um nome de arquivo, defina a propriedade URL ou use *Player*. **newPlaylist**.

## <a name="examples"></a>Exemplos

o exemplo a seguir JScript recupera a primeira lista de reprodução na biblioteca. Em seguida, ele usa **currentPlaylist** para tornar a lista de reprodução recuperada a playlist atual e, em seguida, exibir o nome da lista de reprodução atual. O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Retrieve the first playlist from the library.
var firstPL = Player.playlistCollection.getAll().item(0);

// Make the retrieved playlist the current playlist.
Player.currentPlaylist = firstPL;

// Display the name of the current playlist.
document.write("Found first playlist. Name: " + Player.currentPlaylist.name);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> <dt>

[**Player. newPlaylist**](player-newplaylist.md)
</dt> <dt>

[**Objeto playlist**](playlist-object.md)
</dt> <dt>

[**PlaylistArray. Item**](playlistarray-item.md)
</dt> <dt>

[**Playlistcollection. newPlaylist**](playlistcollection-newplaylist.md)
</dt> <dt>

[**Configurações. autostart**](settings-autostart.md)
</dt> </dl>

 

 





