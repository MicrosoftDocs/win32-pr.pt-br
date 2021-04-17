---
title: Evento MediaCollectionMediaRemoved do objeto AxWindowsMediaPlayer
description: O evento MediaCollectionMediaRemoved ocorre quando um item de mídia é removido da biblioteca local. | Evento MediaCollectionMediaRemoved do objeto AxWindowsMediaPlayer
ms.assetid: 66dae2be-2a71-4d53-b2e2-f106426d4eea
keywords:
- Evento MediaCollectionMediaRemoved do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollectionMediaRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea15ff63fb913cd399a152913a27ffda1090d9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780032"
---
# <a name="mediacollectionmediaremoved-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="fb633-105">Evento MediaCollectionMediaRemoved do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="fb633-105">MediaCollectionMediaRemoved Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="fb633-106">O evento MediaCollectionMediaRemoved ocorre quando um item de mídia é removido da biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="fb633-106">The MediaCollectionMediaRemoved event occurs when a media item is removed from the local library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionMediaRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionMediaRemovedEvent e
)
        
[Visual Basic]
Private Sub player_MediaCollectionMediaRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionMediaRemovedEvent
) Handles player.MediaCollectionMediaRemoved
```

## <a name="event-data"></a><span data-ttu-id="fb633-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="fb633-107">Event Data</span></span>

<span data-ttu-id="fb633-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaRemovedEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="fb633-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaRemovedEventHandler**.</span></span> <span data-ttu-id="fb633-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaRemovedEvent**, que contém a seguinte propriedade relacionada a este evento.</span><span class="sxs-lookup"><span data-stu-id="fb633-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaRemovedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="fb633-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="fb633-110">Property</span></span> | <span data-ttu-id="fb633-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb633-111">Description</span></span>                                                                                                                      |
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb633-112">pMedia</span><span class="sxs-lookup"><span data-stu-id="fb633-112">pMedia</span></span>   | <span data-ttu-id="fb633-113">Item de mídia System. ObjectThe removido da biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="fb633-113">System.ObjectThe media item removed from the local library.</span></span> <span data-ttu-id="fb633-114">Você pode convertê-lo em uma interface IWMPMedia para acessá-lo.</span><span class="sxs-lookup"><span data-stu-id="fb633-114">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fb633-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb633-115">Remarks</span></span>

<span data-ttu-id="fb633-116">Esse evento ocorre apenas para a biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="fb633-116">This event occurs only for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb633-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb633-117">Requirements</span></span>



| <span data-ttu-id="fb633-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb633-118">Requirement</span></span> | <span data-ttu-id="fb633-119">Valor</span><span class="sxs-lookup"><span data-stu-id="fb633-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb633-120">Versão</span><span class="sxs-lookup"><span data-stu-id="fb633-120">Version</span></span><br/>   | <span data-ttu-id="fb633-121">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="fb633-121">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="fb633-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="fb633-122">Namespace</span></span><br/> | <span data-ttu-id="fb633-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="fb633-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="fb633-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="fb633-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fb633-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="fb633-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb633-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb633-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb633-127">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="fb633-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fb633-128">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="fb633-128">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





