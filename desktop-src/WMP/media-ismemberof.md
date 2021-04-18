---
title: Método Media. isMemberOf
description: O método isMemberOf retorna um valor que indica se o item de mídia é um membro da playlist especificada.
ms.assetid: e620741f-6807-4a61-ba9b-f45426d6e33e
keywords:
- método isMemberOf Windows Media Player
- método isMemberOf Windows Media Player, classe de mídia
- Classe de mídia Windows Media Player, método isMemberOf
topic_type:
- apiref
api_name:
- Media.isMemberOf
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41555bd5910ddb3151468a458c5becbf247ea484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813476"
---
# <a name="mediaismemberof-method"></a><span data-ttu-id="7829b-106">Método Media. isMemberOf</span><span class="sxs-lookup"><span data-stu-id="7829b-106">Media.isMemberOf method</span></span>

<span data-ttu-id="7829b-107">O método **isMemberOf** retorna um valor que indica se o item de mídia é um membro da playlist especificada.</span><span class="sxs-lookup"><span data-stu-id="7829b-107">The **isMemberOf** method returns a value indicating whether the media item is a member of the specified playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="7829b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7829b-108">Syntax</span></span>


```JScript
bRetVal = Media.isMemberOf(
  playlist
)
```



## <a name="parameters"></a><span data-ttu-id="7829b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7829b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7829b-110">*lista de reprodução* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7829b-110">*playlist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7829b-111">Objeto de **playlist** que pode conter o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="7829b-111">**Playlist** object that might contain the media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7829b-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7829b-112">Return value</span></span>

<span data-ttu-id="7829b-113">Esse método retorna um **valor booleano**.</span><span class="sxs-lookup"><span data-stu-id="7829b-113">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7829b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7829b-114">Remarks</span></span>

<span data-ttu-id="7829b-115">Esse método não pode verificar as listas de reprodução recuperadas por meio do objeto **mediacollection** .</span><span class="sxs-lookup"><span data-stu-id="7829b-115">This method is cannot check playlists retrieved through the **MediaCollection** object.</span></span> <span data-ttu-id="7829b-116">Para testar se um item de mídia é membro de uma lista de reprodução nomeada específica, recupere a lista de reprodução com o *Player*. *playlistcollection*. **getByName**(*nome*). **Item**(0).</span><span class="sxs-lookup"><span data-stu-id="7829b-116">To test whether a media item is a member of a particular named playlist, retrieve the playlist with *player*.*playlistCollection*.**getByName**(*name*).**item**(0).</span></span> <span data-ttu-id="7829b-117">Esse método também pode ser usado com playlists de CD e listas de reprodução de metarquivo.</span><span class="sxs-lookup"><span data-stu-id="7829b-117">This method can also be used with CD playlists and metafile playlists.</span></span>

<span data-ttu-id="7829b-118">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="7829b-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="7829b-119">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="7829b-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7829b-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7829b-120">Examples</span></span>

<span data-ttu-id="7829b-121">O exemplo de JScript a seguir usa *mídia*. **isMemberOf** para testar se o item de mídia atual é membro da playlist chamada playlist de exemplo.</span><span class="sxs-lookup"><span data-stu-id="7829b-121">The following JScript example uses *Media*.**isMemberOf** to test whether the current media item is a member of the playlist named Sample Playlist.</span></span> <span data-ttu-id="7829b-122">Se não for, o item de mídia atual será anexado à playlist de exemplo.</span><span class="sxs-lookup"><span data-stu-id="7829b-122">If it is not, the current media item is appended to the sample playlist.</span></span> <span data-ttu-id="7829b-123">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="7829b-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the playlist object named Sample Playlist.
var sPlaylist = Player.playlistcollection.getbyname("Sample Playlist").item(0);

// Test whether the current media item is a member of Sample Playlist.
 var answer = ((Player.currentMedia.isMemberOf(sPlaylist))?"Yes":"No");

// If the current media item is not a member of Sample Playlist,
// append the current media item to the playlist.
if (answer == "No"){
   sPlaylist.appendItem(Player.currentMedia);
}

```



## <a name="requirements"></a><span data-ttu-id="7829b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7829b-124">Requirements</span></span>



| <span data-ttu-id="7829b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7829b-125">Requirement</span></span> | <span data-ttu-id="7829b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="7829b-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7829b-127">Versão</span><span class="sxs-lookup"><span data-stu-id="7829b-127">Version</span></span><br/> | <span data-ttu-id="7829b-128">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="7829b-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7829b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7829b-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="7829b-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7829b-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7829b-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="7829b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7829b-132">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="7829b-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="7829b-133">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="7829b-133">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="7829b-134">**Objeto playlistcollection**</span><span class="sxs-lookup"><span data-stu-id="7829b-134">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="7829b-135">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="7829b-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="7829b-136">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="7829b-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





