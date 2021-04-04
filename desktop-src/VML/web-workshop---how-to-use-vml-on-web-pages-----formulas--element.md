---
title: Usando o elemento fórmulas
description: Usando o elemento fórmulas
ms.assetid: f5a381b4-4132-4b66-b41a-3cada26b41e2
keywords:
- Web Workshop, elemento formulas
- Criando páginas da Web, elemento formulas
- Linguagem VML (VML), elemento formulas
- VML (linguagem VML), elemento formulas
- elementos gráficos vetoriais, elemento fórmulas
- elemento formulas
- Elementos de VML, fórmulas
- Formas de VML, elemento formulas
- Linguagem VML (VML), definindo caminhos para formas
- VML (linguagem VML), definindo caminhos para formas
- gráficos vetoriais, definição de caminhos para formas
- Formas de VML, definindo caminhos
- definindo caminhos para formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85ce4ebb6eea05895edf974e3ca86b1fa2ad923
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007607"
---
# <a name="using-the-formulas-element"></a>Usando o elemento fórmulas

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Neste tópico, Ilustraremos como usar o `<formulas>` subelemento para definir um caminho ajustável para uma forma.

Você pode posicionar o <formulas> subelemento dentro `<shape>` ou `<shapetype>` para definir fórmulas que podem variar o caminho de uma forma. Dentro do `<formulas>` subelemento, um subelemento **f** define uma fórmula para que um valor seja avaliado com base na fórmula. Por exemplo, a fórmula `<v:f eqn="prod 10 4 5"/>` define um valor equivalente a "10 x 4/5".

Você pode inserir muitos elementos **f** dentro de um `<formulas>` subelemento. As fórmulas podem referenciar os valores que são definidos anteriormente em outras fórmulas dentro do mesmo `<formulas>` subelemento. O valor definido na primeira fórmula pode ser referido como @0 , o valor definido na segunda fórmula pode ser referido como @1 , e assim por diante.

Além disso, você pode especificar o atributo de propriedade **adj** do `<shape>` elemento, como adj = "100, 200, 150". Dentro do `<formulas>` elemento, você pode fazer referência a esses valores na lista de **adj** . O primeiro valor (100) na lista de **adj** pode ser referido como \# 0, o segundo valor (200) pode ser referido como \# 1 e assim por diante.

Por exemplo, para desenhar um sorriso, você pode digitar a seguinte representação de VML:

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
-   A primeira fórmula, `<v:f eqn="sum 33030 0 #0"/>` , define o valor (= 33030 + 0- \# 0). Esse valor pode ser referenciado como @0 .
-   A segunda fórmula, `<v:f eqn="prod #0 4 3"/>` , define o valor (= \# 0 \* 4/3). Esse valor pode ser referenciado como @1 .
-   A terceira fórmula, `<v:f eqn="prod @0 1 3"/>` , define o valor (= @0 \* 1/3). Esse valor pode ser referenciado como @2 .
-   A quarta fórmula, `<v:f eqn="sum @1 0 @2"/>` , define o valor (= @1 + 0 -@2 ). Esse valor pode ser referenciado como @3 .
-   Dentro do `<path>` elemento, os valores definidos nas @0 fórmulas First () e quarta ( @3 ) são usados para determinar o contorno da forma.

Se você alterar a lista de **adj** , como `adj="20000"` , os valores das fórmulas que fazem referência à lista de **adj** também serão alterados, afetando o sorriso da seguinte maneira:

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





Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858392) .

 

 