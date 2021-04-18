---
title: Método playlistcollection. importPlaylist
description: O método importPlaylist adiciona uma lista de reprodução estática à biblioteca. | Método playlistcollection. importPlaylist
ms.assetid: 0611ba42-fd8f-4fb9-9fbb-809a82775c2a
keywords:
- método importPlaylist Windows Media Player
- método importPlaylist Windows Media Player, classe Playlistcollection
- Classe playlistcollection Windows Media Player, método importPlaylist
topic_type:
- apiref
api_name:
- PlaylistCollection.importPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736e9afa17f571428fada48660726b606268796a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768227"
---
# <a name="playlistcollectionimportplaylist-method"></a><span data-ttu-id="88b2e-107">Método playlistcollection. importPlaylist</span><span class="sxs-lookup"><span data-stu-id="88b2e-107">PlaylistCollection.importPlaylist method</span></span>

<span data-ttu-id="88b2e-108">O método **importPlaylist** adiciona uma lista de reprodução estática à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="88b2e-108">The **importPlaylist** method adds a static playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="88b2e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88b2e-109">Syntax</span></span>


```JScript
retVal = PlaylistCollection.importPlaylist(
  playlist
)
```



## <a name="parameters"></a><span data-ttu-id="88b2e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88b2e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88b2e-111">*lista de reprodução* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="88b2e-111">*playlist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88b2e-112">Objeto de **playlist** a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="88b2e-112">**Playlist** object to be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88b2e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="88b2e-113">Return value</span></span>

<span data-ttu-id="88b2e-114">Esse método retorna o objeto **playlist** que foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="88b2e-114">This method returns the **Playlist** object that was added.</span></span>

## <a name="remarks"></a><span data-ttu-id="88b2e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="88b2e-115">Remarks</span></span>

<span data-ttu-id="88b2e-116">As listas de reprodução que não contêm nenhum item de mídia não podem ser adicionadas à biblioteca usando esse método.</span><span class="sxs-lookup"><span data-stu-id="88b2e-116">Playlists that do not contain any media items cannot be added to the library by using this method.</span></span> <span data-ttu-id="88b2e-117">Para criar uma lista de reprodução vazia na biblioteca, use o método **newPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="88b2e-117">To create an empty playlist in the library, use the **newPlaylist** method.</span></span> <span data-ttu-id="88b2e-118">Em seguida, você pode preencher a lista de reprodução resultante com itens de mídia usando a *lista de reprodução*. **appendItem** ou *playlist*. **insertItem**.</span><span class="sxs-lookup"><span data-stu-id="88b2e-118">You can then fill the resulting playlist with media items by using *Playlist*.**appendItem** or *Playlist*.**insertItem**.</span></span>

<span data-ttu-id="88b2e-119">Se você passar esse método para uma lista de reprodução automática, a consulta será executada uma vez e o resultado será adicionado à biblioteca como uma lista de reprodução estática.</span><span class="sxs-lookup"><span data-stu-id="88b2e-119">If you pass this method an auto playlist, the query is executed once and the result is added to the library as a static playlist.</span></span> <span data-ttu-id="88b2e-120">Para adicionar uma lista de reprodução automática à biblioteca e preservar seu comportamento automático, use *mediacollection*. **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="88b2e-120">To add an auto playlist to the library and preserve its automatic behavior, use *MediaCollection*.**add**.</span></span> <span data-ttu-id="88b2e-121">Para obter mais informações, consulte [playlists estáticas e automáticas](static-and-auto-playlists.md).</span><span class="sxs-lookup"><span data-stu-id="88b2e-121">For more information, see [Static and Auto Playlists](static-and-auto-playlists.md).</span></span>

<span data-ttu-id="88b2e-122">Para usar esse método, é necessário ter acesso completo à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="88b2e-122">To use this method, full access to the library is required.</span></span> <span data-ttu-id="88b2e-123">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="88b2e-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="88b2e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88b2e-124">Requirements</span></span>



| <span data-ttu-id="88b2e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="88b2e-125">Requirement</span></span> | <span data-ttu-id="88b2e-126">Valor</span><span class="sxs-lookup"><span data-stu-id="88b2e-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="88b2e-127">Versão</span><span class="sxs-lookup"><span data-stu-id="88b2e-127">Version</span></span><br/> | <span data-ttu-id="88b2e-128">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="88b2e-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="88b2e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="88b2e-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="88b2e-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88b2e-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88b2e-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="88b2e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88b2e-132">**Gerenciando listas de reprodução**</span><span class="sxs-lookup"><span data-stu-id="88b2e-132">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="88b2e-133">**Objeto mediacollection**</span><span class="sxs-lookup"><span data-stu-id="88b2e-133">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="88b2e-134">**Mediacollection. adicionar**</span><span class="sxs-lookup"><span data-stu-id="88b2e-134">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="88b2e-135">**Playlist. appendItem**</span><span class="sxs-lookup"><span data-stu-id="88b2e-135">**Playlist.appendItem**</span></span>](playlist-appenditem.md)
</dt> <dt>

[<span data-ttu-id="88b2e-136">**Playlist. insertItem**</span><span class="sxs-lookup"><span data-stu-id="88b2e-136">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="88b2e-137">**Objeto playlistcollection**</span><span class="sxs-lookup"><span data-stu-id="88b2e-137">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="88b2e-138">**Playlistcollection. newPlaylist**</span><span class="sxs-lookup"><span data-stu-id="88b2e-138">**PlaylistCollection.newPlaylist**</span></span>](playlistcollection-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="88b2e-139">**Playlistcollection. Remove**</span><span class="sxs-lookup"><span data-stu-id="88b2e-139">**PlaylistCollection.remove**</span></span>](playlistcollection-remove.md)
</dt> <dt>

[<span data-ttu-id="88b2e-140">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="88b2e-140">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="88b2e-141">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="88b2e-141">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





