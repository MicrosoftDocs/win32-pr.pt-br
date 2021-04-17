---
title: Evento MediaError do objeto AxWindowsMediaPlayer
description: O evento MediaError ocorre quando um objeto de mídia tem uma condição de erro.
ms.assetid: a1fb3422-85c4-4856-951a-332517599984
keywords:
- Evento MediaError do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- MediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 874b9297846a8f25f25c68545df234aa1be70594
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759744"
---
# <a name="mediaerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="fa0f7-104">Evento MediaError do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="fa0f7-104">MediaError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="fa0f7-105">O evento MediaError ocorre quando um objeto de mídia tem uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="fa0f7-105">The MediaError event occurs when a media object has an error condition.</span></span>

``` syntax
[C#]
private void player_MediaError(
  object sender,
  _WMPOCXEvents_MediaErrorEvent e
)

[Visual Basic]
Private Sub player_MediaError(
  sender As Object,
  e As _WMPOCXEvents_MediaErrorEvent
) Handles player.MediaError
```

## <a name="event-data"></a><span data-ttu-id="fa0f7-106">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="fa0f7-106">Event Data</span></span>

<span data-ttu-id="fa0f7-107">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaErrorEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="fa0f7-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaErrorEventHandler**.</span></span> <span data-ttu-id="fa0f7-108">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaErrorEvent**, que contém a seguinte propriedade relacionada a este evento.</span><span class="sxs-lookup"><span data-stu-id="fa0f7-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaErrorEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="fa0f7-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="fa0f7-109">Property</span></span>     | <span data-ttu-id="fa0f7-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa0f7-110">Description</span></span>                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa0f7-111">pMediaObject</span><span class="sxs-lookup"><span data-stu-id="fa0f7-111">pMediaObject</span></span> | <span data-ttu-id="fa0f7-112">System. Objectobject que tem uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="fa0f7-112">System.ObjectObject that has an error condition.</span></span> <span data-ttu-id="fa0f7-113">Você pode convertê-lo em uma interface IWMPMedia para acessá-lo.</span><span class="sxs-lookup"><span data-stu-id="fa0f7-113">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fa0f7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa0f7-114">Requirements</span></span>



| <span data-ttu-id="fa0f7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa0f7-115">Requirement</span></span> | <span data-ttu-id="fa0f7-116">Valor</span><span class="sxs-lookup"><span data-stu-id="fa0f7-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa0f7-117">Versão</span><span class="sxs-lookup"><span data-stu-id="fa0f7-117">Version</span></span><br/>   | <span data-ttu-id="fa0f7-118">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="fa0f7-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="fa0f7-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="fa0f7-119">Namespace</span></span><br/> | <span data-ttu-id="fa0f7-120">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="fa0f7-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="fa0f7-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="fa0f7-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fa0f7-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="fa0f7-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa0f7-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa0f7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa0f7-124">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="fa0f7-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fa0f7-125">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="fa0f7-125">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





