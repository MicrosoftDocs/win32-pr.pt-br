---
title: Acessando a biblioteca programaticamente
description: Acessando a biblioteca programaticamente
ms.assetid: f48fbb49-5b79-4a78-af72-8509c460a149
keywords:
- Windows Media Player, biblioteca
- Modelo de objeto do Windows Media Player, biblioteca
- modelo de objeto, biblioteca
- Controle ActiveX do Windows Media Player, biblioteca para modelo de objeto
- Controle ActiveX, biblioteca para modelo de objeto
- Controle ActiveX móvel do Windows Media Player, biblioteca para modelo de objeto
- Windows Media Player Mobile, biblioteca para modelo de objeto
- Biblioteca do Windows Media Player, acessando programaticamente
- biblioteca, acessando
- Acessando a biblioteca do Windows Media Player de forma programática
- Biblioteca do Windows Media Player, adicionando itens de mídia
- biblioteca, adicionando itens de mídia
- Biblioteca do Windows Media Player, recuperando itens de mídia
- biblioteca, recuperando itens de mídia
- Biblioteca do Windows Media Player, removendo itens de mídia
- biblioteca, removendo itens de mídia
- Adicionando itens de mídia à biblioteca do Windows Media Player
- Recuperando itens de mídia da biblioteca do Windows Media Player
- removendo itens de mídia da biblioteca do Windows Media Player
- recuperando metadados
- Biblioteca do Windows Media Player, Recuperando metadados de itens de mídia
- biblioteca, Recuperando metadados de itens de mídia
- metadados, recuperando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d40e03e91b2a67a24cb49b0ac1810ceb7b9544c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364204"
---
# <a name="accessing-the-library-programmatically"></a><span data-ttu-id="4b43d-126">Acessando a biblioteca programaticamente</span><span class="sxs-lookup"><span data-stu-id="4b43d-126">Accessing the Library Programmatically</span></span>

<span data-ttu-id="4b43d-127">No código, a biblioteca é representada pelo objeto **mediacollection** (ou pela interface **IWMPMediaCollection** ).</span><span class="sxs-lookup"><span data-stu-id="4b43d-127">In code, the library is represented by the **MediaCollection** object (or the **IWMPMediaCollection** interface).</span></span> <span data-ttu-id="4b43d-128">Os itens de mídia são representados como objetos de **mídia** (ou pela interface **IWMPMedia** ).</span><span class="sxs-lookup"><span data-stu-id="4b43d-128">Media items are represented as **Media** objects (or by the **IWMPMedia** interface).</span></span> <span data-ttu-id="4b43d-129">Os itens da lista de reprodução são representados como objetos de **playlist** (ou pela interface **IWMPPlaylist** ).</span><span class="sxs-lookup"><span data-stu-id="4b43d-129">Playlist items are represented as **Playlist** objects (or by the **IWMPPlaylist** interface).</span></span> <span data-ttu-id="4b43d-130">Para simplificar, esta seção se referirá apenas a nomes de objetos, quando possível.</span><span class="sxs-lookup"><span data-stu-id="4b43d-130">For simplicity, this section will simply refer to object names, when possible.</span></span>

<span data-ttu-id="4b43d-131">Usando o objeto **mediacollection** , você pode trabalhar com itens de mídia e listas de reprodução.</span><span class="sxs-lookup"><span data-stu-id="4b43d-131">By using the **MediaCollection** object, you can work with media items and playlists.</span></span> <span data-ttu-id="4b43d-132">A biblioteca também expõe o objeto **playlistcollection** (ou a interface **IWMPPlaylistCollection** ), que fornece algumas funcionalidades específicas para trabalhar com listas de reprodução.</span><span class="sxs-lookup"><span data-stu-id="4b43d-132">The library also exposes the **PlaylistCollection** object (or the **IWMPPlaylistCollection** interface), which provides some functionality specific to working with playlists.</span></span> <span data-ttu-id="4b43d-133">Na maioria das vezes, o objeto **mediacollection** fornecerá a você a funcionalidade de que você precisa, mesmo ao trabalhar com listas de reprodução.</span><span class="sxs-lookup"><span data-stu-id="4b43d-133">Most of the time, the **MediaCollection** object will provide you with the functionality you need, even when working with playlists.</span></span> <span data-ttu-id="4b43d-134">Para obter mais informações sobre como trabalhar com itens de mídia, consulte [Gerenciando itens de mídia](managing-media-items.md).</span><span class="sxs-lookup"><span data-stu-id="4b43d-134">For more information about working with media items, see [Managing Media Items](managing-media-items.md).</span></span> <span data-ttu-id="4b43d-135">Para obter mais informações sobre como trabalhar com listas de reprodução, consulte [Gerenciando listas de reprodução](managing-playlists.md).</span><span class="sxs-lookup"><span data-stu-id="4b43d-135">For more information about working with playlists, see [Managing Playlists](managing-playlists.md).</span></span>

