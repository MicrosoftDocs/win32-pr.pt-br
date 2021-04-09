---
description: Curvas de parâmetro
ms.assetid: c073e7d0-c119-4c36-a5b2-b31dd6326ac8
title: Curvas de parâmetro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3c482112c8bd76217f5cbdabdf3cda13b09c3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087771"
---
# <a name="parameter-curves"></a>Curvas de parâmetro

Os parâmetros de mídia podem seguir uma curva ao longo do tempo. Cada curva é descrita por uma fórmula matemática e dois pontos de extremidade. Cada ponto de extremidade é definido por um tempo de referência e o valor da curva nesse momento. A fórmula é usada para calcular valores intermediários entre os pontos e determina a forma da curva. As curvas possíveis são:

-   Relacionados
-   Linear
-   Square
-   Quadrado inverso
-   Seno

"Salto" significa saltar diretamente para o valor final. As outras curvas são mostradas no diagrama a seguir.

![curvas de parâmetro](images/param-curves01.png)

Matematicamente, as curvas funcionam da seguinte maneira. Suponha que uma curva comece no tempo *t*₀ com um valor de *v*₀ e termine no time *t*₁ com um valor de *v*₁. Os dois pontos que definem a curva são (*t*₀, *v*₀) e (*t*₁, *v*₁).

-   Deixe que Δ *t* seja a duração total da curva, *t*₁ –*t*₀.
-   Deixe que Δ *v* seja o intervalo entre os valores inicial e final, *v*₁ –*v*₀.
-   A qualquer momento, *t* ₀ *<*= *t*  <=  *t*₁, deixe Δ *t*' = *t*–*t*₀.

![cálculo de parâmetro](images/param-curves02.png)

O valor do parâmetro na hora *t* é:

*v* = f (Δ *t*'/Δ *t* ) \* Δ *v*  +  *v*₀

em que f (x) é uma função determinada pelo tipo de curva:

-   Linear: y = x
-   Quadrado: y = x ^ 2
-   Quadrado inverso: y = sqrt (x)
-   Seno: y = \[ sin (Πx – π/2) + 1 \] /2

Observe que Δ *t*' < Δ *t*, portanto, o termo Δ *t*'/Δ *t* varia de 0 a 1. Portanto, f (x) também varia de 0 a 1 e *v* sempre cai entre *v*₀ e *v*₁. Isso é verdadeiro se *v*₀ < *v*₁ ou vice-versa. Em outras palavras, a curva é limitada pelo retângulo (*t*₀, *v*₀, *t*₁, *v*₁).

Para a curva senoidal, o valor de (Πx – π/2) varia de – π/2 a π/2, o que significa que o sin (Πx – π/2) varia de – 1 a 1. O resultado é normalizado para que f (x) se encaixe no intervalo (0 – 1).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Parâmetros de mídia](media-parameters.md)
</dt> </dl>

 

 



