---
title: Evento MediaCollectionMediaAdded do objeto AxWindowsMediaPlayer
description: O evento MediaCollectionMediaAdded ocorre quando um item de mídia é adicionado à biblioteca local. | Evento MediaCollectionMediaAdded do objeto AxWindowsMediaPlayer
ms.assetid: ba1779f6-a212-44f4-b52a-c88e22aebcce
keywords:
- Evento MediaCollectionMediaAdded do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollectionMediaAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbb839fccf9a5048b5647480eca36fcfcaeb904e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811350"
---
# <a name="mediacollectionmediaadded-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="e14b5-105">Evento MediaCollectionMediaAdded do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="e14b5-105">MediaCollectionMediaAdded Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="e14b5-106">O evento MediaCollectionMediaAdded ocorre quando um item de mídia é adicionado à biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="e14b5-106">The MediaCollectionMediaAdded event occurs when a media item is added to the local library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionMediaAdded(
  object sender,
  _WMPOCXEvents_MediaCollectionMediaAddedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionMediaAdded(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionMediaAddedEvent
) Handles player.MediaCollectionMediaAdded
```

## <a name="event-data"></a><span data-ttu-id="e14b5-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="e14b5-107">Event Data</span></span>

<span data-ttu-id="e14b5-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaAddedEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="e14b5-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaAddedEventHandler**.</span></span> <span data-ttu-id="e14b5-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaAddedEvent**, que contém a seguinte propriedade relacionada a este evento.</span><span class="sxs-lookup"><span data-stu-id="e14b5-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaAddedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="e14b5-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="e14b5-110">Property</span></span> | <span data-ttu-id="e14b5-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="e14b5-111">Description</span></span>                                                                                                                  |
|----------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e14b5-112">pMedia</span><span class="sxs-lookup"><span data-stu-id="e14b5-112">pMedia</span></span>   | <span data-ttu-id="e14b5-113">Item de mídia System. ObjectThe adicionado à biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="e14b5-113">System.ObjectThe media item added to the local library.</span></span> <span data-ttu-id="e14b5-114">Você pode convertê-lo em uma interface IWMPMedia para acessá-lo.</span><span class="sxs-lookup"><span data-stu-id="e14b5-114">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e14b5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e14b5-115">Remarks</span></span>

<span data-ttu-id="e14b5-116">Esse evento ocorre apenas para a biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="e14b5-116">This event occurs only for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="e14b5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e14b5-117">Requirements</span></span>



| <span data-ttu-id="e14b5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e14b5-118">Requirement</span></span> | <span data-ttu-id="e14b5-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e14b5-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e14b5-120">Versão</span><span class="sxs-lookup"><span data-stu-id="e14b5-120">Version</span></span><br/>   | <span data-ttu-id="e14b5-121">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="e14b5-121">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="e14b5-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="e14b5-122">Namespace</span></span><br/> | <span data-ttu-id="e14b5-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="e14b5-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="e14b5-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="e14b5-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e14b5-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e14b5-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e14b5-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="e14b5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e14b5-127">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e14b5-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e14b5-128">**AxWindowsMediaPlayer. mediacollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e14b5-128">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e14b5-129">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e14b5-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e14b5-130">**Interface IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e14b5-130">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





