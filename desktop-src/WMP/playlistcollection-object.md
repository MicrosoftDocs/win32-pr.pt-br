---
title: Objeto playlistcollection
description: O objeto Playlistcollection fornece uma maneira de organizar suas listas de reprodução.
ms.assetid: 9ea61954-d185-4a77-9016-4d58340a96fc
keywords:
- Objeto playlistcollection Windows Media Player
topic_type:
- apiref
api_name:
- PlaylistCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2266537e0df9fc0ba5527784c254b27313d636d3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105784630"
---
# <a name="playlistcollection-object"></a><span data-ttu-id="06fb8-104">Objeto playlistcollection</span><span class="sxs-lookup"><span data-stu-id="06fb8-104">PlaylistCollection Object</span></span>

<span data-ttu-id="06fb8-105">O objeto **playlistcollection** fornece uma maneira de organizar suas listas de reprodução.</span><span class="sxs-lookup"><span data-stu-id="06fb8-105">The **PlaylistCollection** object provides a way to organize your playlists.</span></span>

<span data-ttu-id="06fb8-106">O objeto **playlistcollection** dá suporte aos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="06fb8-106">The **PlaylistCollection** object supports the following methods.</span></span>



| <span data-ttu-id="06fb8-107">Método</span><span class="sxs-lookup"><span data-stu-id="06fb8-107">Method</span></span>                                                  | <span data-ttu-id="06fb8-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="06fb8-108">Description</span></span>                                                                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06fb8-109">getAll</span><span class="sxs-lookup"><span data-stu-id="06fb8-109">getAll</span></span>](playlistcollection-getall.md)                 | <span data-ttu-id="06fb8-110">Recupera um objeto [PlaylistArray](playlistarray-object.md) que contém todas as listas de reprodução na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="06fb8-110">Retrieves a [PlaylistArray](playlistarray-object.md) object containing all the playlists in the library.</span></span>                |
| [<span data-ttu-id="06fb8-111">getByName</span><span class="sxs-lookup"><span data-stu-id="06fb8-111">getByName</span></span>](playlistcollection-getbyname.md)           | <span data-ttu-id="06fb8-112">Recupera um objeto [PlaylistArray](playlistarray-object.md) contendo listas de reprodução com o nome especificado, se existir.</span><span class="sxs-lookup"><span data-stu-id="06fb8-112">Retrieves a [PlaylistArray](playlistarray-object.md) object containing playlists with the specified name, if any exist.</span></span> |
| [<span data-ttu-id="06fb8-113">importPlaylist</span><span class="sxs-lookup"><span data-stu-id="06fb8-113">importPlaylist</span></span>](playlistcollection-importplaylist.md) | <span data-ttu-id="06fb8-114">Adiciona uma lista de reprodução estática à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="06fb8-114">Adds a static playlist to the library.</span></span>                                                                                   |
| [<span data-ttu-id="06fb8-115">isDeleted</span><span class="sxs-lookup"><span data-stu-id="06fb8-115">isDeleted</span></span>](playlistcollection-isdeleted.md)           | <span data-ttu-id="06fb8-116">Recupera um valor que indica se a playlist especificada está na pasta itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="06fb8-116">Retrieves a value indicating whether the specified playlist is in the deleted items folder.</span></span>                              |
| [<span data-ttu-id="06fb8-117">newPlaylist</span><span class="sxs-lookup"><span data-stu-id="06fb8-117">newPlaylist</span></span>](playlistcollection-newplaylist.md)       | <span data-ttu-id="06fb8-118">Cria uma nova lista de reprodução na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="06fb8-118">Creates a new playlist in the library.</span></span>                                                                                   |
| [<span data-ttu-id="06fb8-119">remove</span><span class="sxs-lookup"><span data-stu-id="06fb8-119">remove</span></span>](playlistcollection-remove.md)                 | <span data-ttu-id="06fb8-120">Remove uma lista de reprodução da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="06fb8-120">Removes a playlist from the library.</span></span>                                                                                     |
| [<span data-ttu-id="06fb8-121">setdeled</span><span class="sxs-lookup"><span data-stu-id="06fb8-121">setDeleted</span></span>](playlistcollection-setdeleted.md)         | <span data-ttu-id="06fb8-122">Move uma lista de reprodução para a pasta itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="06fb8-122">Moves a playlist to the deleted items folder.</span></span>                                                                            |



 

<span data-ttu-id="06fb8-123">O objeto **playlistcollection** é acessado por meio da propriedade a seguir.</span><span class="sxs-lookup"><span data-stu-id="06fb8-123">The **PlaylistCollection** object is accessed through the following property.</span></span>



| <span data-ttu-id="06fb8-124">Objeto</span><span class="sxs-lookup"><span data-stu-id="06fb8-124">Object</span></span>                      | <span data-ttu-id="06fb8-125">Propriedade</span><span class="sxs-lookup"><span data-stu-id="06fb8-125">Property</span></span>                                            |
|-----------------------------|-----------------------------------------------------|
| [<span data-ttu-id="06fb8-126">Jogador</span><span class="sxs-lookup"><span data-stu-id="06fb8-126">Player</span></span>](player-object.md) | [<span data-ttu-id="06fb8-127">playlistcollection</span><span class="sxs-lookup"><span data-stu-id="06fb8-127">playlistCollection</span></span>](player-playlistcollection.md) |



 

## <a name="see-also"></a><span data-ttu-id="06fb8-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="06fb8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06fb8-129">**Referência de modelo de objeto para scripts**</span><span class="sxs-lookup"><span data-stu-id="06fb8-129">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




