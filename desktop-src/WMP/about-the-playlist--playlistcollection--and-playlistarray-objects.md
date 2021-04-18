---
title: Sobre os objetos playlist, Playlistcollection e PlaylistArray
description: Sobre os objetos playlist, Playlistcollection e PlaylistArray
ms.assetid: 19867944-c836-4b7e-ada3-f696905e6327
keywords:
- Windows Media Player, objeto playlist
- Modelo de objeto do Windows Media Player, objeto playlist
- modelo de objeto, objeto playlist
- Controle ActiveX do Windows Media Player, objeto playlist
- Controle ActiveX, objeto playlist
- Controle ActiveX móvel do Windows Media Player, objeto playlist
- Windows Media Player Mobile, objeto playlist
- Objeto playlist
- Windows Media Player, objeto Playlistcollection
- Modelo de objeto do Windows Media Player, objeto Playlistcollection
- modelo de objeto, objeto Playlistcollection
- Controle ActiveX do Windows Media Player, objeto Playlistcollection
- Controle ActiveX, objeto Playlistcollection
- Controle ActiveX móvel do Windows Media Player, objeto Playlistcollection
- Windows Media Player Mobile, objeto Playlistcollection
- Objeto playlistcollection
- Windows Media Player, objeto PlaylistArray
- Modelo de objeto do Windows Media Player, objeto PlaylistArray
- modelo de objeto, objeto PlaylistArray
- Controle ActiveX do Windows Media Player, objeto PlaylistArray
- Controle ActiveX, objeto PlaylistArray
- Controle ActiveX móvel do Windows Media Player, objeto PlaylistArray
- Windows Media Player Mobile, objeto PlaylistArray
- Objeto PlaylistArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee9d24f4f5decc28a369e44910990ff41b99e9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105781067"
---
# <a name="about-the-playlist-playlistcollection-and-playlistarray-objects"></a>Sobre os objetos playlist, Playlistcollection e PlaylistArray

Os objetos **playlist**, **playlistcollection** e **PlaylistArray** regem as listas de reprodução que o Windows Media Player pode usar para especificar a ordem na qual o conteúdo será reproduzido. Você Obtém o objeto **playlistcollection** da propriedade **playlistcollection** do objeto **Player** . A propriedade **playlistcollection** retorna o objeto **playlistcollection** . Você só pode acessar as propriedades do objeto **playlistcollection** depois de criá-lo. Por exemplo, para criar uma nova lista de reprodução, primeiro você deve obter o objeto **playlistcollection** e, em seguida, usar um método nesse objeto.


```C++
player.playlistcollection.newplaylist('myplaylist');
```



Você pode obter a lista de reprodução atual usando a propriedade **currentPlaylist** . Por exemplo, para obter o nome da playlist atual, use o seguinte código:


```C++
myname = player.currentplaylist.name;
```



O objeto **PlaylistArray** é retornado pelos métodos **getAll** e **getByName** do objeto **playlistcollection** . Para obter o número de listas de reprodução, por exemplo, use o seguinte código:


```C++
howmany = player.playlistcollection.getAll().count;
```



Para recuperar uma lista de reprodução conhecida por nome, use o seguinte código:


```C++
if (player.playlistcollection.getbyname('myplaylist').count == 1) {
    pl = player.playlistcollection.getbyname('myplaylist').item(0);
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Modelo de objeto do Player para linguagens de script**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Objeto playlist**](playlist-object.md)
</dt> <dt>

[**Objeto PlaylistArray**](playlistarray-object.md)
</dt> <dt>

[**Objeto playlistcollection**](playlistcollection-object.md)
</dt> </dl>

 

 




