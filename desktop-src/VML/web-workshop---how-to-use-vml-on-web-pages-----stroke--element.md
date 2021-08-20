---
title: Usando o elemento Stroke
description: este artigo descreve como usar o elemento Stroke de VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.
ms.assetid: e3d9dbe5-e087-4b6f-8318-c7d4485cd502
keywords:
- Web Workshop, elemento Stroke
- Criando páginas da Web, elemento Stroke
- Linguagem VML (VML), elemento Stroke
- VML (linguagem VML), elemento Stroke
- gráfico vetorial, elemento Stroke
- elemento Stroke
- Elementos de VML, traço
- Formas VML, elemento Stroke
- Linguagem VML (VML), atributo de propriedade DashStyle
- VML (linguagem VML), atributo de propriedade DashStyle
- gráficos vetoriais, atributo de propriedade DashStyle
- atributo de propriedade DashStyle
- Linguagem VML (VML), atributo de propriedade Opacity
- VML (linguagem VML), atributo de propriedade Opacity
- gráficos vetoriais, atributo de propriedade Opacity
- atributo de propriedade Opacity
- Linguagem VML (VML), atributo de propriedade LineStyle
- VML (linguagem VML), atributo de propriedade LineStyle
- gráficos vetoriais, atributo de propriedade LineStyle
- atributo de propriedade LineStyle
- Linguagem VML (VML), atributo de propriedade joinstyle
- VML (linguagem VML), atributo de propriedade joinstyle
- gráficos vetoriais, atributo de propriedade joinstyle
- atributo de propriedade joinstyle
- Linguagem VML (VML), atributo de propriedade FillType
- VML (linguagem VML), atributo de propriedade FillType
- gráfico vetorial, atributo de propriedade FillType
- atributo de propriedade FillType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0cb69452abe5b3d743036f6a4db094da196281b575a6db65aa48535126fd917
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057362"
---
# <a name="using-the-stroke-element"></a>Usando o elemento Stroke

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Usando `<stroke>`

Como você aprendeu, você pode usar os atributos de propriedade **strokecolor** e **strokeweight** de uma forma predefinida, como,,,, `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` , `<roundrect>` , `<arc>` --para especificar a cor e o peso do contorno de uma forma. Neste tópico, Ilustraremos como desenhar uma forma que tenha uma estrutura de tópicos mais avançada.

