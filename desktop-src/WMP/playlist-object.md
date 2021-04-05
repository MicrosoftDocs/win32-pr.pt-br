---
title: Objeto playlist
description: O objeto playlist fornece uma maneira de organizar itens de mídia em uma lista para facilitar a manipulação usando as propriedades e os métodos a seguir.
ms.assetid: c2d2f265-b207-4b82-bb76-aee467f00659
keywords:
- Objeto de playlist Windows Media Player
topic_type:
- apiref
api_name:
- Playlist Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d517e13f8da103b1f9cee9498cce58a62eaf6462
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006318"
---
# <a name="playlist-object"></a>Objeto playlist

O objeto **playlist** fornece uma maneira de organizar itens de mídia em uma lista para facilitar a manipulação usando as propriedades e os métodos a seguir.

O objeto **playlist** oferece suporte às propriedades a seguir.



| Propriedade                                      | Descrição                                                      |
|-----------------------------------------------|------------------------------------------------------------------|
| [attributeCount](playlist-attributecount.md) | Recupera o número de atributos associados à playlist. |
| [attributeName](playlist-attributename.md)   | Recupera o nome de um atributo especificado por um índice.        |
| [contagem](playlist-count.md)                   | Recupera o número de itens na lista de reprodução.                   |
| [name](playlist-name.md)                     | Especifica ou recupera o nome da lista de reprodução.                 |



 

O objeto **playlist** dá suporte aos seguintes métodos.



| Método                                  | Descrição                                                                                            |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------|
| [appendItem](playlist-appenditem.md)   | Adiciona um item de mídia ao final da lista de reprodução.                                                          |
| **clear**                               | Reservado para uso futuro.                                                                               |
| [getItemInfo](playlist-getiteminfo.md) | Recupera o valor de um atributo de playlist.                                                           |
| [insertItem](playlist-insertitem.md)   | Insere um item de mídia na lista de reprodução no local especificado.                                      |
| [isidêntico](playlist-isidentical.md) | Recupera um valor que indica se o objeto de **playlist** fornecido é idêntico ao atual. |
| [item](playlist-item.md)               | Recupera o item de mídia no índice especificado.                                                       |
| [moveItem](playlist-moveitem.md)       | Altera o local de um item na lista de reprodução.                                                       |
| [removeItem](playlist-removeitem.md)   | Remove o item especificado da lista de reprodução.                                                          |
| [setItemInfo](playlist-setiteminfo.md) | Especifica o valor de um atributo de playlist.                                                           |



 

O objeto **playlist** é acessado por meio das propriedades e métodos a seguir.



| Objeto                                              | Propriedade ou método                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ROMs](cdrom-object.md)                           | [playlist](cdrom-playlist.md)                                                                                                                                                                                                                                                     |
| [Mediacollection](mediacollection-object.md)       | [getAll](mediacollection-getall.md), [getByAlbum](mediacollection-getbyalbum.md), [getByAttribute](mediacollection-getbyattribute.md), [getByAuthor](mediacollection-getbyauthor.md), [getByGenre](mediacollection-getbygenre.md), [getByName](mediacollection-getbyname.md) |
| [Jogador](player-object.md)                         | [currentPlaylist](player-currentplaylist.md), [newPlaylist](player-newplaylist.md)                                                                                                                                                                                               |
| [PlaylistArray](playlistarray-object.md)           | [item](playlistarray-item.md)                                                                                                                                                                                                                                                     |
| [Playlistcollection](playlistcollection-object.md) | [newPlaylist](playlistcollection-newplaylist.md)                                                                                                                                                                                                                                  |



 

Porque é o meio mais comum de acesso, *Player*. **currentPlaylist** é usado para fins de ilustração nas seções de sintaxe de referência.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




