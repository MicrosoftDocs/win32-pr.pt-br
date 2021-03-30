---
title: Modo de Color-Index e gerenciamento de paleta do Windows
description: O modo de índice de cor especifica as cores em uma paleta lógica com um índice para uma entrada de paleta lógica específica.
ms.assetid: 8cf07c3e-8a8b-4f28-a363-34d3c0d33890
keywords:
- OpenGL no Windows, gerenciamento de paleta
- OpenGL no Windows, modo de índice de cor
- modo de índice de cor OpenGL
- gerenciamento de paleta OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873308c4ac64d496e344b1c71d440d4dc8321418
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005796"
---
# <a name="color-index-mode-and-windows-palette-management"></a>Modo de Color-Index e gerenciamento de paleta do Windows

O modo de índice de cor especifica as cores em uma paleta lógica com um índice para uma entrada de paleta lógica específica. A maioria dos programas de GDI usa paletas de índice de cores, mas o modo RGBA funciona melhor para OpenGL em vários efeitos, como sombreamento, iluminação, neblina e mapeamento de textura. Se a cor mais verdadeira não for crítica para seu aplicativo OpenGL, você poderá optar por usar o modo de índice de cor (por exemplo, para um mapa Topographic que usa "cor falsa" para enfatizar o gradiente de elevação).

## <a name="color-index-mode-palette-sample"></a>Exemplo de paleta de modo de Color-Index

O código a seguir configura uma estrutura [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) que define o sinalizador do membro **iPixelType** para PFD \_ tipo \_ COLORINDEX. Isso especifica que o aplicativo usa uma paleta de índice de cor.


```C++
BOOL bSetupPixelFormat(HDC hdc) 
{ 
    PIXELFORMATDESCRIPTOR pfd, *ppfd; 
    int pixelformat; 
 
    ppfd = &pfd; 
 
    ppfd->nSize = sizeof(PIXELFORMATDESCRIPTOR); 
    ppfd->nVersion = 1; 
    ppfd->dwFlags = PFD_DRAW_TO_WINDOW | PFD_SUPPORT_OPENGL |  
                        PFD_DOUBLEBUFFER; 
    ppfd->dwLayerMask = PFD_MAIN_PLANE; 
 
    /* Set to color-index mode and use the default color palette. */ 
    ppfd->iPixelType = PFD_TYPE_COLORINDEX;  
 
    ppfd->cColorBits = 8; 
    ppfd->cDepthBits = 16; 
    ppfd->cAccumBits = 0; 
    ppfd->cStencilBits = 0; 
 
    pixelformat = ChoosePixelFormat(hdc, ppfd); 
 
    if ( (pixelformat = ChoosePixelFormat(hdc, ppfd)) == 0 ) 
    { 
        MessageBox(NULL, "ChoosePixelFormat failed", "Error", MB_OK); 
        return FALSE; 
    } 
 
    if (SetPixelFormat(hdc, pixelformat, ppfd) == FALSE) 
    { 
        MessageBox(NULL, "SetPixelFormat failed", "Error", MB_OK); 
        return FALSE; 
    } 
 
    return TRUE; 
}
```



 

 