Você pode posicionar o `<stroke>` subelemento dentro do `<shape>` , ou `<shapetype>` ou qualquer elemento Shape predefinido para descrever como desenhar o contorno da forma. Em seguida, você pode usar os atributos de propriedade, por exemplo, [DashStyle](#dashstyle), [Opacity](#opacity), [LineStyle](#linestyle), [joinstyle](#joinstyle), [FillType](#filltype) --do `<stroke>` subelemento para personalizar a estrutura de tópicos.

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="dashstyle"></a>DashStyle

Você pode usar o atributo de propriedade **DashStyle** do `<stroke>` subelemento para desenhar um contorno com vários estilos de traço.

**Exemplos:**

Se você especificar `<v:stroke dashstyle="solid" />` dentro do `<line>` elemento, poderá criar uma linha sólida, conforme mostrado na seguinte representação de VML:

![solid.gif (96 bytes)](images/solid.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="solid" />
</v:line>
```





Se você alterar o atributo da propriedade **DashStyle** para "ponto", poderá criar uma linha pontilhada, conforme mostrado na seguinte representação de VML:

![dot.gif (144 bytes)](images/dot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dot" />
</v:line>
```





Se você alterar o atributo da propriedade **DashStyle** para "Dash", poderá criar uma linha tracejada, conforme mostrado na seguinte representação de VML:

![dash.gif (137 bytes)](images/dash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dash" />
</v:line>
```





Se você alterar o atributo da propriedade **DashStyle** para "travessão ponto", poderá criar uma linha com um estilo tracejado e pontilhado, conforme mostrado na seguinte representação de VML:

![dashdot.gif (145 bytes)](images/dashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dashdot" />
</v:line>
```





Se você alterar o atributo da propriedade **DashStyle** para "longdash", poderá criar uma linha com um estilo tracejado longo, conforme mostrado na seguinte representação de VML:

![longdash.gif (123 bytes)](images/longdash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdash" />
</v:line>
```





Se você alterar o atributo da propriedade **DashStyle** para "longdashdot", poderá criar uma linha com um estilo tracejado longo e pontilhado, conforme mostrado na seguinte representação de VML:

![longdashdot.gif (135 bytes)](images/longdashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdashdot" />
</v:line>
```





Se você posicionar `<v:stroke dashstyle="dashdot" />` dentro do `<rect>` elemento, poderá criar um retângulo que tenha um esboço tracejado e pontilhado, conforme mostrado na seguinte representação de VML:

![rect.gif (615 bytes)](images/rect.gif)


```HTML
<v:rect style='width:100pt;height:80pt' strokecolor="red" strokeweight="2pt"/>
<v:stroke dashstyle="dashdot" />
</v:rect>
```





[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="opacity"></a>opacidade

Você pode usar o atributo de propriedade **Opacity** do `<stroke>` subelemento para desenhar um contorno com vários estilos de opacidade. O valor do atributo de propriedade **Opacity** pode ser qualquer número entre 0 e 1. Por padrão, é 1, indicando a opacidade total.

**Exemplos:**

A seguinte representação de VML cria uma linha com opacidade total:

![line1.gif (96 bytes)](images/line1.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
</v:line>
```





Se você adicionar `<v:stroke opacity="0.5" />` dentro do `<line>` elemento, poderá criar uma linha com opacidade de 50%, conforme mostrado na seguinte representação de VML:

![line2.gif (108 bytes)](images/line2.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
<v:stroke opacity="0.5" />
</v:line>
```





[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="linestyle"></a>estilo

Você pode usar o atributo de propriedade **LineStyle** do `<stroke>` subelemento para desenhar um contorno com vários estilos de linha.

**Exemplos:**

Se você especificar `<v:stroke linestyle="single" />` dentro do `<rect>` elemento, poderá criar um retângulo com um único contorno, conforme mostrado na seguinte representação de VML:

![single.gif (537 bytes)](images/single.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red" strokeweight="10pt">
<v:stroke linestyle="single" />
</v:rect>
```





Se você alterar o atributo da propriedade **LineStyle** para "thinthin", poderá criar um retângulo com a estrutura de tópicos (1:1:1), conforme mostrado na seguinte representação de VML:

![thinthin.gif (642 bytes)](images/thinthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthin" />
</v:rect>
```





Se você alterar o atributo da propriedade **LineStyle** para "thinthick", poderá criar um retângulo com a estrutura de tópicos (1:1:2), conforme mostrado na seguinte representação de VML:

![thinthick.gif (646 bytes)](images/thinthick.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthick" />
</v:rect>
```





Se você alterar o atributo da propriedade **LineStyle** para "thickthin", poderá criar um retângulo com a estrutura de tópicos (2:1:1), conforme mostrado na seguinte representação de VML:

![thickthin.gif (676 bytes)](images/thickthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickthin" />
</v:rect>
```





Se você alterar o atributo da propriedade **LineStyle** para "thickbetweenthin", poderá criar um retângulo com a estrutura de tópicos (1:1:2:1:1), conforme mostrado na seguinte representação de VML:

![thickbthin.gif (669 bytes)](images/thickbthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickbetweenthin" />
</v:rect>
```





[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="joinstyle"></a>joinstyle

Você pode usar o atributo **joinstyle** do `<stroke>` subelemento para definir como as linhas são unidas.

Por exemplo, para criar uma forma que tenha a estrutura de tópicos de junção redonda, conforme mostrado na ilustração a seguir, você pode especificar `<v:stroke joinstyle="round" />` dentro do `<polyline>` elemento, conforme mostrado na seguinte representação de VML:

![round.gif (660 bytes)](images/round.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="round" />
</v:polyline>
```





Se você alterar o atributo da propriedade **joinstyle** para "bisel", poderá criar uma forma que tenha a estrutura de tópicos de junção chanfrada, conforme mostrado na seguinte representação de VML:

![bevel.gif (650 bytes)](images/bevel.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="bevel" />
</v:polyline>
```





Se você alterar o atributo da propriedade **joinstyle** para "Mitre", poderá criar uma forma que tenha a estrutura de tópicos de junção de Mitre, conforme mostrado na seguinte representação de VML:

![miter.gif (702 bytes)](images/miter.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="miter" />
</v:polyline>
```





[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="filltype"></a>FillType

Você pode usar o atributo de propriedade **FillType** do `<stroke>` subelemento para desenhar um contorno com vários efeitos de preenchimento.

**Exemplos:**

Se você especificar `<v:stroke filltype="solid" />` dentro do `<roundrect>` elemento, poderá criar um retângulo arredondado com a estrutura de tópicos preenchida de forma sólida, conforme mostrado na seguinte representação de VML:

![solid.gif (701 bytes)](images/solidborder.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="solid" />
</v:roundrect>
```





Se você alterar o atributo da propriedade **FillType** para "Pattern", apontar o atributo da propriedade **src** para o local do arquivo de imagem padrão e definir o atributo da propriedade **color2** para a segunda cor de padrão, poderá criar um retângulo arredondado com um contorno de padrão, conforme mostrado na seguinte representação de VML:

![pattern.gif (1055 bytes)](images/pattern.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="pattern" src="image.gif"
color2="green" />
</v:roundrect>
```





Se você alterar o atributo de propriedade **FillType** para "tile" e apontar o atributo da propriedade **src** para o local do arquivo de imagem, poderá criar um retângulo arredondado com um contorno lado a lado, conforme mostrado na seguinte representação de VML:

![tile.gif (6617 bytes)](images/tile.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="tile" src="image2.gif" />
</v:roundrect>
```





Se você alterar o atributo de propriedade **FillType** para "frame" e apontar o atributo da propriedade **src** para o local do arquivo de imagem, poderá criar um retângulo arredondado com um contorno de imagem, conforme mostrado na seguinte representação de VML:

![frame.gif (6203 bytes)](images/frame.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="frame" src="image2.gif" />
</v:roundrect>
```





Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858395) .

 

 