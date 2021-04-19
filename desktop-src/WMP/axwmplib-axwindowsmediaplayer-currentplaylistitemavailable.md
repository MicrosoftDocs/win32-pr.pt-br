---
title: Evento CurrentPlaylistItemAvailable do objeto AxWindowsMediaPlayer
description: O evento CurrentPlaylistItemAvailable ocorre quando a playlist atual fica disponível. | Evento CurrentPlaylistItemAvailable do objeto AxWindowsMediaPlayer
ms.assetid: 101807c9-b00f-4351-a9a3-5413a52496f4
keywords:
- Evento CurrentPlaylistItemAvailable do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- CurrentPlaylistItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be9362a569fe8296284d92204628627c74ae3b44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810584"
---
# <a name="currentplaylistitemavailable-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="ce9ac-105">Evento CurrentPlaylistItemAvailable do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="ce9ac-105">CurrentPlaylistItemAvailable Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="ce9ac-106">O evento CurrentPlaylistItemAvailable ocorre quando a playlist atual fica disponível.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-106">The CurrentPlaylistItemAvailable event occurs when the current playlist becomes available.</span></span>

``` syntax
[C#]
private void player_CurrentPlaylistItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentPlaylistItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentPlaylistItemAvailable(  
  sender As Object,
  e As _WMPOCXEvents_CurrentPlaylistItemAvailableEvent
) Handles player.CurrentPlaylistItemAvailable
```

## <a name="event-data"></a><span data-ttu-id="ce9ac-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="ce9ac-107">Event Data</span></span>

<span data-ttu-id="ce9ac-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentPlaylistItemAvailableEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistItemAvailableEventHandler**.</span></span> <span data-ttu-id="ce9ac-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentPlaylistItemAvailableEvent**, que contém a seguinte propriedade relacionada a este evento.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistItemAvailableEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="ce9ac-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ce9ac-110">Property</span></span>         | <span data-ttu-id="ce9ac-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce9ac-111">Description</span></span>                                                    |
|------------------|----------------------------------------------------------------|
| <span data-ttu-id="ce9ac-112">**bstrItemName**</span><span class="sxs-lookup"><span data-stu-id="ce9ac-112">**bstrItemName**</span></span> | <span data-ttu-id="ce9ac-113">System. StringThe nome do item da playlist atual.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-113">System.StringThe name of the current playlist item.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ce9ac-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce9ac-114">Remarks</span></span>

<span data-ttu-id="ce9ac-115">O nome da lista de reprodução atual pode ser usado para recuperar a interface **IWMPPlaylist** correspondente da interface IWMPPlaylistArray que é retornada do método IWMPPlaylistCollection. getByName.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-115">The name of the current playlist can be used to retrieve the corresponding **IWMPPlaylist** interface from the IWMPPlaylistArray interface that is returned from the IWMPPlaylistCollection.getByName method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce9ac-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce9ac-116">Requirements</span></span>



| <span data-ttu-id="ce9ac-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce9ac-117">Requirement</span></span> | <span data-ttu-id="ce9ac-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ce9ac-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce9ac-119">Versão</span><span class="sxs-lookup"><span data-stu-id="ce9ac-119">Version</span></span><br/>   | <span data-ttu-id="ce9ac-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="ce9ac-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="ce9ac-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="ce9ac-121">Namespace</span></span><br/> | <span data-ttu-id="ce9ac-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="ce9ac-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="ce9ac-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="ce9ac-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ce9ac-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ce9ac-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce9ac-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce9ac-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce9ac-126">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ce9ac-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ce9ac-127">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ce9ac-127">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ce9ac-128">**Interface IWMPPlaylistArray (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ce9ac-128">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ce9ac-129">**IWMPPlaylistCollection. getByName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ce9ac-129">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





