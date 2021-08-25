---
description: 'Normalmente, os aplicativos gráficos 3D usam dois tipos de sistemas de coordenadas cartesianos: esquerdo e direito.'
ms.assetid: 268c3024-85a5-4fd5-b575-e126dd4be97c
title: Sistemas de coordenadas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e47b87ae6374d68b8c836dfb4818781e83e77c288f7bf05b121dbb4426c9aad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857567"
---
# <a name="coordinate-systems-direct3d-9"></a>Sistemas de coordenadas (Direct3D 9)

Normalmente, os aplicativos gráficos 3D usam dois tipos de sistemas de coordenadas cartesianos: esquerdo e direito. Em ambos os sistemas de coordenadas, o eixo x positivo aponta para a direita e o eixo y positivo aponta para cima. Você pode lembrar para qual direção o eixo z positivo aponta, apontando os dedos de sua mão direita ou esquerda na direção x positiva e curvando-os na direção y positiva. A direção do seu polegar aponta em sua direção ou para longe de você, é a direção em que o eixo z positivo aponta para esse sistema de coordenadas. A ilustração a seguir mostra esses dois sistemas de coordenadas.

![ilustração dos sistemas de coordenadas cartesianas à esquerda e à direita](images/leftrght.png)

O Direct3D usa um sistema de coordenadas à esquerda. Se você estiver portando um aplicativo baseado em um sistema de coordenadas à direita, deverá fazer duas alterações nos dados passados para o Direct3D.

-   Inverter a ordem dos vértices de triângulos, de modo que o sistema os percorra em sentido horário, a partir da frente. Em outras palavras, se os vértices forem v0, v1, v2, passe-os para o Direct3D como v0, v2, v1.
-   Use a matriz de visualização para dimensionar o espaço do mundo em -1 na direção z. Para fazer isso, invada o sinal do \_ membro 31, \_ 32, 33 e 34 da estrutura \_ \_ [**D3DMATRIX**](d3dmatrix.md) que você usa para sua matriz de exibição.

Para obter o que equivale a um mundo de direita, use as funções [**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md) e [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) para definir a transformação de projeção. No entanto, tenha cuidado para usar a função [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) correspondente, inverter a ordem de reversão da face e desemparecar os mapas de cubo de acordo.

Apesar das coordenadas de esquerda e direita serem os sistemas mais comuns, há uma variedade de outros sistemas de coordenadas usados no software 3D. Por exemplo, não é incomum para apps de modelagem 3D usar um sistema de coordenadas no qual o eixo y aponta para o visualizador ou para longe dele, e o eixo z aponta para cima.

Formalmente, a orientação de um conjunto de vetores de base (ou seja, um sistema de coordenadas) pode ser encontrada pela computação do determinante da matriz definida pelo conjunto específico de vetores de base. Se o determinante for positivo, a base será orientada "positivamente" (ou à direita). Se o determinante for negativo, a base será orientada "negativamente" (ou à esquerda). Para uma explicação do que é determinante, consulte qualquer recurso de álgebra linear.

Informalmente, você pode usar a "regra à direita/esquerda" para determinar se um determinado conjunto de vetores de base forma um sistema de coordenadas à direita ou à esquerda.

As operações essenciais executadas em objetos definidos em um sistema de coordenadas 3D são conversão, rotação e dimensionamento. Você pode combinar essas transformações básicas para criar uma matriz de transformação. Para obter detalhes, [consulte Transforms (Direct3D 9)](transforms.md).

Quando você combina essas operações, os resultados não são comutativos; a ordem em que você faz multiplicação das matrizes é importante.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sistemas de coordenadas e geometria](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



