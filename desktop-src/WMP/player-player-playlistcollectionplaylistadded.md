---
title: Evento Player. PlaylistCollectionPlaylistAdded
description: O evento PlaylistCollectionPlaylistAdded ocorre quando uma playlist é adicionada à coleção de playlist. | Evento Player. PlaylistCollectionPlaylistAdded
ms.assetid: 07acb5e6-d832-4f0b-a6bb-2b7ba27c368d
keywords:
- Evento PlaylistCollectionPlaylistAdded do Windows Media Player
- Evento PlaylistCollectionPlaylistAdded Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento PlaylistCollectionPlaylistAdded
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e6a229aff95d29ae93433dab538521d88c50c1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784548"
---
# <a name="playerplaylistcollectionplaylistadded-event"></a><span data-ttu-id="4e982-107">Evento Player. PlaylistCollectionPlaylistAdded</span><span class="sxs-lookup"><span data-stu-id="4e982-107">Player.PlaylistCollectionPlaylistAdded event</span></span>

<span data-ttu-id="4e982-108">O evento **PlaylistCollectionPlaylistAdded** ocorre quando uma playlist é adicionada à coleção de playlist.</span><span class="sxs-lookup"><span data-stu-id="4e982-108">The **PlaylistCollectionPlaylistAdded** event occurs when a playlist is added to the playlist collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e982-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e982-109">Syntax</span></span>


```JScript
Player.PlaylistCollectionPlaylistAdded(
  bstrPlaylistName
)
```



## <a name="parameters"></a><span data-ttu-id="4e982-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e982-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e982-111">*bstrPlaylistName*</span><span class="sxs-lookup"><span data-stu-id="4e982-111">*bstrPlaylistName*</span></span> 
</dt> <dd>

<span data-ttu-id="4e982-112">**Cadeia de caracteres** que especifica o nome da lista de reprodução que foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="4e982-112">**String** specifying the name of the playlist that was added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e982-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4e982-113">Return value</span></span>

<span data-ttu-id="4e982-114">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4e982-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e982-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e982-115">Remarks</span></span>

<span data-ttu-id="4e982-116">O nome da lista de reprodução que foi adicionado pode ser usado para recuperar o objeto de **playlist** correspondente usando a *playlistcollection*. método **getByName** .</span><span class="sxs-lookup"><span data-stu-id="4e982-116">The name of the playlist that was added can be used to retrieve the corresponding **Playlist** object using the *PlaylistCollection*.**getByName** method.</span></span>

<span data-ttu-id="4e982-117">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="4e982-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="4e982-118">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="4e982-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="4e982-119">**Windows Media Player 10 Mobile:** Não há suporte para esse evento.</span><span class="sxs-lookup"><span data-stu-id="4e982-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e982-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e982-120">Requirements</span></span>



| <span data-ttu-id="4e982-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e982-121">Requirement</span></span> | <span data-ttu-id="4e982-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4e982-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4e982-123">Versão</span><span class="sxs-lookup"><span data-stu-id="4e982-123">Version</span></span><br/> | <span data-ttu-id="4e982-124">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="4e982-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4e982-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4e982-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="4e982-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e982-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e982-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e982-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e982-128">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="4e982-128">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="4e982-129">**Playlistcollection. getByName**</span><span class="sxs-lookup"><span data-stu-id="4e982-129">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





