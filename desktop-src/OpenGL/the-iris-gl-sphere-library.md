---
title: A biblioteca de Sphere do íris GL
description: O OpenGL não dá suporte à biblioteca de Sphere do íris GL. Você pode substituir suas chamadas de biblioteca de Sphere por rotinas quadrics da biblioteca GLU. Para obter mais informações sobre a biblioteca GLU, consulte o guia de programação Open GL e a biblioteca de utilitários OpenGL.
ms.assetid: 2b7e6a3d-d2d0-4b54-8dff-8c4d6b113007
keywords:
- Portabilidade do íris GL, biblioteca de Sphere
- portando do íris GL, biblioteca de Sphere
- portando para OpenGL do íris GL, biblioteca de Sphere
- Portabilidade do OpenGL do íris GL, biblioteca de Sphere
- funções de desenho, biblioteca de Sphere
- biblioteca de Sphere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586974c5874aee73121e536cbadca4564a18c250
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292349"
---
# <a name="the-iris-gl-sphere-library"></a>A biblioteca de Sphere do íris GL

O OpenGL não dá suporte à biblioteca de Sphere do íris GL. Você pode substituir suas chamadas de biblioteca de Sphere por rotinas quadrics da biblioteca GLU. Para obter mais informações sobre a biblioteca GLU, consulte o *Guia de programação Open GL* e a [biblioteca de utilitários OpenGL](opengl-utility-library.md).

A tabela a seguir lista as funções OpenGL quadrics.



| Função OpenGL                                        | Significado                                                          |
|--------------------------------------------------------|------------------------------------------------------------------|
| [**gluNewQuadric**](glunewquadric.md)                 | Cria um novo objeto Quadric.                                    |
| [**gluDeleteQuadric**](gludeletequadric.md)           | Exclui um objeto Quadric.                                        |
| [*gluQuadricCallback*](gluquadric.md)                 | Associa um retorno de chamada a um objeto Quadric, para tratamento de erros. |
| [**gluQuadricNormals**](gluquadricnormals.md)         | Especifica Normals: não há normalidades, uma por face ou uma por vértice.  |
| [**gluQuadricOrientation**](gluquadricorientation.md) | Especifica a direção de Normals: para fora ou para dentro.               |
| [**gluQuadricTexture**](gluquadrictexture.md)         | Ativa ou desativa a geração da coordenada de textura.                   |
| [**gluQuadricDrawstyle**](gluquadricdrawstyle.md)     | Especifica o estilo de desenho: polígonos, linhas, pontos e assim por diante.     |
| [**gluSphere**](glusphere.md)                         | Desenha uma esfera.                                                  |
| [**gluCylinder**](glucylinder.md)                     | Desenha um cilindro ou cone.                                        |
| [**gluPartialDisk**](glupartialdisk.md)               | Desenha um arco.                                                    |
| [**gluDisk**](gludisk.md)                             | Desenha um círculo ou disco.                                          |



 

Você pode usar um objeto Quadric para todos os quadrics que você deseja renderizar de maneiras semelhantes. O exemplo de código a seguir usa dois objetos Quadric para desenhar quatro quadrics, dois deles texturizados.


```C++
GLUquadricObj    *texturedQuad, *plainQuad; 
 
texturedQuad = gluNewQuadric(void); 
gluQuadricTexture(texturedQuad, GL_TRUE); 
gluQuadricOrientation(texturedQuad, GLU_OUTSIDE); 
gluQuadricDrawStyle(texturedQuad, GLU_FILL); 
 
plainQuad = gluNewQuadric(void); 
gluQuadricDrawStyle(plainQuad, GLU_LINE); 
 
glColor3f (1.0, 1.0, 1.0); 
 
gluSphere(texturedQuad, 5.0, 20, 20); 
glTranslatef(10.0, 10.0, 0.0); 
gluCylinder(texturedQuad, 2.5, 5, 5, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluDisk(plainQuad, 2.0, 5.0, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluSphere(plainQuad, 5.0, 20, 20);
```



 

 




