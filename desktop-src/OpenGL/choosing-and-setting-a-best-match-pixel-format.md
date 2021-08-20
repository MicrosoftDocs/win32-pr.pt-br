---
title: Escolhendo e definindo um formato Best-Match pixel
description: Este tópico explica o procedimento para corresponder um contexto de dispositivo a um formato de pixel.
ms.assetid: 7b974fb5-e34d-4781-858c-572c4e7754bc
keywords:
- OpenGL em Windows,pixels
- melhor combinação de formato de pixel OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 258364e18ff38cb67edd1315f261a55a91f58fe940b026e1fcb7b63ed2e12eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063296"
---
# <a name="choosing-and-setting-a-best-match-pixel-format"></a>Escolhendo e definindo um formato Best-Match pixel

Este tópico explica o procedimento para corresponder um contexto de dispositivo a um formato de pixel.

**Para obter a melhor combinação de um contexto de dispositivo com um formato de pixel**

1.  Especifique o formato de pixel desejado em uma [**estrutura PIXELFORMATDESCRIPTOR.**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)
2.  Chame [**ChoosePixelFormat.**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)

    A **função ChoosePixelFormat** retorna um índice de formato de pixel, que você pode passar para [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) para definir a melhor combinação de formato de pixel como o formato de pixel atual do contexto do dispositivo.

O exemplo de código a seguir mostra como executar as etapas acima.


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



 

 




