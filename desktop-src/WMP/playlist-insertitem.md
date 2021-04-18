---
title: Método playlist. insertItem
description: O método insertItem insere um item de mídia na lista de reprodução no local especificado.
ms.assetid: c186abc4-0a15-49d2-bbc4-5660e8cc0a4b
keywords:
- método insertItem Windows Media Player
- método insertItem Windows Media Player, classe playlist
- Classe playlist Windows Media Player, método insertItem
topic_type:
- apiref
api_name:
- Playlist.insertItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a456b7a359d59958ce7693cc48c16eabba435621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813649"
---
# <a name="playlistinsertitem-method"></a><span data-ttu-id="0e675-106">Método playlist. insertItem</span><span class="sxs-lookup"><span data-stu-id="0e675-106">Playlist.insertItem method</span></span>

<span data-ttu-id="0e675-107">O método **insertItem** insere um item de mídia na lista de reprodução no local especificado.</span><span class="sxs-lookup"><span data-stu-id="0e675-107">The **insertItem** method inserts a media item into the playlist at the specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e675-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e675-108">Syntax</span></span>


```JScript
Playlist.insertItem(
  index,
  item
)
```



## <a name="parameters"></a><span data-ttu-id="0e675-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e675-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e675-110">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="0e675-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e675-111">**Número** (**longo**) que contém o índice no qual adicionar o item.</span><span class="sxs-lookup"><span data-stu-id="0e675-111">**Number** (**long**) containing the index at which to add the item.</span></span>

</dd> <dt>

<span data-ttu-id="0e675-112">*Item* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="0e675-112">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e675-113">Objeto de **mídia** a ser inserido.</span><span class="sxs-lookup"><span data-stu-id="0e675-113">**Media** object to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e675-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0e675-114">Return value</span></span>

<span data-ttu-id="0e675-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0e675-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e675-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e675-116">Remarks</span></span>

<span data-ttu-id="0e675-117">Todos os itens após o item inserido terão seus números de índice aumentados em um.</span><span class="sxs-lookup"><span data-stu-id="0e675-117">All items after the inserted item will have their index numbers increased by one.</span></span>

<span data-ttu-id="0e675-118">Para usar esse método, é necessário ter acesso completo à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="0e675-118">To use this method, full access to the library is required.</span></span> <span data-ttu-id="0e675-119">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="0e675-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e675-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e675-120">Requirements</span></span>



| <span data-ttu-id="0e675-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e675-121">Requirement</span></span> | <span data-ttu-id="0e675-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0e675-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0e675-123">Versão</span><span class="sxs-lookup"><span data-stu-id="0e675-123">Version</span></span><br/> | <span data-ttu-id="0e675-124">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="0e675-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0e675-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0e675-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="0e675-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e675-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e675-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e675-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e675-128">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="0e675-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="0e675-129">**Lista de reprodução. Item**</span><span class="sxs-lookup"><span data-stu-id="0e675-129">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="0e675-130">**Playlist. removeItem**</span><span class="sxs-lookup"><span data-stu-id="0e675-130">**Playlist.removeItem**</span></span>](playlist-removeitem.md)
</dt> <dt>

[<span data-ttu-id="0e675-131">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="0e675-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="0e675-132">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="0e675-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





