---
title: Funções de retorno de chamada AVICap
description: Funções de retorno de chamada AVICap
ms.assetid: d238a238-9702-4ba6-92bd-5ef1605b4983
keywords:
- Classe AVICap, funções de retorno de chamada
- Funções de retorno de chamada do AVICap, sobre
- WM_CAP_SET_CALLBACK_CAPCONTROL mensagem
- WM_CAP_SET_CALLBACK_ERROR mensagem
- WM_CAP_SET_CALLBACK_FRAME mensagem
- WM_CAP_SET_CALLBACK_STATUS mensagem
- WM_CAP_SET_CALLBACK_VIDEOSTREAM mensagem
- WM_CAP_SET_CALLBACK_WAVESTREAM mensagem
- WM_CAP_SET_CALLBACK_YIELD mensagem
- macro capSetCallbackOnCapControl
- capSetCallbackOnErrormacro
- macro capSetCallbackOnFrame
- macro capSetCallbackOnStatus
- macro capSetCallbackOnVideoStream
- macro capSetCallbackOnWaveStream
- macro capSetCallbackOnYield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9edf96a6ff5b359acb6ef6d6a302b798742ffb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916605"
---
# <a name="avicap-callback-functions"></a><span data-ttu-id="8b399-119">Funções de retorno de chamada AVICap</span><span class="sxs-lookup"><span data-stu-id="8b399-119">AVICap Callback Functions</span></span>

<span data-ttu-id="8b399-120">Seu aplicativo pode registrar funções de retorno de chamada com uma janela de captura para que ela Notifique seu aplicativo quando o status for alterado, quando ocorrerem erros, quando os buffers de áudio e de quadros de vídeo forem disponibilizados e para gerar durante a captura de streaming.</span><span class="sxs-lookup"><span data-stu-id="8b399-120">Your application can register callback functions with a capture window to have it notify your application when the status changes, when errors occur, when video frame and audio buffers become available, and to yield during streaming capture.</span></span> <span data-ttu-id="8b399-121">As mensagens a seguir definem a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="8b399-121">The following messages set the callback function.</span></span>



| <span data-ttu-id="8b399-122">Mensagem</span><span class="sxs-lookup"><span data-stu-id="8b399-122">Message</span></span>                                                                        | <span data-ttu-id="8b399-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b399-123">Description</span></span>                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b399-124">**WM \_ Cap \_ set \_ callback \_ CAPCONTROL**</span><span class="sxs-lookup"><span data-stu-id="8b399-124">**WM\_CAP\_SET\_CALLBACK\_CAPCONTROL**</span></span>](wm-cap-set-callback-capcontrol.md)   | <span data-ttu-id="8b399-125">Especifica a função de retorno de chamada no aplicativo chamado para fornecer controle preciso sobre o início e o término da captura.</span><span class="sxs-lookup"><span data-stu-id="8b399-125">Specifies the callback function in the application called to give precise control over capture start and end.</span></span> <span data-ttu-id="8b399-126">Você também pode usar a macro [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) para enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="8b399-126">You can also use the [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) macro to send this message.</span></span>                   |
| [<span data-ttu-id="8b399-127">**\_erro de \_ retorno de \_ chamada de Set Cap \_ do WM**</span><span class="sxs-lookup"><span data-stu-id="8b399-127">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)             | <span data-ttu-id="8b399-128">Especifica a função de retorno de chamada no aplicativo chamado quando ocorre um erro.</span><span class="sxs-lookup"><span data-stu-id="8b399-128">Specifies the callback function in the application called when an error occurs.</span></span> <span data-ttu-id="8b399-129">Você também pode usar a macro [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) para enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="8b399-129">You can also use the [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) macro to send this message.</span></span>                                                           |
| [<span data-ttu-id="8b399-130">**\_quadro de \_ retorno de \_ chamada Set \_ Cap do WM**</span><span class="sxs-lookup"><span data-stu-id="8b399-130">**WM\_CAP\_SET\_CALLBACK\_FRAME**</span></span>](wm-cap-set-callback-frame.md)             | <span data-ttu-id="8b399-131">Especifica a função de retorno de chamada no aplicativo chamado quando os quadros de visualização são capturados.</span><span class="sxs-lookup"><span data-stu-id="8b399-131">Specifies the callback function in the application called when preview frames are captured.</span></span> <span data-ttu-id="8b399-132">Você também pode usar a macro [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) para enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="8b399-132">You can also use the [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) macro to send this message.</span></span>                                               |
| [<span data-ttu-id="8b399-133">**WM \_ Cap \_ definir \_ status de retorno de chamada \_**</span><span class="sxs-lookup"><span data-stu-id="8b399-133">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)           | <span data-ttu-id="8b399-134">Especifica a função de retorno de chamada no aplicativo chamado quando o status é alterado.</span><span class="sxs-lookup"><span data-stu-id="8b399-134">Specifies the callback function in the application called when the status changes.</span></span> <span data-ttu-id="8b399-135">Você também pode usar a macro [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) para enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="8b399-135">You can also use the [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) macro to send this message.</span></span>                                                      |
| [<span data-ttu-id="8b399-136">**WM \_ Cap \_ set \_ callback \_ VIDEOSTREAM**</span><span class="sxs-lookup"><span data-stu-id="8b399-136">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md) | <span data-ttu-id="8b399-137">Especifica a função de retorno de chamada no aplicativo chamado durante a captura de streaming quando um novo buffer de vídeo fica disponível.</span><span class="sxs-lookup"><span data-stu-id="8b399-137">Specifies the callback function in the application called during streaming capture when a new video buffer becomes available.</span></span> <span data-ttu-id="8b399-138">Você também pode usar a macro [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) para enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="8b399-138">You can also use the [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) macro to send this message.</span></span> |
| [<span data-ttu-id="8b399-139">**\_WAVESTREAM de \_ retorno de \_ chamada de Set Cap \_ do WM**</span><span class="sxs-lookup"><span data-stu-id="8b399-139">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)   | <span data-ttu-id="8b399-140">Especifica a função de retorno de chamada no aplicativo chamado durante a captura de streaming quando um novo buffer de áudio fica disponível.</span><span class="sxs-lookup"><span data-stu-id="8b399-140">Specifies the callback function in the application called during streaming capture when a new audio buffer becomes available.</span></span> <span data-ttu-id="8b399-141">Você também pode usar a macro [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) para enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="8b399-141">You can also use the [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) macro to send this message.</span></span>   |
| [<span data-ttu-id="8b399-142">**o \_ \_ retorno de \_ chamada de Set Cap do WM \_**</span><span class="sxs-lookup"><span data-stu-id="8b399-142">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)             | <span data-ttu-id="8b399-143">Especifica a função de retorno de chamada no aplicativo chamado ao produzir durante a captura de streaming.</span><span class="sxs-lookup"><span data-stu-id="8b399-143">Specifies the callback function in the application called when yielding during streaming capture.</span></span> <span data-ttu-id="8b399-144">Você também pode usar a macro [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) para enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="8b399-144">You can also use the [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) macro to send this message.</span></span>                                         |



 

<span data-ttu-id="8b399-145">Os tópicos a seguir descrevem as diferentes funções de retorno de chamada, as notificações enviadas para as funções e seus usos.</span><span class="sxs-lookup"><span data-stu-id="8b399-145">The following topics describe the different callback functions, the notifications sent to the functions, and their uses.</span></span>

 

 




