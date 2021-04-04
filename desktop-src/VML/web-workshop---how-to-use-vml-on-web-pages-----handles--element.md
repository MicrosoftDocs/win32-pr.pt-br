---
title: Usando o elemento Handles
description: Usando o elemento Handles
ms.assetid: d748f74c-40e5-499a-bb61-94862eb3811c
keywords:
- Web Workshop, elemento Handles
- Criando páginas da Web, elemento Handles
- Linguagem VML (VML), elemento Handles
- VML (linguagem VML), elemento Handles
- elementos gráficos vetoriais, elemento Handles
- elemento Handles
- Elementos de VML, identificadores
- Formas de VML, elemento Handles
- Linguagem VML (VML), anexando texto a formas
- VML (linguagem VML), anexando texto a formas
- gráficos vetoriais, anexando texto a formas
- Formas de VML, anexando texto
- anexando texto a formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d54c721d50f51c46cd4bf08393e85ad83307fc1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007606"
---
# <a name="using-the-handles-element"></a>Usando o elemento Handles

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Neste tópico, Ilustraremos como usar o `<handles>` elemento para anexar texto a uma forma.

Você pode posicionar o `<handles>` subelemento dentro `<shape>` ou `<shapetype>` para definir elementos de interface do usuário que podem variar os valores de **adj** na forma.

Por exemplo, como mostra a representação de VML a seguir, você pode fornecer um identificador de ajuste (caixa amarela) que os usuários podem simplesmente arrastar para ajustar a forma.

Observação: as alças estão disponíveis quando essa forma VML é exibida em aplicativos Microsoft Office, em que a forma é destinada a ser manipulable.

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





Observe que a única diferença entre a representação VML anterior e a seguinte é o valor de **adj** .

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





Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858393) .

 

 