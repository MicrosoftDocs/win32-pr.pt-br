---
title: Portando curvas N LTDA
description: As funções OpenGL para desenhar curvas N LTDAS são muito semelhantes às funções IRIS GL. Especifique sequências de transferência e pontos de controle usando uma função gluN ltda, que deve estar contida em um par gluBeginCurve/gluEndCurve.
ms.assetid: 954e8029-06bd-4072-9b84-53ecba1d05da
keywords:
- Portação IRIS GL, curvas NALTERS
- portando de íris GL, curvas NALTERS
- portando para OpenGL de IRIS GL, curvas NALTERS
- Portação openGL de IRIS GL, curvas N LTDA
- Curvas N LTDAS
- curvas
- Portação IRIS GL, curvas
- portando de IRIS GL, curvas
- portando para OpenGL de IRIS GL, curvas
- Portação openGL de IRIS GL, curvas
- N UNIFORMS (B-Spline racional não uniforme)
- N UNIFORM Rational B-Spline (NALTERS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9aa43bcc40c2b6a93eb5690abe4265f792a58a2520e579d536a08520ca4f29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132395"
---
# <a name="porting-nurbs-curves"></a>Portando curvas N LTDA

As funções OpenGL para desenhar curvas N LTDAS são muito semelhantes às funções IRIS GL. Você especifica sequências de sequências de transferência e pontos de controle usando uma [**função gluNrecisCurve,**](glunurbscurve.md) que deve estar contida em um [**par gluBeginCurve**](glubegincurve.md)  /  [**gluEndCurve.**](gluendcurve.md)

A tabela a seguir lista as funções IRIS GL para desenhar curvas NALTERS e suas funções Equivalentes do OpenGL.



| Função IRIS GL | Função OpenGL                        | Significado                     |
|------------------|----------------------------------------|-----------------------------|
| **bgncurve**     | [**gluBeginCurve**](glubegincurve.md) | Inicia uma definição de curva.  |
| **niascurve**   | [**gluNagisCurve**](glunurbscurve.md) | Especifica atributos de curva. |
| **endcurve**     | [**gluEndCurve**](gluendcurve.md)     | Termina uma definição de curva.    |



 

Associe as coordenadas de posição, textura e cor apresentando cada uma delas como **um gluNcorrescurve** separado dentro do par de início/término. Você não pode fazer mais de uma chamada para **gluN gluCurve** para cada parte dos dados de cor, posição e textura dentro de um único par **gluBeginCurve/gluEndCurve.** Você deve fazer exatamente uma chamada para descrever a posição da curva (uma descrição GL \_ MAP1 \_ VERTEX 3 ou \_ GL \_ MAP1 \_ VERTEX \_ 4). Quando você chama **gluEndCurve**, a curva é mosaica em segmentos de linha e renderizada.

A tabela a seguir lista os tipos de curva IRIS GL e OpenGL N LTDS.



| Tipo IRIS GL | Tipo OpenGL                  | Significado                                 |
|--------------|------------------------------|-----------------------------------------|
| N \_ V3D       | GL \_ MAP1 \_ VÉRTICE \_ 3          | Curva polinomial.                       |
| N \_ V3DR      | GL \_ MAP1 \_ VÉRTICE \_ 4          | Curva racional.                         |
|              | GL \_ MAP1 \_ TEXTURE \_ COORD\_\* | Os pontos de controle são coordenadas de textura. |
|              | GL \_ MAP1 \_ NORMAL             | Os pontos de controle são normais.             |



 

Para obter mais informações sobre os tipos de avaliador disponíveis, consulte [**glMap1**](glmap1.md).

??

 

 




