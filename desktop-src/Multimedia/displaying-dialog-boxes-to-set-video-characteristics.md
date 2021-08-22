---
title: Exibindo caixas de diálogo para definir características de vídeo
description: Exibindo caixas de diálogo para definir características de vídeo
ms.assetid: 8074f7d1-e8ab-46c3-acc2-a18be0eb4cc7
keywords:
- Estrutura CAPDRIVERCAPS
- Macro capDriverGetCaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e6ebfa0f75f4bcec63a693636085f16c342e53761b2cb1e67a0e2536fa5cef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144469"
---
# <a name="displaying-dialog-boxes-to-set-video-characteristics"></a>Exibindo caixas de diálogo para definir características de vídeo

Cada driver de captura pode fornecer até três caixas de diálogo diferentes usadas para controlar aspectos do processo de captura e digitalização de vídeo. O exemplo a seguir demonstra como exibir essas caixas de diálogo. Antes de exibir cada caixa de diálogo, o exemplo chama a macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) e verifica a estrutura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) retornada para ver se o driver de captura pode exibi-la.


```C++
HWND hWndC = capCreateCaptureWindow(TEXT("My Capture Window"),
    WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, hwndParent, nID);

CAPDRIVERCAPS CapDriverCaps = { }; 
CAPSTATUS     CapStatus = { };

capDriverGetCaps(hWndC, &CapDriverCaps, sizeof(CAPDRIVERCAPS)); 
 
// Video source dialog box. 
if (CapDriverCaps.fHasDlgVideoSource)
{
    capDlgVideoSource(hWndC); 
}
 
// Video format dialog box. 
if (CapDriverCaps.fHasDlgVideoFormat) 
{
    capDlgVideoFormat(hWndC); 

    // Are there new image dimensions?
    capGetStatus(hWndC, &CapStatus, sizeof (CAPSTATUS));

    // If so, notify the parent of a size change.
} 
 
// Video display dialog box. 
if (CapDriverCaps.fHasDlgVideoDisplay)
{
    capDlgVideoDisplay(hWndC); 
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando a Captura de Vídeo](using-video-capture.md)
</dt> <dt>

[**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps)
</dt> </dl>

 

 




