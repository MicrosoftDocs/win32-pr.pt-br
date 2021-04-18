---
title: Visualizando vídeo (multimídia do Windows)
description: Visualizando vídeo
ms.assetid: 33ae7d07-5fea-47d7-b60d-4ee412e91dec
keywords:
- macro capPreview
- macro capPreviewRate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79c8e24d30fd5141b5b1ac14de99d83e0b2bc620
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105778546"
---
# <a name="previewing-video-windows-multimedia"></a><span data-ttu-id="3cbb8-105">Visualizando vídeo (multimídia do Windows)</span><span class="sxs-lookup"><span data-stu-id="3cbb8-105">Previewing Video (Windows Multimedia)</span></span>

<span data-ttu-id="3cbb8-106">O exemplo a seguir usa a macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) para definir a taxa de exibição do quadro para o modo de visualização como 66 milissegundos por quadro e, em seguida, usa a macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) para posicionar a janela de captura no modo de visualização.</span><span class="sxs-lookup"><span data-stu-id="3cbb8-106">The following example uses the [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) macro to set the frame display rate for preview mode to 66 milliseconds per frame and then uses the [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) macro to place the capture window in preview mode.</span></span>


```C++
// Create the capture window.
HWND hWndC = capCreateCaptureWindow(TEXT("My Capture Window"),
    WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, hwndParent, nID);

capPreviewRate(hWndC, 66);     // rate, in milliseconds
capPreview(hWndC, TRUE);       // starts preview 

// Preview

capPreview(hWndC, FALSE);        // disables preview 
```



## <a name="related-topics"></a><span data-ttu-id="3cbb8-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3cbb8-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cbb8-108">Usando a captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="3cbb8-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




