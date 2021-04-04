---
title: Captura de quadro manual
description: Captura de quadro manual
ms.assetid: 7c5576ff-2694-4f44-a386-03bbc6f9c2ed
keywords:
- WM_CAP_SINGLE_FRAME_OPEN mensagem
- WM_CAP_SINGLE_FRAME mensagem
- WM_CAP_SINGLE_FRAME_CLOSE mensagem
- macro capCaptureSingleFrameOpen
- macro capCaptureSingleFrame
- macro capCaptureSingleFrameClose
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26899032d8e81be437e8f29acf36f0a37703c560
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822493"
---
# <a name="manual-frame-capture"></a><span data-ttu-id="74e2c-109">Captura de quadro manual</span><span class="sxs-lookup"><span data-stu-id="74e2c-109">Manual Frame Capture</span></span>

<span data-ttu-id="74e2c-110">Se você quiser especificar individualmente os quadros a serem capturados em um fluxo de vídeo, poderá controlar a sequência usando o quadro de visualização do [**WM, \_ \_ \_ \_ abrir**](wm-cap-single-frame-open.md)a extremidade do quadro [**\_ \_ único \_**](wm-cap-single-frame.md)e mensagens de [**\_ \_ \_ \_ fechamento do quadro do WM Cap**](wm-cap-single-frame-close.md) (ou as macros [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen), [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe)e [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) ).</span><span class="sxs-lookup"><span data-stu-id="74e2c-110">If you want to individually specify the frames to capture in a video stream, you can control the sequence by using the [**WM\_CAP\_SINGLE\_FRAME\_OPEN**](wm-cap-single-frame-open.md), [**WM\_CAP\_SINGLE\_FRAME**](wm-cap-single-frame.md), and [**WM\_CAP\_SINGLE\_FRAME\_CLOSE**](wm-cap-single-frame-close.md) messages (or the [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen), [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe), and [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) macros).</span></span> <span data-ttu-id="74e2c-111">Normalmente, essas mensagens são usadas para criar animações acrescentando quadros individuais ao arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="74e2c-111">Typically, these messages are used to create animation by appending individual frames to the capture file.</span></span> <span data-ttu-id="74e2c-112">\_O WM \_ Cap \_ \_ com um único quadro aberto abre um arquivo para uma operação de captura controlada manualmente.</span><span class="sxs-lookup"><span data-stu-id="74e2c-112">WM\_CAP\_SINGLE\_FRAME\_OPEN opens a file for a manually driven capture operation.</span></span> <span data-ttu-id="74e2c-113">\_O quadro do WM Cap \_ \_ captura um quadro individual e o anexa ao arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="74e2c-113">WM\_CAP\_SINGLE\_FRAME captures an individual frame and appends it to the capture file.</span></span> <span data-ttu-id="74e2c-114">\_ \_ \_ \_ O fechamento do quadro do WM Cap fecha o arquivo usado para captura manual de quadros.</span><span class="sxs-lookup"><span data-stu-id="74e2c-114">WM\_CAP\_SINGLE\_FRAME\_CLOSE closes the file used for manual frame capture.</span></span>

> [!Note]  
> <span data-ttu-id="74e2c-115">Este método de captura não dá suporte à captura de áudio simultânea com captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="74e2c-115">This capture method does not support simultaneous audio capture with video capture.</span></span>

 

 

 




