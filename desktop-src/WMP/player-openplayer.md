---
title: Método Player. openPlayer
description: O método openPlayer abre o Windows Media Player usando a URL especificada. | Método Player. openPlayer
ms.assetid: 9ddd63c9-f4a0-490a-8543-51ad0fa74a26
keywords:
- método openPlayer Windows Media Player
- método openPlayer Windows Media Player, classe Player
- Classe de jogador Windows Media Player, método openPlayer
topic_type:
- apiref
api_name:
- Player.openPlayer
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3378df48f961f1aa5e3fccec72e79b7f1c26ff08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105773084"
---
# <a name="playeropenplayer-method"></a><span data-ttu-id="ad02d-107">Método Player. openPlayer</span><span class="sxs-lookup"><span data-stu-id="ad02d-107">Player.openPlayer method</span></span>

<span data-ttu-id="ad02d-108">O método **openPlayer** abre o Windows Media Player usando a URL especificada.</span><span class="sxs-lookup"><span data-stu-id="ad02d-108">The **openPlayer** method opens Windows Media Player using the specified URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad02d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad02d-109">Syntax</span></span>


```JScript
Player.openPlayer(
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="ad02d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad02d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad02d-111">*URL* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="ad02d-111">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad02d-112">**Cadeia de caracteres** que representa a URL do item de mídia a ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="ad02d-112">**String** representing the URL of the media item to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad02d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ad02d-113">Return value</span></span>

<span data-ttu-id="ad02d-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ad02d-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad02d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad02d-115">Remarks</span></span>

<span data-ttu-id="ad02d-116">Esse método inicia o Windows Media Player com a URL especificada definida como o item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="ad02d-116">This method launches Windows Media Player with the specified URL set as the current media item.</span></span> <span data-ttu-id="ad02d-117">Se o Player foi fechado anteriormente no modo de capa, ele será aberto usando a capa escolhida pela última vez pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="ad02d-117">If the Player was previously closed in skin mode it will open using the skin last chosen by the user.</span></span> <span data-ttu-id="ad02d-118">Caso contrário, o Player será aberto no modo completo.</span><span class="sxs-lookup"><span data-stu-id="ad02d-118">Otherwise, the Player opens in full mode.</span></span>

<span data-ttu-id="ad02d-119">Se esse método for chamado de um controle PlayerActiveX de mídia do Windows incorporado no modo remoto, seu comportamento será idêntico ao *PlayerApplication*. método **switchToPlayerApplication** .</span><span class="sxs-lookup"><span data-stu-id="ad02d-119">If this method is called from a Windows Media PlayerActiveX control embedded in remote mode, its behavior is identical to the *PlayerApplication*.**switchToPlayerApplication** method.</span></span>

<span data-ttu-id="ad02d-120">**Windows Media Player 10 Mobile:** Não há suporte para esse método.</span><span class="sxs-lookup"><span data-stu-id="ad02d-120">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad02d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad02d-121">Requirements</span></span>



| <span data-ttu-id="ad02d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad02d-122">Requirement</span></span> | <span data-ttu-id="ad02d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ad02d-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad02d-124">Versão</span><span class="sxs-lookup"><span data-stu-id="ad02d-124">Version</span></span><br/> | <span data-ttu-id="ad02d-125">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ad02d-125">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="ad02d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ad02d-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="ad02d-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad02d-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad02d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad02d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad02d-129">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="ad02d-129">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="ad02d-130">**PlayerApplication.switchToPlayerApplication**</span><span class="sxs-lookup"><span data-stu-id="ad02d-130">**PlayerApplication.switchToPlayerApplication**</span></span>](playerapplication-switchtoplayerapplication.md)
</dt> </dl>

 

 





