---
title: Visualizando vídeo (Multimídia do Windows)
description: Este exemplo em Multimídia do Windows usa capPreviewRate para definir a taxa de exibição do quadro para o modo de visualização e capPreview para colocar a janela de captura no modo de visualização.
ms.assetid: 33ae7d07-5fea-47d7-b60d-4ee412e91dec
keywords:
- macro capPreview
- macro capPreviewRate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc3aaeb9a8ff0f040218fca4822af93ab8bfe29
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405539"
---
# <a name="previewing-video-windows-multimedia"></a><span data-ttu-id="78ee4-105">Visualizando vídeo (Multimídia do Windows)</span><span class="sxs-lookup"><span data-stu-id="78ee4-105">Previewing Video (Windows Multimedia)</span></span>

<span data-ttu-id="78ee4-106">O exemplo a seguir usa a macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) para definir a taxa de exibição do quadro para o modo de visualização como 66 milissegundos por quadro e, em seguida, usa a macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) para colocar a janela de captura no modo de visualização.</span><span class="sxs-lookup"><span data-stu-id="78ee4-106">The following example uses the [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) macro to set the frame display rate for preview mode to 66 milliseconds per frame and then uses the [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) macro to place the capture window in preview mode.</span></span>


```C++
// Create the capture window.
HWND hWndC = capCreateCaptureWindow(TEXT("My Capture Window"),
    WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, hwndParent, nID);

capPreviewRate(hWndC, 66);     // rate, in milliseconds
capPreview(hWndC, TRUE);       // starts preview 

// Preview

capPreview(hWndC, FALSE);        // disables preview 
```



## <a name="related-topics"></a><span data-ttu-id="78ee4-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="78ee4-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78ee4-108">Usando a Captura de Vídeo</span><span class="sxs-lookup"><span data-stu-id="78ee4-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




