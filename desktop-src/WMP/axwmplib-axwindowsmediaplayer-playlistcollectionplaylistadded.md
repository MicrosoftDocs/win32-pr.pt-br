---
title: Evento PlaylistCollectionPlaylistAdded do objeto AxWindowsMediaPlayer
description: O evento PlaylistCollectionPlaylistAdded ocorre quando uma playlist é adicionada à coleção de playlist. | Evento PlaylistCollectionPlaylistAdded do objeto AxWindowsMediaPlayer
ms.assetid: 13d3bc86-6655-4536-a58f-327eabb2b8f9
keywords:
- Evento PlaylistCollectionPlaylistAdded do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b019e58ae8955f6df894101956e4776c2cd71626
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760896"
---
# <a name="playlistcollectionplaylistadded-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="a89cd-105">Evento PlaylistCollectionPlaylistAdded do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="a89cd-105">PlaylistCollectionPlaylistAdded Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="a89cd-106">O evento PlaylistCollectionPlaylistAdded ocorre quando uma playlist é adicionada à coleção de playlist.</span><span class="sxs-lookup"><span data-stu-id="a89cd-106">The PlaylistCollectionPlaylistAdded event occurs when a playlist is added to the playlist collection.</span></span>

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistAdded(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistAdded(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent
) Handles player.PlaylistCollectionPlaylistAdded
```

## <a name="event-data"></a><span data-ttu-id="a89cd-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="a89cd-107">Event Data</span></span>

<span data-ttu-id="a89cd-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistAddedEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="a89cd-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistAddedEventHandler**.</span></span> <span data-ttu-id="a89cd-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistAddedEvent**, que contém a seguinte propriedade relacionada a este evento.</span><span class="sxs-lookup"><span data-stu-id="a89cd-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistAddedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="a89cd-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="a89cd-110">Property</span></span>             | <span data-ttu-id="a89cd-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="a89cd-111">Description</span></span>                                                                |
|----------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="a89cd-112">**bstrPlaylistName**</span><span class="sxs-lookup"><span data-stu-id="a89cd-112">**bstrPlaylistName**</span></span> | <span data-ttu-id="a89cd-113">System. StringSpecifies o nome da lista de reprodução que foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="a89cd-113">System.StringSpecifies the name of the playlist that was added.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a89cd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a89cd-114">Remarks</span></span>

<span data-ttu-id="a89cd-115">O nome da lista de reprodução que foi adicionado pode ser usado para recuperar a playlist correspondente usando o IWMPPlaylistCollection. método **getByName** .</span><span class="sxs-lookup"><span data-stu-id="a89cd-115">The name of the playlist that was added can be used to retrieve the corresponding playlist by using the IWMPPlaylistCollection.**getByName** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a89cd-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a89cd-116">Requirements</span></span>



| <span data-ttu-id="a89cd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a89cd-117">Requirement</span></span> | <span data-ttu-id="a89cd-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a89cd-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a89cd-119">Versão</span><span class="sxs-lookup"><span data-stu-id="a89cd-119">Version</span></span><br/>   | <span data-ttu-id="a89cd-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="a89cd-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="a89cd-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="a89cd-121">Namespace</span></span><br/> | <span data-ttu-id="a89cd-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="a89cd-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="a89cd-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="a89cd-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a89cd-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a89cd-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a89cd-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="a89cd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a89cd-126">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a89cd-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a89cd-127">**IWMPPlaylistCollection. getByName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a89cd-127">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





