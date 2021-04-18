---
title: Evento PlaylistCollectionPlaylistSetAsDeleted do objeto AxWindowsMediaPlayer
description: O evento PlaylistCollectionPlaylistSetAsDeleted é reservado para uso futuro.
ms.assetid: 6c0a4d2c-e965-4a88-acd4-2a2a12265e36
keywords:
- Evento PlaylistCollectionPlaylistSetAsDeleted do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistSetAsDeleted Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf432ede40298abed98cdf0c5b02b0a192f7b3a9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810581"
---
# <a name="playlistcollectionplaylistsetasdeleted-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="4e18a-104">Evento PlaylistCollectionPlaylistSetAsDeleted do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="4e18a-104">PlaylistCollectionPlaylistSetAsDeleted Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="4e18a-105">O evento PlaylistCollectionPlaylistSetAsDeleted é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="4e18a-105">The PlaylistCollectionPlaylistSetAsDeleted event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistSetAsDeleted(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistSetAsDeletedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistSetAsDeleted(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistSetAsDeletedEvent
) Handles player.PlaylistCollectionPlaylistSetAsDeleted
```

## <a name="event-data"></a><span data-ttu-id="4e18a-106">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="4e18a-106">Event Data</span></span>

<span data-ttu-id="4e18a-107">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistSetAsDeletedEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="4e18a-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistSetAsDeletedEventHandler**.</span></span> <span data-ttu-id="4e18a-108">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistSetAsDeletedEvent**, que contém as propriedades a seguir relacionadas a esse evento.</span><span class="sxs-lookup"><span data-stu-id="4e18a-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistSetAsDeletedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="4e18a-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4e18a-109">Property</span></span>         | <span data-ttu-id="4e18a-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e18a-110">Description</span></span>                                 |
|------------------|---------------------------------------------|
| <span data-ttu-id="4e18a-111">bstrPlaylistName</span><span class="sxs-lookup"><span data-stu-id="4e18a-111">bstrPlaylistName</span></span> | <span data-ttu-id="4e18a-112">**System. String** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="4e18a-112">**System.String** Not supported.</span></span><br/>  |
| <span data-ttu-id="4e18a-113">varfIsDeleted</span><span class="sxs-lookup"><span data-stu-id="4e18a-113">varfIsDeleted</span></span>    | <span data-ttu-id="4e18a-114">**System. Boolean** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="4e18a-114">**System.Boolean** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4e18a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e18a-115">Remarks</span></span>

<span data-ttu-id="4e18a-116">Esse evento é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="4e18a-116">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e18a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e18a-117">Requirements</span></span>



| <span data-ttu-id="4e18a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e18a-118">Requirement</span></span> | <span data-ttu-id="4e18a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="4e18a-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e18a-120">Versão</span><span class="sxs-lookup"><span data-stu-id="4e18a-120">Version</span></span><br/>   | <span data-ttu-id="4e18a-121">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="4e18a-121">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="4e18a-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="4e18a-122">Namespace</span></span><br/> | <span data-ttu-id="4e18a-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="4e18a-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="4e18a-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="4e18a-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4e18a-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4e18a-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e18a-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e18a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e18a-127">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4e18a-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





