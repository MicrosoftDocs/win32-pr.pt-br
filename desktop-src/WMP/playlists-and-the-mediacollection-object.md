---
title: Listas de reprodução e o objeto Mediacollection
description: Listas de reprodução e o objeto Mediacollection
ms.assetid: 3c98ceed-2545-4774-998b-c1db0d172a81
keywords:
- Windows Media Player, listas de reprodução
- Modelo de objeto do Windows Media Player, listas de reprodução
- modelo de objeto, listas de reprodução
- Windows Media Player Mobile, listas de reprodução
- Controle ActiveX do Windows Media Player, listas de reprodução
- Controle ActiveX móvel do Windows Media Player, listas de reprodução
- Controle ActiveX, listas de reprodução
- listas de reprodução, objeto Mediacollection
- listas de reprodução de metarquivo, objeto Mediacollection
- Playlists do metarquivo do Windows Media, objeto Mediacollection
- Objeto mediacollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334b693046e6c78e92a4af901816b57bb9c4cddc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363839"
---
# <a name="playlists-and-the-mediacollection-object"></a><span data-ttu-id="7134a-114">Listas de reprodução e o objeto Mediacollection</span><span class="sxs-lookup"><span data-stu-id="7134a-114">Playlists and the MediaCollection Object</span></span>

<span data-ttu-id="7134a-115">O objeto **mediacollection** fornece acesso a uma variedade de listas de reprodução especiais e inclui um método para criar uma nova lista de reprodução a partir de um metarquivo.</span><span class="sxs-lookup"><span data-stu-id="7134a-115">The **MediaCollection** object gives you access to a variety of special playlists, and includes a method for creating a new playlist from a metafile.</span></span>

<span data-ttu-id="7134a-116">Os métodos a seguir recuperam listas de reprodução especiais:</span><span class="sxs-lookup"><span data-stu-id="7134a-116">The following methods retrieve special playlists:</span></span>

-   <span data-ttu-id="7134a-117">**getAll**</span><span class="sxs-lookup"><span data-stu-id="7134a-117">**getAll**</span></span>
-   <span data-ttu-id="7134a-118">**getByAlbum**</span><span class="sxs-lookup"><span data-stu-id="7134a-118">**getByAlbum**</span></span>
-   <span data-ttu-id="7134a-119">**getByAttribute**</span><span class="sxs-lookup"><span data-stu-id="7134a-119">**getByAttribute**</span></span>
-   <span data-ttu-id="7134a-120">**getByAuthor**</span><span class="sxs-lookup"><span data-stu-id="7134a-120">**getByAuthor**</span></span>
-   <span data-ttu-id="7134a-121">**getByGenre**</span><span class="sxs-lookup"><span data-stu-id="7134a-121">**getByGenre**</span></span>
-   <span data-ttu-id="7134a-122">**getByName**</span><span class="sxs-lookup"><span data-stu-id="7134a-122">**getByName**</span></span>

<span data-ttu-id="7134a-123">Como os nomes sugerem, esses métodos recuperam as listas de reprodução que contêm todos os itens de mídia na biblioteca que correspondem a determinados critérios.</span><span class="sxs-lookup"><span data-stu-id="7134a-123">As their names suggest, these methods retrieve playlists containing all of the media items in the library that match certain criteria.</span></span>

<span data-ttu-id="7134a-124">Tenha cuidado para não confundir o *mediacollection*. método **getByName** com a *playlistcollection*. método **getByName** .</span><span class="sxs-lookup"><span data-stu-id="7134a-124">Be careful not to confuse the *MediaCollection*.**getByName** method with the *PlaylistCollection*.**getByName** method.</span></span> <span data-ttu-id="7134a-125">O método **mediacollection** retorna um objeto **playlist** contendo todos os itens de mídia que têm o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="7134a-125">The **MediaCollection** method returns a **Playlist** object containing all of the media items that have the specified name.</span></span> <span data-ttu-id="7134a-126">O método **playlistcollection** retorna um objeto **PlaylistArray** contendo todas as listas de reprodução que têm o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="7134a-126">The **PlaylistCollection** method returns a **PlaylistArray** object containing all of the playlists that have the specified name.</span></span>

<span data-ttu-id="7134a-127">Você pode usar o *mediacollection*. **adicione** o método para adicionar listas de reprodução, bem como itens de mídia à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="7134a-127">You can use the *MediaCollection*.**add** method to add playlists as well as media items to the library.</span></span> <span data-ttu-id="7134a-128">Para adicionar uma lista de reprodução, passe o método do caminho para o metarquivo que define a lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="7134a-128">To add a playlist, you pass the method the path to the metafile that defines the playlist.</span></span> <span data-ttu-id="7134a-129">O método sempre retorna um objeto de **mídia** .</span><span class="sxs-lookup"><span data-stu-id="7134a-129">The method always returns a **Media** object.</span></span> <span data-ttu-id="7134a-130">Não é possível converter entre os objetos de **mídia** e **playlist** .</span><span class="sxs-lookup"><span data-stu-id="7134a-130">You cannot cast between **Media** and **Playlist** objects.</span></span> <span data-ttu-id="7134a-131">Para trabalhar com a lista de reprodução que você adicionou, recupere o objeto de **playlist** que tem o mesmo nome que o objeto de **mídia** .</span><span class="sxs-lookup"><span data-stu-id="7134a-131">To work with the playlist that you added, retrieve the **Playlist** object that has the same name as the **Media** object.</span></span>

