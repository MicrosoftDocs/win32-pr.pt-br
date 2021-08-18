---
title: Atributo de peso de VML
description: Atributo de peso de VML
ms.assetid: 40164818-6b04-4afe-91cc-9fb8b12cb718
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1a4dc7e33a4a1bf8421350bed9df374f7edd31a1c1a48a2b3e1549dc63084d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999086"
---
# <a name="vml-weight-attribute"></a>Atributo de peso de VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define a espessura de um traço. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Curso](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *element* weight=" *expressão* ">

**Sintaxe do script**

*element* .weight="*expression*"

*expressão* = *elemento*.weight

**Comentários**

Esse atributo é o mesmo que o **atributo StrokeWeight** de **Shape** e o substitui. O valor padrão é 1 ponto.

*Atributo padrão VML*

**Exemplo**

O traço tem uma espessura de 5 pontos, não 2 pontos.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="2pt"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke weight="5pt"/>
   </v:shape>
```



 

 