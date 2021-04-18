---
title: Evento PositionChange do objeto AxWindowsMediaPlayer
description: O evento PositionChange ocorre quando a posição de reprodução atual dentro do item de mídia foi alterada.
ms.assetid: 92d469b9-813a-4148-be68-0fcef2e41491
keywords:
- Evento PositionChange do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- PositionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 552b748121668e71ee4d2ffb54feed441620a1cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781279"
---
# <a name="positionchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="f10fa-104">Evento PositionChange do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="f10fa-104">PositionChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="f10fa-105">O evento PositionChange ocorre quando a posição de reprodução atual dentro do item de mídia foi alterada.</span><span class="sxs-lookup"><span data-stu-id="f10fa-105">The PositionChange event occurs when the current playback position within the media item has been changed.</span></span>

``` syntax
[C#]
private void player_PositionChange(
  object sender,
  _WMPOCXEvents_PositionChangeEvent e
)

[Visual Basic]
Private Sub player_PositionChange(  
  sender As Object,
  e As _WMPOCXEvents_PositionChangeEvent
) Handles player.PositionChange
```

## <a name="event-data"></a><span data-ttu-id="f10fa-106">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="f10fa-106">Event Data</span></span>

<span data-ttu-id="f10fa-107">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ PositionChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="f10fa-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PositionChangeEventHandler**.</span></span> <span data-ttu-id="f10fa-108">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ PositionChangeEvent**, que contém as propriedades a seguir relacionadas a esse evento.</span><span class="sxs-lookup"><span data-stu-id="f10fa-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PositionChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="f10fa-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f10fa-109">Property</span></span>    | <span data-ttu-id="f10fa-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f10fa-110">Description</span></span>                                         |
|-------------|-----------------------------------------------------|
| <span data-ttu-id="f10fa-111">oldPosition</span><span class="sxs-lookup"><span data-stu-id="f10fa-111">oldPosition</span></span> | <span data-ttu-id="f10fa-112">System. DoubleSpecifies a posição antiga.</span><span class="sxs-lookup"><span data-stu-id="f10fa-112">System.DoubleSpecifies the old position.</span></span><br/> |
| <span data-ttu-id="f10fa-113">newPosition</span><span class="sxs-lookup"><span data-stu-id="f10fa-113">newPosition</span></span> | <span data-ttu-id="f10fa-114">System. DoubleSpecifies a nova posição.</span><span class="sxs-lookup"><span data-stu-id="f10fa-114">System.DoubleSpecifies the new position.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f10fa-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f10fa-115">Remarks</span></span>

<span data-ttu-id="f10fa-116">Esse evento não é gerado rotineiramente durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="f10fa-116">This event is not raised routinely during playback.</span></span> <span data-ttu-id="f10fa-117">Isso ocorre apenas quando algo altera ativamente a posição atual do item de mídia em reprodução, como quando o usuário move o identificador de busca ou quando o código é executado que especifica um valor para IWMPControls. **CurrentPosition**.</span><span class="sxs-lookup"><span data-stu-id="f10fa-117">It only occurs when something actively changes the current position of the playing media item, such as when the user moves the seek handle or when code is executed that specifies a value for IWMPControls.**currentPosition**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f10fa-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f10fa-118">Requirements</span></span>



| <span data-ttu-id="f10fa-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f10fa-119">Requirement</span></span> | <span data-ttu-id="f10fa-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f10fa-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f10fa-121">Versão</span><span class="sxs-lookup"><span data-stu-id="f10fa-121">Version</span></span><br/>   | <span data-ttu-id="f10fa-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="f10fa-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="f10fa-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="f10fa-123">Namespace</span></span><br/> | <span data-ttu-id="f10fa-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="f10fa-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="f10fa-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="f10fa-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f10fa-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f10fa-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f10fa-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f10fa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f10fa-128">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f10fa-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f10fa-129">**IWMPControls. currentPosition (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f10fa-129">**IWMPControls.currentPosition (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





