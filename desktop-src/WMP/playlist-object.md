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
# <a name="playlist-object"></a><span data-ttu-id="1ed52-104">Objeto playlist</span><span class="sxs-lookup"><span data-stu-id="1ed52-104">Playlist Object</span></span>

<span data-ttu-id="1ed52-105">O objeto **playlist** fornece uma maneira de organizar itens de mídia em uma lista para facilitar a manipulação usando as propriedades e os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="1ed52-105">The **Playlist** object provides a way to organize media items in a list for easy manipulation by using the following properties and methods.</span></span>

<span data-ttu-id="1ed52-106">O objeto **playlist** oferece suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="1ed52-106">The **Playlist** object supports the following properties.</span></span>



| <span data-ttu-id="1ed52-107">Propriedade</span><span class="sxs-lookup"><span data-stu-id="1ed52-107">Property</span></span>                                      | <span data-ttu-id="1ed52-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ed52-108">Description</span></span>                                                      |
|-----------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="1ed52-109">attributeCount</span><span class="sxs-lookup"><span data-stu-id="1ed52-109">attributeCount</span></span>](playlist-attributecount.md) | <span data-ttu-id="1ed52-110">Recupera o número de atributos associados à playlist.</span><span class="sxs-lookup"><span data-stu-id="1ed52-110">Retrieves the number of attributes associated with the playlist.</span></span> |
| [<span data-ttu-id="1ed52-111">attributeName</span><span class="sxs-lookup"><span data-stu-id="1ed52-111">attributeName</span></span>](playlist-attributename.md)   | <span data-ttu-id="1ed52-112">Recupera o nome de um atributo especificado por um índice.</span><span class="sxs-lookup"><span data-stu-id="1ed52-112">Retrieves the name of an attribute specified by an index.</span></span>        |
| [<span data-ttu-id="1ed52-113">contagem</span><span class="sxs-lookup"><span data-stu-id="1ed52-113">count</span></span>](playlist-count.md)                   | <span data-ttu-id="1ed52-114">Recupera o número de itens na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="1ed52-114">Retrieves the number of items in the playlist.</span></span>                   |
| [<span data-ttu-id="1ed52-115">name</span><span class="sxs-lookup"><span data-stu-id="1ed52-115">name</span></span>](playlist-name.md)                     | <span data-ttu-id="1ed52-116">Especifica ou recupera o nome da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="1ed52-116">Specifies or retrieves the name of the playlist.</span></span>                 |



 

<span data-ttu-id="1ed52-117">O objeto **playlist** dá suporte aos seguintes métodos.</span><span class="sxs-lookup"><span data-stu-id="1ed52-117">The **Playlist** object supports the following methods.</span></span>



| <span data-ttu-id="1ed52-118">Método</span><span class="sxs-lookup"><span data-stu-id="1ed52-118">Method</span></span>                                  | <span data-ttu-id="1ed52-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ed52-119">Description</span></span>                                                                                            |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ed52-120">appendItem</span><span class="sxs-lookup"><span data-stu-id="1ed52-120">appendItem</span></span>](playlist-appenditem.md)   | <span data-ttu-id="1ed52-121">Adiciona um item de mídia ao final da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="1ed52-121">Adds a media item to the end of the playlist.</span></span>                                                          |
| <span data-ttu-id="1ed52-122">**clear**</span><span class="sxs-lookup"><span data-stu-id="1ed52-122">**clear**</span></span>                               | <span data-ttu-id="1ed52-123">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="1ed52-123">Reserved for future use.</span></span>                                                                               |
| [<span data-ttu-id="1ed52-124">getItemInfo</span><span class="sxs-lookup"><span data-stu-id="1ed52-124">getItemInfo</span></span>](playlist-getiteminfo.md) | <span data-ttu-id="1ed52-125">Recupera o valor de um atributo de playlist.</span><span class="sxs-lookup"><span data-stu-id="1ed52-125">Retrieves the value of a playlist attribute.</span></span>                                                           |
| [<span data-ttu-id="1ed52-126">insertItem</span><span class="sxs-lookup"><span data-stu-id="1ed52-126">insertItem</span></span>](playlist-insertitem.md)   | <span data-ttu-id="1ed52-127">Insere um item de mídia na lista de reprodução no local especificado.</span><span class="sxs-lookup"><span data-stu-id="1ed52-127">Inserts a media item into the playlist at the specified location.</span></span>                                      |
| [<span data-ttu-id="1ed52-128">isidêntico</span><span class="sxs-lookup"><span data-stu-id="1ed52-128">isIdentical</span></span>](playlist-isidentical.md) | <span data-ttu-id="1ed52-129">Recupera um valor que indica se o objeto de **playlist** fornecido é idêntico ao atual.</span><span class="sxs-lookup"><span data-stu-id="1ed52-129">Retrieves a value indicating whether the supplied **Playlist** object is identical to the current one.</span></span> |
| [<span data-ttu-id="1ed52-130">item</span><span class="sxs-lookup"><span data-stu-id="1ed52-130">item</span></span>](playlist-item.md)               | <span data-ttu-id="1ed52-131">Recupera o item de mídia no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="1ed52-131">Retrieves the media item at the specified index.</span></span>                                                       |
| [<span data-ttu-id="1ed52-132">moveItem</span><span class="sxs-lookup"><span data-stu-id="1ed52-132">moveItem</span></span>](playlist-moveitem.md)       | <span data-ttu-id="1ed52-133">Altera o local de um item na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="1ed52-133">Changes the location of an item in the playlist.</span></span>                                                       |
| [<span data-ttu-id="1ed52-134">removeItem</span><span class="sxs-lookup"><span data-stu-id="1ed52-134">removeItem</span></span>](playlist-removeitem.md)   | <span data-ttu-id="1ed52-135">Remove o item especificado da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="1ed52-135">Removes the specified item from the playlist.</span></span>                                                          |
| [<span data-ttu-id="1ed52-136">setItemInfo</span><span class="sxs-lookup"><span data-stu-id="1ed52-136">setItemInfo</span></span>](playlist-setiteminfo.md) | <span data-ttu-id="1ed52-137">Especifica o valor de um atributo de playlist.</span><span class="sxs-lookup"><span data-stu-id="1ed52-137">Specifies the value of a playlist attribute.</span></span>                                                           |



 

