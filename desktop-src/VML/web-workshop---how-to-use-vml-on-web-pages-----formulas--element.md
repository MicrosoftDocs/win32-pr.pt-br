---
title: Usando o elemento Formulas
description: Usando o elemento Formulas
ms.assetid: f5a381b4-4132-4b66-b41a-3cada26b41e2
keywords:
- Workshop da Web, elemento formulas
- projetando páginas da Web, elemento de fórmulas
- linguagem VML (VML), elemento formulas
- Elemento VML (linguagem VML),fórmulas
- elementos gráficos vetoriais, fórmulas
- elemento formulas
- Elementos VML, fórmulas
- Formas VML, elemento de fórmulas
- linguagem VML (VML), definindo caminhos para formas
- VML (linguagem VML), definindo caminhos para formas
- gráficos vetoriais, definindo caminhos para formas
- Formas VML, definindo caminhos
- definindo caminhos para formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23810ae6612e18132566c7d546db7f1f3a569871050b7919cbd8512f3d832808
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512787"
---
# <a name="using-the-formulas-element"></a>Usando o elemento Formulas

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Neste tópico, ilustramos como usar o `<formulas>` subconjunto para definir um caminho ajustável para uma forma.

Você pode colocar o <formulas> subconjunto dentro `<shape>` de ou para definir `<shapetype>` fórmulas que podem variar o caminho de uma forma. Dentro do `<formulas>` subconjunto, um subconjunto **f** define uma fórmula para que um valor seja avaliado com base nessa fórmula. Por exemplo, a fórmula `<v:f eqn="prod 10 4 5"/>` define um valor equivalente a "10 x 4 /5".

Você pode colocar muitos subconjunto **f** dentro de um `<formulas>` subconjunto. As fórmulas podem referenciar os valores definidos anteriormente em outras fórmulas dentro do mesmo `<formulas>` subconjunto. O valor definido na primeira fórmula pode ser chamado de , o valor definido na segunda fórmula pode ser chamado de @0 @1 e assim por diante.

Além disso, você pode especificar o atributo de propriedade **adj** do elemento, como `<shape>` adj="100, 200, 150". Dentro do `<formulas>` elemento , você pode fazer referência a esses valores na lista **adj.** O primeiro valor (100) na lista **adj** pode ser chamado de 0, o segundo \# valor (200) pode ser chamado de 1 e assim por \# diante.

Por exemplo, para desenhar um rosto de sorriso, você pode digitar a seguinte representação de VML:

![shape1.gif (735 bytes)](images/shape1f.gif)


```HTML
<v:shape style='width:1in;height:1in;' strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="17520"
path="m10800,0qx0,10800,10800,21600,21600,10800,10800,0xe
m7340,6445qx6215,7570,7340,8695,8465,7570,7340,6445xnfe
m14260,6445qx13135,7570,14260,8695,15385,7570,14260,6445xnfe
m4960@0c8853@3,12747@3,16640@0nfe">
<v:formulas>
<v:f eqn="sum 33030 0 #0"/>
<v:f eqn="prod #0 4 3"/>
<v:f eqn="prod @0 1 3"/>
<v:f eqn="sum @1 0 @2"/>
</v:formulas>
</v:shape>
```





-   `adj="17520"` define um valor (= 17520). Esse valor pode ser referenciado como \# 0.
-   A primeira fórmula, `<v:f eqn="sum 33030 0 #0"/>` , define o valor (= 33030 + 0 - \# 0). Esse valor pode ser referenciado como @0 .
-   A segunda fórmula, `<v:f eqn="prod #0 4 3"/>` , define o valor (= \# 0 \* 4 /3). Esse valor pode ser referenciado como @1 .
-   A terceira fórmula, `<v:f eqn="prod @0 1 3"/>` , define o valor (= @0 \* 1 /3). Esse valor pode ser referenciado como @2 .
-   A quarta fórmula, `<v:f eqn="sum @1 0 @2"/>` , define o valor (= + @1 0 -@2 ). Esse valor pode ser referenciado como @3 .
-   Dentro do elemento , os valores definidos na primeira ( ) e na quarta ( ) fórmulas são usados para determinar o contorno `<path>` @0 da @3 forma.

Se você alterar a lista **adj,** como , os valores das fórmulas que referenciam a lista adj também serão alterados, afetando o rosto dela da `adj="20000"` seguinte forma: 

![shape2.gif (765 bytes)](images/shape2f.gif)


```HTML
<v:shape style='width:1in;height:1in;' strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="20000"
path="m10800,0qx0,10800,10800,21600,21600,10800,10800,0xe
m7340,6445qx6215,7570,7340,8695,8465,7570,7340,6445xnfe
m14260,6445qx13135,7570,14260,8695,15385,7570,14260,6445xnfe
m4960@0c8853@3,12747@3,16640@0nfe">
<v:formulas>
<v:f eqn="sum 33030 0 #0"/>
<v:f eqn="prod #0 4 3"/>
<v:f eqn="prod @0 1 3"/>
<v:f eqn="sum @1 0 @2"/>
</v:formulas>
</v:shape>
```





Para obter mais informações sobre esse elemento, consulte a [especificação de VML](https://www.w3.org/TR/NOTE-VML#-toc416858392) .

 

 