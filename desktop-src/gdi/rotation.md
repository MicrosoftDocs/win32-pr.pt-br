---
description: Muitos aplicativos CAD fornecem recursos que giram objetos desenhados na área do cliente.
ms.assetid: 85d8fe2c-5ad9-4e98-b6ff-ca0a78abeee5
title: Rotação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17be42f2826cbad09333b2c37b607dc50c7c9d0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968182"
---
# <a name="rotation"></a>Rotação

Muitos aplicativos CAD fornecem recursos que giram objetos desenhados na área do cliente. Aplicativos que incluem recursos de rotação usam a função [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para definir o espaço mundial apropriado para a transformação de espaço em página. Essa função recebe um ponteiro para uma estrutura [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) que contém os valores apropriados. Os membros eM11, eM12, eM21 e eM22 do XFORM especificam, respectivamente, o cosseno, o seno, o seno negativo e o cosseno do ângulo de rotação.

Quando a *rotação* ocorre, os pontos que constituem um objeto são girados em relação à origem do espaço de coordenadas. A ilustração a seguir mostra um retângulo de 20 a 20 unidades girado em 30 graus quando copiado do espaço de coordenadas mundiais para o espaço de coordenadas de página.

![ilustração mostrando dois espaços de coordenadas; cada um tem um retângulo em um local diferente e com uma rotação diferente](images/cstrn-11.png)

Na ilustração anterior, cada ponto no retângulo foi girado em 30 graus em relação à origem do espaço de coordenadas.

O algoritmo a seguir computa a nova coordenada x (x ') para um ponto (x, y) que é girado pelo ângulo A com relação à origem do espaço de coordenadas.

``` syntax
x' = (x * cos A) - (y * sin A) 
```

O algoritmo a seguir computa a coordenada y (y) para um ponto (x, y) que é girado pelo ângulo a em relação à origem.

``` syntax
y' = (x * sin A) + (y * cos A) 
```

As duas transformações de rotação podem ser combinadas em uma matriz 2-por-2 da seguinte maneira.

``` syntax
|x' y'| == |x y| * | cos A   sin A| 
                   |-sin A   cos A| 
```

A matriz 2-por-2 que produziu a rotação contém os valores a seguir.

``` syntax
| .8660    .5000| 
|-.5000    .8660| 
```

## <a name="rotation-algorithm-derivation"></a>Derivação de algoritmo de rotação

Os algoritmos de rotação são baseados na teorema de adição de trigonometria, informando que a função trigonométrica de uma soma de dois ângulos (a1 e a2) pode ser expressa em termos das funções trigonométricas dos dois ângulos.

``` syntax
sin(A1 + A2) = (sin A1 * cos A2) + (cos A1 * sin A2) 
cos(A1 + A2) = (cos A1 * cos A2) - (sin A1 * sin A2) 
```

A ilustração a seguir mostra um ponto no sentido anti-horário girado para uma nova posição p '. Além disso, ele mostra dois triângulos formados por uma linha desenhada da origem de espaço de coordenadas para cada ponto e uma linha desenhada de cada ponto através do eixo x.

![diagrama mostrando a origem, p e p e dois triângulos](images/cstrn-12.png)

Usando trigonometria, a coordenada x do ponto p pode ser obtida multiplicando o comprimento do hipotenusa h pelo cosseno de a1.

``` syntax
x = h * cos A1 
```

A coordenada y do ponto p pode ser obtida multiplicando-se o comprimento do hipotenusa h pelo seno de a1.

``` syntax
y = h * sin A1 
```

Da mesma forma, a coordenada x do ponto p ' pode ser obtida multiplicando o comprimento do hipotenusa h pelo cosseno de (a1 + a2).

``` syntax
x' = h * cos (A1 + A2) 
```

Por fim, a coordenada y do ponto p ' pode ser obtida multiplicando o comprimento do hipotenusa h pelo seno de (a1 + a2).

``` syntax
y' = h * sin (A1 + A2) 
```

Usando o teorema de adição, os algoritmos anteriores se tornam o seguinte:

``` syntax
x' = (h * cos A1 * cos A2) - (h * sin A1 * sin A2) 
y' = (h * cos A1 * sin A2) + (h * sin A1 * cos A2) 
```

Os algoritmos de rotação para um determinado ponto girados por ângulo a2 podem ser obtidos substituindo x para cada ocorrência de (h \* cos a1) e substituindo y por cada ocorrência de (h \* sin a1).

``` syntax
x' = (x * cos A2) - (y * sin A2) 
y' = (x * sin A2) + (y * cos A2) 
```

 

 



