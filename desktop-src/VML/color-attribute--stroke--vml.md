---
title: Atributo Color (Stroke) (VML)
description: Atributo Color (Stroke) (VML)
ms.assetid: 8fa19789-0bd6-4e9f-8af4-566155eafc6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faa91522adcba5fa854d4749dc257f5489969270
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105784987"
---
# <a name="color-attribute-strokevml"></a>Atributo Color (Stroke) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define a cor de um traço. Leitura/gravação. **VgColor**.

**Aplica-se a**

[Pincel](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *Element* Color = " *expressão* " >

**Sintaxe do script**

*Element* . Color = "*expressão*"

*expressão* = de *elemento*. Color

**Comentários**

Substitui o atributo **StrokeColor** de uma forma. O valor padrão é **preto**.

*Atributo padrão da VML*

**Exemplo**

A forma tem uma cor de traço de **verde**, e não **vermelha**.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke color="green"/>
   </v:shape>
```



 

 