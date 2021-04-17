---
title: Evento EndOfStream do objeto AxWindowsMediaPlayer
description: O evento EndOfStream é reservado para uso futuro.
ms.assetid: 004172e0-abd4-451c-bd5c-6bf0a9277661
keywords:
- Evento EndOfStream do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- EndOfStream Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74a64eea77af43cd3b33cc7edee2177aee7d15e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762102"
---
# <a name="endofstream-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="f2d9b-104">Evento EndOfStream do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="f2d9b-104">EndOfStream Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="f2d9b-105">O evento EndOfStream é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="f2d9b-105">The EndOfStream event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_EndOfStream(
  object sender,
  _WMPOCXEvents_EndOfStreamEvent e
)

[Visual Basic]
Private Sub player_EndOfStream(  
  sender As Object,  
  e As _WMPOCXEvents_EndOfStreamEvent
) Handles player.EndOfStream
```

## <a name="event-data"></a><span data-ttu-id="f2d9b-106">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="f2d9b-106">Event Data</span></span>

<span data-ttu-id="f2d9b-107">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ EndOfStreamEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="f2d9b-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_EndOfStreamEventHandler**.</span></span> <span data-ttu-id="f2d9b-108">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ EndOfStreamEvent**, que contém a seguinte propriedade relacionada a este evento.</span><span class="sxs-lookup"><span data-stu-id="f2d9b-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_EndOfStreamEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="f2d9b-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f2d9b-109">Property</span></span> | <span data-ttu-id="f2d9b-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2d9b-110">Description</span></span>                           |
|----------|---------------------------------------|
| <span data-ttu-id="f2d9b-111">result</span><span class="sxs-lookup"><span data-stu-id="f2d9b-111">result</span></span>   | <span data-ttu-id="f2d9b-112">System. Int32Not com suporte.</span><span class="sxs-lookup"><span data-stu-id="f2d9b-112">System.Int32Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f2d9b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2d9b-113">Remarks</span></span>

<span data-ttu-id="f2d9b-114">Esse evento é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="f2d9b-114">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2d9b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2d9b-115">Requirements</span></span>



| <span data-ttu-id="f2d9b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2d9b-116">Requirement</span></span> | <span data-ttu-id="f2d9b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f2d9b-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2d9b-118">Versão</span><span class="sxs-lookup"><span data-stu-id="f2d9b-118">Version</span></span><br/>   | <span data-ttu-id="f2d9b-119">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="f2d9b-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="f2d9b-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2d9b-120">Namespace</span></span><br/> | <span data-ttu-id="f2d9b-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="f2d9b-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="f2d9b-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="f2d9b-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f2d9b-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f2d9b-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2d9b-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2d9b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2d9b-125">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f2d9b-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





