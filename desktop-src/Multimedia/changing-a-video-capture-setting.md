---
title: Alterando uma configuração de captura de vídeo
description: Alterando uma configuração de captura de vídeo
ms.assetid: a5fe7e1e-084d-4102-91d4-ffe5d1d0e5c8
keywords:
- macro capCaptureGetSetup
- macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b3f2629325c67bcad1fed26a9fed4d053372392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364404"
---
# <a name="changing-a-video-capture-setting"></a><span data-ttu-id="84396-105">Alterando uma configuração de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="84396-105">Changing a Video Capture Setting</span></span>

<span data-ttu-id="84396-106">O exemplo a seguir usa as macros [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) e [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) para alterar a taxa de captura do valor padrão (15 quadros por segundo) para 10 quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="84396-106">The following example uses the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) and [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macros to change the capture rate from the default value (15 frames per second) to 10 frames per second.</span></span>


```C++
CAPTUREPARMS CaptureParms;
float FramesPerSec = 10.0;

capCaptureGetSetup(hWndC, &CaptureParms, sizeof(CAPTUREPARMS));

CaptureParms.dwRequestMicroSecPerFrame = (DWORD) (1.0e6 / 
    FramesPerSec);
capCaptureSetSetup(hWndC, &CaptureParms, sizeof (CAPTUREPARMS)); 
 
```



## <a name="related-topics"></a><span data-ttu-id="84396-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="84396-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84396-108">Usando a captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="84396-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




