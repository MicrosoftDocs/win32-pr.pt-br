---
title: Posicionando formas
description: Este artigo descreve as formas de posicionamento no VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.
ms.assetid: dbd68f54-201a-48dc-a3a9-a8dd42178c11
keywords:
- Web Workshop, posicionando formas
- Criando páginas da Web, posicionando formas
- Linguagem VML (VML), posicionando formas
- VML (linguagem VML), posicionando formas
- gráficos vetoriais, posicionando formas
- Formas de VML, posicionamento
- posicionando formas
- Linguagem VML (VML), estilo de posição estática
- VML (linguagem VML), estilo de posição estática
- gráficos vetoriais, estilo de posição estática
- estilo de posição estática
- Linguagem VML (VML), estilo de posição relativa
- VML (linguagem VML), estilo de posição relativa
- gráficos vetoriais, estilo de posição relativa
- estilo de posição relativa
- Linguagem VML (VML), estilo de posição absoluta
- VML (linguagem VML), estilo de posição absoluta
- gráficos vetoriais, estilo de posição absoluta
- estilo de posição absoluta
- Linguagem VML (VML), estilo de posição de índice z
- VML (linguagem VML), z-estilo da posição do índice
- gráficos vetoriais, estilo de posição de índice z
- estilo de posição de índice z
- Linguagem VML (VML), estilo de posição de rotação
- VML (linguagem VML), estilo de posição de rotação
- gráficos vetoriais, estilo de posição de rotação
- estilo de posição de rotação
- Linguagem VML (VML), inverter estilo de posição
- VML (linguagem VML), inverter estilo de posição
- gráficos vetoriais, inverter estilo de posição
- Inverter estilo de posição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c96a8de891ed1bbd1b9bfee9eff52ede946247b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407709"
---
# <a name="positioning-shapes"></a>Posicionando formas

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Você aprendeu como desenhar e colorir formas em uma página da Web usando a VML. Neste tópico, você usará a VML para posicionar com precisão elementos gráficos em uma página da Web.

