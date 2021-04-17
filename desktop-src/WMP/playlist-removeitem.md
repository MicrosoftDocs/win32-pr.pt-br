---
title: Método playlist. removeItem
description: O método removeItem remove o item especificado da lista de reprodução.
ms.assetid: 294ba4fb-967b-4a03-b0c5-6e9c15db3bff
keywords:
- método removeItem Windows Media Player
- método removeItem Windows Media Player, classe playlist
- Classe playlist Windows Media Player, método removeItem
topic_type:
- apiref
api_name:
- Playlist.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de03333e2373744f9e9197be8ed8582997c557d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782476"
---
# <a name="playlistremoveitem-method"></a><span data-ttu-id="a2ea9-106">Método playlist. removeItem</span><span class="sxs-lookup"><span data-stu-id="a2ea9-106">Playlist.removeItem method</span></span>

<span data-ttu-id="a2ea9-107">O método **RemoveItem** remove o item especificado da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="a2ea9-107">The **removeItem** method removes the specified item from the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2ea9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2ea9-108">Syntax</span></span>


```JScript
Playlist.removeItem(
  item
)
```



## <a name="parameters"></a><span data-ttu-id="a2ea9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2ea9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2ea9-110">*Item* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="a2ea9-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ea9-111">Objeto de **mídia** a ser removido.</span><span class="sxs-lookup"><span data-stu-id="a2ea9-111">**Media** object to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2ea9-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a2ea9-112">Return value</span></span>

<span data-ttu-id="a2ea9-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a2ea9-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2ea9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2ea9-114">Remarks</span></span>

<span data-ttu-id="a2ea9-115">Se o item removido for a faixa em execução no momento (*Player*.**currentMedia**), a reprodução é interrompida e o próximo item na playlist se torna o atual.</span><span class="sxs-lookup"><span data-stu-id="a2ea9-115">If the item removed is the currently playing track (*Player*.**currentMedia**), playback stops and the next item in the playlist becomes the current one.</span></span> <span data-ttu-id="a2ea9-116">Se não houver nenhum item seguinte, o item anterior será usado, ou se não houver outros itens, então o *Player*. **currentMedia** é definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a2ea9-116">If there is no next item, the previous item is used, or if there are no other items, then *Player*.**currentMedia** is set to **NULL**.</span></span>

<span data-ttu-id="a2ea9-117">Para usar esse método, é necessário ter acesso completo à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="a2ea9-117">To use this method, full access to the library is required.</span></span> <span data-ttu-id="a2ea9-118">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a2ea9-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2ea9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2ea9-119">Requirements</span></span>



| <span data-ttu-id="a2ea9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2ea9-120">Requirement</span></span> | <span data-ttu-id="a2ea9-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a2ea9-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a2ea9-122">Versão</span><span class="sxs-lookup"><span data-stu-id="a2ea9-122">Version</span></span><br/> | <span data-ttu-id="a2ea9-123">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="a2ea9-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a2ea9-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a2ea9-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="a2ea9-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2ea9-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2ea9-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2ea9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2ea9-127">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="a2ea9-127">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="a2ea9-128">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="a2ea9-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="a2ea9-129">**Playlist. insertItem**</span><span class="sxs-lookup"><span data-stu-id="a2ea9-129">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="a2ea9-130">**Lista de reprodução. Item**</span><span class="sxs-lookup"><span data-stu-id="a2ea9-130">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="a2ea9-131">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="a2ea9-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="a2ea9-132">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="a2ea9-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





