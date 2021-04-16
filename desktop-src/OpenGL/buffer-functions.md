---
title: Funções de buffer
description: Para copiar o conteúdo de um buffer fora da tela para um buffer na tela, chame SwapBuffers.
ms.assetid: 605eba4e-ee38-4e62-adf8-1b7894030cb0
keywords:
- Funções WGL, buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a93858b8085171a9139bc5ab329e531ddbb699
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105757750"
---
# <a name="buffer-functions"></a>Funções de buffer

Para copiar o conteúdo de um buffer fora da tela para um buffer na tela, chame [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers). A função **SwapBuffers** usa um identificador para um contexto de dispositivo. O formato de pixel atual para o contexto de dispositivo especificado deve incluir um buffer de fundo. Por padrão, o buffer de fundo está fora da tela e o buffer frontal está na tela.

> [!Note]  
> A função **SwapBuffers** não troca de fato o conteúdo dos dois buffers, mas copia o conteúdo de um buffer para outro. O conteúdo do buffer fora da tela é indefinido após uma chamada para **SwapBuffers**. Assim, o resultado de duas chamadas consecutivas para **SwapBuffers** é indefinido.

 

A ilustração a seguir mostra como o conteúdo dos buffers é copiado ao chamar **SwapBuffers**.

![Diagrama mostrando os resultados indefinidos de chamadas consecutivas para a função SwapBuffers.](images/opengl00.png)

Várias funções de núcleo OpenGL também gerenciam buffers. A função [**glDrawBuffer**](gldrawbuffer.md) é a mais relevante para o buffer duplo; Ele especifica o framebuffer ou os buffers que o OpenGL desenha.

As funções a seguir também afetam os buffers:

-   [**glReadBuffer**](glreadbuffer.md)
-   [**glReadPixels**](glreadpixels.md)
-   [**glCopyPixels**](glcopypixels.md)
-   [**glAccum**](glaccum.md)
-   [**glColorMask**](glcolormask.md)
-   [**glDepthMask**](gldepthmask.md)
-   [**glIndexMask**](glindexmask.md)
-   [**glStencilMask**](glstencilmask.md)
-   [**glClearAccum**](glclearaccum.md)
-   [**glClearColor**](glclearcolor.md)
-   [**glClearDepth**](glcleardepth.md)
-   [**glClearIndex**](glclearindex.md)
-   [**glClearStencil**](glclearstencil.md)

 

 




