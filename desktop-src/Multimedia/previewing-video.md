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
# <a name="previewing-video-windows-multimedia"></a>Visualizando vídeo (Multimídia do Windows)

O exemplo a seguir usa a macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) para definir a taxa de exibição do quadro para o modo de visualização como 66 milissegundos por quadro e, em seguida, usa a macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) para colocar a janela de captura no modo de visualização.


```C++
// Create the capture window.
HWND hWndC = capCreateCaptureWindow(TEXT("My Capture Window"),
    WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, hwndParent, nID);

capPreviewRate(hWndC, 66);     // rate, in milliseconds
capPreview(hWndC, TRUE);       // starts preview 

// Preview

capPreview(hWndC, FALSE);        // disables preview 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando a Captura de Vídeo](using-video-capture.md)
</dt> </dl>

 

 




