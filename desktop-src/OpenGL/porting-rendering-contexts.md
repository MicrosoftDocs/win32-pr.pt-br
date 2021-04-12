---
title: Portando contextos de renderização
description: Portando contextos de renderização
ms.assetid: 8655a81b-9f13-4ee5-ba0d-9aa9da1bfd09
keywords:
- contextos de renderização OpenGL, portabilidade
- OpenGL no Windows, contextos de renderização
- portando para OpenGL, contextos de renderização
- Portabilidade do OpenGL, contextos de renderização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e72839d04838b3173d772fbbf29a903a295cfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364172"
---
# <a name="porting-rendering-contexts"></a>Portando contextos de renderização

O sistema de janelas X e o Windows renderizam os contextos de renderização. Seis funções GLX gerenciam contextos de renderização e cinco deles têm uma função equivalente do Windows.

A tabela a seguir lista as funções de renderização GLX e suas funções equivalentes do Windows.



| Função de contexto de renderização GLX                                                                            | Função de contexto de renderização do Windows                                      |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| GLXContext **glXCopyContext**(display *\* dpy*, GLXContext *src*, GLXContext *DST*, GLuint *Mask*)            | Não aplicável.                                                         |
| GLXContext **glXCreateContext**(display *\* dpy*, XVisualInfo *\* vis*, GLXContext *sharelist*, bool *Direct*) | HGLRC [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)(HDC *HDC*)          |
| void **glXDeleteContext**(display *\* dpy*, GLXContext *CTX*)                                              | BOOL [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)(HGLRC *HGLRC*)       |
| GLXContext **glXGetCurrentContext**(*void*)                                                               | HGLRC [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)(*void*)      |
| GLXDrawable **glXGetCurrentDrawable**(*void*)                                                             | HDC [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)(*void*)                  |
| Bool **glXMakeCurrent**(display *\* dpy*, GLXDrawable *draw*, GLXContext *CTX*)                              | BOOL [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)(HDC *HDC*, HGLRC *HGLRC*) |



 

Tipos de retorno e outros tipos têm nomes diferentes no sistema de janelas X do que no Windows. Você pode pesquisar por ocorrências de GLXContext para ajudar a localizar partes do seu código que precisam ser portadas.

As seções a seguir comparam os exemplos de código de contexto de renderização em um programa do sistema de janelas X e o mesmo código após ele ter sido transportado para o Windows.

Para obter mais informações sobre contextos de renderização, consulte [contextos de renderização](rendering-contexts.md).

 

 




