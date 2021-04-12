---
title: Atributo ImageAspect de VML
description: Atributo ImageAspect de VML
ms.assetid: 9ae58a76-f097-4feb-9008-ab6212bae8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b873f7577907acb6d8f88f0290117651077b3c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294220"
---
# <a name="vml-imageaspect-attribute"></a>Atributo ImageAspect de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define como a taxa de proporção da imagem de traço será preservada. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Pincel](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v:

elemento *imageaspect = "* expression *" >*

**Sintaxe do script**

element *. imageaspect = "* expressão *"*

elemento de expressão *=* *. imageaspect*

**Comentários**

Os valores são:



| Valor   | Descrição                                |
|---------|--------------------------------------------|
| Ignorar  | Ignorar problemas de aspecto.                      |
| Mínimo | A imagem é pelo menos tão grande quanto **ImageSize**. |
| AtMost  | A imagem não é maior que **ImageSize**.     |



 

Em cada caso, o atributo **ImageSize** será ajustado para preservar o aspecto da imagem.

*Atributo padrão da VML*

**Exemplo**

A imagem de traço será pelo menos tão grande quanto o tamanho da imagem.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imageaspect="AtLeast"/>
   </v:shape>
```



 

 