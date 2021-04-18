---
title: Player. currentPlaylist
description: A propriedade currentPlaylist especifica ou recupera o objeto de playlist atual.
ms.assetid: fabfb927-5f64-4fc4-8ee5-e2449082dfbc
keywords:
- Player. currentPlaylist Windows Media Player
topic_type:
- apiref
api_name:
- Player.currentPlaylist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceae33a201086d268942e47496874678ec13f459
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781358"
---
# <a name="playercurrentplaylist"></a><span data-ttu-id="0a70e-104">Player. currentPlaylist</span><span class="sxs-lookup"><span data-stu-id="0a70e-104">Player.currentPlaylist</span></span>

<span data-ttu-id="0a70e-105">A propriedade currentPlaylist especifica ou recupera o objeto de **playlist** atual.</span><span class="sxs-lookup"><span data-stu-id="0a70e-105">The currentPlaylist property specifies or retrieves the current **Playlist** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a70e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a70e-106">Syntax</span></span>

<span data-ttu-id="0a70e-107">*Player* . **currentPlaylist**</span><span class="sxs-lookup"><span data-stu-id="0a70e-107">*player* .**currentPlaylist**</span></span>

## <a name="possible-values"></a><span data-ttu-id="0a70e-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="0a70e-108">Possible Values</span></span>

<span data-ttu-id="0a70e-109">Esta propriedade é um objeto de **lista de reprodução** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0a70e-109">This property is a read/write **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a70e-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a70e-110">Remarks</span></span>

<span data-ttu-id="0a70e-111">Se as *configurações*. a propriedade **AutoStart** é true, a reprodução é iniciada automaticamente sempre que você definir **currentPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="0a70e-111">If the *Settings*.**autoStart** property is true, playback begins automatically whenever you set **currentPlaylist**.</span></span>

<span data-ttu-id="0a70e-112">Essa propriedade usa um objeto playlist, que pode ser adquirido de várias maneiras, como ao chamar *PlaylistArray*. **Item** ou *playlistcollection*. **newPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="0a70e-112">This property takes a Playlist object, which can be acquired in several ways, such as by calling *PlaylistArray*.**item** or *PlaylistCollection*.**newPlaylist**.</span></span> <span data-ttu-id="0a70e-113">Para carregar um item da **playlist** usando um nome de arquivo, defina a propriedade URL ou use *Player*. **newPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="0a70e-113">To load a **Playlist** item using a file name, set the URL property or use *Player*.**newPlaylist**.</span></span>

## <a name="examples"></a><span data-ttu-id="0a70e-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0a70e-114">Examples</span></span>

<span data-ttu-id="0a70e-115">O exemplo de JScript a seguir recupera a primeira lista de reprodução na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="0a70e-115">The following JScript example retrieves the first playlist in the library.</span></span> <span data-ttu-id="0a70e-116">Em seguida, ele usa **currentPlaylist** para tornar a lista de reprodução recuperada a playlist atual e, em seguida, exibir o nome da lista de reprodução atual.</span><span class="sxs-lookup"><span data-stu-id="0a70e-116">It then uses **currentPlaylist** to make the retrieved playlist the current playlist, and then to display the name of the current playlist.</span></span> <span data-ttu-id="0a70e-117">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="0a70e-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve the first playlist from the library.
var firstPL = Player.playlistCollection.getAll().item(0);

// Make the retrieved playlist the current playlist.
Player.currentPlaylist = firstPL;

// Display the name of the current playlist.
document.write("Found first playlist. Name: " + Player.currentPlaylist.name);
```



## <a name="requirements"></a><span data-ttu-id="0a70e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a70e-118">Requirements</span></span>



| <span data-ttu-id="0a70e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a70e-119">Requirement</span></span> | <span data-ttu-id="0a70e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0a70e-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0a70e-121">Versão</span><span class="sxs-lookup"><span data-stu-id="0a70e-121">Version</span></span><br/> | <span data-ttu-id="0a70e-122">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="0a70e-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0a70e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0a70e-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="0a70e-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a70e-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a70e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a70e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a70e-126">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="0a70e-126">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="0a70e-127">**Player. newPlaylist**</span><span class="sxs-lookup"><span data-stu-id="0a70e-127">**Player.newPlaylist**</span></span>](player-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="0a70e-128">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="0a70e-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="0a70e-129">**PlaylistArray. Item**</span><span class="sxs-lookup"><span data-stu-id="0a70e-129">**PlaylistArray.item**</span></span>](playlistarray-item.md)
</dt> <dt>

[<span data-ttu-id="0a70e-130">**Playlistcollection. newPlaylist**</span><span class="sxs-lookup"><span data-stu-id="0a70e-130">**PlaylistCollection.newPlaylist**</span></span>](playlistcollection-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="0a70e-131">**Settings. AutoStart**</span><span class="sxs-lookup"><span data-stu-id="0a70e-131">**Settings.autoStart**</span></span>](settings-autostart.md)
</dt> </dl>

 

 





