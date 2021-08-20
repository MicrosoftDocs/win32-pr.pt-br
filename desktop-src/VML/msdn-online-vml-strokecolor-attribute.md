---
title: Atributo StrokeColor do VML
description: Atributo StrokeColor do VML
ms.assetid: e7224d77-f788-43c7-aa8e-d5fc318f9d4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a419813c5bd9db4370320f9f181477013136c70265f4ba1d8572a38ae9e3c473
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124229"
---
# <a name="vml-strokecolor-attribute"></a>Atributo StrokeColor do VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define a cor do pincel que traçou o caminho de uma forma. Leitura/gravação. [IVgColor.](msdn-online-vml-ivgcolor.md)

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* strokecolor=" *expressão* ">

**Sintaxe do script**

*expressão element* .strokecolor=""

*expressão* = *elemento*.strokecolor

**Comentários**

O valor é duplicado do **atributo Color** do [elemento Stroke.](msdn-online-vml-stroke-element.md)

*Atributo padrão VML*

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



[Exemplo de atributo StrokeColor](/previous-versions/bb264093(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 