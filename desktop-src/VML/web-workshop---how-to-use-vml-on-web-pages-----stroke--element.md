---
title: Usando o elemento Stroke
description: Este artigo descreve o uso do elemento Stroke do VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.
ms.assetid: e3d9dbe5-e087-4b6f-8318-c7d4485cd502
keywords:
- Workshop da Web, elemento stroke
- projetando páginas da Web, elemento stroke
- linguagem VML (VML), elemento stroke
- Elemento VML (linguagem VML),traço
- gráficos vetoriais, elemento stroke
- Elemento stroke
- Elementos VML, traço
- Formas VML, elemento de traço
- linguagem VML (VML), atributo de propriedade dashstyle
- VML (linguagem VML), atributo de propriedade dashstyle
- gráficos vetoriais, atributo de propriedade dashstyle
- Atributo de propriedade dashstyle
- linguagem VML (VML), atributo de propriedade opacity
- VML (linguagem VML), atributo de propriedade opacity
- gráficos vetoriais, atributo de propriedade opacidade
- atributo de propriedade opacity
- linguagem VML (VML), atributo de propriedade linestyle
- VML (linguagem VML), atributo de propriedade linestyle
- gráficos vetoriais, atributo de propriedade linestyle
- atributo de propriedade linestyle
- linguagem VML (VML), atributo de propriedade joinstyle
- VML (linguagem VML), atributo de propriedade joinstyle
- gráficos vetoriais, atributo de propriedade joinstyle
- Atributo de propriedade joinstyle
- linguagem VML (VML), atributo de propriedade filltype
- VML (linguagem VML), atributo de propriedade filltype
- gráficos vetoriais, atributo de propriedade filltype
- atributo de propriedade filltype
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dff7a4b3bc654063fe8156476cc9c52453247a0b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407839"
---
# <a name="using-the-stroke-element"></a>Usando o elemento Stroke

Este tópico descreve o VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Usando `<stroke>`

Como você aprendeu, você pode usar os atributos de propriedade **strokecolor** e **strokeweight** de uma forma predefinida – como , , , , , – para especificar a cor e o peso do contorno de uma `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` forma. Neste tópico, ilustramos como desenhar uma forma que tenha um contorno mais avançado.

