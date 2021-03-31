---
title: Usando o espaço de coordenadas local
description: Usando o espaço de coordenadas local
ms.assetid: 8b5bc176-878f-4391-ab03-3f1c0e7713c3
keywords:
- Web Workshop, espaço de coordenadas local
- Criando páginas da Web, espaço de coordenadas local
- Linguagem VML (VML), espaço de coordenadas local
- VML (linguagem VML), espaço de coordenadas local
- gráficos vetoriais, espaço de coordenadas local
- espaço de coordenadas local
- Formas de VML, espaço de coordenadas local
- Linguagem VML (VML), agrupamento de formas
- VML (linguagem VML), agrupamento de formas
- gráficos vetoriais, agrupamento de formas
- Formas de VML, agrupamento
- agrupando formas
- Linguagem VML (VML), dimensionar formas
- VML (linguagem VML), dimensionar formas
- gráficos vetoriais, dimensionando formas
- Formas de VML, dimensionamento
- Dimensionando formas
- Linguagem VML (VML), dimensionando formas
- VML (linguagem VML), dimensionando formas
- gráficos vetoriais, dimensionando formas
- Formas de VML, dimensionamento
- Dimensionando formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c82d77ce16ae60bfc1249125d25b1139aeb8f44e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641708"
---
# <a name="using-local-coordinate-space"></a>Usando o espaço de coordenadas local

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Como você aprendeu, você pode especificar os atributos de estilo de **largura** e **altura** para definir o tamanho de uma caixa contendo dentro da qual o conteúdo de uma forma ou grupo será renderizado. Neste tópico, explicaremos o espaço de coordenadas local e como ele é usado em VML para dimensionar formas.

Se você foi solicitado a desenhar um retângulo de uma polegada por dois centímetros em um pedaço de papel de grade, a primeira coisa que você descobriria é onde começar (o ponto de origem). Em seguida, você descobrirá como mapear uma polegada para as células do papel de grade (a coordenada).

Da mesma forma, quando o conteúdo de uma forma ou grupo é renderizado dentro da caixa que o contém em uma página da Web, o ponto de origem e a coordenada devem ser definidos. A VML fornece espaço de coordenadas local para permitir que cada forma ou grupo defina seu próprio ponto de origem e coordenada. Se você não especificar um espaço de coordenadas, o padrão será usado. Por padrão, a origem começa no canto superior esquerdo da caixa que o contém.

Por exemplo, a representação de VML para a cor vermelha mostrada abaixo não especifica os atributos de propriedade **coordsize** e **coordorigin** . Portanto, um espaço de coordenadas local padrão é usado. O tamanho da elipse é de 100 pontos (largura) por 75 pontos (altura). Você pode redimensionar a elipse especificando uma largura ou altura diferente, como você aprendeu no tópico [dimensionar formas](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md) .

