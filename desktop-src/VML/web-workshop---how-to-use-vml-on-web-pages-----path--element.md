---
title: Usando o elemento Path
description: Usando o elemento Path
ms.assetid: fd7924e7-f94f-4bc9-aa45-02cf8f9bac9b
keywords:
- Web Workshop, elemento Path
- Criando páginas da Web, elemento Path
- Linguagem VML (VML), elemento de caminho
- VML (linguagem VML), elemento Path
- gráficos vetoriais, elemento Path
- elemento Path
- Elementos de VML, caminho
- Formas de VML, elemento Path
- Linguagem VML (VML), personalizando contornos de forma
- VML (linguagem VML), personalizando contornos de forma
- gráficos vetoriais, personalizando contornos de forma
- Formas de VML, personalizando contornos
- Personalizando contornos de forma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba82d0ab946ef8937b68b4934f9c4d928bd25225
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641712"
---
# <a name="using-the-path-element"></a>Usando o elemento Path

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Você aprendeu que pode usar os elementos de forma predefinidos da VML, como `<oval>` , `<line>` , `<polyline>` , `<curve>` , `<rect>` , `<roundrect>` e `<arc>` --para desenhar uma forma. Neste tópico, Ilustraremos como usar o `<path>` subelemento para personalizar a estrutura de tópicos de uma forma.

Você pode posicionar o `<path>` subelemento dentro do `<shape>` `<shapetype>` elemento ou. Você pode usar os atributos de Propriedade do `<path>` subelemento para personalizar a estrutura de tópicos da forma.

Por exemplo, para desenhar a forma personalizada ilustrada na imagem a seguir, você pode usar o `<path>` subelemento para definir o contorno da forma, conforme mostrado na seguinte representação de VML:

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





-   Os valores `m 8,65` indicam que o desenho começa no ponto (8, 65).
-   Os valores `l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155, 92,121, 42,155, 60,100` indicam que uma linha reta começa no ponto atual (8, 65) e termina no ponto determinado (72, 65), que se torna o novo ponto atual. Uma nova linha começa no ponto atual (72, 65) e termina no ponto determinado, que se torna o novo ponto atual e assim por diante, até o ponto final (60, 100).
-   `x` indica que o caminho será fechado por uma linha reta que começa no ponto atual (60, 100) e termina no ponto original (8, 65).
-   `e` indica parar o desenho.

Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858391) .

 

 