---
title: Desenho com buffers duplos
description: Buffers duplos suavizam a transição entre uma imagem e outra na tela.
ms.assetid: 10801cc7-d26c-4bfd-95c0-f352a1c7a1f5
keywords:
- OpenGL no Windows, buffers duplos
- buffers duplos OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbe52d427467b2a6e460ea56a9e72e580ea6f97d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292706"
---
# <a name="drawing-with-double-buffers"></a><span data-ttu-id="70814-105">Desenho com buffers duplos</span><span class="sxs-lookup"><span data-stu-id="70814-105">Drawing with Double Buffers</span></span>

<span data-ttu-id="70814-106">Buffers duplos suavizam a transição entre uma imagem e outra na tela.</span><span class="sxs-lookup"><span data-stu-id="70814-106">Double buffers smooth the transition between one image and another on the screen.</span></span> <span data-ttu-id="70814-107">Os buffers de permuta normalmente são fornecidos no final de uma sequência de comandos de desenho.</span><span class="sxs-lookup"><span data-stu-id="70814-107">Swapping buffers typically comes at the end of a sequence of drawing commands.</span></span> <span data-ttu-id="70814-108">Por padrão, a implementação da Microsoft do OpenGL no Windows desenha-se para o buffer fora da tela; Quando o desenho for concluído, você chamará a função [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) para copiar o buffer fora da tela para o buffer na tela.</span><span class="sxs-lookup"><span data-stu-id="70814-108">By default, the Microsoft implementation of OpenGL in Windows draws to the off-screen buffer; when drawing is complete, you call the [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) function to copy the off-screen buffer to the on-screen buffer.</span></span> <span data-ttu-id="70814-109">O exemplo de código a seguir se prepara para desenhar, chama uma função de desenho e, em seguida, copia a imagem concluída na tela se houver buffer duplo disponível.</span><span class="sxs-lookup"><span data-stu-id="70814-109">The following code sample prepares to draw, calls a drawing function, and then copies the completed image on to the screen if double buffering is available.</span></span>


```C++
void myRedraw(void) 
{ 
    // set up for drawing commands  
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective(45, 1.0, 0.1, 100.0); 
 
    // draw our objects  
    myDrawAllObjects(GL_FALSE); 
 
    // if we're double-buffering ...  
    if (bDoubleBuffering)  
 
        // ...draw the copied image to the screen  
        SwapBuffers(hdc); 
}
```



<span data-ttu-id="70814-110">O exemplo de código a seguir obtém um contexto de dispositivo de janela, renderiza uma cena, copia a imagem na tela (para mostrar a renderização) e, em seguida, libera o contexto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="70814-110">The following code sample obtains a window device context, renders a scene, copies the image to the screen (to show the rendering), and then releases the device context.</span></span>


```C++
hdc = GetDC(hwnd); 
mySceneRenderingFunction(); 
SwapBuffers(hdc); 
ReleaseDC(hWnd, hdc);
```



 

 