<span data-ttu-id="1ed52-138">O objeto **playlist** é acessado por meio das propriedades e métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="1ed52-138">The **Playlist** object is accessed through the following properties and methods.</span></span>



| <span data-ttu-id="1ed52-139">Objeto</span><span class="sxs-lookup"><span data-stu-id="1ed52-139">Object</span></span>                                              | <span data-ttu-id="1ed52-140">Propriedade ou método</span><span class="sxs-lookup"><span data-stu-id="1ed52-140">Property or method</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ed52-141">ROMs</span><span class="sxs-lookup"><span data-stu-id="1ed52-141">Cdrom</span></span>](cdrom-object.md)                           | [<span data-ttu-id="1ed52-142">playlist</span><span class="sxs-lookup"><span data-stu-id="1ed52-142">playlist</span></span>](cdrom-playlist.md)                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="1ed52-143">Mediacollection</span><span class="sxs-lookup"><span data-stu-id="1ed52-143">MediaCollection</span></span>](mediacollection-object.md)       | <span data-ttu-id="1ed52-144">[getAll](mediacollection-getall.md), [getByAlbum](mediacollection-getbyalbum.md), [getByAttribute](mediacollection-getbyattribute.md), [getByAuthor](mediacollection-getbyauthor.md), [getByGenre](mediacollection-getbygenre.md), [getByName](mediacollection-getbyname.md)</span><span class="sxs-lookup"><span data-stu-id="1ed52-144">[getAll](mediacollection-getall.md), [getByAlbum](mediacollection-getbyalbum.md), [getByAttribute](mediacollection-getbyattribute.md), [getByAuthor](mediacollection-getbyauthor.md), [getByGenre](mediacollection-getbygenre.md), [getByName](mediacollection-getbyname.md)</span></span> |
| [<span data-ttu-id="1ed52-145">Jogador</span><span class="sxs-lookup"><span data-stu-id="1ed52-145">Player</span></span>](player-object.md)                         | <span data-ttu-id="1ed52-146">[currentPlaylist](player-currentplaylist.md), [newPlaylist](player-newplaylist.md)</span><span class="sxs-lookup"><span data-stu-id="1ed52-146">[currentPlaylist](player-currentplaylist.md), [newPlaylist](player-newplaylist.md)</span></span>                                                                                                                                                                                               |
| [<span data-ttu-id="1ed52-147">PlaylistArray</span><span class="sxs-lookup"><span data-stu-id="1ed52-147">PlaylistArray</span></span>](playlistarray-object.md)           | [<span data-ttu-id="1ed52-148">item</span><span class="sxs-lookup"><span data-stu-id="1ed52-148">item</span></span>](playlistarray-item.md)                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="1ed52-149">Playlistcollection</span><span class="sxs-lookup"><span data-stu-id="1ed52-149">PlaylistCollection</span></span>](playlistcollection-object.md) | [<span data-ttu-id="1ed52-150">newPlaylist</span><span class="sxs-lookup"><span data-stu-id="1ed52-150">newPlaylist</span></span>](playlistcollection-newplaylist.md)                                                                                                                                                                                                                                  |



 

<span data-ttu-id="1ed52-151">Porque é o meio mais comum de acesso, *Player*. **currentPlaylist** é usado para fins de ilustração nas seções de sintaxe de referência.</span><span class="sxs-lookup"><span data-stu-id="1ed52-151">Because it is the most common means of access, *player*.**currentPlaylist** is used for purposes of illustration in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="1ed52-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ed52-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ed52-153">**Referência de modelo de objeto para scripts**</span><span class="sxs-lookup"><span data-stu-id="1ed52-153">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




