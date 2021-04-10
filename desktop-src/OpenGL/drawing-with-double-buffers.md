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
# <a name="drawing-with-double-buffers"></a>Desenho com buffers duplos

Buffers duplos suavizam a transição entre uma imagem e outra na tela. Os buffers de permuta normalmente são fornecidos no final de uma sequência de comandos de desenho. Por padrão, a implementação da Microsoft do OpenGL no Windows desenha-se para o buffer fora da tela; Quando o desenho for concluído, você chamará a função [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) para copiar o buffer fora da tela para o buffer na tela. O exemplo de código a seguir se prepara para desenhar, chama uma função de desenho e, em seguida, copia a imagem concluída na tela se houver buffer duplo disponível.


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



O exemplo de código a seguir obtém um contexto de dispositivo de janela, renderiza uma cena, copia a imagem na tela (para mostrar a renderização) e, em seguida, libera o contexto do dispositivo.


```C++
hdc = GetDC(hwnd); 
mySceneRenderingFunction(); 
SwapBuffers(hdc); 
ReleaseDC(hWnd, hdc);
```



 

 




