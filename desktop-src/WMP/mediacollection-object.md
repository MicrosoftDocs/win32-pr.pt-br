---
title: Objeto mediacollection
description: O objeto Mediacollection fornece uma maneira de organizar uma grande coleção de itens de mídia. Ele pode ser consultado para gerar listas de reprodução automaticamente.
ms.assetid: afcb2c51-3ecb-4529-8f3e-56aa6d0ec2b4
keywords:
- Objeto mediacollection Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2232e3590acd371039494b31c5d592c2e00f0199
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105800121"
---
# <a name="mediacollection-object"></a><span data-ttu-id="6375c-105">Objeto mediacollection</span><span class="sxs-lookup"><span data-stu-id="6375c-105">MediaCollection Object</span></span>

<span data-ttu-id="6375c-106">O objeto **mediacollection** fornece uma maneira de organizar uma grande coleção de itens de mídia.</span><span class="sxs-lookup"><span data-stu-id="6375c-106">The **MediaCollection** object provides a way to organize a large collection of media items.</span></span> <span data-ttu-id="6375c-107">Ele pode ser consultado para gerar listas de reprodução automaticamente.</span><span class="sxs-lookup"><span data-stu-id="6375c-107">It can be queried to generate playlists automatically.</span></span>

<span data-ttu-id="6375c-108">O objeto **mediacollection** dá suporte aos seguintes métodos.</span><span class="sxs-lookup"><span data-stu-id="6375c-108">The **MediaCollection** object supports the following methods.</span></span>



