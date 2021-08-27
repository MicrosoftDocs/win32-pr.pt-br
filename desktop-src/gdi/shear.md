---
description: Alguns aplicativos fornecem recursos que distorcem objetos desenhados na área do cliente.
ms.assetid: e5b82013-f6b9-460d-9f53-1b50dee2064f
title: Quantidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32edb9484fd8bb2a9da15220b0acf39fd5c44c50091551205022c6458b50d4e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092626"
---
# <a name="shear"></a>Quantidade

Alguns aplicativos fornecem recursos que distorcem objetos desenhados na área do cliente. Os aplicativos que usam recursos de distorção usam a função [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para definir os valores apropriados no espaço mundial para a transformação de espaço em página. Essa função recebe um ponteiro para uma estrutura [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) que contém os valores apropriados. Os membros eM12 e eM21 do XFORM especificam as constantes Proportionality horizontais e verticais, respectivamente.

Há dois componentes da *transformação distorcer*. O primeiro altera as linhas verticais em um objeto; o segundo altera as linhas horizontais. A ilustração a seguir mostra um retângulo de 20 por 20 unidades distorcido horizontalmente quando copiado do espaço de mundo para o espaço de página.

![ilustração mostrando um retângulo no espaço do mundo e um trapeziod no espaço da página](images/cstrn-13.png)

Uma distorção horizontal pode ser representada pelo seguinte algoritmo:

``` syntax
x' = x + (Sx * y) 
```

em que x é a coordenada x original, SX é a constante Proportionality e x ' é o resultado da transformação distorcer.

Uma distorção vertical pode ser representada pelo seguinte algoritmo:

``` syntax
y' = y + (Sy * x) 
```

em que y é a coordenada y original, Sy é a constante Proportionality e y ' é o resultado da transformação distorcer.

As transformações horizontal de distorção e de distorção vertical podem ser combinadas em uma única operação usando uma matriz 2-por-2.

``` syntax
|x' y'| == |x y| * |  1   Sx| 
                   | Sy    1| 
```

A matriz 2-por-2 que produziu a distorção contém os seguintes valores:

``` syntax
|1    1| 
|0    1| 
```

 

 



