---
title: Escolhendo e definindo um formato de pixel Best-Match
description: Este tópico explica o procedimento para corresponder um contexto de dispositivo a um formato de pixel.
ms.assetid: 7b974fb5-e34d-4781-858c-572c4e7754bc
keywords:
- OpenGL no Windows, pixels
- formato de pixel de melhor correspondência OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 143800a9c43d8c8a7779bb5e6cd119c6737f8129
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105784170"
---
# <a name="choosing-and-setting-a-best-match-pixel-format"></a>Escolhendo e definindo um formato de pixel Best-Match

Este tópico explica o procedimento para corresponder um contexto de dispositivo a um formato de pixel.

**Para obter a melhor correspondência de um contexto de dispositivo para um formato de pixel**

1.  Especifique o formato de pixel desejado em uma estrutura [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) .
2.  Chame [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).

    A função **ChoosePixelFormat** retorna um índice de formato de pixel, que você pode passar para [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) para definir a melhor correspondência de formato de pixel como o formato de pixel atual do contexto do dispositivo.

O exemplo de código a seguir mostra como realizar as etapas acima.


```C++
PIXELFORMATDESCRIPTOR pfd = { 
    sizeof(PIXELFORMATDESCRIPTOR),    // size of this pfd  
    1,                                // version number  
    PFD_DRAW_TO_WINDOW |              // support window  
    PFD_SUPPORT_OPENGL |              // support OpenGL  
    PFD_DOUBLEBUFFER,                 // double buffered  
    PFD_TYPE_RGBA,                    // RGBA type  
    24,                               // 24-bit color depth  
    0, 0, 0, 0, 0, 0,                 // color bits ignored  
    0,                                // no alpha buffer  
    0,                                // shift bit ignored  
    0,                                // no accumulation buffer  
    0, 0, 0, 0,                       // accum bits ignored  
    32,                               // 32-bit z-buffer      
    0,                                // no stencil buffer  
    0,                                // no auxiliary buffer  
    PFD_MAIN_PLANE,                   // main layer  
    0,                                // reserved  
    0, 0, 0                           // layer masks ignored  
}; 
HDC  hdc; 
int  iPixelFormat; 
 
// get the device context's best, available pixel format match  
iPixelFormat = ChoosePixelFormat(hdc, &pfd); 
 
// make that match the device context's current pixel format  
SetPixelFormat(hdc, iPixelFormat, &pfd);
```



 

 




