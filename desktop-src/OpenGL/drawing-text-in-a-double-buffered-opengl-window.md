---
title: Desenho de texto em uma janela Double-Buffered OpenGL
description: Você desenha o texto em uma janela OpenGL com buffer duplo criando listas de exibição para os caracteres selecionados em uma fonte e, em seguida, executando a lista de exibição apropriada para cada caractere que você deseja desenhar.
ms.assetid: 59ac0414-a845-4f40-be9c-9962fd1585f6
keywords:
- OpenGL no Windows, texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b0bf4cc99a1806d734ccde5cfae98f4d367da13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637050"
---
# <a name="drawing-text-in-a-double-buffered-opengl-window"></a><span data-ttu-id="7e3fc-104">Desenho de texto em uma janela Double-Buffered OpenGL</span><span class="sxs-lookup"><span data-stu-id="7e3fc-104">Drawing Text in a Double-Buffered OpenGL Window</span></span>

<span data-ttu-id="7e3fc-105">Você desenha o texto em uma janela OpenGL com buffer duplo criando listas de exibição para os caracteres selecionados em uma fonte e, em seguida, executando a lista de exibição apropriada para cada caractere que você deseja desenhar.</span><span class="sxs-lookup"><span data-stu-id="7e3fc-105">You draw text in a double-buffered OpenGL window by creating display lists for selected characters in a font, and then executing the appropriate display list for each character you want to draw.</span></span> <span data-ttu-id="7e3fc-106">O exemplo de código a seguir cria um contexto de renderização, desenha um triângulo vermelho e o rotula com texto.</span><span class="sxs-lookup"><span data-stu-id="7e3fc-106">The following code sample creates a rendering context, draws a red triangle, and then labels it with text.</span></span> <span data-ttu-id="7e3fc-107">Para este código de exemplo, presumimos que haja um contexto de dispositivo, com um formato de fonte e pixel.</span><span class="sxs-lookup"><span data-stu-id="7e3fc-107">For this sample code, we assume that there is a device context, with a font and pixel format.</span></span>


```C++
// create an OpenGL rendering context  
hglrc = wglCreateContext(hdc); 
 
// make it this thread's current rendering context  
wglMakeCurrent(hdc, hglrc); 
 
// make the color a deep blue hue  
glClearColor(0.0F, 0.0F, 0.4F, 1.0F); 
 
// make the shading smooth 
glShadeModel(GL_SMOOTH); 
 
// clear the color buffers  
glClear(GL_COLOR_BUFFER_BIT); 
 
// specify a red triangle  
glBegin(GL_TRIANGLES); 
    glColor3f(1.0F, 0.0F, 0.0F); 
    glVertex2f(10.0F, 10.0F); 
    glVertex2f(250.0F, 50.0F); 
    glVertex2f(105.0F, 280.0F); 
glEnd(); 
 
// create bitmaps for the device context font's first 256 glyphs  
wglUseFontBitmaps(hdc, 0, 256, 1000); 
 
// move bottom left, southwest of the red triangle  
glRasterPos2f(30.0F, 300.0F); 
 
// set up for a string-drawing display list call  
glListBase(1000); 
 
// draw a string using font display lists  
glCallLists(12, GL_UNSIGNED_BYTE, "Red Triangle"); 
 
// get all those commands to execute  
glFlush(); 
 
// delete our 256 glyph display lists  
glDeleteLists(1000, 256) ; 
 
// make the rendering context not current  
wglMakeCurrent (NULL, NULL) ; 
 
// release the device context  
ReleaseDC(hdc) ; 
 
// delete the rendering context  
wglDeleteContext(hglrc);
```



 

 