## <a name="adding-media-items-to-the-library"></a><span data-ttu-id="4b43d-136">Adicionando itens de mídia à biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b43d-136">Adding Media Items to the Library</span></span>

<span data-ttu-id="4b43d-137">Adicionar conteúdo de mídia digital à biblioteca é simples.</span><span class="sxs-lookup"><span data-stu-id="4b43d-137">Adding digital media content to the library is straightforward.</span></span> <span data-ttu-id="4b43d-138">Basta chamar o método [mediacollection. Add](mediacollection-add.md) , fornecendo o caminho para o arquivo de mídia como um argumento.</span><span class="sxs-lookup"><span data-stu-id="4b43d-138">Simply call the [MediaCollection.add](mediacollection-add.md) method, providing the path to the media file as an argument.</span></span>

## <a name="retrieving-media-items-from-the-library"></a><span data-ttu-id="4b43d-139">Recuperando itens de mídia da biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b43d-139">Retrieving Media Items from the Library</span></span>

<span data-ttu-id="4b43d-140">Quando você recupera itens de mídia da biblioteca, o que você realmente recupera é uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="4b43d-140">When you retrieve media items from the library, what you really retrieve is a playlist.</span></span> <span data-ttu-id="4b43d-141">Mesmo que você espere recuperar apenas um item de mídia, obterá um objeto de **playlist** contendo um único item, que será associado ao índice zero.</span><span class="sxs-lookup"><span data-stu-id="4b43d-141">Even if you expect to retrieve only one media item, you will get a **Playlist** object containing a single item, which will be associated with index zero.</span></span> <span data-ttu-id="4b43d-142">Por exemplo, se você quiser recuperar um objeto de **mídia** que representa a música denominada "Jeanne", poderá usar o seguinte código JScript:</span><span class="sxs-lookup"><span data-stu-id="4b43d-142">For example, if you want to retrieve a **Media** object that represents the song named "Jeanne", you could use the following JScript code:</span></span>


```C++
// Retrieve media named Jeanne from the library.
var playlist = player.mediaCollection.getByName("Jeanne");

```



<span data-ttu-id="4b43d-143">O código anterior recupera uma lista de reprodução que contém todos os itens de mídia com o nome "Jeanne" como o título.</span><span class="sxs-lookup"><span data-stu-id="4b43d-143">The preceding code retrieves a playlist containing all the media items having the name "Jeanne" as the title.</span></span> <span data-ttu-id="4b43d-144">Para este exemplo, suponha que você saiba que há apenas uma música com esse nome na biblioteca (Observe que a biblioteca dá suporte a várias músicas com o mesmo nome).</span><span class="sxs-lookup"><span data-stu-id="4b43d-144">For this example, assume that you know there is only one song by that name in the library (note that the library supports multiple songs having the same name).</span></span> <span data-ttu-id="4b43d-145">Isso significa que você pode esperar que a contagem de itens na playlist que você recuperou para igual um e o item de mídia fossem representados pelo índice zero.</span><span class="sxs-lookup"><span data-stu-id="4b43d-145">This means you could expect the count of items in the playlist you retrieved to equal one and the media item would be represented by index zero.</span></span> <span data-ttu-id="4b43d-146">O código de exemplo a seguir continua o exemplo anterior para demonstrar como você recuperaria o item de mídia da lista de reprodução usando o método [playlist. Item](playlist-item.md) .</span><span class="sxs-lookup"><span data-stu-id="4b43d-146">The following example code continues the previous example to demonstrate how you would retrieve the media item from the playlist by using the [Playlist.item](playlist-item.md) method.</span></span>


```C++
// Retrieve the individual media item from the playlist.
var media = playlist.item(0);

```



<span data-ttu-id="4b43d-147">Para obter mais informações sobre como recuperar itens de mídia de listas de reprodução, consulte [listas de reprodução e itens de mídia](playlists-and-media-items.md) no [Guia de controle do Player](player-control-guide.md).</span><span class="sxs-lookup"><span data-stu-id="4b43d-147">For more information about retrieving media items from playlists, see [Playlists and Media Items](playlists-and-media-items.md) in the [Player Control Guide](player-control-guide.md).</span></span>

