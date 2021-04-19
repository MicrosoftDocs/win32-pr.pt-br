---
title: Evento MouseUp do objeto AxWindowsMediaPlayer
description: O evento MouseUp ocorre quando o usuário libera um botão do mouse. | Evento MouseUp do objeto AxWindowsMediaPlayer
ms.assetid: 26bb6e82-d744-4770-b4de-07c9f52b76ec
keywords:
- Evento MouseUp do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- MouseUp Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2bf9c209b4fa263eb0a6cbcba2a32b0b1c46fa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800162"
---
# <a name="mouseup-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="4f2a1-105">Evento MouseUp do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="4f2a1-105">MouseUp Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="4f2a1-106">O evento MouseUp ocorre quando o usuário libera um botão do mouse.</span><span class="sxs-lookup"><span data-stu-id="4f2a1-106">The MouseUp event occurs when the user releases a mouse button.</span></span>

``` syntax
[C#]
private void player_MouseUpEvent(
  object sender,
  _WMPOCXEvents_MouseUpEvent e
)

[Visual Basic]
Private Sub player_MouseUpEvent(  
  sender As Object,
  e As _WMPOCXEvents_MouseUpEvent
) Handles player.MouseUpEvent
```

## <a name="event-data"></a><span data-ttu-id="4f2a1-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="4f2a1-107">Event Data</span></span>

<span data-ttu-id="4f2a1-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ MouseUpEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="4f2a1-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MouseUpEventHandler**.</span></span> <span data-ttu-id="4f2a1-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ MouseUpEvent**, que contém as propriedades a seguir relacionadas a esse evento.</span><span class="sxs-lookup"><span data-stu-id="4f2a1-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MouseUpEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="4f2a1-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4f2a1-110">Property</span></span>    | <span data-ttu-id="4f2a1-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="4f2a1-111">Description</span></span>                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f2a1-112">Nnovo</span><span class="sxs-lookup"><span data-stu-id="4f2a1-112">nButton</span></span>     | <span data-ttu-id="4f2a1-113">O campo do sistema. Int16a com bits correspondente ao botão esquerdo (bit 0), botão direito (bit 1) e botão do meio (bit 2).</span><span class="sxs-lookup"><span data-stu-id="4f2a1-113">System.Int16A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="4f2a1-114">Esses bits correspondem aos valores 1, 2 e 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="4f2a1-114">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="4f2a1-115">Apenas um dos bits é definido, indicando o botão que causou o evento.</span><span class="sxs-lookup"><span data-stu-id="4f2a1-115">Only one of the bits is set, indicating the button that caused the event.</span></span><br/>                                                |
| <span data-ttu-id="4f2a1-116">nShiftState</span><span class="sxs-lookup"><span data-stu-id="4f2a1-116">nShiftState</span></span> | <span data-ttu-id="4f2a1-117">O campo do sistema. Int16a com os bits menos significativos correspondentes à tecla SHIFT (bit 0), a tecla CTRL (bit 1) e a tecla ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="4f2a1-117">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="4f2a1-118">Esses bits correspondem aos valores 1, 2 e 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="4f2a1-118">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="4f2a1-119">Alguns, todos ou nenhum dos bits podem ser definidos, indicando que algumas, todas ou nenhuma das chaves são pressionadas.</span><span class="sxs-lookup"><span data-stu-id="4f2a1-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |
| <span data-ttu-id="4f2a1-120">Efeito</span><span class="sxs-lookup"><span data-stu-id="4f2a1-120">fX</span></span>          | <span data-ttu-id="4f2a1-121">System. Int32The x-coordenada do ponteiro do mouse em relação ao canto superior esquerdo do controle.</span><span class="sxs-lookup"><span data-stu-id="4f2a1-121">System.Int32The x-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |
| <span data-ttu-id="4f2a1-122">SAR</span><span class="sxs-lookup"><span data-stu-id="4f2a1-122">fY</span></span>          | <span data-ttu-id="4f2a1-123">System. Int32The y-coordenada do ponteiro do mouse em relação ao canto superior esquerdo do controle.</span><span class="sxs-lookup"><span data-stu-id="4f2a1-123">System.Int32The y-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="4f2a1-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f2a1-124">Requirements</span></span>



| <span data-ttu-id="4f2a1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f2a1-125">Requirement</span></span> | <span data-ttu-id="4f2a1-126">Valor</span><span class="sxs-lookup"><span data-stu-id="4f2a1-126">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f2a1-127">Versão</span><span class="sxs-lookup"><span data-stu-id="4f2a1-127">Version</span></span><br/>   | <span data-ttu-id="4f2a1-128">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="4f2a1-128">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="4f2a1-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="4f2a1-129">Namespace</span></span><br/> | <span data-ttu-id="4f2a1-130">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="4f2a1-130">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="4f2a1-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="4f2a1-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4f2a1-132"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4f2a1-132"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f2a1-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f2a1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f2a1-134">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4f2a1-134">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





