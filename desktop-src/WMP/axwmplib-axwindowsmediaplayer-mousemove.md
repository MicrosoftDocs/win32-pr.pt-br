---
title: Evento MouseMove do objeto AxWindowsMediaPlayer
description: O evento MouseMove ocorre quando o ponteiro do mouse é movido. | Evento MouseMove do objeto AxWindowsMediaPlayer
ms.assetid: abf20c86-3bae-4677-8901-0af030a53286
keywords:
- Evento MouseMove do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- MouseMove Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c623bf60f2951b1a82e59a7d63056bcf8a0b5da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794514"
---
# <a name="mousemove-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="63575-105">Evento MouseMove do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="63575-105">MouseMove Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="63575-106">O evento MouseMove ocorre quando o ponteiro do mouse é movido.</span><span class="sxs-lookup"><span data-stu-id="63575-106">The MouseMove event occurs when the mouse pointer is moved.</span></span>

``` syntax
[C#]
private void player_MouseMoveEvent(
  object sender,
  _WMPOCXEvents_MouseMoveEvent e
)

[Visual Basic]
Private Sub player_MouseMoveEvent(
  sender As Object,
  e As _WMPOCXEvents_MouseMoveEvent
) Handles player.MouseMoveEvent
```

## <a name="event-data"></a><span data-ttu-id="63575-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="63575-107">Event Data</span></span>

<span data-ttu-id="63575-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ MouseMoveEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="63575-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MouseMoveEventHandler**.</span></span> <span data-ttu-id="63575-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ MouseMoveEvent**, que contém as propriedades a seguir relacionadas a esse evento.</span><span class="sxs-lookup"><span data-stu-id="63575-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MouseMoveEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="63575-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="63575-110">Property</span></span>    | <span data-ttu-id="63575-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="63575-111">Description</span></span>                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63575-112">Nnovo</span><span class="sxs-lookup"><span data-stu-id="63575-112">nButton</span></span>     | <span data-ttu-id="63575-113">O campo do sistema. Int16a com bits correspondente ao botão esquerdo (bit 0), botão direito (bit 1) e botão do meio (bit 2).</span><span class="sxs-lookup"><span data-stu-id="63575-113">System.Int16A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="63575-114">Esses bits correspondem aos valores 1, 2 e 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="63575-114">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="63575-115">Apenas um dos bits é definido, indicando o botão que causou o evento.</span><span class="sxs-lookup"><span data-stu-id="63575-115">Only one of the bits is set, indicating the button that caused the event.</span></span><br/>                                                |
| <span data-ttu-id="63575-116">nShiftState</span><span class="sxs-lookup"><span data-stu-id="63575-116">nShiftState</span></span> | <span data-ttu-id="63575-117">O campo do sistema. Int16a com os bits menos significativos correspondentes à tecla SHIFT (bit 0), a tecla CTRL (bit 1) e a tecla ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="63575-117">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="63575-118">Esses bits correspondem aos valores 1, 2 e 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="63575-118">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="63575-119">Alguns, todos ou nenhum dos bits podem ser definidos, indicando que algumas, todas ou nenhuma das chaves são pressionadas.</span><span class="sxs-lookup"><span data-stu-id="63575-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |
| <span data-ttu-id="63575-120">Efeito</span><span class="sxs-lookup"><span data-stu-id="63575-120">fX</span></span>          | <span data-ttu-id="63575-121">System. Int32The x-coordenada do ponteiro do mouse em relação ao canto superior esquerdo do controle.</span><span class="sxs-lookup"><span data-stu-id="63575-121">System.Int32The x-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |
| <span data-ttu-id="63575-122">SAR</span><span class="sxs-lookup"><span data-stu-id="63575-122">fY</span></span>          | <span data-ttu-id="63575-123">System. Int32The y-coordenada do ponteiro do mouse em relação ao canto superior esquerdo do controle.</span><span class="sxs-lookup"><span data-stu-id="63575-123">System.Int32The y-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="63575-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63575-124">Requirements</span></span>



| <span data-ttu-id="63575-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="63575-125">Requirement</span></span> | <span data-ttu-id="63575-126">Valor</span><span class="sxs-lookup"><span data-stu-id="63575-126">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63575-127">Versão</span><span class="sxs-lookup"><span data-stu-id="63575-127">Version</span></span><br/>   | <span data-ttu-id="63575-128">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="63575-128">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="63575-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="63575-129">Namespace</span></span><br/> | <span data-ttu-id="63575-130">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="63575-130">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="63575-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="63575-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="63575-132"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="63575-132"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63575-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="63575-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63575-134">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="63575-134">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





