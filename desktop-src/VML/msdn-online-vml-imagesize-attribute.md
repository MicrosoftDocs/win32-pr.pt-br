---
title: Atributo imagesização de VML
description: Atributo imagesização de VML
ms.assetid: 6b021ac1-e447-46ad-9153-91f936fca0d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be63fb0adf39e2494ae2fa4d1037b96c7873a7c12524215de0d1ecfd016e116
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600242"
---
# <a name="vml-imagesize-attribute"></a>Atributo imagesização de VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Define o tamanho da imagem para o traço. Leitura/gravação. **VgVector2D**.

**Aplica-se a**

[Pincel](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *Element* ImageSize = " *expression* " >

**Sintaxe do script**

*Element* . ImageSize = "*expression*"

*expressão* = de *elemento*. ImageSize

**Comentários**

O padrão é o tamanho da imagem.

*Atributo padrão da VML*

**Exemplo**

A imagem de traço será de um tamanho de 10 a 10 pontos.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagesize="10pt,10pt"/>
   </v:shape>
```



 

 