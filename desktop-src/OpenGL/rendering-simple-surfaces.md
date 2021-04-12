---
title: Renderizando superfícies simples
description: A biblioteca GLU inclui um conjunto de funções para desenhar várias superfícies simples (diferir, cilindros, discos e partes de discos) em uma variedade de estilos e orientações. Essas funções são descritas em detalhes no manual de referência do OpenGL.
ms.assetid: 403bdf8d-de4c-49e2-87d0-11109061b4c2
keywords:
- Utilitário OpenGL (GLU), superfícies simples
- GLU (utilitário OpenGL), superfícies simples
- superfícies simples OpenGL
- Utilitário OpenGL (GLU),
- GLU (utilitário OpenGL),
- por meio do OpenGL
- Utilitário OpenGL (GLU), cilindros
- GLU (utilitário OpenGL), cilindros
- cilindros OpenGL
- Utilitário OpenGL (GLU), discos
- GLU (utilitário OpenGL), discos
- discos OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab766c661f89cbdec30b3295dfef8dc85b59f7fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364475"
---
# <a name="rendering-simple-surfaces"></a>Renderizando superfícies simples

A biblioteca GLU inclui um conjunto de funções para desenhar várias superfícies simples (diferir, cilindros, discos e partes de discos) em uma variedade de estilos e orientações. Essas funções são descritas em detalhes no *manual de referência do OpenGL*.

**Para renderizar superfícies simples**

1.  Crie um objeto Quadric com [**gluNewQuadric**](glunewquadric.md).

    Para destruir esse objeto quando tiver terminado, use [**gluDeleteQuadric**](gludeletequadric.md).

2.  Especifique o estilo de renderização desejado, conforme listado abaixo, com a função apropriada (a menos que você esteja satisfeito com os valores padrão):
    -   Se os normais da superfície devem ser gerados e, nesse caso, se deve haver um normal por vértice ou um normal por face: [ **gluQuadricNormals**](gluquadricnormals.md)
    -   Se as coordenadas de textura devem ser geradas: [ **gluQuadricTexture**](gluquadrictexture.md)
    -   Qual lado do Quadric deve ser considerado o exterior e qual o interior: [ **gluQuadricOrientation**](gluquadricorientation.md)
    -   Se o Quadric deve ser desenhado como um conjunto de polígonos, linhas ou pontos: [ **gluQuadricDrawStyle**](gluquadricdrawstyle.md)
3.  Depois de especificar o estilo de renderização, invoque a função de renderização para o tipo desejado de objeto Quadric: [**gluSphere**](glusphere.md), [**gluCylinder**](glucylinder.md), [**gluDisk**](gludisk.md)ou [**gluPartialDisk**](glupartialdisk.md).

    Se ocorrer um erro durante a renderização, a função de tratamento de erros que você especificou com [*gluQuadricCallBack*](gluquadric.md) será invocada.

Use os argumentos *\* RADIUS*, *Height* e similar, em vez da função [**glScale**](glscale.md) , para dimensionar o quadrics, para que você não precise renormalizar qualquer normal de comprimento de unidade gerado. Para forçar cálculos de iluminação com uma granularidade mais refinada, especialmente se a especulação de material for alta, defina os argumentos *loops* e *pilhas* para valores diferentes de 1.

 

 




