---
title: Evento Player. CurrentPlaylistItemAvailable
description: O evento CurrentPlaylistItemAvailable ocorre quando a playlist atual fica disponível. | Evento Player. CurrentPlaylistItemAvailable
ms.assetid: 4894e2fc-3464-413f-8abf-8b5e91899946
keywords:
- Evento CurrentPlaylistItemAvailable do Windows Media Player
- Evento CurrentPlaylistItemAvailable Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento CurrentPlaylistItemAvailable
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fe5809e50d572cfb8eb7a36220d083ec18a0a76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771526"
---
# <a name="playercurrentplaylistitemavailable-event"></a><span data-ttu-id="50912-107">Evento Player. CurrentPlaylistItemAvailable</span><span class="sxs-lookup"><span data-stu-id="50912-107">Player.CurrentPlaylistItemAvailable event</span></span>

<span data-ttu-id="50912-108">O evento **CurrentPlaylistItemAvailable** ocorre quando a playlist atual fica disponível.</span><span class="sxs-lookup"><span data-stu-id="50912-108">The **CurrentPlaylistItemAvailable** event occurs when the current playlist becomes available.</span></span>

## <a name="syntax"></a><span data-ttu-id="50912-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50912-109">Syntax</span></span>


```JScript
Player.CurrentPlaylistItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a><span data-ttu-id="50912-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50912-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50912-111">*bstrItemName*</span><span class="sxs-lookup"><span data-stu-id="50912-111">*bstrItemName*</span></span> 
</dt> <dd>

<span data-ttu-id="50912-112">**Cadeia de caracteres** que contém o nome do item da playlist atual.</span><span class="sxs-lookup"><span data-stu-id="50912-112">**String** containing the name of the current playlist item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50912-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="50912-113">Return value</span></span>

<span data-ttu-id="50912-114">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="50912-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50912-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="50912-115">Remarks</span></span>

<span data-ttu-id="50912-116">O nome da lista de reprodução atual pode ser usado para recuperar o objeto de **playlist** correspondente usando a *playlistcollection*. método **getByName** .</span><span class="sxs-lookup"><span data-stu-id="50912-116">The name of the current playlist can be used to retrieve the corresponding **Playlist** object using the *PlaylistCollection*.**getByName** method.</span></span>

<span data-ttu-id="50912-117">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="50912-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="50912-118">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="50912-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="50912-119">**Windows Media Player 10 Mobile:** Não há suporte para esse evento.</span><span class="sxs-lookup"><span data-stu-id="50912-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="50912-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50912-120">Requirements</span></span>



| <span data-ttu-id="50912-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="50912-121">Requirement</span></span> | <span data-ttu-id="50912-122">Valor</span><span class="sxs-lookup"><span data-stu-id="50912-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="50912-123">Versão</span><span class="sxs-lookup"><span data-stu-id="50912-123">Version</span></span><br/> | <span data-ttu-id="50912-124">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="50912-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="50912-125">DLL</span><span class="sxs-lookup"><span data-stu-id="50912-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="50912-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50912-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50912-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="50912-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50912-128">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="50912-128">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="50912-129">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="50912-129">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="50912-130">**Playlistcollection. getByName**</span><span class="sxs-lookup"><span data-stu-id="50912-130">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





