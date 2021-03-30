---
title: Dimensionando formas
description: Dimensionando formas
ms.assetid: fe975ebd-9b27-409d-a7c2-ac5ee08d1d4f
keywords:
- Web Workshop, dimensionando formas
- Criando páginas da Web, dimensionando formas
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
ms.openlocfilehash: e2e7c64fdc0eaa32df1f22b06734b366609ee319
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641259"
---
# <a name="scaling-shapes"></a>Dimensionando formas

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Você aprendeu como desenhar e colorir formas em uma página da Web usando a VML. Neste tópico, Ilustraremos como dimensionar formas para qualquer tamanho desejado.

A VML usa a mesma sintaxe definida na seção [detalhes do modelo de renderização visual](https://www.w3.org/TR/PR-CSS2/visudet.mdl) da [especificação CSS2](https://www.w3.org/TR/PR-CSS2/) para especificar o tamanho da caixa que o contém para que o conteúdo de uma forma seja renderizado (desenhado) dentro da caixa que o contém. Você pode usar os atributos de estilo **Width** e **Height** para definir o tamanho da caixa que o contém.

Por exemplo, se você desenhar uma oval e especificar **Style**= ' largura: 75pt; altura: 100pt ', a elipse será desenhada dentro de uma caixa que contém um tamanho de 75 pontos (largura) por 100 pontos (altura), conforme mostrado na figura a seguir:

![oval1.gif (660 bytes)](images/oval1.gif)


```HTML
<v:oval style='width:75pt;height:100pt'
fillcolor="red" />
```





Se você alterar o tamanho para **Style**= ' largura: 120pt; altura: 140pt ', a elipse se tornará maior porque é dimensionada na nova caixa de conteúdo em um tamanho de 120 pontos (largura) por 140 pontos (altura), conforme mostrado na figura a seguir:

![oval2.gif (966 bytes)](images/oval2.gif)


```HTML
<v:oval style='width:120pt;height:140pt'
fillcolor="red" />
```





Se você alterar o tamanho para **Style**= ' largura: 60pt; altura: 40pt ', a elipse se tornará menor porque é dimensionada na nova caixa de conteúdo em um tamanho de 60 pontos (largura) por 40 pontos (altura), conforme mostrado na figura a seguir:

![oval3.gif (394 bytes)](images/oval3.gif)


```HTML
<v:oval style='width:60pt;height:40pt'
fillcolor="red" />
```





 

 