![oval1.gif (627 bytes)](images/oval1.gif)


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red">
</v:oval>
```





Quando a forma se torna mais complicada, ou quando você deseja agrupar várias formas e dimensioná-las juntas, você deve usar o recurso de espaço de coordenadas local fornecido em VML.

Para cada forma ou grupo, você pode usar os atributos de propriedade **coordsize** e **coordorigin** para definir o espaço de coordenadas local do grupo ou da forma. O atributo **coordsize** especifica o número de unidades ao longo da largura e a altura da caixa que a contém. O atributo **coordorigin** define a coordenada no canto superior esquerdo da caixa que o contém. Todas as informações relacionadas à posição (como largura, altura, esquerda, superior, caminho etc.) são expressas em termos da unidade no espaço de coordenadas local.

Por exemplo, como mostrado na representação VML a seguir, `width: 100pt; height: 100pt;` define o tamanho da caixa que contém para que a forma seja de 100 pontos por 100 pontos.

![cord1.gif (836 bytes)](images/cord1.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt; width:100pt; height:100pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





-   `coordsize="21600,21600"` define o tamanho do espaço de coordenadas local para que a forma seja de 21600 unidades por 21600 unidades. Portanto, uma unidade no espaço de coordenadas local é equivalente a 1/216 pontos.
-   `path="m10800,0l0,10800,10800,21600,21600,10800xe"` define o contorno da forma como uma forma de losango. Como aprendemos, todas as informações relacionadas à posição (como largura, altura, esquerda, superior, caminho etc.) são expressas em termos da unidade no espaço de coordenadas local. Portanto, 10800 nos `<path>` significa 10800 unidades, que é equivalente a 50 pontos.

Quando você quiser redimensionar essa forma de losango, basta especificar uma largura ou altura diferente, isto é, Você não precisa alterar nenhum valor no `<path>` . Para essa forma complicada, se você não usou o recurso de espaço de coordenadas local, precisaria alterar cada valor no `<path>` sempre que quisesse redimensioná-lo.

Por exemplo, você pode dimensionar a forma de losango simplesmente especificando uma largura ou altura diferente, conforme mostrado na seguinte representação de VML:

![cord2.gif (1692 bytes)](images/cord2.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt;width:200pt; height:200pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





Você também pode usar o espaço de coordenadas local no `<group>` elemento para que o conteúdo de todas as formas dentro do grupo seja dimensionado em conjunto de acordo com a mesma coordenada. Em seguida, sempre que desejar dimensionar ou mover um grupo de formas, basta alterar as configurações de largura e altura, ou **coordsize** e **coordorigin** , do grupo.

Por exemplo, na representação VML a seguir, `<v:group style='... width:200pt;height:200pt;'>` define o tamanho da caixa que contém para que o grupo seja de 200 pontos por 200 pontos.

![cord3.gif (645 bytes)](images/cord3.gif)


```HTML
<v:group style='position:relative;left:1pt;top:2pt;width:200pt; height:200pt;'
coordsize="1000,1000" coordorigin="-500,-500">
<v:oval style='position:relative;left:0;top:0;width:400;height:300;' fillcolor="red" />
<v:roundrect style='position:relative;left:0;top:0;width:250;height:200;' fillcolor="green" />
</v:group>
```





-   `coordsize="1000,1000"` define o tamanho do espaço de coordenadas local para o grupo ser de 1000 unidades por 1000 unidades. Portanto, uma unidade no espaço de coordenadas local é equivalente a 1/5 pontos.
-   `coordorigin="-500,-500"` define o canto superior esquerdo da caixa que o contém como "-500,-500". Portanto, o sistema de coordenadas dentro da caixa recipiente varia de-500 a 500 ao longo do eixo x e-500 a 500 ao longo do eixo y. Em outras palavras, o centro da caixa que o contém é "0, 0".
-   `<v:oval style='... width:400;height:300;'>` define o tamanho da caixa que contém para que a oval vermelha seja de 400 unidades (largura) por 300 unidades (altura). Como uma unidade no espaço de coordenadas local é equivalente ao ponto de 1/5, o tamanho da caixa de conteúdo da oval vermelha é de 80 pontos (largura) por 60 pontos (altura).

Da mesma forma, o tamanho da caixa que a contém para o RoundRect verde é de 50 pontos (largura) por 40 pontos (altura).

Quando você quiser redimensionar a elipse vermelha e a RoundRect verde, basta alterar `<v:group style='... width:200pt;height:200pt;'>` . É isso – você não precisa alterar o tamanho das duas formas individualmente.

Por exemplo, se você alterar `<v:group style='... width:200pt;height:200pt;'>` para `<v:group style='... width:300pt;height:300pt;'>` , as formas se tornarão maiores, conforme mostrado na figura a seguir:

![cord4.gif (943 bytes)](images/cord4.gif)



Você também observaria que as formas estão localizadas de forma diferente. Isso ocorre porque as formas são desenhadas de "0, 0" que está localizado no centro da caixa que o contém. Como você torna a caixa de conteúdo maior, o centro da caixa que a contém também é movido.

Se você alterar `coordorigin="-500,-500"` para `coordorigin="0,0"` , conforme mostrado na imagem a seguir, observará que a elipse vermelha e as RoundRect verdes são deslocadas para o novo local. Isso ocorre porque "0, 0" Agora localiza no canto superior esquerdo da caixa que o contém.

![cord5.gif (648 bytes)](images/cord5.gif)



Também é importante observar que a caixa que o contém não estabelece uma região de recorte. Os gráficos podem ser desenhados fora dos limites da caixa que o contém. A caixa que o contém simplesmente serve para mapear o espaço de coordenadas local para o espaço da página.

Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858382) .

 

 