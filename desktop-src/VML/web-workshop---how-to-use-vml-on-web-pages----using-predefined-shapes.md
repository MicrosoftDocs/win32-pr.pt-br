---
title: Usando formas predefinidas
description: Este artigo descreve como usar formas predefinidas em VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.
ms.assetid: 9a2e8b5a-b1d0-4a73-b058-24dac1f0b655
keywords:
- Web Workshop, formas predefinidas
- Criando páginas da Web, formas predefinidas
- Linguagem VML (VML), formas predefinidas
- VML (linguagem VML), formas predefinidas
- gráficos vetoriais, formas predefinidas
- Formas de VML, predefinidas
- formas predefinidas
- Linguagem VML (VML), elemento Rect
- VML (linguagem VML), elemento Rect
- gráfico vetorial, elemento Rect
- elemento Rect
- Elementos de VML, Rect
- Linguagem VML (VML), elemento RoundRect
- VML (linguagem VML), elemento RoundRect
- gráficos vetoriais, elemento RoundRect
- elemento RoundRect
- Elementos de VML, RoundRect
- Linguagem VML (VML), elemento de linha
- VML (linguagem VML), elemento de linha
- elementos gráficos vetoriais, elemento line
- elemento de linha
- Elementos de VML, linha
- Linguagem VML (VML), elemento Polyline
- VML (linguagem VML), elemento Polyline
- gráficos vetoriais, elemento Polyline
- elemento Polyline
- Elementos de VML, polilinha
- Linguagem VML (VML), elemento de curva
- VML (linguagem VML), elemento de curva
- gráficos vetoriais, elemento de curva
- elemento Curve
- Elementos de VML, curva
- Linguagem VML (VML), elemento Arc
- VML (linguagem VML), elemento Arc
- gráficos vetoriais, elemento Arc
- elemento Arc
- Elementos de VML, arco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b410cf288a3ba63e4c1d745fd962a445b0b220b8
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407679"
---
# <a name="using-predefined-shapes"></a>Usando formas predefinidas

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Como você aprendeu, você pode usar o `<oval>` elemento de VML para criar uma elipse simples. A VML fornece vários outros elementos predefinidos. Neste tópico, Ilustraremos como desenhar gráficos usando esses elementos.

Neste tópico:

-   [Rect](#roundrect)
-   [RoundRect](#roundrect)
-   [line](#polyline)
-   [múltipla](#polyline)
-   [curva](#curve)
-   [arco](#arc)
-   [Resumo](#summary)

## <a name="rect"></a>rect

Você pode usar o `<rect>` elemento para desenhar um retângulo. Em seguida, você pode personalizar o retângulo especificando atributos de propriedade diferentes.

Por exemplo, você pode desenhar um retângulo que é preenchido com azul especificando **FillColor**= "Blue" e dar a ele um esboço vermelho de 3,5 pontos especificando **strokecolor**= "Red" **strokeweight**= "3.5 pt", conforme mostrado na seguinte representação de VML:

![rect1.gif (485 bytes)](images/rect1.gif)


```HTML
<v:rect style='width:100pt;height:75pt' fillcolor="blue"
strokecolor="red" strokeweight="3.5pt"/>
```





Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) . (Observação: a especificação de VML não tem um indicador para o `<rect>` elemento.)

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="roundrect"></a>RoundRect

Você pode usar o `<roundrect>` elemento para desenhar um retângulo com cantos arredondados. Em seguida, você pode personalizar o retângulo arredondado especificando atributos de propriedade diferentes.

Por exemplo, você pode desenhar um retângulo com cantos arredondados 30% da metade da dimensão menor do retângulo, especificando **arcoize**= "0,3", preenchê-lo com amarelo especificando **FillColor**= "amarelo" e dê a ele um contorno vermelho de dois pontos especificando **strokecolor**= "Red" **strokeweight**= "2PT", conforme mostrado na seguinte representação de VML:

![roundrect1.gif (622 bytes)](images/roundrect1.gif)


```HTML
<v:roundrect style='width:100pt;height:75pt"
arcsize="0.3" fillcolor="yellow"
strokecolor="red" strokeweight="2pt"/>
```





Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="line"></a>line

Você pode usar o `<line>` elemento para criar uma linha reta. Em seguida, você pode personalizar a linha especificando atributos de propriedade diferentes.

Por exemplo, você pode desenhar uma linha horizontal especificando **from**= "20pt, 20pt" **to**= "100pt, 20pt" e torná-lo 2 e vermelho especificando **strokecolor**= "Red" **strokeweight**= "2PT", conforme mostrado na seguinte representação de VML:

![line1.gif (88 bytes)](images/line1.gif)


```HTML
<v:line from="20pt,20pt" to="100pt,20pt" '
strokecolor="red" strokeweight="2pt">
```





Você pode desenhar uma linha vertical ou diagonal simplesmente especificando valores diferentes para os atributos **de propriedade from** e **to** , conforme mostrado na seguinte representação de VML:

![line2.gif (86 bytes)](images/line2.gif)


```HTML
<v:line from="20pt,20pt" to="20pt,100pt"
strokecolor="red" strokeweight="2pt">
```





Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="polyline"></a>múltipla

Você pode usar o `<polyline>` elemento para definir formas que são criadas a partir de segmentos de linha conectados. Em seguida, você pode personalizar a forma especificando atributos de propriedade diferentes.

Por exemplo, para desenhar a forma mostrada na imagem a seguir, você pode digitar a seguinte representação de VML:

![polyline1.gif (957 bytes)](images/polyline1.gif)


```HTML
<v:polyline points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt"
strokecolor="red" strokeweight="2pt"/>
```





Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="curve"></a>curva

Você pode usar o `<curve>` elemento para desenhar uma curva Bézier cúbica. Em seguida, você pode personalizar a curva especificando atributos de propriedade diferentes.

Por exemplo, para desenhar uma curva, conforme mostrado na imagem a seguir, você pode digitar a seguinte representação de VML:

![curve1.gif (992 bytes)](images/curve1.gif)


```HTML
<v:curve style='position:relative'
from="0,0" control1="100pt,100pt" control2="200pt,100pt"
to="300pt,0" strokecolor="red" strokeweight="3pt"/>
```





Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="arc"></a>arco

Você pode usar o `<arc>` elemento para desenhar um arco que é definido como um segmento de uma oval. O arco é definido pela interseção da elipse com os vetores RADIUS inicial e final fornecidos pelos ângulos. Os ângulos são calculados usando as propriedades de um círculo (largura igual à altura) e, em seguida, escalados anisotropicamente para a largura e a altura desejadas.

Por exemplo, você pode desenhar um arco que começa com 0 graus e termina em 90 graus especificando **StartAngle**= "0" **EndAngle**= "90", conforme mostrado na seguinte representação de VML:

![arc1.gif (410 bytes)](images/arc1.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="90"
strokecolor="red" strokeweight="2pt"/>
```





Você pode alterar o arco especificando diferentes valores de **StartAngle** e de **ângulo de endangular** , conforme mostrado na seguinte representação de VML:

![arc2.gif (608 bytes)](images/arc2.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="180"
strokecolor="red" strokeweight="2pt"/>
```





![arc3.gif (807 bytes)](images/arc3.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="270"
strokecolor="red" strokeweight="2pt"/>
```





Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="summary"></a>Resumo

Você pode usar elementos predefinidos da VML, como,,,,, `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` e `<arc>` para desenhar gráficos facilmente em uma página da Web e, em seguida, personalizar esses gráficos simplesmente alterando seus atributos de propriedade.

 

 