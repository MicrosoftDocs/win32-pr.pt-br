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
# <a name="playlists-and-the-playlistcollection-object"></a><span data-ttu-id="4a9e3-114">Listas de reprodução e o objeto Playlistcollection</span><span class="sxs-lookup"><span data-stu-id="4a9e3-114">Playlists and the PlaylistCollection Object</span></span>

<span data-ttu-id="4a9e3-115">O objeto **playlistcollection** fornece acesso a listas de reprodução na biblioteca e tem métodos para criar listas de reprodução novas e vazias e novas listas de reprodução de metaarquivos.</span><span class="sxs-lookup"><span data-stu-id="4a9e3-115">The **PlaylistCollection** object gives you access to playlists in the library and has methods for creating new, empty playlists and new playlists from metafiles.</span></span>

## <a name="working-with-existing-playlists"></a><span data-ttu-id="4a9e3-116">Trabalhando com listas de reprodução existentes</span><span class="sxs-lookup"><span data-stu-id="4a9e3-116">Working with Existing Playlists</span></span>

<span data-ttu-id="4a9e3-117">A *playlistcollection*. **getAll** e *playlistcollection*. os métodos **getByName** retornam um objeto **PlaylistArray** , que pode conter várias listas de reprodução.</span><span class="sxs-lookup"><span data-stu-id="4a9e3-117">The *PlaylistCollection*.**getAll** and *PlaylistCollection*.**getByName** methods each return a **PlaylistArray** object, which can contain multiple playlists.</span></span>

<span data-ttu-id="4a9e3-118">A *playlistcollection*. o método **getAll** retorna todas as listas de reprodução existentes que estão na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="4a9e3-118">The *PlaylistCollection*.**getAll** method returns all of the existing playlists that are in the library.</span></span> <span data-ttu-id="4a9e3-119">Por exemplo, você pode chamar esse método e, em seguida, recuperar as listas de reprodução no objeto **PlaylistArray** para determinar se um determinado nome de playlist já foi usado ou para exibir todas as listas de reprodução para o usuário.</span><span class="sxs-lookup"><span data-stu-id="4a9e3-119">For example, you can call this method and then retrieve the playlists in the **PlaylistArray** object to determine whether a given playlist name has already been used, or to display all of the playlists to the user.</span></span> <span data-ttu-id="4a9e3-120">O código de exemplo em [atributos de playlist](playlist-attributes.md) usa o método **getAll** .</span><span class="sxs-lookup"><span data-stu-id="4a9e3-120">The sample code in [Playlist Attributes](playlist-attributes.md) uses the **getAll** method.</span></span>

<span data-ttu-id="4a9e3-121">A *playlistcollection*. o método **getByName** retorna todas as listas de reprodução com um nome específico.</span><span class="sxs-lookup"><span data-stu-id="4a9e3-121">The *PlaylistCollection*.**getByName** method returns all of the playlists with a given name.</span></span> <span data-ttu-id="4a9e3-122">Você pode usar esse método para lidar com cada uma dessas listas de reprodução separadamente.</span><span class="sxs-lookup"><span data-stu-id="4a9e3-122">You can use this method to handle each of those playlists separately.</span></span>

<span data-ttu-id="4a9e3-123">Você também pode usar o método **getByName** para recuperar uma lista de reprodução exclusiva por nome.</span><span class="sxs-lookup"><span data-stu-id="4a9e3-123">You can also use the **getByName** method to retrieve a unique playlist by name.</span></span> <span data-ttu-id="4a9e3-124">Nesse caso, o objeto **PlaylistArray** tem apenas um elemento.</span><span class="sxs-lookup"><span data-stu-id="4a9e3-124">In that case, the **PlaylistArray** object has only one element.</span></span> <span data-ttu-id="4a9e3-125">O exemplo de C# a seguir demonstra essa técnica.</span><span class="sxs-lookup"><span data-stu-id="4a9e3-125">The following C# example demonstrates this technique.</span></span>


```C++
IWMPPlaylistArray PlayListArray;
IWMPPlaylist Playlist;
// Store the playlist named "BluesTest" in the array
PlayListArray = Player.playlistCollection.getByName("BluesTest");
// Retrieve the first playlist in the collection.
Playlist = PlaylistArray.Item(0);

```



## <a name="working-with-new-playlists"></a><span data-ttu-id="4a9e3-126">Trabalhando com novas listas de reprodução</span><span class="sxs-lookup"><span data-stu-id="4a9e3-126">Working with New Playlists</span></span>

