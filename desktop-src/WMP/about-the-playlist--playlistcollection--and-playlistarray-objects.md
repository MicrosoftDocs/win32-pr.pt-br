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
# <a name="about-the-playlist-playlistcollection-and-playlistarray-objects"></a><span data-ttu-id="4c377-127">Sobre os objetos playlist, Playlistcollection e PlaylistArray</span><span class="sxs-lookup"><span data-stu-id="4c377-127">About the Playlist, PlaylistCollection, and PlaylistArray Objects</span></span>

<span data-ttu-id="4c377-128">Os objetos **playlist**, **playlistcollection** e **PlaylistArray** regem as listas de reprodução que o Windows Media Player pode usar para especificar a ordem na qual o conteúdo será reproduzido.</span><span class="sxs-lookup"><span data-stu-id="4c377-128">The **Playlist**, **PlaylistCollection**, and **PlaylistArray** objects govern the playlists that Windows Media Player can use to specify the order in which content will be played.</span></span> <span data-ttu-id="4c377-129">Você Obtém o objeto **playlistcollection** da propriedade **playlistcollection** do objeto **Player** .</span><span class="sxs-lookup"><span data-stu-id="4c377-129">You get the **PlaylistCollection** object from the **playlistCollection** property of the **Player** object.</span></span> <span data-ttu-id="4c377-130">A propriedade **playlistcollection** retorna o objeto **playlistcollection** .</span><span class="sxs-lookup"><span data-stu-id="4c377-130">The **playlistCollection** property returns the **PlaylistCollection** object.</span></span> <span data-ttu-id="4c377-131">Você só pode acessar as propriedades do objeto **playlistcollection** depois de criá-lo.</span><span class="sxs-lookup"><span data-stu-id="4c377-131">You can only access the properties of the **PlaylistCollection** object after you have created it.</span></span> <span data-ttu-id="4c377-132">Por exemplo, para criar uma nova lista de reprodução, primeiro você deve obter o objeto **playlistcollection** e, em seguida, usar um método nesse objeto.</span><span class="sxs-lookup"><span data-stu-id="4c377-132">For example, to create a new playlist, you must first get the **PlaylistCollection** object and then use a method on that object.</span></span>


```C++
player.playlistcollection.newplaylist('myplaylist');
```



<span data-ttu-id="4c377-133">Você pode obter a lista de reprodução atual usando a propriedade **currentPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="4c377-133">You can get the current playlist by using the **currentPlaylist** property.</span></span> <span data-ttu-id="4c377-134">Por exemplo, para obter o nome da playlist atual, use o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="4c377-134">For example, to get the name of the current playlist, use the following code:</span></span>


```C++
myname = player.currentplaylist.name;
```



<span data-ttu-id="4c377-135">O objeto **PlaylistArray** é retornado pelos métodos **getAll** e **getByName** do objeto **playlistcollection** .</span><span class="sxs-lookup"><span data-stu-id="4c377-135">The **PlaylistArray** object is returned by the **getAll** and **getByName** methods of the **PlaylistCollection** object.</span></span> <span data-ttu-id="4c377-136">Para obter o número de listas de reprodução, por exemplo, use o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="4c377-136">To get the number of playlists, for example, use the following code:</span></span>


```C++
howmany = player.playlistcollection.getAll().count;
```



<span data-ttu-id="4c377-137">Para recuperar uma lista de reprodução conhecida por nome, use o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="4c377-137">To retrieve a known playlist by name, use the following code:</span></span>


```C++
if (player.playlistcollection.getbyname('myplaylist').count == 1) {
    pl = player.playlistcollection.getbyname('myplaylist').item(0);
}
```



## <a name="related-topics"></a><span data-ttu-id="4c377-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4c377-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c377-139">**Modelo de objeto do Player para linguagens de script**</span><span class="sxs-lookup"><span data-stu-id="4c377-139">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="4c377-140">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="4c377-140">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="4c377-141">**Objeto PlaylistArray**</span><span class="sxs-lookup"><span data-stu-id="4c377-141">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="4c377-142">**Objeto playlistcollection**</span><span class="sxs-lookup"><span data-stu-id="4c377-142">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> </dl>

 

 




