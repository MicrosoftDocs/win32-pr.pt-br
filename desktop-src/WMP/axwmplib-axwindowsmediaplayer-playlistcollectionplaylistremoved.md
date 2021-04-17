---
title: Evento PlaylistCollectionPlaylistRemoved do objeto AxWindowsMediaPlayer
description: O evento PlaylistCollectionPlaylistRemoved ocorre quando uma playlist é removida da coleção de playlist. | Evento PlaylistCollectionPlaylistRemoved do objeto AxWindowsMediaPlayer
ms.assetid: 96935a9e-4c08-42e9-a63f-7b6cda41b243
keywords:
- Evento PlaylistCollectionPlaylistRemoved do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b982ff566380a7aa5bf4d0b1a1219739b52dd35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783628"
---
# <a name="playlistcollectionplaylistremoved-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="9b4b3-105">Evento PlaylistCollectionPlaylistRemoved do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="9b4b3-105">PlaylistCollectionPlaylistRemoved Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="9b4b3-106">O evento PlaylistCollectionPlaylistRemoved ocorre quando uma playlist é removida da coleção de playlist.</span><span class="sxs-lookup"><span data-stu-id="9b4b3-106">The PlaylistCollectionPlaylistRemoved event occurs when a playlist is removed from the playlist collection.</span></span>

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistRemoved(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistRemovedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistRemoved(  
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistRemovedEvent
) Handles player.PlaylistCollectionPlaylistRemoved
```

## <a name="event-data"></a><span data-ttu-id="9b4b3-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="9b4b3-107">Event Data</span></span>

<span data-ttu-id="9b4b3-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistRemovedEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="9b4b3-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistRemovedEventHandler**.</span></span> <span data-ttu-id="9b4b3-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistRemovedEvent**, que contém a seguinte propriedade relacionada a este evento.</span><span class="sxs-lookup"><span data-stu-id="9b4b3-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistRemovedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="9b4b3-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="9b4b3-110">Property</span></span>             | <span data-ttu-id="9b4b3-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b4b3-111">Description</span></span>                                                                  |
|----------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9b4b3-112">**bstrPlaylistName**</span><span class="sxs-lookup"><span data-stu-id="9b4b3-112">**bstrPlaylistName**</span></span> | <span data-ttu-id="9b4b3-113">System. StringSpecifies o nome da lista de reprodução que foi removida.</span><span class="sxs-lookup"><span data-stu-id="9b4b3-113">System.StringSpecifies the name of the playlist that was removed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9b4b3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b4b3-114">Requirements</span></span>



| <span data-ttu-id="9b4b3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b4b3-115">Requirement</span></span> | <span data-ttu-id="9b4b3-116">Valor</span><span class="sxs-lookup"><span data-stu-id="9b4b3-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b4b3-117">Versão</span><span class="sxs-lookup"><span data-stu-id="9b4b3-117">Version</span></span><br/>   | <span data-ttu-id="9b4b3-118">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="9b4b3-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="9b4b3-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="9b4b3-119">Namespace</span></span><br/> | <span data-ttu-id="9b4b3-120">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="9b4b3-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="9b4b3-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="9b4b3-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9b4b3-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9b4b3-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b4b3-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b4b3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b4b3-124">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9b4b3-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9b4b3-125">**IWMPPlaylistCollection. getByName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9b4b3-125">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





