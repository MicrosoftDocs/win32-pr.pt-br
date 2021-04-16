---
title: Evento MarkerHit do objeto AxWindowsMediaPlayer
description: O evento MarkerHit ocorre quando um marcador é atingido. | Evento MarkerHit do objeto AxWindowsMediaPlayer
ms.assetid: 247fc22c-18c4-46b6-b42c-4882209a47f4
keywords:
- Evento MarkerHit do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- MarkerHit Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03bad8d9d64b4711937cd984bbd9d335acebfe67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794517"
---
# <a name="markerhit-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="75f7b-105">Evento MarkerHit do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="75f7b-105">MarkerHit Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="75f7b-106">O evento MarkerHit ocorre quando um marcador é atingido.</span><span class="sxs-lookup"><span data-stu-id="75f7b-106">The MarkerHit event occurs when a marker is reached.</span></span>

``` syntax
[C#]
private void player_MarkerHit(
  object sender,
  _WMPOCXEvents_MarkerHitEvent e
)

[Visual Basic]
Private Sub player_MarkerHit(  
  sender As Object,  
  e As _WMPOCXEvents_MarkerHitEvent
) Handles player.MarkerHit
```

## <a name="event-data"></a><span data-ttu-id="75f7b-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="75f7b-107">Event Data</span></span>

<span data-ttu-id="75f7b-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ MarkerHitEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="75f7b-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MarkerHitEventHandler**.</span></span> <span data-ttu-id="75f7b-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ MarkerHitEvent**, que contém a seguinte propriedade relacionada a este evento.</span><span class="sxs-lookup"><span data-stu-id="75f7b-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MarkerHitEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="75f7b-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="75f7b-110">Property</span></span>      | <span data-ttu-id="75f7b-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="75f7b-111">Description</span></span>                                                             |
|---------------|-------------------------------------------------------------------------|
| <span data-ttu-id="75f7b-112">**MarkerNum**</span><span class="sxs-lookup"><span data-stu-id="75f7b-112">**MarkerNum**</span></span> | <span data-ttu-id="75f7b-113">System. Int32Indicates o número do marcador que foi atingido.</span><span class="sxs-lookup"><span data-stu-id="75f7b-113">System.Int32Indicates the number of the marker that was hit.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="75f7b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75f7b-114">Requirements</span></span>



| <span data-ttu-id="75f7b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="75f7b-115">Requirement</span></span> | <span data-ttu-id="75f7b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="75f7b-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75f7b-117">Versão</span><span class="sxs-lookup"><span data-stu-id="75f7b-117">Version</span></span><br/>   | <span data-ttu-id="75f7b-118">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="75f7b-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="75f7b-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="75f7b-119">Namespace</span></span><br/> | <span data-ttu-id="75f7b-120">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="75f7b-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="75f7b-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="75f7b-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="75f7b-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="75f7b-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75f7b-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="75f7b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75f7b-124">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="75f7b-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





