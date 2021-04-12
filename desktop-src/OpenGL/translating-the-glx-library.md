---
title: Convertendo a biblioteca GLX
description: Convertendo a biblioteca GLX
ms.assetid: 040fe6f1-f6ba-4dfa-b294-447efd686361
keywords:
- OpenGL no Windows, biblioteca GLX
- portando para OpenGL, biblioteca GLX
- Portabilidade do OpenGL, biblioteca GLX
- GLX biblioteca OpenGL
- Xlib funções OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e4cede2b74dc2881f867370744ee14c00cceba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366534"
---
# <a name="translating-the-glx-library"></a>Convertendo a biblioteca GLX

Os programas do sistema de janelas OpenGL X usam a extensão OpenGL com a biblioteca do sistema de janelas X (GLX). A biblioteca é um conjunto de funções e rotinas que inicializam o formato de pixel, controlam a renderização e executam outras tarefas específicas do OpenGL. Ele conecta a biblioteca OpenGL ao sistema de janelas X Gerenciando identificadores de janela e contextos de renderização. Você deve converter essas funções em suas funções equivalentes do Windows. A tabela a seguir lista as funções do sistema de janela X GLX e suas funções equivalentes do Windows.



| Função GLX/Xlib         | Função do Windows                                                                                                                                       |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **glXChooseVisual**       | [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                                                                                                         |
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
| **glXQueryExtension**     | [**Obter versão**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                      |
| **glXQueryVersion**       | [**Obter versão**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                      |
| **glXSwapBuffers**        | [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)                                                                                                                     |
| **glXUseXFont**           | [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)                                                                                                         |
| **XGetVisualInfo**        | [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                                                                                                               |
| **XCreateWindow**         | [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa), [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa), [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc), [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) |
| **XSync**                 | [**GdiFlush**](/windows/desktop/api/wingdi/nf-wingdi-gdiflush)                                                                                                                           |
| Não aplicável.           | [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                                                                                                               |



 

Algumas funções do GLX não têm uma função equivalente do Windows. Para portar essas funções para o Windows, reescreva o código para obter a mesma funcionalidade. Por exemplo, **glXWaitGL** não tem nenhuma função equivalente do Windows, mas você pode obter o mesmo resultado, executando quaisquer comandos OpenGL pendentes, chamando [**glFinish**](glfinish.md).

Os tópicos a seguir descrevem como portar funções GLX que definem o formato de pixel e gerenciar contextos de renderização, pixmaps e bitmaps.

 

 