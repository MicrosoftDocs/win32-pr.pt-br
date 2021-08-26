---
title: GLX e WGL/Windows
description: Algumas das funções WGL e Windows funções são mais ou menos análogas às funções de Janela GLX X. A lista a seguir mostra as funções GLX e suas funções WGL/Windows correspondentes, se disponíveis.
ms.assetid: 428c0fdc-a541-4720-908f-99f0539d9f4b
keywords:
- Funções OpenGL Windows,GLX
- Funções GLX OpenGL
- Funções WGL, em comparação com funções GLX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24b88caeed9aea7bae8e38f73818ac180aad9117806508f40550b02eb8a4e76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035376"
---
# <a name="glx-and-wglwindows"></a>GLX e WGL/Windows

Algumas das funções WGL e Windows funções são mais ou menos análogas às funções de Janela GLX X. A lista a seguir mostra as funções GLX e suas funções WGL/Windows correspondentes, se disponíveis.



| Funções GLX             | Funções WGL/Windows                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **glXChooseVisual**       | [**EscolhaPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                                                                                                              |
| **glXCopyContext**        |                                                                                                                                                             |
| **glXCreateContext**      | [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)                                                                                                                |
| **glXCreateGLXPixmap**    | [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap)  /  [ **CreateDIBSection**](/windows/desktop/api/wingdi/nf-wingdi-createdibsection)                                                                     |
| **glXDestroyContext**     | [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)                                                                                                                |
| **glXDestroyGLXPixmap**   | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                                                                                                                        |
| **glXGetConfig**          | [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)                                                                                                          |
| **glXGetCurrentContext**  | [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)                                                                                                        |
| **glXGetCurrentDrawable** | [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)                                                                                                                  |
| **glXIsDirect**           |                                                                                                                                                             |
| **glXMakeCurrent**        | [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)                                                                                                                    |
| **glXQueryExtension**     | [**Getversion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                           |
| **glXQueryVersion**       | [**Getversion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                           |
| **glXSwapBuffers**        | [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)                                                                                                                          |
| **glXUseXFont**           | [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)  /  [ **wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa)                                                           |
| **glXWaitGL**             |                                                                                                                                                             |
| **glXWaitX**              |                                                                                                                                                             |
| **XGetVisualInfo**        | [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                                                                                                                    |
| **XCreateWindow**         | [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)  /  [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) e [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc)  /  [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) |
| **XSync**                 | [**GdiFlush**](/windows/desktop/api/wingdi/nf-wingdi-gdiflush)                                                                                                                                |
|                           | [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                                                                                                                    |
|                           | [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)                                                                                                              |
|                           | [**wglShareLists**](/windows/desktop/api/wingdi/nf-wingdi-wglsharelists)                                                                                                                      |



 

Para obter mais informações, consulte o *Guia de Portação*.

 

 