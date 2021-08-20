---
title: Atributo Color (Stroke) (VML)
description: Atributo Color (Stroke) (VML)
ms.assetid: 8fa19789-0bd6-4e9f-8af4-566155eafc6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17b3dd30d95765c98ec754526349b2bdc274696112043065fa7ddc7d894b582
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125366"
---
# <a name="color-attribute-strokevml"></a>Atributo Color (Stroke) (VML)

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

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



 

 