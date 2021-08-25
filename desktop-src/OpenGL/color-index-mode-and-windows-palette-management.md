---
title: Modo Color-Index e gerenciamento Windows paleta
description: O modo de índice de cores especifica cores em uma paleta lógica com um índice para uma entrada de paleta lógica específica.
ms.assetid: 8cf07c3e-8a8b-4f28-a363-34d3c0d33890
keywords:
- OpenGL no Windows, gerenciamento de paleta
- OpenGL no Windows, modo de índice de cores
- modo de índice de cores OpenGL
- gerenciamento de paleta OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e4d7c9db02a80bdffdef93655e88cc5b2ca8197a58c5ffdb488c2b782f10d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889256"
---
# <a name="color-index-mode-and-windows-palette-management"></a>Modo Color-Index e gerenciamento Windows paleta

O modo de índice de cores especifica cores em uma paleta lógica com um índice para uma entrada de paleta lógica específica. A maioria dos programas GDI usa paletas de índice de cores, mas o modo RGBA funciona melhor para OpenGL para vários efeitos, como sombreamento, iluminação, luz e mapeamento de textura. Se ter a cor mais verdadeira não for essencial para seu aplicativo OpenGL, você poderá optar por usar o modo de índice de cores (por exemplo, para um mapa topográfico que usa "cor falsa" para enfatizar o gradiente de elevação).

## <a name="color-index-mode-palette-sample"></a>Exemplo Color-Index paleta de modo de Color-Index

O código a seguir configura uma [**estrutura PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) que define o sinalizador do membro **iPixelType** como PFD \_ TYPE \_ COLORINDEX. Isso especifica que o aplicativo usa uma paleta de índice de cores.


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



 

 




