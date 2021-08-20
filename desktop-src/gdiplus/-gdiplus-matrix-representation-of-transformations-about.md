---
description: Uma matriz m&\# 215; n é um conjunto de números organizados em m linhas e n colunas. A ilustração a seguir mostra diversas matrizes.
ms.assetid: 62215ae0-b095-42b2-911c-aa7607a8b61a
title: Representação matricial de transformações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 122d59787038cd75a9806cac6cb0d225e8660eb13d7482d3ee1f47ff0732ca5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036654"
---
# <a name="matrix-representation-of-transformations"></a>Representação matricial de transformações

Uma matriz *m × n* é um conjunto de números organizados em *m* linhas e *n* colunas. A ilustração a seguir mostra diversas matrizes.

![ilustração mostrando seis matrizes de dimensões variadas](images/aboutgdip05-art04.png)

Você pode adicionar duas matrizes do mesmo tamanho ao adicionar elementos individuais. A ilustração a seguir mostra dois exemplos de adição de matriz.

![ilustração que mostra como executar a adição de matriz](images/aboutgdip05-art05.png)

Uma matriz *m × n* pode ser multiplicada por uma matriz *n × p* e o resultado é uma matriz *m × p* . O número de colunas da primeira matriz deve ser igual ao número de linhas da segunda. Por exemplo, uma matriz de 4 × 2 pode ser multiplicada por uma matriz de 2 × 3 para produzir uma matriz 4 × 3.

Os pontos no plano e as linhas e as colunas de uma matriz podem ser pensados como vetores. Por exemplo, (2, 5) é um vetor com dois componentes e (3, 7, 1) é um vetor com três componentes. O produto escalar de dois vetores é definido da seguinte maneira:

(a, b) • (c, d) = ac + bd

(a, b, c) • (d, e, f) = ad + be + cf

Por exemplo, o produto escalar (2, 3) e (5, 4) é (2)(5) + (3)(4) = 22. O produto escalar (2, 5, 1) e (4, 3, 1) é (2)(4) + (5)(3) + (1)(1) = 24. Observe que o produto escalar de dois vetores é um número e não outro vetor. Observe também que você pode calcular o produto escalar somente se os dois vetores tiverem o mesmo número de componentes.

Permita que uma (i, j) seja a entrada na matriz A **na linha i** e a **coluna j.** Por exemplo, A (3, 2) é a entrada na matriz A na linha 3 **RD** e na coluna 2 **ND** . Suponha que A, B e C são matrizes e AB = C. As entradas de C são calculadas da seguinte maneira:

C(i, j) = (linha i de A) • (coluna j de B)

A ilustração a seguir mostra dois exemplos de multiplicação de matriz.

![ilustração que mostra como executar a multiplicação de matriz](images/aboutgdip05-art06.png)

Se você considerar um ponto no plano como uma matriz 1 × 2, poderá transformar esse ponto multiplicando-o por uma matriz 2 × 2. A ilustração a seguir mostra várias transformações aplicadas ao ponto (2, 1).

![ilustração que mostra como usar a multiplicação de matriz para dimensionar, girar ou refletir um ponto em um plano](images/aboutgdip05-art07.png)

Todas as transformações mostradas na figura anterior são transformações lineares. Algumas outras transformações, como translação, não são lineares, e não podem ser expressas como multiplicação por uma matriz 2 × 2. Suponha que você deseja começar com o ponto (2, 1), girá-lo 90 graus, movê-lo em 3 unidades na direção x e 4 unidades na direção y. Você pode fazer isso executando uma multiplicação de matriz seguida por uma adição de matriz.

![ilustração que mostra como a multiplicação de matriz e a adição podem girar um ponto e convertê-lo duas vezes](images/aboutgdip05-art08.png)

Uma transformação linear (multiplicação por uma matriz 2 × 2) seguida por uma tradução (adição de uma matriz de 1 × 2) é chamada de transformação afim. Uma alternativa ao armazenamento de uma transformação afim em um par de matrizes (uma para a parte linear e outra para a tradução) é armazenar toda a transformação em uma matriz 3 × 3. Para fazer isso funcionar, um ponto no plano deve ser armazenado em uma matriz 1 × 3 com uma terceira coordenada fictícia. A técnica comum é fazer todas as terceiras coordenadas iguais a 1. Por exemplo, o ponto (2, 1) é representado pela matriz \[ 2 1 1 \] . A ilustração a seguir mostra uma transformação afim (girar 90 graus; traduzir 3 unidades na direção x, 4 unidades na direção y) expressas como multiplicação por uma única matriz 3 × 3.

