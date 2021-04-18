---
title: Atributo AltHRef (Stroke) (VML)
description: Atributo AltHRef (Stroke) (VML)
ms.assetid: ee7c1710-1f8e-42c4-895f-d0f3d15ca6db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021e89e87f70910561e55406e282920cdbed2963
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105810654"
---
# <a name="althref-attribute-strokevml"></a>Atributo AltHRef (Stroke) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica uma referência alternativa para uma imagem. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Pincel](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *Element* o:althref = " *expressão* " >

**Sintaxe do script**

*Element* . althref = "*expressão*"

*expressão* = de *elemento*. althref

**Comentários**

Dá suporte à preservação de dados PICT por meio de roundtripping HTML. Na gravação em HTML, a representação alternativa (ou seja, os dados originais do PICT, se o arquivo foi originado do Macintosh) é salvo. Em HTML Read, **AltHRef** é favorecedo sobre **src**.

*Atributo de extensões de Microsoft Office*

**Exemplo**

O traço da forma tem um **AltHRef** que aponta para um arquivo chamado myimage.gif.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200, 200, 200,1 x e">
   <v:stroke o:althref="myimage.gif"/>
   </v:shape>
```



 

 