---
description: 'Você pode usar um coletor de tinta (InkCollector, InkOverlay ou InkPicture) para acessar diretamente o reconhecedor de gestos da Microsoft. Para usar um coletor de tinta para acessar o reconhecedor de gestos: defina a Propriedade CollectionMode do coletor de tinta para o modo InkAndGesture ou GestureOnly Mode. inkOverlay. CollectionMode = CollectionMode. GestureOnly; Escolha o gesto para o qual você deseja dar suporte. inkOverlay. SetGestureStatus (ApplicationGesture. algestos, true); implemente um manipulador de eventos que receba notificações de gesto. No manipulador de eventos, você precisa implementar a ação correspondente a cada evento recebido. Observação o modo misto dá suporte apenas a gestos de traço único. O modo de gesto dá suporte a vários gestos de traço. inkOverlay. gesto + = New InkCollectorGestureEventHandler (gesto de inkOverlay \_ ); no modo InkAndGesture, cada traço individual é enviado para o reconhecedor de gestos da Microsoft. Se for reconhecido como um gesto que você habilitou, uma notificação de evento será enviada. Se o aplicativo aceitar a notificação de eventos, o traço será apagado. Se o aplicativo não aceitar a notificação ou se o traço não for reconhecido como um gesto, o traço será armazenado no objeto de tinta. No modo GestureOnly, os traços são delimitados por tempos limite antes e depois dos traços. Os traços coletados no tempo limite são enviados para o reconhecedor. Se os traços forem reconhecidos como um gesto que você habilitou, uma notificação de evento será enviada. O aplicativo pode aceitar ou rejeitar o evento, afetando a ação correspondente ou não. No modo somente gesto, os traços nunca são salvos no objeto Ink.'
ms.assetid: 3f5f00a3-1f2c-4fa2-9738-bc5fb56e2208
title: Usando apenas o reconhecedor de gestos da Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80504e8b32c0b9596936bb4f07d029cd4ea8ddbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827075"
---
# <a name="using-the-microsoft-gesture-recognizer-only"></a><span data-ttu-id="8f663-113">Usando apenas o reconhecedor de gestos da Microsoft</span><span class="sxs-lookup"><span data-stu-id="8f663-113">Using the Microsoft Gesture Recognizer Only</span></span>

<span data-ttu-id="8f663-114">Você pode usar um coletor de tinta ([**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)ou [InkPicture](inkpicture-control-reference.md)) para acessar diretamente o reconhecedor de gestos da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8f663-114">You can use an ink collector ([**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md), or [InkPicture](inkpicture-control-reference.md)) to access the default Microsoft gesture recognizer directly.</span></span>

<span data-ttu-id="8f663-115">Para usar um coletor de tinta para acessar o reconhecedor de gestos:</span><span class="sxs-lookup"><span data-stu-id="8f663-115">To use an ink collector to access the gesture recognizer:</span></span>

-   <span data-ttu-id="8f663-116">Defina a propriedade [**CollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) do coletor de tinta para o modo **InkAndGesture** ou **GestureOnly** .</span><span class="sxs-lookup"><span data-stu-id="8f663-116">Set the [**CollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) property of the ink collector to either **InkAndGesture** mode or **GestureOnly** mode.</span></span>

`inkOverlay.CollectionMode = CollectionMode.GestureOnly;`

-   <span data-ttu-id="8f663-117">Escolha o gesto para o qual você deseja dar suporte.</span><span class="sxs-lookup"><span data-stu-id="8f663-117">Choose the gesture that you want to support.</span></span>

`inkOverlay.SetGestureStatus(ApplicationGesture.AllGestures, true);`