Você pode colocar o subconjunto dentro do , ou ou qualquer elemento de forma predefinido para descrever como desenhar o contorno `<stroke>` `<shape>` da `<shapetype>` forma. Em seguida, você pode usar os atributos de propriedade – por exemplo, [dashstyle](#dashstyle), [opacity](#opacity), [linestyle](#linestyle), [joinstyle](#joinstyle), [filltype](#filltype) – do subconjunto para personalizar o `<stroke>` contorno.

[![voltar ao início ](images/top.gif) Voltar ao início](#top)

## <a name="dashstyle"></a>Dashstyle

Você pode usar o **atributo de propriedade dashstyle** do `<stroke>` sub-elemento para desenhar um contorno com vários estilos de traço.

**Exemplos:**

Se você especificar `<v:stroke dashstyle="solid" />` dentro do elemento , poderá criar uma linha sólida, conforme mostrado na seguinte representação de `<line>` VML:

![solid.gif (96 bytes)](images/solid.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="solid" />
</v:line>
```





Se você alterar o atributo de propriedade **dashstyle** para "ponto", poderá criar uma linha pontilhada, conforme mostrado na seguinte representação de VML:

![dot.gif (144 bytes)](images/dot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dot" />
</v:line>
```





Se você alterar o atributo de propriedade **dashstyle** para "traço", poderá criar uma linha tracejada, conforme mostrado na seguinte representação de VML:

![dash.gif (137 bytes)](images/dash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dash" />
</v:line>
```





Se você alterar o atributo de propriedade **dashstyle** para "dashdot", poderá criar uma linha com um estilo tracejado e pontilhado, conforme mostrado na seguinte representação de VML:

![dashdot.gif (145 bytes)](images/dashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dashdot" />
</v:line>
```





Se você alterar o atributo de propriedade **dashstyle** para "longdash", poderá criar uma linha com um estilo longo tracejado, conforme mostrado na seguinte representação de VML:

![longdash.gif (123 bytes)](images/longdash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdash" />
</v:line>
```





Se você alterar o atributo de propriedade **dashstyle** para "longdashdot", poderá criar uma linha com um estilo longo tracejado e pontilhado, conforme mostrado na seguinte representação de VML:

![longdashdot.gif (135 bytes)](images/longdashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdashdot" />
</v:line>
```





Se você colocar dentro do elemento , poderá criar um retângulo com um contorno tracejado e pontilhado, conforme mostrado na seguinte representação `<v:stroke dashstyle="dashdot" />` `<rect>` de VML:

![rect.gif (615 bytes)](images/rect.gif)


```HTML
<v:rect style='width:100pt;height:80pt' strokecolor="red" strokeweight="2pt"/>
<v:stroke dashstyle="dashdot" />
</v:rect>
```





[![voltar ao início ](images/top.gif) Voltar ao início](#top)

## <a name="opacity"></a>opacidade

Você pode usar o **atributo de propriedade de opacidade** do subconjunto para desenhar um contorno com vários estilos de `<stroke>` opacidade. O valor do atributo **de propriedade opacidade** pode ser qualquer número entre 0 e 1. Por padrão, é 1, indicando opacidade total.

**Exemplos:**

A seguinte representação de VML cria uma linha com opacidade total:

![line1.gif (96 bytes)](images/line1.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
</v:line>
```





Se você adicionar dentro do elemento , poderá criar uma linha com `<v:stroke opacity="0.5" />` 50% de opacidade, conforme mostrado na seguinte representação `<line>` de VML:

![line2.gif (108 bytes)](images/line2.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
<v:stroke opacity="0.5" />
</v:line>
```





[![voltar ao início ](images/top.gif) Voltar ao início](#top)

## <a name="linestyle"></a>Linestyle

Você pode usar o **atributo de propriedade linestyle** do `<stroke>` sub-elemento para desenhar um contorno com vários estilos de linha.

**Exemplos:**

Se você especificar dentro do elemento , poderá criar um retângulo com um único contorno, conforme mostrado na seguinte representação `<v:stroke linestyle="single" />` `<rect>` de VML:

![single.gif (537 bytes)](images/single.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red" strokeweight="10pt">
<v:stroke linestyle="single" />
</v:rect>
```





Se você alterar o atributo de propriedade **linestyle** para "thinthin", poderá criar um retângulo com o contorno (1:1:1), conforme mostrado na seguinte representação de VML:

![thinthin.gif (642 bytes)](images/thinthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthin" />
</v:rect>
```





Se você alterar o atributo de propriedade **linestyle** para "thinthick", poderá criar um retângulo com o contorno (1:1:2), conforme mostrado na seguinte representação de VML:

![thinthick.gif (646 bytes)](images/thinthick.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthick" />
</v:rect>
```





Se você alterar o atributo de propriedade **linestyle** para "thickthin", poderá criar um retângulo com o contorno (2:1:1), conforme mostrado na seguinte representação de VML:

![thickthin.gif (676 bytes)](images/thickthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickthin" />
</v:rect>
```





Se você alterar o atributo de propriedade **linestyle** para "thickbetweenthin", poderá criar um retângulo com o contorno (1:1:2:1:1), conforme mostrado na seguinte representação de VML:

![thickbthin.gif (669 bytes)](images/thickbthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickbetweenthin" />
</v:rect>
```





[![voltar ao início ](images/top.gif) Voltar ao início](#top)

## <a name="joinstyle"></a>joinstyle

Você pode usar o **atributo joinstyle** do `<stroke>` subconjunto para definir como as linhas são unidas.

Por exemplo, para criar uma forma que tenha o contorno de junção de ida e volta, conforme mostrado na ilustração a seguir, você pode especificar dentro do elemento , conforme mostrado na seguinte representação `<v:stroke joinstyle="round" />` `<polyline>` de VML:

![round.gif (660 bytes)](images/round.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="round" />
</v:polyline>
```





Se você alterar o atributo de propriedade **joinstyle** para "bevel", poderá criar uma forma que tenha o contorno de junção de nível, conforme mostrado na seguinte representação de VML:

![bevel.gif (650 bytes)](images/bevel.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="bevel" />
</v:polyline>
```





Se você alterar o atributo de propriedade **joinstyle** para "miter", poderá criar uma forma que tenha o contorno miter-join, conforme mostrado na seguinte representação de VML:

![miter.gif (702 bytes)](images/miter.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="miter" />
</v:polyline>
```





[![voltar ao início ](images/top.gif) Voltar ao início](#top)

## <a name="filltype"></a>Filltype

Você pode usar o **atributo de propriedade filltype** do `<stroke>` sub-elemento para desenhar um contorno com vários efeitos de preenchimento.

**Exemplos:**

Se você especificar dentro do elemento , poderá criar um retângulo arredondado com a estrutura de contorno preenchida sólida, conforme mostrado na seguinte representação `<v:stroke filltype="solid" />` `<roundrect>` de VML:

![solid.gif (701 bytes)](images/solidborder.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="solid" />
</v:roundrect>
```





Se você alterar o atributo de propriedade **filltype** para "pattern", aponte o atributo de propriedade **src** para o local do arquivo de imagem padrão e de definir o atributo de propriedade **color2** como a segunda cor padrão, você poderá criar um retângulo arredondado com um contorno de padrão, conforme mostrado na seguinte representação VML:

![pattern.gif (1055 bytes)](images/pattern.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="pattern" src="image.gif"
color2="green" />
</v:roundrect>
```





Se você alterar o atributo de propriedade **filltype** para "bloco" e apontar o atributo de propriedade **src** para o local do arquivo de imagem, poderá criar um retângulo arredondado com um contorno lado a lado, conforme mostrado na seguinte representação de VML:

![tile.gif (6617 bytes)](images/tile.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="tile" src="image2.gif" />
</v:roundrect>
```





Se você alterar o atributo de propriedade **filltype** para "frame" e apontar o atributo de propriedade **src** para o local do arquivo de imagem, poderá criar um retângulo arredondado com um contorno de imagem, conforme mostrado na seguinte representação de VML:

![frame.gif (6203 bytes)](images/frame.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="frame" src="image2.gif" />
</v:roundrect>
```





Para obter mais informações sobre esse elemento, consulte a [especificação de VML](https://www.w3.org/TR/NOTE-VML#-toc416858395) .

 

 