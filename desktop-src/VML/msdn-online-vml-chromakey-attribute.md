---
title: Atributo Chromakey de VML
description: Atributo Chromakey de VML
ms.assetid: 937ced3f-2e55-4a22-a9e0-83dc198104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b69b10fe617de23783cf5e2e69b8b1a97b82fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294226"
---
# <a name="vml-chromakey-attribute"></a>Atributo Chromakey de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o valor de cor da imagem que será tratada como transparente. Leitura/gravação. **VgColor**.

**Aplica-se a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxe de marca**

<v: *Element* Chromakey = " *expressão* " >

**Sintaxe do script**

*Element* . Chromakey = "*expressão*"

*expressão* = de *elemento*. Chromakey

**Comentários**

Use esse atributo para tornar partes de uma imagem transparentes, inserindo a transparência em uma cor específica. Por exemplo, se você tornar o  valor Chromakey **preto**, qualquer parte da imagem preta será transparente e a cor de preenchimento será "mostrada" nessa parte da imagem.

*Atributo padrão da VML*

**Exemplo**

As áreas da imagem que são pretas sólidas ficarão transparentes, permitindo que a cor de preenchimento verde apareça nessas áreas.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata chromakey="black" src="kids.jpg"/>
   </v:shape>
```



 

 