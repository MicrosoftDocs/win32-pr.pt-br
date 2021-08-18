---
title: Usando o elemento TextPath
description: Usando o elemento TextPath
ms.assetid: 7728cdd6-d291-4ec5-b5e0-4a44a7d72eae
keywords:
- Web Workshop, elemento TextPath
- Criando páginas da Web, elemento TextPath
- Linguagem VML (VML), elemento TextPath
- VML (linguagem VML), elemento TextPath
- gráficos vetoriais, elemento TextPath
- elemento TextPath
- Elementos de VML, TextPath
- Formas de VML, elemento TextPath
- Linguagem VML (VML), texto de desenho
- VML (linguagem VML), texto de desenho
- gráficos vetoriais, desenho de texto em VML
- desenhando texto
- Formas de VML, texto de desenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5db3b76d0c4ad2e56c59cfcf6dd39a2af51317b63ee190f47d794933282b5a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056964"
---
# <a name="using-the-textpath-element"></a>Usando o elemento TextPath

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Neste tópico, Ilustraremos como usar o `<textpath>` elemento para desenhar texto com vários estilos.

Você pode posicionar o `<textpath>` subelemento dentro `<shape>` ou `<shapetype>` para desenhar o texto. Você pode usar os atributos de Propriedade do `<textpath>` subelemento para personalizar o texto. Você também pode usar o `<formulas>` subelemento para definir a estrutura de tópicos do texto.

Por exemplo, para criar o texto mostrado na imagem a seguir, você pode digitar a representação de VML abaixo. Observe que usamos o `<shapetype>` elemento para definir um protótipo para o contorno do texto. Em seguida, criamos uma instância de duas formas a partir do mesmo ShapeType. Você pode simplesmente alterar o atributo de propriedade da **cadeia de caracteres** para exibir texto diferente.

![\-1.gif Shape1 (4898 bytes)](images/shape1-1t.gif)

![\-2.gif Shape1 (2789 bytes)](images/shape1-2t.gif)


```HTML
<v:shapetype id="MyShape"
coordsize="21600,21600" adj="9931"
path="m0@0c7200@2,14400@1,21600,0m0@5c7200@6,14400@6,21600@5e">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="prod #0 3 4"/>
<v:f eqn="prod #0 5 4"/>
<v:f eqn="prod #0 3 8"/>
<v:f eqn="prod #0 1 8"/>
<v:f eqn="sum 21600 0 @3"/>
<v:f eqn="sum @4 21600 0"/>
<v:f eqn="prod #0 1 2"/>
<v:f eqn="prod @5 1 2"/>
<v:f eqn="sum @7 @8 0"/>
<v:f eqn="prod #0 7 8"/>
<v:f eqn="prod @5 1 3"/>
<v:f eqn="sum @1 @2 0"/>
<v:f eqn="sum @12 @0 0"/>
<v:f eqn="prod @13 1 4"/>
<v:f eqn="sum @11 14400 @14"/>
</v:formulas>
<v:path textpathok="t" />
<v:textpath on="t" fitshape="t" xscale="t"/>
</v:shapetype>

<v:shape type="#MyShape" style='position:relative; top:5; left:5;
width:261.6pt;height:71.45pt;' adj="8717" fillcolor="red" strokeweight="1pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/> <v:textpath
style='font-family:"Arial Black";v-text-kern:t' trim="t"
fitpath="t" xscale="f" string="Hello World !"/>
</v:shape>

<v:shape type="#MyShape" style='position:relative; top:120; left:5; width:207pt;
height:63pt;' adj="8717" fillcolor="blue" strokeweight="2pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/>
<v:textpath style='font-family:"Times New Roman";v-text-kern:t'
trim="t" fitpath="t" xscale="f" string="VML"/>
</v:shape>
```





Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858398) .

 

 