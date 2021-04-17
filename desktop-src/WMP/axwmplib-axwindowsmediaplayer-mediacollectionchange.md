---
title: Evento MediaCollectionChange do objeto AxWindowsMediaPlayer
description: O evento MediaCollectionChange ocorre quando a coleção de mídia é alterada. | Evento MediaCollectionChange do objeto AxWindowsMediaPlayer
ms.assetid: 99a6d512-ed8e-4f1b-856a-22ca8092741d
keywords:
- Evento MediaCollectionChange do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollectionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 720207de3475544074b87c56686d0a47da97785c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813193"
---
# <a name="mediacollectionchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="dbf06-105">Evento MediaCollectionChange do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="dbf06-105">MediaCollectionChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="dbf06-106">O evento MediaCollectionChange ocorre quando a coleção de mídia é alterada.</span><span class="sxs-lookup"><span data-stu-id="dbf06-106">The MediaCollectionChange event occurs when the media collection changes.</span></span>

``` syntax
[C#]
private void player_MediaCollectionChange(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_MediaCollectionChange(
  sender As Object,
  e As System.EventArgs
) Handles player.MediaCollectionChange
```

## <a name="event-data"></a><span data-ttu-id="dbf06-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="dbf06-107">Event Data</span></span>

<span data-ttu-id="dbf06-108">Este evento não contém dados.</span><span class="sxs-lookup"><span data-stu-id="dbf06-108">This event does not contain data.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbf06-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbf06-109">Requirements</span></span>



| <span data-ttu-id="dbf06-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbf06-110">Requirement</span></span> | <span data-ttu-id="dbf06-111">Valor</span><span class="sxs-lookup"><span data-stu-id="dbf06-111">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbf06-112">Versão</span><span class="sxs-lookup"><span data-stu-id="dbf06-112">Version</span></span><br/>   | <span data-ttu-id="dbf06-113">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="dbf06-113">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="dbf06-114">Namespace</span><span class="sxs-lookup"><span data-stu-id="dbf06-114">Namespace</span></span><br/> | <span data-ttu-id="dbf06-115">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="dbf06-115">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="dbf06-116">Assembly</span><span class="sxs-lookup"><span data-stu-id="dbf06-116">Assembly</span></span><br/>  | <dl> <span data-ttu-id="dbf06-117"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="dbf06-117"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbf06-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbf06-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbf06-119">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dbf06-119">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dbf06-120">**AxWindowsMediaPlayer. mediacollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dbf06-120">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dbf06-121">**Interface IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dbf06-121">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





