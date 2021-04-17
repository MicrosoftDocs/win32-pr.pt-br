---
title: Evento MouseDown do objeto AxWindowsMediaPlayer
description: O evento MouseDown ocorre quando o usuário pressiona um botão do mouse. | Evento MouseDown do objeto AxWindowsMediaPlayer
ms.assetid: 3dfbd034-67d4-4b7e-88d8-a77d301c5df7
keywords:
- Evento MouseDown do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- MouseDown Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0779df27f406691903a0362c9eb3a1df993f595f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813191"
---
# <a name="mousedown-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="893a2-105">Evento MouseDown do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="893a2-105">MouseDown Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="893a2-106">O evento MouseDown ocorre quando o usuário pressiona um botão do mouse.</span><span class="sxs-lookup"><span data-stu-id="893a2-106">The MouseDown event occurs when the user presses a mouse button.</span></span>

``` syntax
[C#]
private void player_MouseDownEvent(
  object sender,
  _WMPOCXEvents_MouseDownEvent e
)

[Visual Basic]
Private Sub player_MouseDownEvent(  
  sender As Object,
  e As _WMPOCXEvents_MouseDownEvent
) Handles player.MouseDownEvent
```

## <a name="event-data"></a><span data-ttu-id="893a2-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="893a2-107">Event Data</span></span>

<span data-ttu-id="893a2-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ MouseDownEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="893a2-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MouseDownEventHandler**.</span></span> <span data-ttu-id="893a2-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ MouseDownEvent**, que contém as propriedades a seguir relacionadas a esse evento.</span><span class="sxs-lookup"><span data-stu-id="893a2-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MouseDownEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="893a2-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="893a2-110">Property</span></span>    | <span data-ttu-id="893a2-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="893a2-111">Description</span></span>                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="893a2-112">Nnovo</span><span class="sxs-lookup"><span data-stu-id="893a2-112">nButton</span></span>     | <span data-ttu-id="893a2-113">O campo do sistema. Int16a com bits correspondente ao botão esquerdo (bit 0), botão direito (bit 1) e botão do meio (bit 2).</span><span class="sxs-lookup"><span data-stu-id="893a2-113">System.Int16A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="893a2-114">Esses bits correspondem aos valores 1, 2 e 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="893a2-114">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="893a2-115">Apenas um dos bits é definido, indicando o botão que causou o evento.</span><span class="sxs-lookup"><span data-stu-id="893a2-115">Only one of the bits is set, indicating the button that caused the event.</span></span><br/>                                                |
| <span data-ttu-id="893a2-116">nShiftState</span><span class="sxs-lookup"><span data-stu-id="893a2-116">nShiftState</span></span> | <span data-ttu-id="893a2-117">O campo do sistema. Int16a com os bits menos significativos correspondentes à tecla SHIFT (bit 0), a tecla CTRL (bit 1) e a tecla ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="893a2-117">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="893a2-118">Esses bits correspondem aos valores 1, 2 e 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="893a2-118">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="893a2-119">Alguns, todos ou nenhum dos bits podem ser definidos, indicando que algumas, todas ou nenhuma das chaves são pressionadas.</span><span class="sxs-lookup"><span data-stu-id="893a2-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |
| <span data-ttu-id="893a2-120">Efeito</span><span class="sxs-lookup"><span data-stu-id="893a2-120">fX</span></span>          | <span data-ttu-id="893a2-121">System. Int32The x-coordenada do ponteiro do mouse em relação ao canto superior esquerdo do controle.</span><span class="sxs-lookup"><span data-stu-id="893a2-121">System.Int32The x-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |
| <span data-ttu-id="893a2-122">SAR</span><span class="sxs-lookup"><span data-stu-id="893a2-122">fY</span></span>          | <span data-ttu-id="893a2-123">System. Int32The y-coordenada do ponteiro do mouse em relação ao canto superior esquerdo do controle.</span><span class="sxs-lookup"><span data-stu-id="893a2-123">System.Int32The y-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="893a2-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="893a2-124">Requirements</span></span>



| <span data-ttu-id="893a2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="893a2-125">Requirement</span></span> | <span data-ttu-id="893a2-126">Valor</span><span class="sxs-lookup"><span data-stu-id="893a2-126">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="893a2-127">Versão</span><span class="sxs-lookup"><span data-stu-id="893a2-127">Version</span></span><br/>   | <span data-ttu-id="893a2-128">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="893a2-128">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="893a2-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="893a2-129">Namespace</span></span><br/> | <span data-ttu-id="893a2-130">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="893a2-130">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="893a2-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="893a2-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="893a2-132"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="893a2-132"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="893a2-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="893a2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="893a2-134">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="893a2-134">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





