---
title: Listas de reprodução e o objeto Playlistcollection
description: Listas de reprodução e o objeto Playlistcollection
ms.assetid: 63c8955b-34ad-447b-b734-657207bcecbb
keywords:
- Windows Media Player, listas de reprodução
- Modelo de objeto do Windows Media Player, listas de reprodução
- modelo de objeto, listas de reprodução
- Windows Media Player Mobile, listas de reprodução
- Controle ActiveX do Windows Media Player, listas de reprodução
- Controle ActiveX móvel do Windows Media Player, listas de reprodução
- Controle ActiveX, listas de reprodução
- listas de reprodução, objeto Playlistcollection
- listas de reprodução de metarquivo, objeto Playlistcollection
- Playlists do metarquivo do Windows Media, objeto Playlistcollection
- Objeto playlistcollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98744c2c5b97129db2824c42567802a374f90b6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105762393"
---
# <a name="playlists-and-the-playlistcollection-object"></a>Listas de reprodução e o objeto Playlistcollection

O objeto **playlistcollection** fornece acesso a listas de reprodução na biblioteca e tem métodos para criar listas de reprodução novas e vazias e novas listas de reprodução de metaarquivos.

## <a name="working-with-existing-playlists"></a>Trabalhando com listas de reprodução existentes

A *playlistcollection*. **getAll** e *playlistcollection*. os métodos **getByName** retornam um objeto **PlaylistArray** , que pode conter várias listas de reprodução.

A *playlistcollection*. o método **getAll** retorna todas as listas de reprodução existentes que estão na biblioteca. Por exemplo, você pode chamar esse método e, em seguida, recuperar as listas de reprodução no objeto **PlaylistArray** para determinar se um determinado nome de playlist já foi usado ou para exibir todas as listas de reprodução para o usuário. O código de exemplo em [atributos de playlist](playlist-attributes.md) usa o método **getAll** .

A *playlistcollection*. o método **getByName** retorna todas as listas de reprodução com um nome específico. Você pode usar esse método para lidar com cada uma dessas listas de reprodução separadamente.

Você também pode usar o método **getByName** para recuperar uma lista de reprodução exclusiva por nome. Nesse caso, o objeto **PlaylistArray** tem apenas um elemento. O exemplo de C# a seguir demonstra essa técnica.


```C++
IWMPPlaylistArray PlayListArray;
IWMPPlaylist Playlist;
// Store the playlist named "BluesTest" in the array
PlayListArray = Player.playlistCollection.getByName("BluesTest");
// Retrieve the first playlist in the collection.
Playlist = PlaylistArray.Item(0);

```



## <a name="working-with-new-playlists"></a>Trabalhando com novas listas de reprodução

Você pode usar a *playlistcollection*. método **newPlaylist** para criar uma lista de reprodução nova e vazia. O método retorna uma referência ao novo objeto de **lista de reprodução** . Em seguida, você pode chamar a *lista de reprodução*. método **appendItem** para adicionar itens de mídia à lista de reprodução.

Você também pode criar uma nova lista de reprodução com base em um metarquivo de playlist. Primeiro, passe o nome da lista de reprodução e o caminho para o metarquivo para o *Player*. método **newPlaylist** . Esse método retorna uma referência ao novo objeto de **lista de reprodução** . Em seguida, passe o novo objeto **playlist** para a *playlistcollection*. método **importPlaylist** para adicioná-lo à biblioteca.

Observe a diferença entre *playlistcollection*. método **newPlaylist** e o *Player*. método **newPlaylist** . O método **playlistcollection** cria uma nova lista de reprodução vazia e a adiciona à biblioteca. O método **Player** cria um novo objeto de **lista de reprodução** populado, mas não o adiciona à biblioteca.

Ao longo deste tópico, o objeto **Player** foi definido da seguinte maneira:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



O exemplo de C# a seguir demonstra a importação de uma lista de reprodução de um metarquivo. O argumento *strPListName* especifica o nome da nova lista de reprodução. O *strMetaFileName* especifica o nome do metarquivo do qual a lista de reprodução é importada.


```C++
private IWMPPlaylist importPlaylist(string strPlaylistName, string strMetaFileName)
{
    IWMPPlaylist  NewPlaylist;
    IWMPPlaylist  ImportPlaylist;

    NewPlaylist = Player.newPlaylist(strPlaylistName, strMetaFileName);
    ImportPlaylist = Player.playlistCollection.importPlaylist(NewPlaylist);

    return ImportPlaylist;
}

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gerenciando listas de reprodução**](managing-playlists.md)
</dt> <dt>

[**Player. newPlaylist**](player-newplaylist.md)
</dt> <dt>

[**Playlist. appendItem**](playlist-appenditem.md)
</dt> <dt>

[**Objeto PlaylistArray**](playlistarray-object.md)
</dt> <dt>

[**Objeto playlistcollection**](playlistcollection-object.md)
</dt> <dt>

[**Listas de reprodução e itens de mídia**](playlists-and-media-items.md)
</dt> </dl>

 

 