| <span data-ttu-id="6375c-109">Método</span><span class="sxs-lookup"><span data-stu-id="6375c-109">Method</span></span>                                                                           | <span data-ttu-id="6375c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="6375c-110">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6375c-111">add</span><span class="sxs-lookup"><span data-stu-id="6375c-111">add</span></span>](mediacollection-add.md)                                                   | <span data-ttu-id="6375c-112">Adiciona um novo item de mídia ou lista de reprodução à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="6375c-112">Adds a new media item or playlist to the library.</span></span>                                                                                                              |
| [<span data-ttu-id="6375c-113">createQuery</span><span class="sxs-lookup"><span data-stu-id="6375c-113">createQuery</span></span>](mediacollection-createquery.md)                                   | <span data-ttu-id="6375c-114">Cria um novo objeto de [consulta](query-object.md) .</span><span class="sxs-lookup"><span data-stu-id="6375c-114">Creates a new [Query](query-object.md) object.</span></span>                                                                                                                |
| [<span data-ttu-id="6375c-115">getAll</span><span class="sxs-lookup"><span data-stu-id="6375c-115">getAll</span></span>](mediacollection-getall.md)                                             | <span data-ttu-id="6375c-116">Recupera um objeto [playlist](playlist-object.md) contendo todos os itens de mídia na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="6375c-116">Retrieves a [Playlist](playlist-object.md) object containing all media items in the library.</span></span>                                                                  |
| [<span data-ttu-id="6375c-117">getAttributeStringCollection</span><span class="sxs-lookup"><span data-stu-id="6375c-117">getAttributeStringCollection</span></span>](mediacollection-getattributestringcollection.md) | <span data-ttu-id="6375c-118">Recupera um objeto [StringCollection](stringcollection-object.md) que representa o conjunto de todos os valores de um atributo especificado dentro de um tipo de mídia especificado.</span><span class="sxs-lookup"><span data-stu-id="6375c-118">Retrieves a [StringCollection](stringcollection-object.md) object representing the set of all values for a specified attribute within a specified media type.</span></span> |
| [<span data-ttu-id="6375c-119">getByAlbum</span><span class="sxs-lookup"><span data-stu-id="6375c-119">getByAlbum</span></span>](mediacollection-getbyalbum.md)                                     | <span data-ttu-id="6375c-120">Recupera um objeto [playlist](playlist-object.md) contendo itens de mídia do álbum especificado.</span><span class="sxs-lookup"><span data-stu-id="6375c-120">Retrieves a [Playlist](playlist-object.md) object containing media items from the specified album.</span></span>                                                            |
| [<span data-ttu-id="6375c-121">getByAttribute</span><span class="sxs-lookup"><span data-stu-id="6375c-121">getByAttribute</span></span>](mediacollection-getbyattribute.md)                             | <span data-ttu-id="6375c-122">Recupera um objeto [playlist](playlist-object.md) contendo itens de mídia com o atributo especificado com o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="6375c-122">Retrieves a [Playlist](playlist-object.md) object containing media items with the specified attribute having the specified value.</span></span>                             |
| [<span data-ttu-id="6375c-123">getByAttributeAndMediaType</span><span class="sxs-lookup"><span data-stu-id="6375c-123">getByAttributeAndMediaType</span></span>](mediacollection-getbyattributeandmediatype.md)     | <span data-ttu-id="6375c-124">Recupera um objeto [playlist](playlist-object.md) contendo objetos de [mídia](media-object.md) com o tipo de mídia e o atributo especificados.</span><span class="sxs-lookup"><span data-stu-id="6375c-124">Retrieves a [Playlist](playlist-object.md) object containing [Media](media-object.md) objects having the specified attribute and media type.</span></span>                 |
| [<span data-ttu-id="6375c-125">getByAuthor</span><span class="sxs-lookup"><span data-stu-id="6375c-125">getByAuthor</span></span>](mediacollection-getbyauthor.md)                                   | <span data-ttu-id="6375c-126">Recupera um objeto [playlist](playlist-object.md) contendo itens de mídia pelo autor especificado.</span><span class="sxs-lookup"><span data-stu-id="6375c-126">Retrieves a [Playlist](playlist-object.md) object containing media items by the specified author.</span></span>                                                             |
| [<span data-ttu-id="6375c-127">getByGenre</span><span class="sxs-lookup"><span data-stu-id="6375c-127">getByGenre</span></span>](mediacollection-getbygenre.md)                                     | <span data-ttu-id="6375c-128">Recupera um objeto [playlist](playlist-object.md) contendo itens de mídia com o gênero especificado.</span><span class="sxs-lookup"><span data-stu-id="6375c-128">Retrieves a [Playlist](playlist-object.md) object containing media items with the specified genre.</span></span>                                                            |
| [<span data-ttu-id="6375c-129">getByName</span><span class="sxs-lookup"><span data-stu-id="6375c-129">getByName</span></span>](mediacollection-getbyname.md)                                       | <span data-ttu-id="6375c-130">Recupera um objeto [playlist](playlist-object.md) contendo itens de mídia com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="6375c-130">Retrieves a [Playlist](playlist-object.md) object containing media items with the specified name.</span></span>                                                             |
| [<span data-ttu-id="6375c-131">getMediaAtom</span><span class="sxs-lookup"><span data-stu-id="6375c-131">getMediaAtom</span></span>](mediacollection-getmediaatom.md)                                 | <span data-ttu-id="6375c-132">Recupera o índice no qual uma propriedade especificada reside no conjunto de propriedades disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6375c-132">Retrieves the index at which a specified property resides within the set of available properties.</span></span>                                                              |
| [<span data-ttu-id="6375c-133">getPlaylistByQuery</span><span class="sxs-lookup"><span data-stu-id="6375c-133">getPlaylistByQuery</span></span>](mediacollection-getplaylistbyquery.md)                     | <span data-ttu-id="6375c-134">Recupera um objeto [playlist](playlist-object.md) contendo objetos de [mídia](media-object.md) que correspondem às condições de consulta.</span><span class="sxs-lookup"><span data-stu-id="6375c-134">Retrieves a [Playlist](playlist-object.md) object containing [Media](media-object.md) objects that match the query conditions.</span></span>                               |
| [<span data-ttu-id="6375c-135">getStringCollectionByQuery</span><span class="sxs-lookup"><span data-stu-id="6375c-135">getStringCollectionByQuery</span></span>](mediacollection-getstringcollectionbyquery.md)     | <span data-ttu-id="6375c-136">Recupera um objeto [StringCollection](stringcollection-object.md) que contém cadeias de caracteres que correspondem às condições de consulta.</span><span class="sxs-lookup"><span data-stu-id="6375c-136">Retrieves a [StringCollection](stringcollection-object.md) object containing strings that match the query conditions.</span></span>                                         |
| [<span data-ttu-id="6375c-137">isDeleted</span><span class="sxs-lookup"><span data-stu-id="6375c-137">isDeleted</span></span>](mediacollection-isdeleted.md)                                       | <span data-ttu-id="6375c-138">Recupera um valor que indica se o item de mídia especificado está na pasta itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="6375c-138">Retrieves a value indicating whether the specified media item is in the deleted items folder.</span></span>                                                                  |
| [<span data-ttu-id="6375c-139">remove</span><span class="sxs-lookup"><span data-stu-id="6375c-139">remove</span></span>](mediacollection-remove.md)                                             | <span data-ttu-id="6375c-140">Remove um item da coleção de mídia.</span><span class="sxs-lookup"><span data-stu-id="6375c-140">Removes an item from the media collection.</span></span>                                                                                                                     |
| [<span data-ttu-id="6375c-141">setdeled</span><span class="sxs-lookup"><span data-stu-id="6375c-141">setDeleted</span></span>](mediacollection-setdeleted.md)                                     | <span data-ttu-id="6375c-142">Move o item de mídia especificado para a pasta itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="6375c-142">Moves the specified media item to the deleted items folder.</span></span>                                                                                                    |



 

<span data-ttu-id="6375c-143">O objeto **mediacollection** é acessado por meio da propriedade a seguir.</span><span class="sxs-lookup"><span data-stu-id="6375c-143">The **MediaCollection** object is accessed through the following property.</span></span>



| <span data-ttu-id="6375c-144">Objeto</span><span class="sxs-lookup"><span data-stu-id="6375c-144">Object</span></span>                      | <span data-ttu-id="6375c-145">Propriedade</span><span class="sxs-lookup"><span data-stu-id="6375c-145">Property</span></span>                                      |
|-----------------------------|-----------------------------------------------|
| [<span data-ttu-id="6375c-146">Jogador</span><span class="sxs-lookup"><span data-stu-id="6375c-146">Player</span></span>](player-object.md) | [<span data-ttu-id="6375c-147">mediacollection</span><span class="sxs-lookup"><span data-stu-id="6375c-147">mediaCollection</span></span>](player-mediacollection.md) |



 

## <a name="see-also"></a><span data-ttu-id="6375c-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="6375c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6375c-149">**Referência de modelo de objeto para scripts**</span><span class="sxs-lookup"><span data-stu-id="6375c-149">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