![ilustração que mostra como a multiplicação de matriz pode executar uma transformação afim](images/aboutgdip05-art09.png)

No exemplo anterior, o ponto (2, 1) é mapeado para o ponto (2, 6). Observe que a terceira coluna da matriz 3 × 3 contém os números 0, 0, 1. Esse será sempre o caso da matriz 3 × 3 de uma transformação afim. Os números importantes são os seis números nas colunas 1 e 2. A parte superior esquerda 2 × 2 da matriz representa a parte linear da transformação e as duas primeiras entradas na terceira linha representam a tradução.

![ilustração mostrando que as duas primeiras colunas são mais significativas para uma matriz 3x3 de uma transformação afim](images/aboutgdip05-art10.png)

no Windows GDI+ você pode armazenar uma transformação afim em um objeto de [**matriz**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) . Como a terceira coluna de uma matriz que representa uma transformação afim é sempre (0, 0, 1), você especifica apenas seis números nas duas primeiras colunas ao construir um objeto de **matriz** . A instrução `Matrix myMatrix(0.0f, 1.0f, -1.0f, 0.0f, 3.0f, 4.0f);` constrói a matriz mostrada na figura anterior.

## <a name="composite-transformations"></a>Transformações de composição

Uma transformação de composição é uma sequência de transformações, uma seguida da outra. Considere as matrizes e transformações na lista a seguir:

-   Matriz A gira 90 graus
-   Escala da matriz B por um fator de 2 na direção x
-   Matriz C converte 3 unidades na direção y

Se você começar com o ponto (2, 1) — representado pela matriz \[ 2 1 1 \] — e multiplicado por a, B, então C, o ponto (2, 1) passará as três transformações na ordem listada.

\[2 1 1 \] ABC = \[ – 2 5 1\]

Em vez de armazenar as três partes da transformação composta em três matrizes separadas, você pode multiplicar a, B e C em conjunto para obter uma única matriz 3 × 3 que armazena toda a transformação composta. Suponha que a ABC = D. Em seguida, um ponto multiplicado por D fornece o mesmo resultado que um ponto multiplicado por A, B e, em seguida, C.

\[2 1 1 \] D = \[ – 2 5 1\]

A ilustração a seguir mostra as matrizes A, B, C e D.

![ilustração mostrando como executar várias transformações multiplicando as matrizes constituintes](images/aboutgdip05-art12.png)

O fato de que a matriz de uma transformação composta pode ser formada multiplicando as matrizes de transformação individuais significa que qualquer sequência de transformações afim pode ser armazenada em um único objeto [**matriz**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) .

> [!Note]  
> A ordem de uma transformação de composição é importante. Em geral, girar, dimensionar e converter não é o mesmo que dimensionar, girar e converter. Da mesma forma, a ordem de multiplicação de matriz é importante. Em geral, ABC não é o mesmo que BAC.

 

A classe [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) fornece vários métodos para criar uma transformação composta: [**Matrix:: multiplicar**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-multiply), [**matriz:: Rotate**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotate), [**Matrix:: RotateAt**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotateat), [**matriz:: Scale**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-scale), [**Matrix:: distorcer**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear)e [**Matrix:: translate**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-translate). O exemplo a seguir cria a matriz de uma transformação composta que gira em primeiro lugar 30 graus e, em seguida, é dimensionada por um fator de 2 na direção y e, em seguida, converte 5 unidades na direção x.


```
Matrix myMatrix;
myMatrix.Rotate(30.0f);
myMatrix.Scale(1.0f, 2.0f, MatrixOrderAppend);
myMatrix.Translate(5.0f, 0.0f, MatrixOrderAppend);
```



A ilustração a seguir mostra a matriz.

![ilustração que mostra uma matriz com valores expressos como funções trigonométricas e uma matriz com valores aproximados dessas funções](images/aboutgdip05-art13.png)

 

 



