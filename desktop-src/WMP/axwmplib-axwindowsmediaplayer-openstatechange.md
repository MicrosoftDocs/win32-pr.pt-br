---
title: Evento OpenStateChange do objeto AxWindowsMediaPlayer
description: O evento OpenStateChange ocorre quando a propriedade OpenState muda de valor. | Evento OpenStateChange do objeto AxWindowsMediaPlayer
ms.assetid: 0229f8b4-7216-44f6-9838-a640b99bd9f3
keywords:
- Evento OpenStateChange do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- OpenStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcd1f2b7e59fdfd35bf31719cbb6a1a5e6c29e66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794513"
---
# <a name="openstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="ea6e7-105">Evento OpenStateChange do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="ea6e7-105">OpenStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="ea6e7-106">O evento OpenStateChange ocorre quando a propriedade **OpenState** muda de valor.</span><span class="sxs-lookup"><span data-stu-id="ea6e7-106">The OpenStateChange event occurs when the **openState** property changes value.</span></span>

``` syntax
[C#]
private void player_OpenStateChange(
  object sender,
  _WMPOCXEvents_OpenStateChangeEvent e
)

[Visual Basic]
Private Sub player_OpenStateChange(
  sender As Object,
  e As _WMPOCXEvents_OpenStateChangeEvent
) Handles player.OpenStateChange
```

## <a name="event-data"></a><span data-ttu-id="ea6e7-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="ea6e7-107">Event Data</span></span>

<span data-ttu-id="ea6e7-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ OpenStateChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="ea6e7-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_OpenStateChangeEventHandler**.</span></span> <span data-ttu-id="ea6e7-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ OpenStateChangeEvent**, que contém a seguinte propriedade relacionada a este evento.</span><span class="sxs-lookup"><span data-stu-id="ea6e7-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_OpenStateChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="ea6e7-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ea6e7-110">Property</span></span> | <span data-ttu-id="ea6e7-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="ea6e7-111">Description</span></span>                                                                                                                                         |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea6e7-112">NewState</span><span class="sxs-lookup"><span data-stu-id="ea6e7-112">NewState</span></span> | <span data-ttu-id="ea6e7-113">System. Int32Specifies o novo estado aberto.</span><span class="sxs-lookup"><span data-stu-id="ea6e7-113">System.Int32Specifies the new open state.</span></span> <span data-ttu-id="ea6e7-114">Para obter uma tabela de valores, consulte [OpenState](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md).</span><span class="sxs-lookup"><span data-stu-id="ea6e7-114">For a table of values, see [openState](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ea6e7-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea6e7-115">Remarks</span></span>

<span data-ttu-id="ea6e7-116">O Windows Media Player pode passar por vários Estados abertos enquanto tenta abrir um arquivo de rede, como localizar o servidor, conectar-se ao servidor e, finalmente, abrir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="ea6e7-116">Windows Media Player can go through several open states while it attempts to open a network file, such as locating the server, connecting to the server, and finally opening the file.</span></span> <span data-ttu-id="ea6e7-117">Esse evento será acionado sempre que o estado aberto for alterado.</span><span class="sxs-lookup"><span data-stu-id="ea6e7-117">This event will be fired each time the open state changes.</span></span>

<span data-ttu-id="ea6e7-118">Não há garantia de que os Estados do Windows Media Player ocorram em uma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="ea6e7-118">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="ea6e7-119">Além disso, nem todo estado ocorre necessariamente durante uma sequência de eventos.</span><span class="sxs-lookup"><span data-stu-id="ea6e7-119">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="ea6e7-120">Você não deve escrever código que dependa da ordem de estado.</span><span class="sxs-lookup"><span data-stu-id="ea6e7-120">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea6e7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea6e7-121">Requirements</span></span>



| <span data-ttu-id="ea6e7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea6e7-122">Requirement</span></span> | <span data-ttu-id="ea6e7-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ea6e7-123">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea6e7-124">Versão</span><span class="sxs-lookup"><span data-stu-id="ea6e7-124">Version</span></span><br/>   | <span data-ttu-id="ea6e7-125">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="ea6e7-125">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="ea6e7-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="ea6e7-126">Namespace</span></span><br/> | <span data-ttu-id="ea6e7-127">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="ea6e7-127">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="ea6e7-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="ea6e7-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ea6e7-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ea6e7-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea6e7-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea6e7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea6e7-131">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ea6e7-131">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ea6e7-132">**AxWindowsMediaPlayer. OpenState (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ea6e7-132">**AxWindowsMediaPlayer.openState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> </dl>

 

 





