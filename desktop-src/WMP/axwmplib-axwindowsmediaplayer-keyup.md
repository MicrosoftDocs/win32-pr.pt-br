---
title: Evento KeyUp do objeto AxWindowsMediaPlayer
description: O evento KeyUp ocorre quando uma chave é liberada. | Evento KeyUp do objeto AxWindowsMediaPlayer
ms.assetid: db814481-6099-4dbd-8ab1-808e1875ae35
keywords:
- Evento KeyUp do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- KeyUp Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 509f520ff7624b0b29302d7bf5cd825cd45b4254
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761485"
---
# <a name="keyup-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="9eb4f-105">Evento KeyUp do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="9eb4f-105">KeyUp Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="9eb4f-106">O evento KeyUp ocorre quando uma chave é liberada.</span><span class="sxs-lookup"><span data-stu-id="9eb4f-106">The KeyUp event occurs when a key is released.</span></span>

``` syntax
[C#]
private void player_KeyUpEvent(
  object sender,
  _WMPOCXEvents_KeyUpEvent e
)

[Visual Basic]
Private Sub player_KeyUpEvent(
    sender As Object,
    e As _WMPOCXEvents_KeyUpEvent
) Handles player.KeyUpEvent
```

## <a name="event-data"></a><span data-ttu-id="9eb4f-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="9eb4f-107">Event Data</span></span>

<span data-ttu-id="9eb4f-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyUpEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="9eb4f-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_KeyUpEventHandler**.</span></span> <span data-ttu-id="9eb4f-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyUpEvent**, que contém as propriedades a seguir relacionadas a esse evento.</span><span class="sxs-lookup"><span data-stu-id="9eb4f-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_KeyUpEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="9eb4f-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="9eb4f-110">Property</span></span>    | <span data-ttu-id="9eb4f-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="9eb4f-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eb4f-112">nKeyCode</span><span class="sxs-lookup"><span data-stu-id="9eb4f-112">nKeyCode</span></span>    | <span data-ttu-id="9eb4f-113">System. Int16Specifies que a chave física é pressionada.</span><span class="sxs-lookup"><span data-stu-id="9eb4f-113">System.Int16Specifies which physical key is pressed.</span></span> <span data-ttu-id="9eb4f-114">Para obter os valores possíveis, consulte a seção comentários do evento KeyDown.</span><span class="sxs-lookup"><span data-stu-id="9eb4f-114">For possible values, see the Remarks section of the KeyDown event.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="9eb4f-115">nShiftState</span><span class="sxs-lookup"><span data-stu-id="9eb4f-115">nShiftState</span></span> | <span data-ttu-id="9eb4f-116">O campo do sistema. Int16a com os bits menos significativos correspondentes à tecla SHIFT (bit 0), a tecla CTRL (bit 1) e a tecla ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="9eb4f-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="9eb4f-117">Esses bits correspondem aos valores 1, 2 e 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9eb4f-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="9eb4f-118">O argumento Shift indica o estado dessas chaves.</span><span class="sxs-lookup"><span data-stu-id="9eb4f-118">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="9eb4f-119">Alguns, todos ou nenhum dos bits podem ser definidos, indicando que algumas, todas ou nenhuma das chaves são pressionadas.</span><span class="sxs-lookup"><span data-stu-id="9eb4f-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9eb4f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9eb4f-120">Requirements</span></span>



| <span data-ttu-id="9eb4f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eb4f-121">Requirement</span></span> | <span data-ttu-id="9eb4f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9eb4f-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eb4f-123">Versão</span><span class="sxs-lookup"><span data-stu-id="9eb4f-123">Version</span></span><br/>   | <span data-ttu-id="9eb4f-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="9eb4f-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="9eb4f-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="9eb4f-125">Namespace</span></span><br/> | <span data-ttu-id="9eb4f-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="9eb4f-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="9eb4f-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="9eb4f-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9eb4f-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9eb4f-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eb4f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="9eb4f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eb4f-130">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9eb4f-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





