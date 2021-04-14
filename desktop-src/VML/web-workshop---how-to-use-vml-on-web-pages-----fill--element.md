---
title: Usar o elemento Fill
description: Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.
ms.assetid: ed36601d-2e90-412e-ac3f-58324fac300d
keywords:
- Web Workshop, elemento Fill
- Criando páginas da Web, elemento Fill
- Linguagem VML (VML), elemento Fill
- VML (linguagem VML), elemento Fill
- gráfico vetorial, elemento Fill
- elemento Fill
- Elementos de VML, preenchimento
- Formas de VML, elemento Fill
- Linguagem VML (VML), preenchimento gradual
- VML (linguagem VML), preenchimento gradual
- gráficos vetoriais, preenchimento gradual
- Formas de VML, preenchimento gradual
- formas preenchidas com gradiente
- Linguagem VML (VML), preenchimento de padrão
- VML (linguagem VML), preenchimento de padrão
- gráficos vetoriais, preenchimento de padrão
- Formas de VML, preenchimento de padrão
- formas preenchidas por padrão
- Linguagem VML (VML), preenchimento de imagem
- VML (linguagem VML), preenchimento de imagem
- gráficos vetoriais, preenchimento de imagem
- Formas de VML, preenchimento de imagem
- formas preenchidas por imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf497a3120f53e24f1cff2bf7084469754bbaf7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104552511"
---
# <a name="using-the-fill-element"></a>Usar o elemento Fill

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Como você aprendeu, você pode usar o atributo da propriedade **FillColor** de um elemento Shape predefinido, como,,,,, `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` , `<arc>` --para especificar a cor usada para preencher a forma. Neste tópico, Ilustraremos como desenhar uma forma que é preenchida com efeitos mais avançados.

Você pode posicionar o `<fill>` subelemento dentro do `<shape>` , ou `<shapetype>` ou qualquer elemento Shape predefinido para descrever como preencher a forma. Você pode usar os atributos de Propriedade do `<fill>` subelemento para personalizar o efeito de preenchimento, como preenchimento de [gradiente](#gradient-fill), [preenchimento de padrão](#pattern-fill), [preenchimento de imagem](#picture-fill).

Neste tópico:

-   [Preenchimento gradual](#gradient-fill)
-   [Preenchimento de padrão](#pattern-fill)
-   [Preenchimento de imagem](#picture-fill)

## <a name="gradient-fill"></a>Preenchimento gradual

Para desenhar uma forma preenchida com gradiente, você pode definir o atributo de propriedade **Type** do `<fill>` subelemento como "gradation" ou "gradientRadial" e, em seguida, especificar outros atributos de Propriedade do `<fill>` subelemento, como **Method**, **color2**, **Focus** e **Angle**.

**Exemplos:**

Para criar uma forma que seja preenchida com gradiente horizontalmente, você pode definir o atributo da propriedade **Type** como "gradation", conforme mostrado na seguinte representação de VML:

![horizontal1.gif (3055 bytes)](images/horizontal1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="gradient" />
</v:rect>
```




Se você alterar o atributo da propriedade **FillColor** da forma, a forma será preenchida com gradiente com uma cor diferente. Você pode adicionar uma segunda cor especificando o atributo de propriedade **color2** do `<fill>` subelemento. Por exemplo, para criar uma forma que seja preenchida com gradiente em duas cores, você pode adicionar uma segunda cor especificando o atributo da propriedade **color2** do `<fill>` subelemento, conforme mostrado na seguinte representação de VML:

![horizontal2.gif (3127 bytes)](images/horizontal2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill color2="blue" type="gradient" />
</v:rect>
```




Você pode definir o atributo de Propriedade do **método** como "linear" ou "Sigma" ou "any" ou "None". O efeito do gradiente é ligeiramente diferente. Além disso, você pode usar o atributo de propriedade **Angle**,**Focus**,**focussize** ou **focusposition** para alterar a forma como o gradiente é.

**Exemplos:**

 

Para criar uma forma que seja preenchida com gradiente verticalmente, você pode definir o atributo de Propriedade Angle como Angle = "-90", conforme mostrado na seguinte representação de VML:

![vertical1.gif (3836 bytes)](images/vertical1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-90"
type="gradient" />
</v:rect>
```




Para criar uma forma que seja preenchida com gradiente da diagonal se movendo para cima, você pode definir o atributo de propriedade **Angle** como Angle = "-135", conforme mostrado na seguinte representação de VML:

![dialgonalup1.gif (5816 bytes)](images/dialgonalup1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-135"
type="gradient" />
</v:rect>
```




Para criar uma forma que seja preenchida com gradiente de uma diagonal para baixo, você pode definir o atributo de propriedade **Angle** como Angle = "-45", conforme mostrado na seguinte representação de VML:

![diagonaldown1.gif (5753 bytes)](images/diagonaldown1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
type="gradient" />
</v:rect>
```




Para criar uma forma que seja preenchida com gradiente do centro, você pode especificar `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"` , conforme mostrado na seguinte representação de VML:

![fromcenter1.gif (4598 bytes)](images/fromcenter1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
focus="100%" focusposition=".5,.5" focussize="0,0"
type="gradientRadial" />
</v:rect>
```




[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="pattern-fill"></a>Preenchimento de padrão

Para desenhar uma forma preenchida por padrão, você pode definir o atributo de propriedade **Type** do `<fill>` subelemento como "Pattern" e, em seguida, especificar outros atributos de Propriedade do `<fill>` subelemento, como **src** e **color2**.

**Exemplos:**

Para criar uma forma que é preenchida com uma imagem de padrão, você pode especificar o atributo de propriedade **Type** como "Pattern" e apontar o atributo de propriedade **src** para o local do arquivo de imagem de padrão, conforme mostrado na seguinte representação de VML:

![pattern1.gif (872 bytes)](images/pattern1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="pattern" src="image1.gif"/>
</v:rect>
```




Se você apontar o atributo de propriedade **src** para um arquivo de padrão diferente, poderá criar uma forma que é preenchida com um padrão diferente. Além disso, você pode alterar a cor especificando um valor diferente para o atributo de propriedade **FillColor** ou **color2** , conforme mostrado na seguinte representação de VML:

![pattern2.gif (831 bytes)](images/pattern2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="white">
<v:fill type="pattern" src="image2.gif"
color2="blue" />
</v:rect>
```




[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="picture-fill"></a>Preenchimento de imagem

Para desenhar uma forma preenchida por imagem, você pode definir o atributo de propriedade **Type** do `<fill>` subelemento como "frame" e, em seguida, especificar outros atributos de Propriedade do `<fill>` subelemento, como **src** e **color2**.

**Exemplos:**

Para criar uma forma que é preenchida com um arquivo de imagem, você pode especificar o atributo de propriedade **Type** como "frame" e, em seguida, apontar o atributo de propriedade **src** para o local do arquivo de imagem, conforme mostrado na seguinte representação de VML:

![picture1.gif (8496 bytes)](images/picture1.gif)


```HTML
<v:oval style='width:120pt;height:90pt' strokecolor="red"
strokeweight="2.5pt">
<v:fill type="frame" src="image1.jpg" />
</v:oval>
```




Você pode criar facilmente uma forma que é preenchida com uma imagem diferente apontando o atributo de propriedade **src** para outro arquivo.

Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858394) .

 

 