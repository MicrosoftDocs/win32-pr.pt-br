---
title: visualizando vídeo (Windows multimídia)
description: este exemplo em Windows multimídia usa capPreviewRate para definir a taxa de exibição do quadro para o modo de visualização e capPreview para colocar a janela de captura no modo de visualização.
ms.assetid: 33ae7d07-5fea-47d7-b60d-4ee412e91dec
keywords:
- macro capPreview
- macro capPreviewRate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e70d0520af3bb71906c6b0ea4d1c0a61464559eedfd2385753b228841fa6af4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037906"
---
# <a name="previewing-video-windows-multimedia"></a>visualizando vídeo (Windows multimídia)

O exemplo a seguir usa a macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) para definir a taxa de exibição do quadro para o modo de visualização como 66 milissegundos por quadro e, em seguida, usa a macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) para posicionar a janela de captura no modo de visualização.


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

[Usando a captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 




