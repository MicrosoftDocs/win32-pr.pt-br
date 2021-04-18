---
title: Método playlist. moveItem
description: O método moveItem altera o local de um item na lista de reprodução.
ms.assetid: 82a8de86-4419-48a7-89f8-f7b9084b51d4
keywords:
- método moveItem Windows Media Player
- método moveItem Windows Media Player, classe playlist
- Classe playlist Windows Media Player, método moveItem
topic_type:
- apiref
api_name:
- Playlist.moveItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e2e48b2987af4becd8c07357ff2eecf137f31d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812180"
---
# <a name="playlistmoveitem-method"></a><span data-ttu-id="2068b-106">Método playlist. moveItem</span><span class="sxs-lookup"><span data-stu-id="2068b-106">Playlist.moveItem method</span></span>

<span data-ttu-id="2068b-107">O método **moveItem** altera o local de um item na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="2068b-107">The **moveItem** method changes the location of an item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="2068b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2068b-108">Syntax</span></span>


```JScript
Playlist.moveItem(
  oldIndex,
  newIndex
)
```



## <a name="parameters"></a><span data-ttu-id="2068b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2068b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2068b-110">*oldIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2068b-110">*oldIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2068b-111">**Número** (**longo**) que contém o índice antigo.</span><span class="sxs-lookup"><span data-stu-id="2068b-111">**Number** (**long**) containing the old index.</span></span>

</dd> <dt>

<span data-ttu-id="2068b-112">*NewIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2068b-112">*newIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2068b-113">**Número** (**longo**) que contém o novo índice.</span><span class="sxs-lookup"><span data-stu-id="2068b-113">**Number** (**long**) containing the new index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2068b-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2068b-114">Return value</span></span>

<span data-ttu-id="2068b-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2068b-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2068b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2068b-116">Remarks</span></span>

<span data-ttu-id="2068b-117">As listas de reprodução armazenadas na biblioteca podem ser alteradas fora do seu controle.</span><span class="sxs-lookup"><span data-stu-id="2068b-117">Playlists stored in the library can change outside your control.</span></span> <span data-ttu-id="2068b-118">Certifique-se de monitorar e lidar com todos os eventos relacionados à playlist apropriados para que a ordem dos itens na lista de reprodução não mude inesperadamente.</span><span class="sxs-lookup"><span data-stu-id="2068b-118">Be sure to monitor and handle all appropriate playlist-related events so that the order of items in the playlist does not change unexpectedly.</span></span>

<span data-ttu-id="2068b-119">Para usar esse método, é necessário ter acesso completo à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2068b-119">To use this method, full access to the library is required.</span></span> <span data-ttu-id="2068b-120">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2068b-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2068b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2068b-121">Requirements</span></span>



| <span data-ttu-id="2068b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2068b-122">Requirement</span></span> | <span data-ttu-id="2068b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="2068b-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2068b-124">Versão</span><span class="sxs-lookup"><span data-stu-id="2068b-124">Version</span></span><br/> | <span data-ttu-id="2068b-125">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="2068b-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2068b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2068b-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="2068b-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2068b-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2068b-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2068b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2068b-129">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="2068b-129">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="2068b-130">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="2068b-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="2068b-131">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="2068b-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





