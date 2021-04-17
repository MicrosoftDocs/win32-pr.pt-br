---
title: Método IWMPPlaylistCollection importPlaylist
description: O método importPlaylist adiciona uma lista de reprodução estática à biblioteca. | Método IWMPPlaylistCollection importPlaylist
ms.assetid: 7a64e618-920d-419d-8769-612ab5dff49b
keywords:
- método importPlaylist Windows Media Player
- método importPlaylist Windows Media Player, interface IWMPPlaylistCollection
- Interface IWMPPlaylistCollection Windows Media Player, método importPlaylist
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.importPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3ca727155d6ae859123d427812d93ebaa0b05c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797975"
---
# <a name="iwmpplaylistcollectionimportplaylist-method"></a><span data-ttu-id="e8166-107">Método IWMPPlaylistCollection:: importPlaylist</span><span class="sxs-lookup"><span data-stu-id="e8166-107">IWMPPlaylistCollection::importPlaylist method</span></span>

<span data-ttu-id="e8166-108">O método **importPlaylist** adiciona uma lista de reprodução estática à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e8166-108">The **importPlaylist** method adds a static playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8166-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8166-109">Syntax</span></span>


```CSharp
public IWMPPlaylist importPlaylist(
  IWMPPlaylist pItem
);
```


```VB

Public Function importPlaylist( _
  ByVal pItem As IWMPPlaylist _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.importPlaylist
```





## <a name="parameters"></a><span data-ttu-id="e8166-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8166-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8166-111">*pItem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e8166-111">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8166-112">Uma interface **WMPLib. IWMPPlaylist** para a lista de reprodução que esse método adicionará.</span><span class="sxs-lookup"><span data-stu-id="e8166-112">A **WMPLib.IWMPPlaylist** interface for the playlist that this method will add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8166-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e8166-113">Return value</span></span>

<span data-ttu-id="e8166-114">Uma interface **WMPLib. IWMPPlaylist** para a lista de reprodução adicionada.</span><span class="sxs-lookup"><span data-stu-id="e8166-114">A **WMPLib.IWMPPlaylist** interface for the added playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8166-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8166-115">Remarks</span></span>

<span data-ttu-id="e8166-116">As listas de reprodução que não contêm nenhum item de mídia não podem ser adicionadas à biblioteca usando esse método.</span><span class="sxs-lookup"><span data-stu-id="e8166-116">Playlists that do not contain any media items cannot be added to the library by using this method.</span></span> <span data-ttu-id="e8166-117">Para criar uma lista de reprodução vazia na biblioteca, use o método **newPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="e8166-117">To create an empty playlist in the library, use the **newPlaylist** method.</span></span> <span data-ttu-id="e8166-118">Em seguida, você pode preencher a lista de reprodução resultante com itens de mídia usando **IWMPPlaylist. appendItem** ou **IWMPPlaylist. insertItem**.</span><span class="sxs-lookup"><span data-stu-id="e8166-118">You can then fill the resulting playlist with media items by using **IWMPPlaylist.appendItem** or **IWMPPlaylist.insertItem**.</span></span>

<span data-ttu-id="e8166-119">Se você passar esse método para uma lista de reprodução automática, a consulta será executada uma vez e o resultado será adicionado à biblioteca como uma lista de reprodução estática.</span><span class="sxs-lookup"><span data-stu-id="e8166-119">If you pass this method an auto playlist, the query is executed once and the result is added to the library as a static playlist.</span></span> <span data-ttu-id="e8166-120">Para adicionar uma lista de reprodução automática à biblioteca e preservar seu comportamento automático, use **IWMPMediaCollection. Add**.</span><span class="sxs-lookup"><span data-stu-id="e8166-120">To add an auto playlist to the library and preserve its automatic behavior, use **IWMPMediaCollection.add**.</span></span> <span data-ttu-id="e8166-121">Para obter mais informações, consulte [playlists estáticas e automáticas](static-and-auto-playlists.md).</span><span class="sxs-lookup"><span data-stu-id="e8166-121">For more information, see [Static and Auto Playlists](static-and-auto-playlists.md).</span></span>

<span data-ttu-id="e8166-122">Antes de chamar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e8166-122">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="e8166-123">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e8166-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8166-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8166-124">Requirements</span></span>



| <span data-ttu-id="e8166-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8166-125">Requirement</span></span> | <span data-ttu-id="e8166-126">Valor</span><span class="sxs-lookup"><span data-stu-id="e8166-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8166-127">Versão</span><span class="sxs-lookup"><span data-stu-id="e8166-127">Version</span></span><br/>   | <span data-ttu-id="e8166-128">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e8166-128">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="e8166-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="e8166-129">Namespace</span></span><br/> | <span data-ttu-id="e8166-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e8166-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e8166-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="e8166-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e8166-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e8166-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8166-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8166-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8166-134">**IWMPMediaCollection. Add (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e8166-134">**IWMPMediaCollection.add (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e8166-135">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e8166-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e8166-136">**IWMPPlaylist. appendItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e8166-136">**IWMPPlaylist.appendItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e8166-137">**IWMPPlaylist. insertItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e8166-137">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e8166-138">**Interface IWMPPlaylistCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e8166-138">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e8166-139">**IWMPPlaylistCollection. newPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e8166-139">**IWMPPlaylistCollection.newPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





