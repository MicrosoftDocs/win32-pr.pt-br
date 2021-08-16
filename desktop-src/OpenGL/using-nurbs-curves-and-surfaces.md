---
title: Usando curvas e superfícies N LTDAS
description: As funções N UNIFORM Rational B-Spline (N DIMENSIONS) fornecem descrições gerais e poderosas de curvas e superfícies em duas e três dimensões, convertendo as curvas e superfícies em avaliadores OpenGL.
ms.assetid: 0b55659d-9fa2-47fc-ae15-0c296bd94dcb
keywords:
- Utilitário OpenGL (GLU), N UNIFORM Rational B-Spline (NALTERS)
- GLU (Utilitário OpenGL), N UNIFORM Rational B-Spline (N GLUS)
- OpenGL não uniforme De spline B (NALTERS)
- N UNIFORMS (N-Uniform Rational B-Spline) OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c1b366571be7a9210576e78540c77970667aca2f37ec8a092de07edb97493d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932766"
---
# <a name="using-nurbs-curves-and-surfaces"></a>Usando curvas e superfícies N LTDAS

As funções N UNIFORM Rational B-Spline (N DIMENSIONS) fornecem descrições gerais e poderosas de curvas e superfícies em duas e três dimensões, convertendo as curvas e superfícies em avaliadores OpenGL. As funções N LTDAS podem representar geometria em muitos sistemas de design mecânico auxiliados por computador. Eles podem renderizar curvas e superfícies em uma variedade de estilos e podem lidar automaticamente com a subdivisão adaptável que mosaica o domínio em triângulos menores em regiões de alta curvatura e bordas de paleta próximas. As funções N LTDA se enquadram nas categorias a seguir.

Para gerenciar um objeto NALTERS, use:

-   [**gluNewNheisRenderer**](glunewnurbsrenderer.md) (criar um objeto NALTERS)
-   [**gluDeleteNdelasRenderer**](gludeletenurbsrenderer.md) (exclui um objeto NALTERS)
-   [*gluNaltsCallback*](glunurbs.md) (estabelece uma função de tratamento de erro)

Para especificar as curvas desejadas, use:

-   [**gluBeginCurve**](glubegincurve.md)
-   [**gluNagisCurve**](glunurbscurve.md)
-   [**gluEndCurve**](gluendcurve.md)

Para especificar as superfícies desejadas, use:

-   [**gluBeginSurface**](glubeginsurface.md)
-   [**gluNagisSurface**](glunurbssurface.md)
-   [**gluEndSurface**](gluendsurface.md)

Você também pode especificar uma região de corte, que define um subconjunto do domínio de superfície NALTERS a ser avaliado para que você possa criar superfícies que tenham limites suaves ou que contenham orifícios.

Para especificar a região de corte, use:

-   [**gluBeginTrim**](glubegintrim.md)
-   [**gluPwlCurve**](glupwlcurve.md)
-   [**gluNagisCurve**](glunurbscurve.md)
-   [**gluEndTrim**](gluendtrim.md)

Assim como com objetos quadc, você pode controlar como as curvas e superfícies N LTDS são renderizadas. Você pode determinar:

-   Se uma curva ou superfície deve ser descartada cujo poliedro de controle está fora do viewport atual.
-   O comprimento máximo (em pixels) de bordas de polígonos usados para renderizar curvas e superfícies.
-   Se você vai pegar a matriz de projeção, a matriz de modelview e o viewport do servidor OpenGL ou fornecer a eles explictly [**com gluLoadSamplingMatrices**](gluloadsamplingmatrices.md).

Use [**gluNagisProperty**](glunurbsproperty.md) para definir essas propriedades ou use os valores padrão. Você pode consultar um objeto NGETS sobre seu estilo de renderização [**com gluGetNariaProperty**](glugetnurbsproperty.md).

 

 




