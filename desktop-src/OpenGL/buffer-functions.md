---
title: Funções de buffer
description: Para copiar o conteúdo de um buffer fora da tela para um buffer na tela, chame SwapBuffers.
ms.assetid: 605eba4e-ee38-4e62-adf8-1b7894030cb0
keywords:
- Funções WGL, buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96b03a12cd07b76d1329f51cc982508c707e011701b072a42b099df05327842d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618587"
---
# <a name="buffer-functions"></a>Funções de buffer

Para copiar o conteúdo de um buffer fora da tela para um buffer na tela, [**chame SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers). A **função SwapBuffers** leva um handle para um contexto de dispositivo. O formato de pixel atual para o contexto do dispositivo especificado deve incluir um buffer de fundo. Por padrão, o buffer de fundo está fora da tela e o buffer frontal está na tela.

> [!Note]  
> A **função SwapBuffers** não troca realmente o conteúdo dos dois buffers, mas copia o conteúdo de um buffer para outro. O conteúdo do buffer fora da tela é indefinido após uma chamada para **SwapBuffers.** Portanto, o resultado de duas chamadas consecutivas para **SwapBuffers** é indefinido.

 

A ilustração a seguir mostra como o conteúdo dos buffers é copiado ao chamar **SwapBuffers**.

![Diagrama mostrando os resultados indefinido de chamadas consecutivas para a função SwapBuffers.](images/opengl00.png)

Várias funções principais do OpenGL também gerenciam buffers. A [**função glDrawBuffer**](gldrawbuffer.md) é a mais relevante para o buffer duplo; ele especifica o framebuffer ou buffers em que o OpenGL se desenha.

As seguintes funções também afetam buffers:

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

 

 




