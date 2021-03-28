---
description: A maioria dos aplicativos de CAD e de desenho fornece recursos que dimensionam a saída criada pelo usuário.
ms.assetid: 819d2026-dd5c-48d3-8af1-e96364acae72
title: Scaling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3c1ba409abda6e9c6b471a4d0a143b28d4c08e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968088"
---
# <a name="scaling"></a>Scaling

A maioria dos aplicativos de CAD e de desenho fornece recursos que dimensionam a saída criada pelo usuário. Os aplicativos que incluem recursos de dimensionamento (ou zoom) chamam a função [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para definir o espaço mundial apropriado para a transformação de espaço em página. Essa função recebe um ponteiro para uma estrutura [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) que contém os valores apropriados. Os membros eM11 e eM22 do XFORM especificam os componentes de dimensionamento horizontal e vertical, respectivamente.

Quando ocorre o *dimensionamento* , as linhas vertical e horizontal (ou vetores), que constituem um objeto, são ampliadas ou compactadas com relação ao eixo x ou y. A ilustração a seguir mostra um retângulo de 20 por 20 unidades dimensionado verticalmente para duas vezes sua altura original quando copiado do espaço de coordenadas mundiais para o espaço de coordenadas de página.

![ilustração mostrando um pequeno retângulo no espaço do mundo e um mais alto no espaço da página](images/cstrn-10.png)

Na ilustração anterior, as linhas verticais que definem a medida do lado do retângulo original 20 unidades, enquanto as linhas verticais que definem os lados do retângulo dimensionado medem 40 unidades.

O dimensionamento vertical pode ser representado pelo seguinte algoritmo.

``` syntax
y' = y * Dy 
```

Onde y ' é o novo comprimento, y é o comprimento original e dy é o fator de dimensionamento vertical.

O dimensionamento horizontal pode ser representado pelo seguinte algoritmo.

``` syntax
x' = x * Dx 
```

Onde x ' é o novo comprimento, x é o comprimento original e DX é o fator de dimensionamento horizontal.

As transformações de escala vertical e horizontal podem ser combinadas em uma única operação usando uma matriz 2-por-2.

``` syntax
|x' y'|  =  |Dx   0|  *  |x y| 
            |0   Dy| 
```

A matriz 2-por-2 que produziu a transformação dimensionamento contém os valores a seguir.

``` syntax
|1    0| 
|0    2| 
```

 

 