-   <span data-ttu-id="8f663-118">Implemente um manipulador de eventos que receba notificações de gestos.</span><span class="sxs-lookup"><span data-stu-id="8f663-118">Implement an event handler that receives gesture notifications.</span></span> <span data-ttu-id="8f663-119">No manipulador de eventos, você precisa implementar a ação correspondente a cada evento recebido.</span><span class="sxs-lookup"><span data-stu-id="8f663-119">In the event handler, you need to implement the action corresponding to each event received.</span></span>
    > [!Note]  
    > <span data-ttu-id="8f663-120">O modo misto dá suporte apenas a gestos de traço único.</span><span class="sxs-lookup"><span data-stu-id="8f663-120">Mixed mode supports only single-stroke gestures.</span></span> <span data-ttu-id="8f663-121">O modo de gesto dá suporte a vários gestos de traço.</span><span class="sxs-lookup"><span data-stu-id="8f663-121">Gesture mode supports multiple stroke gestures.</span></span>

     

`inkOverlay.Gesture += new InkCollectorGestureEventHandler(inkOverlay_Gesture);`

<span data-ttu-id="8f663-122">No modo **InkAndGesture** , cada traço individual é enviado para o reconhecedor de gestos da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8f663-122">In **InkAndGesture** mode, each individual stroke is sent to the Microsoft gesture recognizer.</span></span> <span data-ttu-id="8f663-123">Se for reconhecido como um gesto que você habilitou, uma notificação de evento será enviada.</span><span class="sxs-lookup"><span data-stu-id="8f663-123">If it is recognized as a gesture that you have enabled, an event notification is sent.</span></span> <span data-ttu-id="8f663-124">Se o aplicativo aceitar a notificação de eventos, o traço será apagado.</span><span class="sxs-lookup"><span data-stu-id="8f663-124">If the application accepts the event notification, the stroke is erased.</span></span> <span data-ttu-id="8f663-125">Se o aplicativo não aceitar a notificação ou se o traço não for reconhecido como um gesto, o traço será armazenado no objeto de [**tinta**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="8f663-125">If the application does not accept the notification or if the stroke is not recognized to be a gesture, the stroke is stored in the [**Ink**](inkdisp-class.md) object.</span></span>

<span data-ttu-id="8f663-126">No modo **GestureOnly** , os traços são delimitados por tempos limite antes e depois dos traços.</span><span class="sxs-lookup"><span data-stu-id="8f663-126">In **GestureOnly** mode, the strokes are delimited by timeouts before and after the strokes.</span></span> <span data-ttu-id="8f663-127">Os traços coletados no tempo limite são enviados para o reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="8f663-127">The strokes collected within the timeout are sent to the recognizer.</span></span> <span data-ttu-id="8f663-128">Se os traços forem reconhecidos como um gesto que você habilitou, uma notificação de evento será enviada.</span><span class="sxs-lookup"><span data-stu-id="8f663-128">If the strokes are recognized as a gesture that you have enabled, an event notification is sent.</span></span> <span data-ttu-id="8f663-129">O aplicativo pode aceitar ou rejeitar o evento, afetando a ação correspondente ou não.</span><span class="sxs-lookup"><span data-stu-id="8f663-129">The application may accept or reject the event, effecting the corresponding action or not.</span></span> <span data-ttu-id="8f663-130">No modo somente gesto, os traços nunca são salvos no objeto [**Ink**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="8f663-130">In gesture-only mode, the strokes are never saved in the [**Ink**](inkdisp-class.md) object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f663-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8f663-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8f663-132">[Microsoft. Ink. InkCollector. CollectionMode](/previous-versions/ms836497(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="8f663-132">[Microsoft.Ink.InkCollector.CollectionMode](/previous-versions/ms836497(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="8f663-133">[Microsoft. Ink. InkOverlay. CollectionMode](/previous-versions/ms833092(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="8f663-133">[Microsoft.Ink.InkOverlay.CollectionMode](/previous-versions/ms833092(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="8f663-134">[Microsoft. Ink. InkPicture. CollectionMode](/previous-versions/ms582182(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="8f663-134">[Microsoft.Ink.InkPicture.CollectionMode](/previous-versions/ms582182(v=vs.100))</span></span>
</dt> </dl>

 

 
