---
title: Atributo StrokeColor de VML
description: Atributo StrokeColor de VML
ms.assetid: e7224d77-f788-43c7-aa8e-d5fc318f9d4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d379f41f3d2c1f03349beae8d0420a7c1a26429
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007708"
---
# <a name="vml-strokecolor-attribute"></a>Atributo StrokeColor de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define a cor do pincel que traça o caminho de uma forma. Leitura/gravação. [IVgColor](msdn-online-vml-ivgcolor.md).

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* strokecolor = " *expressão* " >

**Sintaxe do script**

*Element* . strokecolor = "*expressão*"

*expressão* = de *elemento*. strokecolor

**Comentários**

O valor é duplicado do atributo **Color** do elemento [Stroke](msdn-online-vml-stroke-element.md) .

*Atributo padrão da VML*

**Exemplo**

A cor do traço do retângulo é vermelha.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Exemplo do atributo StrokeColor](/previous-versions/bb264093(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 