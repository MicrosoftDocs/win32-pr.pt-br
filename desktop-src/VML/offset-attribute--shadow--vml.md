---
title: Atributo de deslocamento (sombra) (VML)
description: Atributo de deslocamento (sombra) (VML)
ms.assetid: bb5810cd-bd9a-4888-a0ce-8de732215c80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0683e9536e10bed141ecca56b4335d6221c5ced7e3d26220908aa388b453843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596901"
---
# <a name="offset-attribute-shadowvml"></a>Atributo de deslocamento (sombra) (VML)

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Define até que distância a sombra ultrapassa a forma. Leitura/gravação. **VgVector2D**.

**Aplica-se a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxe de marca**

<v: *elemento* offset = " *expressão* " >

**Sintaxe do script**

*elemento* . Offset = "*expressão*"

*expressão* = de *elemento*. Offset

**Comentários**

O deslocamento padrão para o valor x é 2PT e o padrão para o valor y é 2PT. Os valores são uma medida absoluta ou um valor fracionário de Shape. Se houver frações, elas vão de 50% a-50%.

*Atributo padrão da VML*

**Exemplo**

A forma tem uma sombra com um deslocamento de 5 pontos para baixo e 10 pontos à direita.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" offset="10pt,5pt"/>
   </v:shape>
```



 

 