<span data-ttu-id="4a9e3-127">Você pode usar a *playlistcollection*. método **newPlaylist** para criar uma lista de reprodução nova e vazia.</span><span class="sxs-lookup"><span data-stu-id="4a9e3-127">You can use the *PlaylistCollection*.**newPlaylist** method to create a new, empty playlist.</span></span> <span data-ttu-id="4a9e3-128">O método retorna uma referência ao novo objeto de **lista de reprodução** .</span><span class="sxs-lookup"><span data-stu-id="4a9e3-128">The method returns a reference to the new **Playlist** object.</span></span> <span data-ttu-id="4a9e3-129">Em seguida, você pode chamar a *lista de reprodução*. método **appendItem** para adicionar itens de mídia à lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="4a9e3-129">You can then call the *Playlist*.**appendItem** method to add media items to the playlist.</span></span>

<span data-ttu-id="4a9e3-130">Você também pode criar uma nova lista de reprodução com base em um metarquivo de playlist.</span><span class="sxs-lookup"><span data-stu-id="4a9e3-130">You can also create a new playlist based on a playlist metafile.</span></span> <span data-ttu-id="4a9e3-131">Primeiro, passe o nome da lista de reprodução e o caminho para o metarquivo para o *Player*. método **newPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="4a9e3-131">First, pass the name of the playlist and the path to the metafile to the *Player*.**newPlaylist** method.</span></span> <span data-ttu-id="4a9e3-132">Esse método retorna uma referência ao novo objeto de **lista de reprodução** .</span><span class="sxs-lookup"><span data-stu-id="4a9e3-132">That method returns a reference to the new **Playlist** object.</span></span> <span data-ttu-id="4a9e3-133">Em seguida, passe o novo objeto **playlist** para a *playlistcollection*. método **importPlaylist** para adicioná-lo à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="4a9e3-133">Then, pass the new **Playlist** object to the *PlaylistCollection*.**importPlaylist** method to add it to the library.</span></span>

<span data-ttu-id="4a9e3-134">Observe a diferença entre *playlistcollection*. método **newPlaylist** e o *Player*. método **newPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="4a9e3-134">Notice the difference between the *PlaylistCollection*.**newPlaylist** method and the *Player*.**newPlaylist** method.</span></span> <span data-ttu-id="4a9e3-135">O método **playlistcollection** cria uma nova lista de reprodução vazia e a adiciona à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="4a9e3-135">The **PlaylistCollection** method creates a new, empty playlist and adds it to the library.</span></span> <span data-ttu-id="4a9e3-136">O método **Player** cria um novo objeto de **lista de reprodução** populado, mas não o adiciona à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="4a9e3-136">The **Player** method creates a new, populated **Playlist** object but does not add it to the library.</span></span>

<span data-ttu-id="4a9e3-137">Ao longo deste tópico, o objeto **Player** foi definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="4a9e3-137">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="4a9e3-138">O exemplo de C# a seguir demonstra a importação de uma lista de reprodução de um metarquivo.</span><span class="sxs-lookup"><span data-stu-id="4a9e3-138">The following C# example demonstrates importing a playlist from a metafile.</span></span> <span data-ttu-id="4a9e3-139">O argumento *strPListName* especifica o nome da nova lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="4a9e3-139">The *strPListName* argument specifies the name of the new playlist.</span></span> <span data-ttu-id="4a9e3-140">O *strMetaFileName* especifica o nome do metarquivo do qual a lista de reprodução é importada.</span><span class="sxs-lookup"><span data-stu-id="4a9e3-140">The *strMetaFileName* specifies the name of the metafile from which the playlist is imported.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="4a9e3-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a9e3-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a9e3-142">**Gerenciando listas de reprodução**</span><span class="sxs-lookup"><span data-stu-id="4a9e3-142">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="4a9e3-143">**Player. newPlaylist**</span><span class="sxs-lookup"><span data-stu-id="4a9e3-143">**Player.newPlaylist**</span></span>](player-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="4a9e3-144">**Playlist. appendItem**</span><span class="sxs-lookup"><span data-stu-id="4a9e3-144">**Playlist.appendItem**</span></span>](playlist-appenditem.md)
</dt> <dt>

[<span data-ttu-id="4a9e3-145">**Objeto PlaylistArray**</span><span class="sxs-lookup"><span data-stu-id="4a9e3-145">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="4a9e3-146">**Objeto playlistcollection**</span><span class="sxs-lookup"><span data-stu-id="4a9e3-146">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="4a9e3-147">**Listas de reprodução e itens de mídia**</span><span class="sxs-lookup"><span data-stu-id="4a9e3-147">**Playlists and Media Items**</span></span>](playlists-and-media-items.md)
</dt> </dl>

 

 




