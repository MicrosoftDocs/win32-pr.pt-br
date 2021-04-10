---
title: Advertência de profundidade de portabilidade e comandos de neblina
description: Advertência de profundidade de portabilidade e comandos de neblina
ms.assetid: 16982d11-88a1-4a35-960f-28f10491e0ac
keywords:
- Portabilidade do íris GL, advertência de profundidade
- portando do íris GL, Depth advertência
- portando para OpenGL do íris GL, Depth advertência
- Portabilidade OpenGL do íris GL, Depth advertência
- Portabilidade do íris GL, neblina
- portando do íris GL, neblina
- portando para OpenGL do íris GL, neblina
- Portabilidade OpenGL do íris GL, neblina
- advertência de profundidade
- neblina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd9f65a29e0ae594bf9344cd960d3fc2b9aa646
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160207"
---
# <a name="porting-depth-cueing-and-fog-commands"></a>Advertência de profundidade de portabilidade e comandos de neblina

Ao portar comandos de profundidade-advertência e sombra, tenha os seguintes pontos em mente:

-   A chamada do íris GL, **fogvertex**, define um modo e os parâmetros que afetam esse modo. No OpenGL, você chama [**glFog**](glfog.md) uma vez para definir o modo e, em seguida, duas vezes ou mais para definir vários parâmetros.
-   No OpenGL, advertência de profundidade não é um recurso separado. Use a neblina linear em vez de profundidade advertência. (Esta seção fornece um exemplo de como fazer isso.) As seguintes funções do íris GL não têm equivalente a OpenGL direto:

    **depthcue**

    **lRGBrange**

    **lshaderange**

    **getdcm**

-   Para ajustar a qualidade da neblina, use [**glHint**](glhint.md)(dica de neblina do GL \_ \_ ).

A tabela a seguir lista as funções do íris GL para gerenciar a neblina e suas funções OpenGL equivalentes.



| Função GL de íris         | Função OpenGL                                     | Significado                           |
|--------------------------|-----------------------------------------------------|-----------------------------------|
| **fogvertex**            | [**glFog**](glfog.md)                              | Define vários parâmetros de neblina.      |
| **fogvertex**(FG \_ ligado)  | [**glEnable**](glenable.md) (neblina do GL \_ )            | Ativa a neblina.                     |
| **fogvertex**(FG \_ desativado) | [**glDisable**](gldisable.md) (neblina do GL \_ )          | Desativa a neblina.                    |
| **depthcue**             | [**glFog**](glfog.md) (GL \_ neblina \_ mod, GL \_ linear) | Usa a neblina linear para advertência de profundidade. |



 

A tabela a seguir lista os parâmetros que você pode passar para **glFog**.



| Parâmetro de neblina    | Significado                       | Padrão                  |
|------------------|-------------------------------|--------------------------|
| \_densidade de neblina GL \_ | Densidade da neblina.                  | 1,0                      |
| \_início da neblina do GL \_   | Perto da distância para a neblina linear. | 0.0                      |
| \_fim da neblina do GL \_     | Distância distante para a neblina linear.  | 1,0                      |
| \_índice de neblina GL \_   | Índice de cores de neblina.              | 0.0                      |
| \_cor da neblina do GL \_   | Cor RGBA de neblina.               | (0, 0, 0, 0)             |
| \_modo de neblina GL \_    | Modo de neblina.                     | Confira a tabela a seguir. |



 

O parâmetro de densidade de neblina do OpenGL difere do um no íris GL. Eles estão relacionados da seguinte maneira:

-   Se *fogMode* = EXP2
     

    *openGLfogDensity* = (*irisGLfogDensity* ) ( **sqrt** ( **log** (1/255)))
-   Se *fogMode* = exp
     

    *openGLfogDensity* = (*irisGLfogDensity* ) ( **log** (1/255))

em que **sqrt** é a operação raiz quadrada, o **log** é o logaritmo natural, *irisGLfogDensity* é a densidade de neblina do íris GL e *OpenGLfogDensity* é a densidade de neblina do OpenGL.

Para alternar entre calcular a sombra no modo por pixel e por vértice, use [**glHint**](glhint.md)( \_ dica de neblina do GL \_ , *hintmode*). Dois modos de dica estão disponíveis:

-   RAZÃO \_ de cálculo de neblina por pixel mais interessante
-   \_Redirecionamento rápido por vértice de cálculo de neblina

A tabela a seguir lista os modos de neblina do íris GL e seus equivalentes em OpenGL.



| Modo de neblina GL de íris                       | Modo de neblina OpenGL | Modo de dica                         | Significado                                  |
|----------------------------------------|-----------------|-----------------------------------|------------------------------------------|
| FG \_ VTX \_ exp, FG \_ PIX \_ exp<br/>   | GL \_ exp         | GL \_ mais rápido, GL mais \_ interessante<br/> | Modo de neblina pesada (padrão).                |
| FG \_ VTX \_ EXP2, FG \_ PIX \_ EXP2<br/> | \_EXP2 GL        | GL \_ mais rápido, GL mais \_ interessante<br/> | Modo de criações.                               |
| FG \_ VTX \_ Lin, FG \_ PIX \_ Lin<br/>   | GL \_ linear      | GL \_ mais rápido, GL mais \_ interessante<br/> | Modo de neblina linear. (Use para advertência de profundidade.) |



 

O exemplo de código a seguir demonstra advertência de profundidade em OpenGL:


```C++
/* 
 *  depthcue.c 
 *  This program draws a wire frame model, which uses 
 *  intensity (brightness) to give clues to distance 
 *  Fog is used to achieve this effect 
 */ 
#include <GL/gl.h> 
#include <GL/glu.h> 
#include "aux.h" 
 
/*  Initialize linear fog for depth cueing 
 */ 
void myinit(void) 
{ 
    GLfloat fogColor[4] = {0.0, 0.0, 0.0, 1.0}; 
 
    glEnable(GL_FOG); 
    glFogi (GL_FOG_MODE, GL_LINEAR); 
    glHint (GL_FOG_HINT, GL_NICEST);  /*  per pixel  */ 
    glFogf (GL_FOG_START, 3.0); 
    glFogf (GL_FOG_END, 5.0); 
    glFogfv (GL_FOG_COLOR, fogColor); 
    glClearColor(0.0, 0.0, 0.0, 1.0); 
 
    glDepthFunc(GL_LEQUAL); 
    glEnable(GL_DEPTH_TEST); 
    glShadeModel(GL_FLAT); 
} 
 
/*  display() draws an icosahedron 
 */ 
void display(void) 
{ 
    glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT); 
    glColor3f (1.0, 1.0, 1.0); 
    auxWireIcosahedron(1.0); 
    glFlush(); 
} 
 
void myReshape(GLsizei w, GLsizei h) 
{ 
    glViewport(0, 0, w, h); 
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective (45.0, (GLfloat) w/(GLfloat) h, 3.0, 5.0); 
    glMatrixMode(GL_MODELVIEW); 
    glLoadIdentity (); 
    glTranslatef (0.0, 0.0, -4.0); /*move object into view*/ 
} 
/*  Main Loop 
 */ 
int main(int argc, char** argv) 
{ 
    auxInitDisplayMode (AUX_SINGLE | AUX_RGBA | AUX_DEPTH); 
    auxInitPosition (0, 0, 400, 400); 
    auxInitWindow (argv[0]); 
    myinit(); 
    auxReshapeFunc (myReshape); 
    auxMainLoop(display); 
}
```



 

 





