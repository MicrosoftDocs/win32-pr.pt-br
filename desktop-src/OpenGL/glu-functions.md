---
title: Funções GLU
description: Funções GLU
ms.assetid: 8304a291-1a26-42bc-8887-386732980722
keywords:
- Funções de biblioteca OpenGL, GLU
- Referência de OpenGL, funções de biblioteca GLU
- Biblioteca GLU, funções
- Utilitário OpenGL (GLU), funções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4483b364d2d67daff0bbc04b9a30cd7cdb3059f3977f763b247f77be74d62f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777696"
---
# <a name="glu-functions"></a>Funções GLU

Esta seção inclui páginas de referência, em ordem alfabética, para todas as funções da Biblioteca do Utilitário OpenGL. Para obter informações em segundo plano sobre essas funções, consulte [Biblioteca do Utilitário OpenGL](opengl-utility-library.md).



| Função                                                                                           | Descrição                                                                                              |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**gluBeginCurve**](glubegincurve.md), [ **gluEndCurve**](gluendcurve.md)                         | Delimita uma definição de curva[NALTERS](using-nurbs-curves-and-surfaces.md)(Rational B-Spline ) não uniforme. |
| [**gluBeginPolygon**](glubeginpolygon.md), [ **gluEndPolygon**](gluendpolygon.md)                 | Delimita uma descrição de polígono.                                                                           |
| [**gluBeginSurface,**](glubeginsurface.md) [ **gluEndSurface**](gluendsurface.md)                 | Delimitar uma definição de superfície NALTERS.                                                                      |
| [**gluBeginTrim,**](glubegintrim.md) [ **gluEndTrim**](gluendtrim.md)                             | Delimita uma definição de loop de corte NALTERS.                                                                |
| [**gluBuild1DMipmaps**](glubuild1dmipmaps.md)                                                     | Cria mipmaps 1D.                                                                                     |
| [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)                                                     | Cria mipmaps 2D.                                                                                     |
| [**gluCylinder**](glucylinder.md)                                                                 | Desenha um cilindro.                                                                                        |
| [**gluDeleteNdelasRenderer**](gludeletenurbsrenderer.md)                                           | Destrói um objeto NALTERS.                                                                                 |
| [**gluDeleteQuadric**](gludeletequadric.md)                                                       | Destrói um objeto quadc.                                                                               |
| [**gluDeleteTess**](gludeletetess.md)                                                             | Destrói um objeto de mosaico.                                                                          |
| [**gluDisk**](gludisk.md)                                                                         | Desenha um disco.                                                                                            |
| [**gluErrorString**](gluerrorstring.md)                                                           | Produz uma cadeia de caracteres de erro de um código de erro OpenGL ou GLU. A cadeia de caracteres de erro é somente ANSI.                |
| [**gluGetNagisProperty**](glugetnurbsproperty.md)                                                 | Recupera uma propriedade NALTERS.                                                                              |
| [**gluGetString**](glugetstring.md)                                                               | Recupera uma cadeia de caracteres que descreve o número de versão do GLU ou chamadas de extensão GLU com suporte.               |
| [**gluGetTessProperty**](glugettessproperty.md)                                                   | Recupera uma propriedade de objeto de mosaico.                                                                |
| [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md)                                         | Carrega matrizes de amostragem e rebabalho N LTDA.                                                               |
| [**gluLookAt**](glulookat.md)                                                                     | Define uma transformação de exibição.                                                                        |
| [**gluNewNagisRenderer**](glunewnurbsrenderer.md)                                                 | Cria um objeto N LTDA.                                                                                  |
| [**gluNewQuadric**](glunewquadric.md)                                                             | Cria um objeto quadc.                                                                                |
| [**gluNewTess**](glunewtess.md)                                                                   | Cria um objeto de mosaico.                                                                           |
| [**gluNextContour**](glunextcontour.md)                                                           | Marca o início de outro contorno.                                                                  |
| [*gluNagisCallback*](glunurbs.md)                                                                 | Define um retorno de chamada para um objeto NALTERS.                                                                   |
| [**gluNagisCurve**](glunurbscurve.md)                                                             | Define a forma de uma curva N LTDA.                                                                      |
| [**gluNagisProperty**](glunurbsproperty.md)                                                       | Define uma propriedade N LTDA.                                                                                   |
| [**gluNagisSurface**](glunurbssurface.md)                                                         | Define a forma de uma superfície N LTDA.                                                                    |
| [**gluOrtho2D**](gluortho2d.md)                                                                   | Define uma matriz de projeção ortográfica 2D.                                                            |
| [**gluPartialDisk**](glupartialdisk.md)                                                           | Desenha um arco de um disco.                                                                                  |
| [**gluPerspective**](gluperspective.md)                                                           | Configura uma matriz de projeção de perspectiva.                                                                 |
| [**gluPickMatrix**](glupickmatrix.md)                                                             | Define uma região de escolha.                                                                                |
| [**gluProject**](gluproject.md)                                                                   | Mapas coordenadas de objeto para coordenadas de janela.                                                           |
| [**gluPwlCurve**](glupwlcurve.md)                                                                 | Descreve uma curva de corte NALTERS linear por parte.                                                       |
| [*gluQuadricCallback*](gluquadric.md)                                                             | Define um retorno de chamada para um objeto quadc.                                                                 |
| [**gluQuadricDrawStyle**](gluquadricdrawstyle.md)                                                 | Especifica o estilo de desenho desejado para os quadrics.                                                           |
| [**gluQuadricNormals**](gluquadricnormals.md)                                                     | Especifica que tipo de normal deve ser usado para quadrics.                                              |
| [**gluQuadricOrientation**](gluquadricorientation.md)                                             | Especifica a orientação interna ou externa para os quadrics.                                                    |
| [**gluQuadricTexture**](gluquadrictexture.md)                                                     | Especifica se os quadcs devem ser texturados.                                                           |
| [**gluScaleImage**](gluscaleimage.md)                                                             | Dimensiona uma imagem para um tamanho arbitrário.                                                                    |
| [**gluSphere**](glusphere.md)                                                                     | Desenha uma esfera.                                                                                          |
| [**gluTessBeginContour**](glutessbegincontour.md), [ **gluTessEndContour**](glutessendcontour.md) | Delimita uma descrição de contorno.                                                                           |
| [**gluTessBeginPolygon**](glutessbeginpolygon.md), [ **gluTessEndPolygon**](glutessendpolygon.md) | Delimita uma descrição de polígono.                                                                           |
| [*gluTessCallback*](glutess.md)                                                                   | Define um retorno de chamada para um objeto de mosaico.                                                            |
| [**gluTessNormal**](glutessnormal.md)                                                             | Especifica um normal para um polígono.                                                                        |
| [**gluTessProperty**](glutessproperty.md)                                                         | Define a propriedade de um objeto de mosaico.                                                              |
| [**gluTessVertex**](glutessvertex.md)                                                             | Especifica um vértice em um polígono.                                                                         |
| [**gluUnProject**](gluunproject.md)                                                               | Mapas janela coordena para coordenadas de objeto.                                                           |



 

 

 




