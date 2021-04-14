---
title: Cortando uma imagem
description: Cortando uma imagem
ms.assetid: 6600751c-d4b6-481d-bf69-be2d34244c05
keywords:
- Macro MCIWndGetSource
- Macro MCIWndPutSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d73eb37792c124ad907f660d4b906ca80e715d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453583"
---
# <a name="cropping-an-image"></a>Cortando uma imagem

O exemplo a seguir cria uma janela MCIWnd e carrega um arquivo AVI. A janela inclui um comando de corte no menu, que corta um trimestre da altura ou largura de cada um dos quatro lados do quadro. O exemplo recupera as dimensões atuais (iniciais) do retângulo de origem usando a macro [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) . O retângulo de origem modificado é metade da altura e largura originais e é centralizado no quadro original. A chamada para a macro [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) redefine as coordenadas do retângulo de origem.


```C++
// extern RECT rSource, rDest; 
 
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate( hwnd, 
                g_hinst, 
                WS_CHILD | WS_VISIBLE, 
                "sample.avi" ); 
            break; 
        case IDM_CROPIMAGE:                          // crops image 
            MCIWndGetSource(g_hwndMCIWnd, &rSource); // source rectangle
            rDest.left = rSource.left +              // new boundaries
                ((rSource.right - rSource.left) / 4); 
            rDest.right = rSource.right - 
                ((rSource.right - rSource.left) / 4); 
            rDest.top = rSource.top + 
                ((rSource.bottom - rSource.top) / 4); 
            rDest.bottom = rSource.bottom - 
                ((rSource.bottom - rSource.top) / 4); 
 
            MCIWndPutSource(g_hwndMCIWnd, &rDest);   // new source rectangle 
    } 
    break; 

    // Handle other messages here. 
```



 

 