<span data-ttu-id="7134a-132">O exemplo de C# a seguir demonstra como recuperar mídia por tipo usando o **mediacollection**. método **getByAttribute** .</span><span class="sxs-lookup"><span data-stu-id="7134a-132">The following C# example demonstrates how to retrieve media by type using the **MediaCollection**.**getByAttribute** method.</span></span> <span data-ttu-id="7134a-133">Esse código recupera os nomes de todos os atributos associados a um determinado tipo, bem como o status de leitura/gravação ou somente leitura desses atributos.</span><span class="sxs-lookup"><span data-stu-id="7134a-133">This code retrieves the names of all attributes associated with a given type as well as the read/write or read-only status of those attributes.</span></span> <span data-ttu-id="7134a-134">Ele gera um único arquivo que contém listas de atributos para o áudio, vídeo, rádio, lista de reprodução, outros tipos de foto, música e tipo.</span><span class="sxs-lookup"><span data-stu-id="7134a-134">It generates a single file that contains lists of attributes for the Audio, Video, Radio, Playlist, Other, Music, and Photo types.</span></span>


```C++
string strOutFile = "AttribList.txt";    // Name of the output file
...
StreamWriter sw = new StreamWriter(strOutFile, true);

sw.Write(getMediaCollectionNames("Audio"));
sw.Write(getMediaCollectionNames("Video"));
sw.Write(getMediaCollectionNames("Radio"));
sw.Write(getMediaCollectionNames("Playlist"));
sw.Write(getMediaCollectionNames("Other"));
sw.Write(getMediaCollectionNames("Music"));
sw.Write(getMediaCollectionNames("Photo"));
sw.Close();
...
// The getMediaCollection method retrieves the names of
// all attributes for a specified type.
private string getMediaCollectionNames(string sSchema)
{
IWMPPlaylist playlist;
IWMPMedia media;
string strResult = "";    // Cumulative list of attributes
string strAttrName = "";  // Attribute name
string strReadWrite = ""; // Read/Write status of attribute
int iAttrCount = 0;       // Count of playlist attributes

// Retrieve a playlist corresponding to the requested type.
playlist = Player.mediaCollection.getByAttribute("MediaType", sSchema);

// Initialize the result string
strResult += "\n" + sSchema.ToString() + " Schema: \n";

// Retrieve the attributes for the playlist
if (playlist.count != 0)
{
    media = playlist.get_Item(0);
    iAttrCount = media.attributeCount;
    for (int i = 0; i < iAttrCount; i++)
    {
        strAttrName = media.getAttributeName(i);
        strResult += "   " + strAttrName  +"\n";
        if (media.isReadOnlyItem(strAttrName))
            strReadWrite = "Read Only";
        else
            strReadWrite = "Read/Write";
        strResult += "         " + strReadWrite + "\n";
    }
}

return strResult;
}

```



<span data-ttu-id="7134a-135">O exemplo de C# a seguir demonstra como adicionar uma lista de reprodução de um metarquivo à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="7134a-135">The following C# example demonstrates how to add a playlist from a metafile to the library.</span></span>


```C++
// Add a playlist as a media item
IWMPMedia Media = Player.mediaCollection.add("c:\\testPlayList.asx");

```



<span data-ttu-id="7134a-136">As listas de reprodução estáticas incluem itens de mídia específicos.</span><span class="sxs-lookup"><span data-stu-id="7134a-136">Static playlists include specific media items.</span></span> <span data-ttu-id="7134a-137">As listas de reprodução automática pesquisam a biblioteca toda vez que são abertas e podem conter itens de mídia diferentes em momentos diferentes.</span><span class="sxs-lookup"><span data-stu-id="7134a-137">Auto playlists search the library every time they are opened and may contain different media items at different times.</span></span> <span data-ttu-id="7134a-138">Você pode adicionar listas de reprodução estáticas e automáticas à biblioteca usando o *mediacollection*. **Adicionar** método.</span><span class="sxs-lookup"><span data-stu-id="7134a-138">You can add both static and auto playlists to the library by using the *MediaCollection*.**add** method.</span></span> <span data-ttu-id="7134a-139">Você também pode adicionar listas de reprodução estáticas usando a *playlistcollection*. método **importPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="7134a-139">You can also add static playlists by using the *PlaylistCollection*.**importPlaylist** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7134a-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7134a-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7134a-141">**Gerenciando listas de reprodução**</span><span class="sxs-lookup"><span data-stu-id="7134a-141">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="7134a-142">**Objeto mediacollection**</span><span class="sxs-lookup"><span data-stu-id="7134a-142">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="7134a-143">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="7134a-143">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="7134a-144">**Objeto playlistcollection**</span><span class="sxs-lookup"><span data-stu-id="7134a-144">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="7134a-145">**Listas de reprodução e o objeto Playlistcollection**</span><span class="sxs-lookup"><span data-stu-id="7134a-145">**Playlists and the PlaylistCollection Object**</span></span>](playlists-and-the-playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="7134a-146">**Listas de reprodução estáticas e automáticas**</span><span class="sxs-lookup"><span data-stu-id="7134a-146">**Static and Auto Playlists**</span></span>](static-and-auto-playlists.md)
</dt> </dl>

 

 




