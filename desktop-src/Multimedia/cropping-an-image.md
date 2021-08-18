---
title: Corte de uma imagem
description: Corte de uma imagem
ms.assetid: 6600751c-d4b6-481d-bf69-be2d34244c05
keywords:
- Macro MCIWndGetSource
- Macro MCIWndPutSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0150962dc85e1e179e52a06c7af6c29193b40b50e9acc7a9feecd0570ab4214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144599"
---
# <a name="cropping-an-image"></a>Corte de uma imagem

O exemplo a seguir cria uma janela MCIWnd e carrega um arquivo AVI. A janela inclui um comando de corte no menu, que recorta um quarto da altura ou largura de cada um dos quatro lados do quadro. O exemplo recupera as dimensões atuais (iniciais) do retângulo de origem usando a macro [**MCIWndGetSource.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) O retângulo de origem modificado tem metade da altura e largura originais e é centralizado no quadro original. A chamada para a macro [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) redefine as coordenadas do retângulo de origem.


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



 

 




