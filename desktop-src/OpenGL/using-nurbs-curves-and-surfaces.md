---
title: Usando curvas e superfícies NURBS
description: As funções de B-spline racional não uniformes (NURBS) fornecem descrições gerais e poderosas de curvas e superfícies em duas e três dimensões, convertendo as curvas e superfícies em avaliadores OpenGL.
ms.assetid: 0b55659d-9fa2-47fc-ae15-0c296bd94dcb
keywords:
- Utilitário OpenGL (GLU), B-spline racional não uniforme (NURBS)
- GLU (utilitário OpenGL), B-spline racional não uniforme (NURBS)
- B-spline racional não uniforme (NURBS) OpenGL
- NURBS (B-spline racional não uniforme) OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f85e9a2045c417007c34d714ae6635ebfaf1180
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291989"
---
# <a name="using-nurbs-curves-and-surfaces"></a>Usando curvas e superfícies NURBS

As funções de B-spline racional não uniformes (NURBS) fornecem descrições gerais e poderosas de curvas e superfícies em duas e três dimensões, convertendo as curvas e superfícies em avaliadores OpenGL. As funções NURBS podem representar geometria em vários sistemas de design mecânico auxiliados por computador. Eles podem renderizar curvas e superfícies em uma variedade de estilos, e podem lidar automaticamente com a subdivisão adaptável que tessellates o domínio em triângulos menores em regiões de alta curvatura e bordas de silhueta próxima. As funções NURBS se enquadram nas categorias a seguir.

Para gerenciar um objeto NURBS, use:

-   [**gluNewNurbsRenderer**](glunewnurbsrenderer.md) (criar um objeto NURBS)
-   [**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) (exclui um objeto NURBS)
-   [*gluNurbsCallback*](glunurbs.md) (estabelece uma função de tratamento de erros)

Para especificar as curvas desejadas, use:

-   [**gluBeginCurve**](glubegincurve.md)
-   [**gluNurbsCurve**](glunurbscurve.md)
-   [**gluEndCurve**](gluendcurve.md)

Para especificar as superfícies desejadas, use:

-   [**gluBeginSurface**](glubeginsurface.md)
-   [**gluNurbsSurface**](glunurbssurface.md)
-   [**gluEndSurface**](gluendsurface.md)

Você também pode especificar uma região de corte, que define um subconjunto do domínio de superfície NURBS a ser avaliado para que você possa criar superfícies com limites suaves ou que contenham buracos.

Para especificar a região de corte, use:

-   [**gluBeginTrim**](glubegintrim.md)
-   [**gluPwlCurve**](glupwlcurve.md)
-   [**gluNurbsCurve**](glunurbscurve.md)
-   [**gluEndTrim**](gluendtrim.md)

Assim como acontece com objetos Quadric, você pode controlar como as curvas NURBS e as superfícies são renderizadas. Você pode determinar:

-   Se deve-se descartar uma curva ou superfície cujo controle poliedde está fora do visor atual.
-   O comprimento máximo (em pixels) das bordas dos polígonos usados para renderizar curvas e superfícies.
-   Se você vai pegar a matriz de projeção, a matriz modelview e o visor do servidor OpenGL ou fornecê-las explicitamente com [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md).

Use [**gluNurbsProperty**](glunurbsproperty.md) para definir essas propriedades ou use os valores padrão. Você pode consultar um objeto NURBS sobre seu estilo de renderização com [**gluGetNurbsProperty**](glugetnurbsproperty.md).

 

 