A VML usa a mesma sintaxe definida nas seções [modelo de caixa](https://www.w3.org/TR/PR-CSS2/box.mdl) e modelo de [renderização visual](https://www.w3.org/TR/PR-CSS2/visuren.mdl) de [CSS2](https://www.w3.org/TR/PR-CSS2/) para posicionar formas em uma página da Web. Você pode usar [estático](#static), [relativo](#relative)ou [absoluto](#absolute) para determinar onde o ponto base está localizado em uma página da Web. Você pode usar os atributos de estilo **superior** e **esquerdo** para especificar o deslocamento do ponto de base no qual a caixa de contenção da forma será posicionada.

Você também pode usar o [z-index](#z-index) para especificar a ordem z das formas em uma página da Web.

Além disso, a VML fornece [rotação](#rotation) e [inverter](#flip) para girar ou inverter formas.

Neste tópico:

-   [static](#static)
-   [relative](#relative)
-   [absolute](#absolute)
-   [índice z](#z-index)
-   [gira](#rotation)
-   [flip](#flip)
-   [Resumo](#summary)

## <a name="static"></a>static

O estilo de posição padrão é estático, o que instrui os navegadores a posicionar a forma no ponto atual (o ponto base) no fluxo de texto e ignorar as configurações nos atributos de estilo **superior** e **esquerdo** .

Por exemplo, na representação de VML a seguir, a elipse vermelha é posicionada imediatamente após o texto "início da forma:", conforme mostrado na figura a seguir:

![\-ps.gif Shape1 (2123 bytes)](images/shape1-ps.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='width:80pt;height:90pt' fillcolor="red" />
End.
</body>
```





[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="relative"></a>relative

Definir o atributo de estilo de posição como "relativo" permite que você coloque a caixa de conteúdo com um deslocamento do ponto atual (o ponto base) no fluxo de texto. O deslocamento é determinado pelas configurações nos atributos de estilo **superior** e **esquerdo** . Lembre-se de que a caixa que a contém posicionada como relativa ocupa espaço no fluxo de texto.

Por exemplo, na representação de VML a seguir, a elipse vermelha é posicionada em 20 pontos à esquerda e 10 pontos da parte superior em relação ao ponto atual no fluxo de texto, conforme mostrado na figura a seguir:

![shape3.gif (2048 bytes)](images/shape3.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;width:80pt;
height:90pt;' fillcolor="red" />
End.
</body>
```





[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="absolute"></a>absoluto

Definir o atributo de estilo de posição como "absoluto" permite colocar a caixa de conteúdo em uma distância exata do canto superior esquerdo (o ponto de base) de seu elemento pai (o elemento posicionado que contém a forma). Lembre-se de que a caixa que o contém está posicionada como absoluta não ocupa espaço no fluxo de texto.

Por exemplo, na representação de VML a seguir, a elipse vermelha está contida no `<body>` elemento (a página da Web inteira); portanto, o ponto base está no canto superior esquerdo da página da Web. A caixa que o contém para a oval é posicionada exatamente 20 pontos da esquerda e 10 pontos da parte superior, em relação ao canto superior esquerdo da página da Web, conforme mostrado na figura a seguir:

![shape2.gif (2006 bytes)](images/shape2.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt
width:80pt; height:90pt;' fillcolor="red" />
End.
</body>
```





[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="z-index"></a>z-index

É possível posicionar uma forma que se sobrepõe a outra forma. Normalmente, o elemento gráfico listado por último no código HTML aparece na parte superior.

Na VML, você pode controlar a ordem z usando o atributo **z-index** Style. O valor desse atributo pode ser zero, um inteiro positivo ou um inteiro negativo. O gráfico que tem um valor maior de índice z é exibido na parte superior do gráfico que tem um valor menor de índice z. Quando ambos os elementos gráficos tiverem o mesmo valor de índice z, o gráfico listado por último no código HTML aparecerá na parte superior.

Por exemplo, na representação de VML a seguir, a elipse vermelha é exibida na parte superior do retângulo azul. Isso ocorre porque o valor do índice z da elipse vermelha é maior que o valor do índice z do retângulo azul.

![shape4.gif (572 bytes)](images/shape4.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index: 1'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt; z-index:0' fillcolor="blue" />
```





Se você alterar o índice z, conforme mostrado na representação de VML a seguir, a elipse vermelha se moverá para trás do retângulo azul.

![shape5.gif (469 bytes)](images/shape5.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index:0'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt;z-index:1'
fillcolor="blue" />
```





Se você fornecer um inteiro negativo, poderá usar o índice z para posicionar gráficos atrás do fluxo de texto normal, conforme mostrado na representação de VML a seguir.

![shape6.gif (2125 bytes)](images/shape6.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;z-index:-1;
width:80pt;height:90pt;' fillcolor="red" />
End.
</body>
```





[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="rotation"></a>rotação

Você pode usar o atributo de estilo de **rotação** para especificar quantos graus você deseja que uma forma ative em seu eixo. Um valor positivo indica uma rotação horária; um valor negativo indica uma rotação no sentido anti-horário.

Por exemplo, se você especificar **Style**= '... rotação: 90 ', você pode girar a forma 90 graus no sentido horário.

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="flip"></a>flip

Você pode usar o atributo **flip** Style para inverter uma forma em seu eixo x ou y de acordo com a tabela a seguir:



| Valor | Descrição                                                  |
|-------|--------------------------------------------------------------|
| x     | Virar a forma girada sobre o eixo y (Inverter x ordenada) |
| a     | Virar a forma girada sobre o eixo x (inverter as ordenada y) |



 

X e y podem ser especificados na propriedade flip.

Por exemplo, se você digitar **Style**= '... virar: x y ', você inverterá a forma em ambos os eixos x e y.

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="summary"></a>Resumo

Com base no que você aprendeu, você pode posicionar precisamente uma forma em uma página da Web seguindo estas etapas:

1.  Decida onde você deseja que a forma apareça em uma página da Web e o tamanho da forma.
2.  Especifique **Style**= ' posição: relativa (ou relativa) ' para determinar o ponto base.
3.  Use **Left** e **Top** para especificar o deslocamento do ponto de base.
4.  Use **largura** e **altura** para especificar o tamanho da caixa que contém para a forma.
5.  Use **z-index** para especificar a ordem z da forma.

 

 