---
title: Método Player. newPlaylist
description: O método newPlaylist cria um novo objeto de lista de reprodução.
ms.assetid: a566006e-8647-4c51-ab77-762728f25a30
keywords:
- método newPlaylist Windows Media Player
- método newPlaylist Windows Media Player, classe Player
- Classe de jogador Windows Media Player, método newPlaylist
topic_type:
- apiref
api_name:
- Player.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa65ae4b453fe919116a33c5ee86b14ba353f681
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763052"
---
# <a name="playernewplaylist-method"></a><span data-ttu-id="7a789-106">Método Player. newPlaylist</span><span class="sxs-lookup"><span data-stu-id="7a789-106">Player.newPlaylist method</span></span>

<span data-ttu-id="7a789-107">O método **newPlaylist** cria um novo objeto de **lista de reprodução** .</span><span class="sxs-lookup"><span data-stu-id="7a789-107">The **newPlaylist** method creates a new **Playlist** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a789-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a789-108">Syntax</span></span>


```JScript
retVal = Player.newPlaylist(
  name,
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="7a789-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a789-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a789-110">*nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="7a789-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a789-111">**Cadeia de caracteres** que contém o nome da nova lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="7a789-111">**String** containing the name of the new playlist.</span></span>

</dd> <dt>

<span data-ttu-id="7a789-112">*URL* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="7a789-112">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a789-113">**Cadeia de caracteres** que contém a URL da lista de reprodução do metarquivo do Windows Media com a qual criar o objeto de **playlist** .</span><span class="sxs-lookup"><span data-stu-id="7a789-113">**String** containing the URL of the Windows Media metafile playlist to create the **Playlist** object with.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a789-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7a789-114">Return value</span></span>

<span data-ttu-id="7a789-115">Esse método retorna um objeto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="7a789-115">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a789-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a789-116">Remarks</span></span>

<span data-ttu-id="7a789-117">Se o parâmetro de *URL* for definido como nulo ou "" (cadeia de caracteres vazia), um objeto de **playlist** vazio será criado.</span><span class="sxs-lookup"><span data-stu-id="7a789-117">If the *URL* parameter is set to null or "" (empty string), an empty **Playlist** object will be created.</span></span> <span data-ttu-id="7a789-118">Se o parâmetro *Name* for definido como "", o nome no metarquivo será usado.</span><span class="sxs-lookup"><span data-stu-id="7a789-118">If the *name* parameter is set to "", the name in the metafile is used.</span></span>

<span data-ttu-id="7a789-119">A nova lista de reprodução criada com esse método não é adicionada à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="7a789-119">The new playlist created with this method is not added to the library.</span></span> <span data-ttu-id="7a789-120">Para adicionar uma nova lista de reprodução à biblioteca, use *playlistcollection*. **importPlaylist** ou *playlistcollection*. **newPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="7a789-120">To add a new playlist to the library, use *PlaylistCollection*.**importPlaylist** or *PlaylistCollection*.**newPlaylist**.</span></span> <span data-ttu-id="7a789-121">Os espaços à esquerda ou à direita no nome da playlist são removidos automaticamente quando adicionados à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="7a789-121">Any leading or trailing spaces in the playlist name are automatically removed when it is added to the library.</span></span>

<span data-ttu-id="7a789-122">Como a biblioteca permite várias listas de reprodução com o mesmo nome, talvez você queira verificar a presença de uma lista de reprodução com um nome específico antes de adicionar uma nova.</span><span class="sxs-lookup"><span data-stu-id="7a789-122">Because the library allows multiple playlists with the same name, you may want to check for the presence of a playlist with a given name before adding a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a789-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a789-123">Requirements</span></span>



| <span data-ttu-id="7a789-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a789-124">Requirement</span></span> | <span data-ttu-id="7a789-125">Valor</span><span class="sxs-lookup"><span data-stu-id="7a789-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7a789-126">Versão</span><span class="sxs-lookup"><span data-stu-id="7a789-126">Version</span></span><br/> | <span data-ttu-id="7a789-127">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="7a789-127">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="7a789-128">DLL</span><span class="sxs-lookup"><span data-stu-id="7a789-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="7a789-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a789-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a789-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a789-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a789-131">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="7a789-131">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="7a789-132">**Playlistcollection. importPlaylist**</span><span class="sxs-lookup"><span data-stu-id="7a789-132">**PlaylistCollection.importPlaylist**</span></span>](playlistcollection-importplaylist.md)
</dt> <dt>

[<span data-ttu-id="7a789-133">**Playlistcollection. newPlaylist**</span><span class="sxs-lookup"><span data-stu-id="7a789-133">**PlaylistCollection.newPlaylist**</span></span>](playlistcollection-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="7a789-134">**Metaarquivos do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7a789-134">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 





