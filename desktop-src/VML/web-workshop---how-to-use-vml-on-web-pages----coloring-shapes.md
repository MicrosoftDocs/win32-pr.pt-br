---
title: Formas de cores
description: este artigo descreve as formas de cores na VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.
ms.assetid: f528f0c7-1351-4bca-b309-67511431b711
keywords:
- Web Workshop, formas de cores
- Criando páginas da Web, formas de cores
- Linguagem VML (VML), formas de cores
- VML (linguagem VML), formas de cor
- gráficos vetoriais, formas de cores
- Formas de VML, coloração
- formas de cores
- Linguagem VML (VML), nomes de cor de palavra-chave
- VML (linguagem VML), nomes de cor de palavra-chave
- gráficos vetoriais, nomes de cor de palavra-chave
- nomes de cor de palavra-chave
- Linguagem VML (VML), RGB tercetos
- VML (linguagem VML), RGB tercetos
- gráficos vetoriais, tercetos RGB
- Tercetos RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8edd8b067f1e3648d2b69f473c02c59392a10b5716afea74b8f7b0c9d093989
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057034"
---
# <a name="coloring-shapes"></a>Formas de cores

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Como mencionamos nas seções anteriores, você pode usar "vermelho" para representar uma cor em vermelho, "azul" para representar uma cor em azul e assim por diante. Neste tópico, Ilustraremos como desenhar formas de qualquer cor desejada.

A VML estende a sintaxe de cor HTML e CSS. Quando o tipo de atributo de um elemento VML é Color--como **FillColor** e **strokecolor** , você pode expressar a cor usando um [nome de cor de palavra-chave](#keyword-color-name) ou um [terceto RGB](#rgb-triplet).

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="keyword-color-name"></a>Nome da cor da palavra-chave

O HTML 4,0 define uma lista de nomes de cor de palavra-chave. Eles são azul-piscina, preto, azul, Fuchsia, cinza, verde, limão, bordô, marrom, verde-oliva, roxo, vermelho, prata, azul-petróleo, branco e amarelo. O valor RGB para essas 16 cores é definido na [especificação de HTML 4,0](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) .

Por exemplo, você pode desenhar um retângulo preenchido com amarelo especificando e `fillcolor="yellow"` dar a ele um contorno azul especificando `strokecolor="blue"` , conforme mostrado na seguinte representação de VML:

![color1.gif (305 bytes)](images/color1.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="yellow" strokecolor="blue"/>
```





[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="rgb-triplet"></a>Terceto RGB

Se a cor não for um [nome de cor de palavra-chave](#keyword-color-name), você poderá expressar a cor como uma TERCETO decimal RGB ou um TERCETO hexadecimal RGB. Com o tercetos RGB, você pode especificar valores para os componentes vermelho, verde e azul da cor, definindo cada componente com um valor que varia de 0 a 255 em decimal, ou 00 a FF em hexadecimal.

Por exemplo, você pode criar um retângulo que é preenchido com uma cor personalizada com um valor RGB de 253, 249, 186 em decimal especificando `fillcolor="rgb(253,249, 186)"` ou `fillcolor="#FDF9BA"` , conforme mostrado na representação de VML a seguir. Em hexadecimal, o valor 253 torna-se FD, 249 torna-se F9 e 186 se torna BA.

![color2.gif (305 bytes)](images/color2.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="#FDF9BA" strokecolor="blue"/>
```





Se o RGB em hexadecimal tiver um padrão como XXYYZZ, você poderá abreviar isso como XYZ. Por exemplo, " \# 66FF99" pode ser escrito como " \# 6F9".

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="summary"></a>Resumo

Na VML, você pode representar uma cor em um dos seguintes formatos:

1.  FillColor = "Blue"
2.  FillColor = "RGB (0, 0255)"
3.  FillColor = " \# 0000FF"

 

 