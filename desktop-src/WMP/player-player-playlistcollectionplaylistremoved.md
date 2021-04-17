---
title: Evento Player. PlaylistCollectionPlaylistRemoved
description: O evento PlaylistCollectionPlaylistRemoved ocorre quando uma playlist é removida da coleção de playlist. | Evento Player. PlaylistCollectionPlaylistRemoved
ms.assetid: 2405be98-b4c2-4b4e-bea6-0c48a3e26f18
keywords:
- Evento PlaylistCollectionPlaylistRemoved do Windows Media Player
- Evento PlaylistCollectionPlaylistRemoved Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento PlaylistCollectionPlaylistRemoved
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a449a7b00516f4fee613722d1cc126eb74227948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782604"
---
# <a name="playerplaylistcollectionplaylistremoved-event"></a><span data-ttu-id="c17a6-107">Evento Player. PlaylistCollectionPlaylistRemoved</span><span class="sxs-lookup"><span data-stu-id="c17a6-107">Player.PlaylistCollectionPlaylistRemoved event</span></span>

<span data-ttu-id="c17a6-108">O evento **PlaylistCollectionPlaylistRemoved** ocorre quando uma playlist é removida da coleção de playlist.</span><span class="sxs-lookup"><span data-stu-id="c17a6-108">The **PlaylistCollectionPlaylistRemoved** event occurs when a playlist is removed from the playlist collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c17a6-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c17a6-109">Syntax</span></span>


```JScript
Player.PlaylistCollectionPlaylistRemoved(
  bstrPlaylistName
)
```



## <a name="parameters"></a><span data-ttu-id="c17a6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c17a6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c17a6-111">*bstrPlaylistName*</span><span class="sxs-lookup"><span data-stu-id="c17a6-111">*bstrPlaylistName*</span></span> 
</dt> <dd>

<span data-ttu-id="c17a6-112">**Cadeia de caracteres** que especifica o nome da lista de reprodução que foi removida.</span><span class="sxs-lookup"><span data-stu-id="c17a6-112">**String** specifying the name of the playlist that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c17a6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c17a6-113">Return value</span></span>

<span data-ttu-id="c17a6-114">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c17a6-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c17a6-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c17a6-115">Remarks</span></span>

<span data-ttu-id="c17a6-116">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="c17a6-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="c17a6-117">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="c17a6-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="c17a6-118">**Windows Media Player 10 Mobile:** Não há suporte para esse evento.</span><span class="sxs-lookup"><span data-stu-id="c17a6-118">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="c17a6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c17a6-119">Requirements</span></span>



| <span data-ttu-id="c17a6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c17a6-120">Requirement</span></span> | <span data-ttu-id="c17a6-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c17a6-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c17a6-122">Versão</span><span class="sxs-lookup"><span data-stu-id="c17a6-122">Version</span></span><br/> | <span data-ttu-id="c17a6-123">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c17a6-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c17a6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c17a6-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="c17a6-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c17a6-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c17a6-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c17a6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c17a6-127">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="c17a6-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="c17a6-128">**Playlistcollection. getByName**</span><span class="sxs-lookup"><span data-stu-id="c17a6-128">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