## <a name="retrieving-metadata-from-a-media-item"></a><span data-ttu-id="4b43d-148">Recuperando metadados de um item de mídia</span><span class="sxs-lookup"><span data-stu-id="4b43d-148">Retrieving Metadata from a Media Item</span></span>

<span data-ttu-id="4b43d-149">Depois de recuperar um objeto de **mídia** , você pode ler os valores de atributo associados ao conteúdo.</span><span class="sxs-lookup"><span data-stu-id="4b43d-149">After you retrieve a **Media** object, you can read the attribute values associated with the content.</span></span> <span data-ttu-id="4b43d-150">No caso mais simples, você pode simplesmente querer saber um único valor, como o nome do artista que realizou uma faixa de música. O exemplo de JScript a seguir mostra como usar o método [Media. getItemInfo](media-getiteminfo.md) para recuperar o nome do artista da mídia recuperada no exemplo anterior:</span><span class="sxs-lookup"><span data-stu-id="4b43d-150">In the simplest case, you might simply want to know a single value, such as the name of the artist who performed a music track. The following JScript example shows how to use the [Media.getItemInfo](media-getiteminfo.md) method to retrieve the name of the artist from the media retrieved in the previous example:</span></span>


```C++
// Retrieve the artist name string.
var author = media.getItemInfo("Artist");

```



<span data-ttu-id="4b43d-151">Um item de mídia pode ter muitos atributos diferentes, e trabalhar com metadados nem sempre é tão simples quanto o caso simples mostrado no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="4b43d-151">A media item can have many different attributes, and working with metadata is not always as straightforward as the simple case shown in the previous example.</span></span> <span data-ttu-id="4b43d-152">Por exemplo, alguns atributos podem conter vários valores ou ter valores em mais de um idioma.</span><span class="sxs-lookup"><span data-stu-id="4b43d-152">For instance, some attributes can contain multiple values or have values in more than one language.</span></span> <span data-ttu-id="4b43d-153">Para obter mais informações sobre como trabalhar com metadados, consulte [atributos de item de mídia](media-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="4b43d-153">For more information about working with metadata, see [Media Item Attributes](media-item-attributes.md).</span></span> <span data-ttu-id="4b43d-154">Para obter mais informações sobre os vários atributos, seus significados e o suporte de tipo de arquivo, consulte a [referência de atributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="4b43d-154">For more information about the various attributes, their meanings, and file type support, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="removing-media-items-from-the-library"></a><span data-ttu-id="4b43d-155">Removendo itens de mídia da biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b43d-155">Removing Media Items from the Library</span></span>

<span data-ttu-id="4b43d-156">A remoção do conteúdo de mídia digital da biblioteca também é simples.</span><span class="sxs-lookup"><span data-stu-id="4b43d-156">Removing digital media content from the library is also straightforward.</span></span> <span data-ttu-id="4b43d-157">Basta chamar **mediacollection. Remove**, fornecendo o objeto de **mídia** que representa o item como o primeiro argumento e o valor **true** como o segundo.</span><span class="sxs-lookup"><span data-stu-id="4b43d-157">Simply call **MediaCollection.remove**, providing the **Media** object that represents the item as the first argument and the value **true** as the second.</span></span> <span data-ttu-id="4b43d-158">O exemplo de JScript a seguir remove o arquivo chamado Jeanne (recuperado no exemplo anterior) da biblioteca:</span><span class="sxs-lookup"><span data-stu-id="4b43d-158">The following JScript example removes the file named Jeanne (retrieved in the previous example) from the library:</span></span>


```C++
// Remove Jeanne from the library.
playst.mediaCollection.remove(media, true);

```



## <a name="related-topics"></a><span data-ttu-id="4b43d-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4b43d-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b43d-160">**Sobre a biblioteca**</span><span class="sxs-lookup"><span data-stu-id="4b43d-160">**About the Library**</span></span>](about-the-library.md)
</dt> <dt>

[<span data-ttu-id="4b43d-161">**Sobre o Mediacollection e os objetos de mídia**</span><span class="sxs-lookup"><span data-stu-id="4b43d-161">**About the MediaCollection and Media Objects**</span></span>](about-the-mediacollection-and-media-objects.md)
</dt> <dt>

[<span data-ttu-id="4b43d-162">**Sobre os objetos playlist, Playlistcollection e PlaylistArray**</span><span class="sxs-lookup"><span data-stu-id="4b43d-162">**About the Playlist, PlaylistCollection, and PlaylistArray Objects**</span></span>](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
</dt> <dt>

[<span data-ttu-id="4b43d-163">**Trabalhando com a biblioteca**</span><span class="sxs-lookup"><span data-stu-id="4b43d-163">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




