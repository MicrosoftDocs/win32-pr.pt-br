---
title: Método playlistcollection. newPlaylist
description: O método newPlaylist cria uma nova lista de reprodução na biblioteca.
ms.assetid: 428b5779-4dc0-466b-9834-6b2c43324013
keywords:
- método newPlaylist Windows Media Player
- método newPlaylist Windows Media Player, classe Playlistcollection
- Classe playlistcollection Windows Media Player, método newPlaylist
topic_type:
- apiref
api_name:
- PlaylistCollection.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d94c25a8dfe6f1eb7c4dac40dd644433a5f0d7e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813673"
---
# <a name="playlistcollectionnewplaylist-method"></a><span data-ttu-id="17c2d-106">Método playlistcollection. newPlaylist</span><span class="sxs-lookup"><span data-stu-id="17c2d-106">PlaylistCollection.newPlaylist method</span></span>

<span data-ttu-id="17c2d-107">O método **newPlaylist** cria uma nova lista de reprodução na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="17c2d-107">The **newPlaylist** method creates a new playlist in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="17c2d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17c2d-108">Syntax</span></span>


```JScript
retVal = PlaylistCollection.newPlaylist(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="17c2d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17c2d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17c2d-110">*nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="17c2d-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17c2d-111">**Cadeia de caracteres** que contém o nome da lista de reprodução a ser criada.</span><span class="sxs-lookup"><span data-stu-id="17c2d-111">**String** containing the name of the playlist to be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17c2d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17c2d-112">Return value</span></span>

<span data-ttu-id="17c2d-113">Esse método retorna um objeto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="17c2d-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="17c2d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="17c2d-114">Remarks</span></span>

<span data-ttu-id="17c2d-115">Esse método cria uma lista de reprodução vazia na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="17c2d-115">This method creates an empty playlist in the library.</span></span> <span data-ttu-id="17c2d-116">Para preencher a lista de reprodução com itens de mídia, use a *lista de reprodução*. **appendItem** ou *playlist*. **insertItem**.</span><span class="sxs-lookup"><span data-stu-id="17c2d-116">To fill the playlist with media items, use *Playlist*.**appendItem** or *Playlist*.**insertItem**.</span></span>

<span data-ttu-id="17c2d-117">Várias listas de reprodução com o mesmo nome são permitidas na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="17c2d-117">Multiple playlists having the same name are permitted in the library.</span></span> <span data-ttu-id="17c2d-118">Para evitar a criação de um nome de playlist duplicado com esse método, use **getByName** e *PlaylistArray*. **contagem** para determinar se já existe uma lista de reprodução com um nome específico.</span><span class="sxs-lookup"><span data-stu-id="17c2d-118">To avoid creating a duplicate playlist name with this method, use **getByName** and *PlaylistArray*.**count** to determine whether a playlist with a particular name already exists.</span></span>

<span data-ttu-id="17c2d-119">Espaços à esquerda e à direita não são permitidos em nomes de playlist e são removidos automaticamente do valor especificado para o parâmetro de *nome* .</span><span class="sxs-lookup"><span data-stu-id="17c2d-119">Leading and trailing spaces are not permitted in playlist names, and are automatically removed from the value specified for the *name* parameter.</span></span>

<span data-ttu-id="17c2d-120">Para usar esse método, é necessário ter acesso completo à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="17c2d-120">To use this method, full access to the library is required.</span></span> <span data-ttu-id="17c2d-121">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="17c2d-121">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="17c2d-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="17c2d-122">Examples</span></span>

<span data-ttu-id="17c2d-123">O exemplo de JScript a seguir cria uma nova lista de reprodução vazia chamada "Trêslist".</span><span class="sxs-lookup"><span data-stu-id="17c2d-123">The following JScript example creates a new empty playlist called "ThreeList".</span></span> <span data-ttu-id="17c2d-124">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="17c2d-124">The **Player** object was created with ID="Player".</span></span>


```JScript
//Add a new empty playlist, named ThreeList, to the playlist collection.
var NewList = Player.playlistCollection.newPlaylist("ThreeList");

```



## <a name="requirements"></a><span data-ttu-id="17c2d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17c2d-125">Requirements</span></span>



| <span data-ttu-id="17c2d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="17c2d-126">Requirement</span></span> | <span data-ttu-id="17c2d-127">Valor</span><span class="sxs-lookup"><span data-stu-id="17c2d-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="17c2d-128">Versão</span><span class="sxs-lookup"><span data-stu-id="17c2d-128">Version</span></span><br/> | <span data-ttu-id="17c2d-129">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="17c2d-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="17c2d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="17c2d-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="17c2d-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17c2d-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17c2d-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="17c2d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17c2d-133">**Mediacollection. adicionar**</span><span class="sxs-lookup"><span data-stu-id="17c2d-133">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="17c2d-134">**Playlist. appendItem**</span><span class="sxs-lookup"><span data-stu-id="17c2d-134">**Playlist.appendItem**</span></span>](playlist-appenditem.md)
</dt> <dt>

[<span data-ttu-id="17c2d-135">**Playlist. insertItem**</span><span class="sxs-lookup"><span data-stu-id="17c2d-135">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="17c2d-136">**Contagem de PlaylistArray.**</span><span class="sxs-lookup"><span data-stu-id="17c2d-136">**PlaylistArray.count**</span></span>](playlistarray-count.md)
</dt> <dt>

[<span data-ttu-id="17c2d-137">**Objeto playlistcollection**</span><span class="sxs-lookup"><span data-stu-id="17c2d-137">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="17c2d-138">**Playlistcollection. getByName**</span><span class="sxs-lookup"><span data-stu-id="17c2d-138">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> <dt>

[<span data-ttu-id="17c2d-139">**Playlistcollection. importPlaylist**</span><span class="sxs-lookup"><span data-stu-id="17c2d-139">**PlaylistCollection.importPlaylist**</span></span>](playlistcollection-importplaylist.md)
</dt> <dt>

[<span data-ttu-id="17c2d-140">**Playlistcollection. Remove**</span><span class="sxs-lookup"><span data-stu-id="17c2d-140">**PlaylistCollection.remove**</span></span>](playlistcollection-remove.md)
</dt> <dt>

[<span data-ttu-id="17c2d-141">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="17c2d-141">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="17c2d-142">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="17c2d-142">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





