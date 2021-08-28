---
title: Atributo VML Control2
description: Atributo VML Control2
ms.assetid: fd0f92fa-ae70-46c9-bfbe-fad8deea34f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 702c0eee9ba861a73ec6d9f0fd07cca22a551c92c5add5498cd0e33522419fcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999246"
---
# <a name="vml-control2-attribute"></a>Atributo VML Control2

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define o segundo ponto de controle de uma curva dezier. Leitura/gravação. **VgVector2D.**

**Aplica-se a**

[Curva](msdn-online-vml-curve-element.md)

**Sintaxe de marca**

<v: *element* control2=" *expressão* ">

**Sintaxe do script**

*element* .control2="*expression*"

*expressão* = *elemento*.control2

**Comentários**

Define o segundo ponto de controle de uma curva dezier cúbica no espaço de coordenadas do elemento pai. Se o pai não for um [](msdn-online-vml-units.md) elemento VML, a unidade padrão será um pixel (mas em, cm, mm, pt, pc também poderá ser especificado). O padrão é 20.0.

*Atributo padrão VML*

**Exemplo**

A curva está rindo. Ele começa à esquerda e termina à direita. Os dois pontos de controle são organizados ao longo do caminho, de modo a efetuar pull da curva para baixo para dar a aparência de um sorriso.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```





 

 