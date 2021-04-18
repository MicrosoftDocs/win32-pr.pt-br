---
title: Evento CdromRipMediaError do objeto AxWindowsMediaPlayer
description: O evento CdromRipMediaError ocorre quando um erro ocorre ao copiar uma faixa individual de um CD.
ms.assetid: 542d0184-d893-4b98-903e-339909276fd6
keywords:
- Evento CdromRipMediaError do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- CdromRipMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39b429505996cd5e85bc1e0e2e85c3f47103d244
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760472"
---
# <a name="cdromripmediaerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="3a2f3-104">Evento CdromRipMediaError do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="3a2f3-104">CdromRipMediaError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="3a2f3-105">O evento CdromRipMediaError ocorre quando um erro ocorre ao copiar uma faixa individual de um CD.</span><span class="sxs-lookup"><span data-stu-id="3a2f3-105">The CdromRipMediaError event occurs when an error happens while ripping an individual track from a CD.</span></span>

``` syntax
[C#]
private void player_CdromRipMediaError(
  object sender,
  _WMPOCXEvents_CdromRipMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromRipMediaError( 
  sender As Object,
  e As _WMPOCXEvents_CdromRipMediaErrorEvent
) Handles player.CdromRipMediaError
```

## <a name="event-data"></a><span data-ttu-id="3a2f3-106">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="3a2f3-106">Event Data</span></span>

<span data-ttu-id="3a2f3-107">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromRipMediaErrorEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="3a2f3-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromRipMediaErrorEventHandler**.</span></span> <span data-ttu-id="3a2f3-108">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromRipMediaErrorEvent**, que contém as propriedades a seguir relacionadas a esse evento.</span><span class="sxs-lookup"><span data-stu-id="3a2f3-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromRipMediaErrorEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="3a2f3-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3a2f3-109">Property</span></span>  | <span data-ttu-id="3a2f3-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="3a2f3-110">Description</span></span>                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a2f3-111">pCdromRip</span><span class="sxs-lookup"><span data-stu-id="3a2f3-111">pCdromRip</span></span> | <span data-ttu-id="3a2f3-112">A interface WMPLib. IWMPCdromRipThe que representa a operação de cópia de CDs que gerou o erro.</span><span class="sxs-lookup"><span data-stu-id="3a2f3-112">WMPLib.IWMPCdromRipThe interface that represents the ripping operation that raised the error.</span></span><br/>                |
| <span data-ttu-id="3a2f3-113">pMedia</span><span class="sxs-lookup"><span data-stu-id="3a2f3-113">pMedia</span></span>    | <span data-ttu-id="3a2f3-114">O item de mídia System. ObjectThe que gerou o erro.</span><span class="sxs-lookup"><span data-stu-id="3a2f3-114">System.ObjectThe media item that raised the error.</span></span> <span data-ttu-id="3a2f3-115">Você pode convertê-lo em uma interface IWMPMedia para acessá-lo.</span><span class="sxs-lookup"><span data-stu-id="3a2f3-115">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3a2f3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a2f3-116">Requirements</span></span>



| <span data-ttu-id="3a2f3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a2f3-117">Requirement</span></span> | <span data-ttu-id="3a2f3-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3a2f3-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a2f3-119">Versão</span><span class="sxs-lookup"><span data-stu-id="3a2f3-119">Version</span></span><br/>   | <span data-ttu-id="3a2f3-120">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="3a2f3-120">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="3a2f3-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a2f3-121">Namespace</span></span><br/> | <span data-ttu-id="3a2f3-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="3a2f3-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="3a2f3-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="3a2f3-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3a2f3-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3a2f3-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a2f3-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a2f3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a2f3-126">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3a2f3-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3a2f3-127">**Interface IWMPCdromRip (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3a2f3-127">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3a2f3-128">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3a2f3-128">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





