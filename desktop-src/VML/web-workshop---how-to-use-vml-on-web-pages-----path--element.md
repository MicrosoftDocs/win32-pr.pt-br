---
title: Usando o elemento Path
description: Usando o elemento Path
ms.assetid: fd7924e7-f94f-4bc9-aa45-02cf8f9bac9b
keywords:
- Workshop da Web, elemento path
- projetando páginas da Web, elemento path
- linguagem VML (VML), elemento path
- Elemento VML (linguagem VML),path
- gráficos vetoriais, elemento path
- elemento path
- Elementos VML, caminho
- Formas VML, elemento path
- linguagem VML (VML), personalização de contornos de forma
- VML (linguagem VML), personalização de contornos de forma
- gráficos vetoriais, personalização de contornos de forma
- Formas VML, personalização de contornos
- personalização de contornos de forma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cbb27dbc2b039478903f697b02cefb14464b71a96ab2165db124d0a0053a400
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057175"
---
# <a name="using-the-path-element"></a>Usando o elemento Path

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Você aprendeu que pode usar os elementos de forma predefinidos do VML – como `<oval>` , , , , , , e – para desenhar uma `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` forma. Neste tópico, ilustramos como usar o `<path>` subconjunto para personalizar o contorno de uma forma.

Você pode colocar o `<path>` subconjunto dentro do `<shape>` elemento `<shapetype>` ou . Em seguida, você pode usar os atributos de propriedade do `<path>` subconjunto para personalizar o contorno da forma.

Por exemplo, para desenhar a forma personalizada ilustrada na figura a seguir, você pode usar o subconjunto para definir o contorno da forma, conforme mostrado na seguinte representação `<path>` de VML:

![shape1.gif (1301 bytes)](images/shape1p.gif)


```HTML
<body>
<v:shape style='width:250;height:250' strokecolor="red" strokeweight="1.5pt"
fillcolor="blue" coordorigin="0 0" coordsize="200 200">
<v:path v="m 8,65 l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155,
92,121, 42,155, 60,100 x e"/>
</v:shape>
</body>
```





-   Os valores `m 8,65` indicam que o desenho começa no ponto (8,65).
-   Os valores indicam que uma linha reta começa no ponto atual (8, 65) e termina no ponto determinado `l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155, 92,121, 42,155, 60,100` (72, 65), que se torna o novo ponto atual. Uma nova linha começa no ponto atual (72, 65) e termina no ponto determinado, que se torna o novo ponto atual e assim por diante, até o ponto final (60, 100).
-   `x` indica que o caminho será fechado por uma linha reta que começa no ponto atual (60, 100) e termina no ponto original (8, 65).
-   `e` indica parar o desenho.

Para obter mais informações sobre esse elemento, consulte a [especificação de VML](https://www.w3.org/TR/NOTE-VML#-toc416858391) .

 

 