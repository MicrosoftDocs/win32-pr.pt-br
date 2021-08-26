---
description: Curvas de parâmetro
ms.assetid: c073e7d0-c119-4c36-a5b2-b31dd6326ac8
title: Curvas de parâmetro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5130cf158271ffe3cb3da5e4e16b5fffa8a5a6994b14b9f8766fe20cdf1510ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997368"
---
# <a name="parameter-curves"></a>Curvas de parâmetro

Os parâmetros de mídia são capazes de seguir uma curva ao longo do tempo. Cada curva é descrita por uma fórmula matemática e dois pontos de extremidade. Cada ponto de extremidade é definido por um tempo de referência e o valor da curva nesse momento. A fórmula é usada para calcular valores intermediários entre os pontos e determina a forma da curva. As possíveis curvas são:

-   Saltar
-   Linear
-   Square
-   Quadrado inverso
-   Seno

"Jump" significa ir diretamente para o valor final. As outras curvas são mostradas no diagrama a seguir.

![curvas de parâmetro](images/param-curves01.png)

Matematicamente, as curvas funcionam da seguinte maneira. Suponha que uma curva comece no tempo *t* com um valor *de v* e termine no tempo *t* com um valor *de v*. Os dois pontos que definem a curva são (*t*, *v*) e (*t*, *v*).

-   Não deixe *que seja* a duração total da curva, *t*–*t*.
-   Deixe v ser *o* intervalo entre os valores inicial e final, *v–**v*.
-   A qualquer momento *t* tal *que t*<= *t*  <=  *t*, deixe ª *t*' = *t*–*t*.

![cálculo de parâmetro](images/param-curves02.png)

O valor do parâmetro no momento *em que t* é:

*v* = f( ª *t*' / ª *t* ) \* ª *v*  +  *v*

em que f(x) é uma função determinada pelo tipo de curva:

-   Linear: y = x
-   Quadrado: y = x^2
-   Quadrado inverso: y = sqrt(x)
-   Seno: y = \[ sin(πx – π/2) + \] 1/2

Observe que 0 *t*' < 0 *t*, de modo que o termo 0 *t*'/0 *t varia* de 0 a 1. Portanto, f(x) também varia de 0 a 1 e *v* sempre se enquadra entre *v* e *v*. Isso é verdadeiro se v *< 3* v *ou* vice-versa. Em outras palavras, a curva é limitada pelo retângulo (*t*, *v*, *t*, *v*).

Para a curva seno, o valor de (πx – π/2) varia de –π/2 a π/2, o que significa que sin(πx – π/2) varia de –1 a 1. O resultado é normalizado para que f(x) caia no intervalo (0–1).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Parâmetros de mídia](media-parameters.md)
</dt> </dl>

 

 



