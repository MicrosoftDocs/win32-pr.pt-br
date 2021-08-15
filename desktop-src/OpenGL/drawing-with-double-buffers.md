---
title: Desenhando com buffers duplos
description: Buffers duplos suavizam a transição entre uma imagem e outra na tela.
ms.assetid: 10801cc7-d26c-4bfd-95c0-f352a1c7a1f5
keywords:
- OpenGL no Windows, buffers duplos
- openGL de buffers duplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133a6e0794eb903215411016aeff14e3426854dcddc3a60bcfb2ba318481bee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361386"
---
# <a name="drawing-with-double-buffers"></a>Desenhando com buffers duplos

Buffers duplos suavizam a transição entre uma imagem e outra na tela. A troca de buffers normalmente vem no final de uma sequência de comandos de desenho. Por padrão, a implementação da Microsoft do OpenGL no Windows desenha para o buffer fora da tela; Quando o desenho for concluído, você chamará a [**função SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) para copiar o buffer fora da tela para o buffer na tela. O exemplo de código a seguir se prepara para desenhar, chama uma função de desenho e copia a imagem concluída na tela se o buffer duplo estiver disponível.


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



O exemplo de código a seguir obtém um contexto de dispositivo de janela, renderiza uma cena, copia a imagem para a tela (para mostrar a renderização) e, em seguida, libera o contexto do dispositivo.


```C++
hdc = GetDC(hwnd); 
mySceneRenderingFunction(); 
SwapBuffers(hdc); 
ReleaseDC(hWnd, hdc);
```



 

 




