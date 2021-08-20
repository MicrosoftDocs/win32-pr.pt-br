---
title: Limitando o escopo de reprodução
description: Limitando o escopo de reprodução
ms.assetid: 080ab96f-1cb5-48d4-ac0a-8fd9ba68a31a
keywords:
- Macro MCIWndPlayFrom
- Macro MCIWndPlayTo
- Macro MCIWndPlayFromTo
- Comandos de reprodução da MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 064f62e913c33bef0582efaa950ee376e31a5b06a54d0e70674192e31a679a9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139479"
---
# <a name="limiting-the-playback-scope"></a>Limitando o escopo de reprodução

O controle da reprodução começa com a macro [**MCIWndPlay,**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) que reproduz o conteúdo ou o arquivo associado a uma janela MCIWnd da posição de reprodução atual até o final do conteúdo. Se você quiser limitar a reprodução a uma parte específica do conteúdo ou arquivo, poderá escolher entre as outras macros MCIWnd de reprodução: [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom), [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)e [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto).

Você também precisa definir um formato de hora apropriado. O formato de hora determina se o conteúdo é medido em quadros, milissegundos, faixas ou algumas outras unidades.

O exemplo a seguir cria uma janela MCIWnd e fornece comandos de menu para reproduzir o último terceiro, o primeiro terceiro ou o terceiro meio do conteúdo. Esses comandos de menu usam **MCIWndPlayFrom**, **MCIWndPlayTo** e **MCIWndPlayFromTo** para reproduzir os segmentos de conteúdo. O exemplo também usa as macros [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) e [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) para identificar o início e o fim do conteúdo e usa a macro [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) para mover a posição de reprodução para o início do conteúdo.

A [**função MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) usa os estilos WS CAPTION e MCIWNDF SHOWALL, além dos estilos de janela padrão para exibir o nome do arquivo, o modo e a posição de reprodução atual na barra de título da janela \_ \_ MCIWnd.


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate(hwnd, 
                g_hinst, 
                WS_CHILD | WS_VISIBLE | WS_CAPTION | 
                MCIWNDF_SHOWALL, 
                "sample.avi"); 
            break;
        case IDM_PLAYFROM:                // plays last third of clip 
            MCIWndUseTime(g_hwndMCIWnd);  // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback end position. 
            lPlayStart = 2 * (lEnd - lStart) / 3 + lStart; 
 
            MCIWndPlayFrom(g_hwndMCIWnd, lPlayStart); 
            break; 
        case IDM_PLAYTO:                  // plays first third of clip 
            MCIWndUseTime(g_hwndMCIWnd);  // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback start position. 
            lPlayEnd = (lEnd - lStart) / 3 + lStart;
 
            MCIWndHome(g_hwndMCIWnd); 
            MCIWndPlayTo(g_hwndMCIWnd, lPlayEnd); 
            break; 
        case IDM_PLAYSOME:               // plays middle third of clip 
            MCIWndUseTime(g_hwndMCIWnd); // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback start and end positions. 
            lPlayStart = (lEnd - lStart) / 3 + lStart;
            lPlayEnd = 2 * (lEnd - lStart) / 3 + lStart; 
 
            MCIWndPlayFromTo(g_hwndMCIWnd, lPlayStart, lPlayEnd); 
            break; 
    
    // Handle other commands here. 
    } 
```



 

 




