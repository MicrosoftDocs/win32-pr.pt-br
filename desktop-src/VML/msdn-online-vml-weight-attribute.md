---
title: Atributo de peso da VML
description: Atributo de peso da VML
ms.assetid: 40164818-6b04-4afe-91cc-9fb8b12cb718
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba7a1a4d5dca91da6b3750f0d901d4e278a80dd7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105807189"
---
# <a name="vml-weight-attribute"></a>Atributo de peso da VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define a espessura de um traço. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Pincel](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *elemento* Weight = " *expressão* " >

**Sintaxe do script**

*elemento* . Weight = "*expressão*"

*expressão* = de *elemento*. Weight

**Comentários**

Esse atributo é o mesmo que o atributo **StrokeWeight** da **forma** e o substitui. O valor padrão é 1 ponto.

*Atributo padrão da VML*

**Exemplo**

O traço tem uma espessura de 5 pontos, e não dois pontos.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="2pt"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke weight="5pt"/>
   </v:shape>
```



 

 