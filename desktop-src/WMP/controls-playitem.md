---
title: Método Controls. playItem
description: O método playItem reproduz o item de mídia especificado. | Método Controls. playItem
ms.assetid: 410e315d-8d5f-4f45-82a7-4249e656c809
keywords:
- método playItem Windows Media Player
- método playItem Windows Media Player, classe Controls
- Classe Controls Windows Media Player, método playItem
topic_type:
- apiref
api_name:
- Controls.playItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9096e378a328f43147a0a94d97034c8e566b611
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783618"
---
# <a name="controlsplayitem-method"></a><span data-ttu-id="0e452-107">Método Controls. playItem</span><span class="sxs-lookup"><span data-stu-id="0e452-107">Controls.playItem method</span></span>

<span data-ttu-id="0e452-108">O método **playItem** reproduz o item de mídia especificado.</span><span class="sxs-lookup"><span data-stu-id="0e452-108">The **playItem** method plays the specified media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e452-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e452-109">Syntax</span></span>


```JScript
Controls.playItem(
  theMediaItem
)
```



## <a name="parameters"></a><span data-ttu-id="0e452-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e452-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e452-111">*theMediaItem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0e452-111">*theMediaItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e452-112">Objeto de **mídia** a ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="0e452-112">**Media** object to be played.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e452-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0e452-113">Return value</span></span>

<span data-ttu-id="0e452-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0e452-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e452-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e452-115">Remarks</span></span>

<span data-ttu-id="0e452-116">O item de mídia será carregado e reproduzido automaticamente, independentemente do valor das *configurações*. Propriedade **AutoStart** .</span><span class="sxs-lookup"><span data-stu-id="0e452-116">The media item will be loaded and played automatically, regardless of the value of the *Settings*.**autoStart** property.</span></span> <span data-ttu-id="0e452-117">Para carregar um item sem reproduzi-lo automaticamente, defina *configurações*. **AutoStart** para false e atribuir um valor ao *Player*. A **URL**, após a qual a **reprodução** pode ser chamada para iniciar a reprodução do item.</span><span class="sxs-lookup"><span data-stu-id="0e452-117">To load an item without playing it automatically, set *Settings*.**autoStart** to false and assign a value to *Player*.**URL**, after which **play** can be called to start playing the item.</span></span>

<span data-ttu-id="0e452-118">Observação</span><span class="sxs-lookup"><span data-stu-id="0e452-118">Note</span></span>

<span data-ttu-id="0e452-119">**playItem** funciona apenas com itens em *currentPlaylist*.</span><span class="sxs-lookup"><span data-stu-id="0e452-119">**playItem** works only with items in *currentPlaylist*.</span></span> <span data-ttu-id="0e452-120">Não há suporte para chamar **playItem** com uma referência a um item de mídia salvo.</span><span class="sxs-lookup"><span data-stu-id="0e452-120">Calling **playItem** with a reference to a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="0e452-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0e452-121">Examples</span></span>

<span data-ttu-id="0e452-122">O exemplo de JScript a seguir usa **playItem** para reproduzir um item de mídia da playlist atual.</span><span class="sxs-lookup"><span data-stu-id="0e452-122">The following JScript example uses **playItem** to play a media item from the current playlist.</span></span> <span data-ttu-id="0e452-123">O item a ser tocado é escolhido com base na sua posição na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="0e452-123">The item to play is chosen based upon its position in the playlist.</span></span> <span data-ttu-id="0e452-124">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="0e452-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
var index = 3

// Retrieve the media item at the fourth position in the current playlist.
var media = Player.currentPlaylist.item(index);

// Play the media item.
Player.controls.playItem(media);

```



## <a name="requirements"></a><span data-ttu-id="0e452-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e452-125">Requirements</span></span>



| <span data-ttu-id="0e452-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e452-126">Requirement</span></span> | <span data-ttu-id="0e452-127">Valor</span><span class="sxs-lookup"><span data-stu-id="0e452-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0e452-128">Versão</span><span class="sxs-lookup"><span data-stu-id="0e452-128">Version</span></span><br/> | <span data-ttu-id="0e452-129">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="0e452-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0e452-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0e452-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="0e452-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e452-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e452-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e452-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e452-133">**Objeto Controls**</span><span class="sxs-lookup"><span data-stu-id="0e452-133">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="0e452-134">**Lista de reprodução. Item**</span><span class="sxs-lookup"><span data-stu-id="0e452-134">**Playlist.item**</span></span>](playlist-item.md)
</dt> </dl>

 

 





