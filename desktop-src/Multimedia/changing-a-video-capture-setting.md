---
title: Alterando uma configuração de captura de vídeo
description: Alterando uma configuração de captura de vídeo
ms.assetid: a5fe7e1e-084d-4102-91d4-ffe5d1d0e5c8
keywords:
- macro capCaptureGetSetup
- macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af4142880fcbd272bc133d7f488afac02928614cfe33be6d209df27ccd1bc76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145109"
---
# <a name="changing-a-video-capture-setting"></a>Alterando uma configuração de captura de vídeo

O exemplo a seguir usa as macros [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) e [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) para alterar a taxa de captura do valor padrão (15 quadros por segundo) para 10 quadros por segundo.


```C++
CAPTUREPARMS CaptureParms;
float FramesPerSec = 10.0;

capCaptureGetSetup(hWndC, &CaptureParms, sizeof(CAPTUREPARMS));

CaptureParms.dwRequestMicroSecPerFrame = (DWORD) (1.0e6 / 
    FramesPerSec);
capCaptureSetSetup(hWndC, &CaptureParms, sizeof (CAPTUREPARMS)); 
 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando a captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 




