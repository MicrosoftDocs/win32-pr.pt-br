---
title: Método playlist. appendItem
description: O método appendItem adiciona um item de mídia ao final da lista de reprodução.
ms.assetid: cc956491-7936-49e7-90ca-1f71e03448cd
keywords:
- método appendItem Windows Media Player
- método appendItem Windows Media Player, classe playlist
- Classe playlist Windows Media Player, método appendItem
topic_type:
- apiref
api_name:
- Playlist.appendItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 828799d5b6e71e7ff0e7be4c1e55714f6343be51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105772979"
---
# <a name="playlistappenditem-method"></a><span data-ttu-id="b5c6f-106">Método playlist. appendItem</span><span class="sxs-lookup"><span data-stu-id="b5c6f-106">Playlist.appendItem method</span></span>

<span data-ttu-id="b5c6f-107">O método **appendItem** adiciona um item de mídia ao final da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="b5c6f-107">The **appendItem** method adds a media item to the end of the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5c6f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5c6f-108">Syntax</span></span>


```JScript
Playlist.appendItem(
  item
)
```



## <a name="parameters"></a><span data-ttu-id="b5c6f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5c6f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5c6f-110">*Item* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="b5c6f-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5c6f-111">Objeto de **mídia** a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="b5c6f-111">**Media** object to be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5c6f-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b5c6f-112">Return value</span></span>

<span data-ttu-id="b5c6f-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b5c6f-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5c6f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5c6f-114">Remarks</span></span>

<span data-ttu-id="b5c6f-115">Para usar esse método, é necessário ter acesso completo à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="b5c6f-115">To use this method, full access to the library is required.</span></span> <span data-ttu-id="b5c6f-116">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b5c6f-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b5c6f-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b5c6f-117">Examples</span></span>

<span data-ttu-id="b5c6f-118">O exemplo de JScript a seguir usa a *lista de reprodução*. **appendItem** para adicionar o item de mídia atual à lista de reprodução denominada "trêslist".</span><span class="sxs-lookup"><span data-stu-id="b5c6f-118">The following JScript example uses *Playlist*.**appendItem** to add the current media item to the playlist named "ThreeList".</span></span> <span data-ttu-id="b5c6f-119">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="b5c6f-119">The **Player** object was created with ID="Player".</span></span>


```JScript
// Get the current media item.
var currMedia = Player.currentMedia;

// Get the playlist object by name.
var plThreeList = Player.playlistCollection.getByName("ThreeList").item(0);

// Append the media item to the playlist.
plThreeList.appendItem(currMedia);

```



## <a name="requirements"></a><span data-ttu-id="b5c6f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5c6f-120">Requirements</span></span>



| <span data-ttu-id="b5c6f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5c6f-121">Requirement</span></span> | <span data-ttu-id="b5c6f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b5c6f-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5c6f-123">Versão</span><span class="sxs-lookup"><span data-stu-id="b5c6f-123">Version</span></span><br/> | <span data-ttu-id="b5c6f-124">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="b5c6f-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b5c6f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b5c6f-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="b5c6f-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5c6f-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5c6f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5c6f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5c6f-128">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="b5c6f-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="b5c6f-129">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b5c6f-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="b5c6f-130">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b5c6f-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





