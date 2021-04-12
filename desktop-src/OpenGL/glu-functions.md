---
title: Funções GLU
description: Funções GLU
ms.assetid: 8304a291-1a26-42bc-8887-386732980722
keywords:
- Funções de biblioteca GLU, OpenGL
- Referência OpenGL, funções de biblioteca GLU
- Biblioteca GLU, funções
- Utilitário OpenGL (GLU), funções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fae3ece873f4e1e015861f597c0d51ebfc3436de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363869"
---
# <a name="glu-functions"></a>Funções GLU

Esta seção inclui as páginas de referência, em ordem alfabética, para todas as funções de biblioteca do utilitário OpenGL. Para obter informações básicas sobre essas funções, consulte [biblioteca de utilitários OpenGL](opengl-utility-library.md).



| Função                                                                                           | Descrição                                                                                              |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**gluBeginCurve**](glubegincurve.md), [ **gluEndCurve**](gluendcurve.md)                         | Delimite uma definição de curva de B-spline racional não uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)). |
| [**gluBeginPolygon**](glubeginpolygon.md), [ **gluEndPolygon**](gluendpolygon.md)                 | Delimite uma descrição de polígono.                                                                           |
| [**gluBeginSurface**](glubeginsurface.md), [ **gluEndSurface**](gluendsurface.md)                 | Delimite uma definição de superfície NURBS.                                                                      |
| [**gluBeginTrim**](glubegintrim.md), [ **gluEndTrim**](gluendtrim.md)                             | Delimite uma definição de loop de aparagem NURBS.                                                                |
| [**gluBuild1DMipmaps**](glubuild1dmipmaps.md)                                                     | Cria mipmaps de 1 D.                                                                                     |
| [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)                                                     | Cria mipmaps 2D.                                                                                     |
| [**gluCylinder**](glucylinder.md)                                                                 | Desenha um cilindro.                                                                                        |
| [**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md)                                           | Destrói um objeto NURBS.                                                                                 |
| [**gluDeleteQuadric**](gludeletequadric.md)                                                       | Destrói um objeto Quadric.                                                                               |
| [**gluDeleteTess**](gludeletetess.md)                                                             | Destrói um objeto de mosaico.                                                                          |
| [**gluDisk**](gludisk.md)                                                                         | Desenha um disco.                                                                                            |
| [**gluErrorString**](gluerrorstring.md)                                                           | Produz uma cadeia de caracteres de erro de um código de erro OpenGL ou GLU. A cadeia de caracteres de erro é somente ANSI.                |
| [**gluGetNurbsProperty**](glugetnurbsproperty.md)                                                 | Recupera uma propriedade NURBS.                                                                              |
| [**gluGetString**](glugetstring.md)                                                               | Recupera uma cadeia de caracteres que descreve o número de versão do GLU ou as chamadas de extensão GLU com suporte.               |
| [**gluGetTessProperty**](glugettessproperty.md)                                                   | Recupera uma propriedade de objeto de mosaico.                                                                |
| [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md)                                         | Carrega a amostragem de NURBS e as matrizes de remoção.                                                               |
| [**gluLookAt**](glulookat.md)                                                                     | Define uma transformação de exibição.                                                                        |
| [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)                                                 | Cria um objeto NURBS.                                                                                  |
| [**gluNewQuadric**](glunewquadric.md)                                                             | Cria um objeto Quadric.                                                                                |
| [**gluNewTess**](glunewtess.md)                                                                   | Cria um objeto de mosaico.                                                                           |
| [**gluNextContour**](glunextcontour.md)                                                           | Marca o início de outra delimitação.                                                                  |
| [*gluNurbsCallback*](glunurbs.md)                                                                 | Define um retorno de chamada para um objeto NURBS.                                                                   |
| [**gluNurbsCurve**](glunurbscurve.md)                                                             | Define a forma de uma curva NURBS.                                                                      |
| [**gluNurbsProperty**](glunurbsproperty.md)                                                       | Define uma propriedade NURBS.                                                                                   |
| [**gluNurbsSurface**](glunurbssurface.md)                                                         | Define a forma de uma superfície NURBS.                                                                    |
| [**gluOrtho2D**](gluortho2d.md)                                                                   | Define uma matriz de projeção ortográfica 2D.                                                            |
| [**gluPartialDisk**](glupartialdisk.md)                                                           | Desenha um arco de um disco.                                                                                  |
| [**gluPerspective**](gluperspective.md)                                                           | Configura uma matriz de projeção em perspectiva.                                                                 |
| [**gluPickMatrix**](glupickmatrix.md)                                                             | Define uma região de separação.                                                                                |
| [**gluProject**](gluproject.md)                                                                   | Mapeia coordenadas de objeto para coordenadas de janela.                                                           |
| [**gluPwlCurve**](glupwlcurve.md)                                                                 | Descreve uma curva de corte de NURBS linear piecewise.                                                       |
| [*gluQuadricCallback*](gluquadric.md)                                                             | Define um retorno de chamada para um objeto Quadric.                                                                 |
| [**gluQuadricDrawStyle**](gluquadricdrawstyle.md)                                                 | Especifica o estilo de desenho desejado para quadrics.                                                           |
| [**gluQuadricNormals**](gluquadricnormals.md)                                                     | Especifica que tipo de Normals deve ser usado para quadrics.                                              |
| [**gluQuadricOrientation**](gluquadricorientation.md)                                             | Especifica a orientação interna ou externa para quadrics.                                                    |
| [**gluQuadricTexture**](gluquadrictexture.md)                                                     | Especifica se quadrics deve ser texturizado.                                                           |
| [**gluScaleImage**](gluscaleimage.md)                                                             | Dimensiona uma imagem para um tamanho arbitrário.                                                                    |
| [**gluSphere**](glusphere.md)                                                                     | Desenha uma esfera.                                                                                          |
| [**gluTessBeginContour**](glutessbegincontour.md), [ **gluTessEndContour**](glutessendcontour.md) | Delimite uma descrição de contorno.                                                                           |
| [**gluTessBeginPolygon**](glutessbeginpolygon.md), [ **gluTessEndPolygon**](glutessendpolygon.md) | Delimite uma descrição de polígono.                                                                           |
| [*gluTessCallback*](glutess.md)                                                                   | Define um retorno de chamada para um objeto de mosaico.                                                            |
| [**gluTessNormal**](glutessnormal.md)                                                             | Especifica um normal para um polígono.                                                                        |
| [**gluTessProperty**](glutessproperty.md)                                                         | Define a propriedade de um objeto de mosaico.                                                              |
| [**gluTessVertex**](glutessvertex.md)                                                             | Especifica um vértice em um polígono.                                                                         |
| [**gluUnProject**](gluunproject.md)                                                               | Mapeia coordenadas de janela para coordenadas de objeto.                                                           |



 

 

 




