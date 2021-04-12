---
title: Portando curvas NURBS
description: As funções OpenGL para desenhar curvas NURBS são muito semelhantes às funções do íris GL. Você especifica sequências de nós e pontos de controle usando uma função gluNurbsCurve, que deve estar contida em um par gluBeginCurve/gluEndCurve.
ms.assetid: 954e8029-06bd-4072-9b84-53ecba1d05da
keywords:
- Portabilidade do íris GL, curvas NURBS
- portando do íris GL, curvas NURBS
- portando para OpenGL do íris GL, curvas NURBS
- Portabilidade do OpenGL do íris GL, curvas NURBS
- Curvas NURBS
- curvas
- Portabilidade do íris GL, curvas
- portando do íris GL, curvas
- portando para OpenGL do íris GL, curvas
- Portabilidade OpenGL do íris GL, curvas
- NURBS (B racional não uniforme-spline)
- B-spline racional não uniforme (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f539e466ce8ade17d135c9369e1f641831792e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364176"
---
# <a name="porting-nurbs-curves"></a>Portando curvas NURBS

As funções OpenGL para desenhar curvas NURBS são muito semelhantes às funções do íris GL. Você especifica sequências de nós e pontos de controle usando uma função [**gluNurbsCurve**](glunurbscurve.md) , que deve estar contida em um par [**gluBeginCurve**](glubegincurve.md)  /  [**gluEndCurve**](gluendcurve.md) .

A tabela a seguir lista as funções do íris GL para desenhar curvas NURBS e suas funções OpenGL equivalentes.



| Função GL de íris | Função OpenGL                        | Significado                     |
|------------------|----------------------------------------|-----------------------------|
| **bgncurve**     | [**gluBeginCurve**](glubegincurve.md) | Inicia uma definição de curva.  |
| **nurbscurve**   | [**gluNurbsCurve**](glunurbscurve.md) | Especifica atributos de curva. |
| **curva de fim**     | [**gluEndCurve**](gluendcurve.md)     | Termina uma definição de curva.    |



 

Associe as coordenadas de posição, textura e cor apresentando cada uma delas como um **gluNurbsCurve** separado dentro do par de início/término. Você pode não fazer mais do que uma chamada para **gluNurbsCurve** para cada parte dos dados de cor, posição e textura em um único par **gluBeginCurve/gluEndCurve** . Você deve fazer exatamente uma chamada para descrever a posição da curva (uma descrição GL \_ MAP1 \_ Vertex \_ 3 ou GL \_ MAP1 \_ Vertex \_ 4). Quando você chama **gluEndCurve**, a curva é mosaico em segmentos de linha e, em seguida, renderizada.

A tabela a seguir lista os tipos de curva íris GL e OpenGL NURBS.



| Tipo de GL de íris | Tipo OpenGL                  | Significado                                 |
|--------------|------------------------------|-----------------------------------------|
| N \_ V3D       | GL \_ MAP1 \_ Vertex \_ 3          | Curva polinomial.                       |
| N \_ V3DR      | MAP1 do GL de \_ \_ vértice \_ 4          | Curva racional.                         |
|              | GL \_ MAP1 \_ Texture \_ coord\_\* | Pontos de controle são coordenadas de textura. |
|              | GL \_ MAP1 \_ normal             | Os pontos de controle são normais.             |



 

Para obter mais informações sobre os tipos de avaliadores disponíveis, consulte [**glMap1**](glmap1.md).

??

 

 




