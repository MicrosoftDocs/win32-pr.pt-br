---
description: Muitos aplicativos CAD fornecem recursos que giram objetos desenhados na área do cliente.
ms.assetid: 85d8fe2c-5ad9-4e98-b6ff-ca0a78abeee5
title: Rotação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aa6552411e2e018d04ff55cbeeb430d185fe62d61dc59d421d08dbe6e0d7174
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602696"
---
# <a name="rotation"></a>Rotação

Muitos aplicativos CAD fornecem recursos que giram objetos desenhados na área do cliente. Os aplicativos que incluem recursos de rotação usam [**a função SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para definir o espaço do mundo apropriado para a transformação de espaço na página. Essa função recebe um ponteiro para uma estrutura [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) que contém os valores apropriados. Os membros eM11, eM12, eM21 e eM22 do XFORM especificam respectivamente, o cosseno, o seno, o seno negativo e o cosseno do ângulo de rotação.

Quando *ocorre* a rotação, os pontos que constituem um objeto são girados em relação à origem do espaço de coordenadas. A ilustração a seguir mostra um retângulo de 20 por 20 unidades girado 30 graus quando copiado do espaço de coordenadas do mundo para o espaço de coordenadas de página.

![ilustração mostrando dois espaços de coordenadas; cada tem um retange em um local diferente e com uma rotação diferente](images/cstrn-11.png)

Na ilustração anterior, cada ponto no retângulo foi girado 30 graus em relação à origem do espaço de coordenadas.

O algoritmo a seguir calcula a nova coordenada x (x ') para um ponto (x,y ) que é girado pelo ângulo A em relação à origem do espaço de coordenadas.

``` syntax
x' = (x * cos A) - (y * sin A) 
```

O algoritmo a seguir calcula a coordenada y (y ') para um ponto (x,y ) que é girado pelo ângulo A em relação à origem.

``` syntax
y' = (x * sin A) + (y * cos A) 
```

As duas transformações de rotação podem ser combinadas em uma matriz 2 por 2 da seguinte forma.

``` syntax
|x' y'| == |x y| * | cos A   sin A| 
                   |-sin A   cos A| 
```

A matriz 2 por 2 que produziu a rotação contém os valores a seguir.

``` syntax
| .8660    .5000| 
|-.5000    .8660| 
```

## <a name="rotation-algorithm-derivation"></a>Derivação de algoritmo de rotação

Algoritmos de rotação são baseados no teorema de adição de trigonometry informando que a função trigonométrica de uma soma de dois ângulos (A1 e A2 ) pode ser expressa em termos das funções trigonométricas dos dois ângulos.

``` syntax
sin(A1 + A2) = (sin A1 * cos A2) + (cos A1 * sin A2) 
cos(A1 + A2) = (cos A1 * cos A2) - (sin A1 * sin A2) 
```

A ilustração a seguir mostra um ponto p girado no sentido anti-horário para uma nova posição p'. Além disso, ele mostra dois triângulos formados por uma linha desenhada da origem do espaço de coordenadas para cada ponto e uma linha desenhada de cada ponto pelo eixo x.

![diagrama mostrando a origem, p e p' e dois triângulos](images/cstrn-12.png)

Usando trigonometry, a coordenada x do ponto p pode ser obtida multiplicando o comprimento da hipotenuse h pelo cosseno de A1.

``` syntax
x = h * cos A1 
```

A coordenada y do ponto p pode ser obtida multiplicando o comprimento da hipotenuse h pelo seno de A1.

``` syntax
y = h * sin A1 
```

Da mesma forma, a coordenada x do ponto p' pode ser obtida multiplicando o comprimento da hipotenuse h pelo cosseno de (A1 +A2 ).

``` syntax
x' = h * cos (A1 + A2) 
```

Por fim, a coordenada y do ponto p' pode ser obtida multiplicando o comprimento da hipotenuse h pelo seno de (A1 +A2 ).

``` syntax
y' = h * sin (A1 + A2) 
```

Usando o teorema de adição, os algoritmos anteriores se tornam o seguinte:

``` syntax
x' = (h * cos A1 * cos A2) - (h * sin A1 * sin A2) 
y' = (h * cos A1 * sin A2) + (h * sin A1 * cos A2) 
```

Os algoritmos de rotação para um determinado ponto girado pelo ângulo A2 podem ser obtidos substituindo x para cada ocorrência de (h cos A1 ) e substituindo y para cada ocorrência de \* (h \* sin A1 ).

``` syntax
x' = (x * cos A2) - (y * sin A2) 
y' = (x * sin A2) + (y * cos A2) 
```

 

 



