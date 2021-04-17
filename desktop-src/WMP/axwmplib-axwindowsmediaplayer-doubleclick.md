---
title: Evento DoubleClick do objeto AxWindowsMediaPlayer
description: O evento DoubleClick ocorre quando o usuário clica duas vezes em um botão do mouse em um controle do Windows Media Player.
ms.assetid: 4f116d8a-1ad5-443a-9c91-66214bbdebcf
keywords:
- Evento DoubleClick do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- DoubleClick Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ac809e8ea61b3abbbc964f6dc9ee2976442fc31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759747"
---
# <a name="doubleclick-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="0cb33-104">Evento DoubleClick do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="0cb33-104">DoubleClick Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="0cb33-105">O evento DoubleClick ocorre quando o usuário clica duas vezes em um botão do mouse em um controle do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0cb33-105">The DoubleClick event occurs when the user double-clicks a mouse button on a Windows Media Player control.</span></span>

``` syntax
[C#]
private void player_DoubleClickEvent(
  object sender,
  _WMPOCXEvents_DoubleClickEvent e
)

[Visual Basic]
Private Sub player_DoubleClickEvent(  
  sender As Object,  
  e As _WMPOCXEvents_DoubleClickEvent
) Handles player.DoubleClickEvent
```

## <a name="event-data"></a><span data-ttu-id="0cb33-106">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="0cb33-106">Event Data</span></span>

<span data-ttu-id="0cb33-107">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ DoubleClickEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="0cb33-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DoubleClickEventHandler**.</span></span> <span data-ttu-id="0cb33-108">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ DoubleClickEvent**, que contém as propriedades a seguir relacionadas a esse evento.</span><span class="sxs-lookup"><span data-stu-id="0cb33-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DoubleClickEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="0cb33-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="0cb33-109">Property</span></span>    | <span data-ttu-id="0cb33-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="0cb33-110">Description</span></span>                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb33-111">Nnovo</span><span class="sxs-lookup"><span data-stu-id="0cb33-111">nButton</span></span>     | <span data-ttu-id="0cb33-112">O campo do sistema. Int16a com bits correspondente ao botão esquerdo (bit 0), botão direito (bit 1) e botão do meio (bit 2).</span><span class="sxs-lookup"><span data-stu-id="0cb33-112">System.Int16A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="0cb33-113">Esses bits correspondem aos valores 1, 2 e 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="0cb33-113">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="0cb33-114">Apenas um dos bits é definido, indicando o botão que causou o evento.</span><span class="sxs-lookup"><span data-stu-id="0cb33-114">Only one of the bits is set, indicating the button that caused the event.</span></span><br/>                                                |
| <span data-ttu-id="0cb33-115">nShiftState</span><span class="sxs-lookup"><span data-stu-id="0cb33-115">nShiftState</span></span> | <span data-ttu-id="0cb33-116">O campo do sistema. Int16a com os bits menos significativos correspondentes à tecla SHIFT (bit 0), a tecla CTRL (bit 1) e a tecla ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="0cb33-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="0cb33-117">Esses bits correspondem aos valores 1, 2 e 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="0cb33-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="0cb33-118">Alguns, todos ou nenhum dos bits podem ser definidos, indicando que algumas, todas ou nenhuma das chaves são pressionadas.</span><span class="sxs-lookup"><span data-stu-id="0cb33-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |
| <span data-ttu-id="0cb33-119">Efeito</span><span class="sxs-lookup"><span data-stu-id="0cb33-119">fX</span></span>          | <span data-ttu-id="0cb33-120">System. Int32The x-coordenada do ponteiro do mouse em relação ao canto superior esquerdo do controle.</span><span class="sxs-lookup"><span data-stu-id="0cb33-120">System.Int32The x-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |
| <span data-ttu-id="0cb33-121">SAR</span><span class="sxs-lookup"><span data-stu-id="0cb33-121">fY</span></span>          | <span data-ttu-id="0cb33-122">System. Int32The y-coordenada do ponteiro do mouse em relação ao canto superior esquerdo do controle.</span><span class="sxs-lookup"><span data-stu-id="0cb33-122">System.Int32The y-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="0cb33-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cb33-123">Requirements</span></span>



| <span data-ttu-id="0cb33-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cb33-124">Requirement</span></span> | <span data-ttu-id="0cb33-125">Valor</span><span class="sxs-lookup"><span data-stu-id="0cb33-125">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb33-126">Versão</span><span class="sxs-lookup"><span data-stu-id="0cb33-126">Version</span></span><br/>   | <span data-ttu-id="0cb33-127">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="0cb33-127">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="0cb33-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="0cb33-128">Namespace</span></span><br/> | <span data-ttu-id="0cb33-129">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="0cb33-129">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="0cb33-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="0cb33-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0cb33-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0cb33-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cb33-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="0cb33-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cb33-133">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="0cb33-133">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





