---
title: Portando contextos de renderização
description: Portando contextos de renderização
ms.assetid: 8655a81b-9f13-4ee5-ba0d-9aa9da1bfd09
keywords:
- renderização de contextos OpenGL, portando
- OpenGL em Windows, renderização de contextos
- portando para OpenGL, renderização de contextos
- Portação openGL, contextos de renderização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f4fcb6a70f6858ac9c11258c681345ee88a8807c91230f8d3d35fc579ab3371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358335"
---
# <a name="porting-rendering-contexts"></a>Portando contextos de renderização

O sistema de janela x e Windows renderizar por meio de contextos de renderização. Seis funções GLX gerenciam contextos de renderização e cinco delas têm uma função Windows equivalente.

A tabela a seguir lista as funções de renderização GLX e suas funções Windows equivalentes.



| Função de contexto de renderização GLX                                                                            | Windows de contexto de renderização                                      |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| GLXContext **glXCopyContext**( Exibir *\* dpy*, GLXContext *src*, GLXContext *dst*, GLuint *mask*)            | Não aplicável.                                                         |
| GLXContext **glXCreateContext**( Exibir *\* dpy,* XVisualInfo *\* vis*, GLXContext *shareList*, Bool *direct*) | HGLRC [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)( HDC *hdc*)          |
| void **glXDeleteContext**( Exibir *\* dpy,* GLXContext *ctx*)                                              | BOOL [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)( HGLRC *hglrc*)       |
| GLXContext **glXGetCurrentContext**(*void*)                                                               | HGLRC [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)(*VOID*)      |
| GLXDrawable **glXGetCurrentDrawable**(*void*)                                                             | HDC [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)(*VOID*)                  |
| Bool **glXMakeCurrent**( Exibir *\* dpy,* desenho GLXDrawable , GLXContext *ctx*)                              | BOOL [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)( HDC *hdc,* HGLRC *hglrc*) |



 

Os tipos de retorno e outros tipos têm nomes diferentes no Sistema de JanelaS X do que no Windows. Você pode pesquisar ocorrências de GLXContext para ajudar a encontrar partes do seu código que precisam ser portadas.

As seções a seguir comparam exemplos de código de contexto de renderização em um programa sistema de janela X e o mesmo código depois que ele é portado para Windows.

Para obter mais informações sobre contextos de renderização, consulte [Contextos de renderização.](rendering-contexts.md)

 

 




