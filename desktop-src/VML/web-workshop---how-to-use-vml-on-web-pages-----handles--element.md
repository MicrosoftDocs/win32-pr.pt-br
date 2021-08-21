---
title: Usando o elemento Handles
description: Usando o elemento Handles
ms.assetid: d748f74c-40e5-499a-bb61-94862eb3811c
keywords:
- Workshop da Web, elemento handles
- projetando páginas da Web, elemento handles
- linguagem VML (VML), elemento handles
- Elemento VML (linguagem VML),handles
- gráficos vetoriais, elemento handles
- elemento handles
- Elementos VML,handles
- Formas VML, elemento handles
- linguagem VML (VML), anexando texto a formas
- VML (linguagem VML), anexando texto a formas
- gráficos vetoriais, anexando texto a formas
- Formas VML, anexando texto
- anexando texto a formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d504024a3d5c42caf8af116a08e5bd8787905991f14c4181fe3a75b10f4814
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057195"
---
# <a name="using-the-handles-element"></a>Usando o elemento Handles

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Neste tópico, ilustramos como usar o elemento `<handles>` para anexar texto a uma forma.

Você pode colocar o subconjunto dentro de ou para definir elementos de interface do usuário que podem variar os valores `<handles>` `<shape>` `<shapetype>` **adj** na forma.

Por exemplo, conforme mostrado na representação VML a seguir, você pode fornecer uma alça de ajuste (caixa amarela) que os usuários podem simplesmente arrastar para ajustar a forma.

Observação: os alças estão disponíveis quando essa forma VML é exibida Microsoft Office aplicativos, em que a forma deve ser manipulável.

![shape1.gif (564 bytes)](images/shape1h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="16200,5400"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





Observe que a única diferença entre a representação VML anterior e a seguinte é o **valor adj.**

![shape2.gif (1361 bytes)](images/shape2h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="11304,6600"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





Para obter mais informações sobre esse elemento, consulte a [especificação de VML](https://www.w3.org/TR/NOTE-VML#-toc416858393) .

 

 