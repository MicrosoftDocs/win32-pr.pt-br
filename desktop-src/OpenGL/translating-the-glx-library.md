---
title: Traduzindo a biblioteca GLX
description: Traduzindo a biblioteca GLX
ms.assetid: 040fe6f1-f6ba-4dfa-b294-447efd686361
keywords:
- OpenGL na Windows, biblioteca GLX
- portando para OpenGL, biblioteca GLX
- Portação openGL, biblioteca GLX
- Biblioteca GLX OpenGL
- Funções Xlib OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6864173cf85e0db24e77c53a7627a90e6110a1ff3ec3d94a7c85e456f98ffd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034446"
---
# <a name="translating-the-glx-library"></a>Traduzindo a biblioteca GLX

Os programas do OpenGL X Window System usam a Extensão OpenGL com a biblioteca GLX (Sistema de Janela X). A biblioteca é um conjunto de funções e rotinas que inicializam o formato de pixel, controlam a renderização e executam outras tarefas específicas do OpenGL. Ele conecta a biblioteca OpenGL ao Sistema de JanelaS X gerenciando os controles de janela e os contextos de renderização. Você deve converter essas funções em suas funções Windows equivalentes. A tabela a seguir lista as funções GLX do Sistema de Janela X e suas funções Windows funções equivalentes.



| Função GLX/Xlib         | Windows função                                                                                                                                       |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **glXChooseVisual**       | [**EscolhaPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                                                                                                         |
| **glXCopyContext**        | Não aplicável.                                                                                                                                        |
| **glXCreateContext**      | [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)                                                                                                           |
| **glXCreateGLXPixmap**    | [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap)[**CreateDIBSection**](/windows/desktop/api/wingdi/nf-wingdi-createdibsection)                                                                   |
| **glXDestroyContext**     | [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)                                                                                                           |
| **glXDestroyGLXPixmap**   | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                                                                                                                   |
| **glXGetConfig**          | [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)                                                                                                     |
| **glXGetCurrentContext**  | [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)                                                                                                   |
| **glXGetCurrentDrawable** | [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)                                                                                                             |
| **glXIsDirect**           | Não aplicável.                                                                                                                                        |
| **glXMakeCurrent**        | [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)                                                                                                               |
| **glXQueryExtension**     | [**Getversion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                      |
| **glXQueryVersion**       | [**Getversion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                      |
| **glXSwapBuffers**        | [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)                                                                                                                     |
| **glXUseXFont**           | [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)                                                                                                         |
| **XGetVisualInfo**        | [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                                                                                                               |
| **XCreateWindow**         | [**CreateWindow,**](/windows/win32/api/winuser/nf-winuser-createwindowa) [**CreateWindowEx,**](/windows/win32/api/winuser/nf-winuser-createwindowexa) [**GetDC,**](/windows/desktop/api/winuser/nf-winuser-getdc) [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) |
| **XSync**                 | [**GdiFlush**](/windows/desktop/api/wingdi/nf-wingdi-gdiflush)                                                                                                                           |
| Não aplicável.           | [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                                                                                                               |



 

Algumas funções GLX não têm uma função Windows equivalente. Para portabilidade dessas funções para Windows, reescreva seu código para obter a mesma funcionalidade. Por exemplo, **glXWaitGL** não tem nenhuma função Windows equivalente, mas você pode obter o mesmo resultado, executando qualquer comando OpenGL pendente, chamando [**glFinish**](glfinish.md).

Os tópicos a seguir descrevem como portar funções GLX que definem o formato de pixel e gerenciam contextos de renderização,maps e bitmaps.

 

 