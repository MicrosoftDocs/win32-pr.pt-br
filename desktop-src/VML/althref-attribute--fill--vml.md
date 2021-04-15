---
title: Atributo AltHRef (Fill) (VML)
description: Atributo AltHRef (Fill) (VML)
ms.assetid: 3f6376e3-24db-412c-b265-5916950c3824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0679e5aa01b934092c21bfa5d0504b056f620f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454147"
---
# <a name="althref-attribute-fillvml"></a>Atributo AltHRef (Fill) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define uma referência alternativa para uma imagem. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Preencher](msdn-online-vml-fill-element.md)

**Sintaxe de marca**

<v: *Element* o:althref = " *expressão* " >

**Sintaxe do script**

*Element* . althref = "*expressão*"

*expressão* = de *elemento*. althref

**Comentários**

Dá suporte à preservação de dados PICT por meio de roundtripping HTML. Na gravação em HTML, a representação alternativa (os dados originais do PICT se o arquivo foi originado do Apple Macintosh) é salva. Em HTML Read, **AltHRef** é favorecedo sobre **src**.

*Atributo de extensões de Microsoft Office*

**Exemplo**

O preenchimento da forma tem um **AltHRef** que aponta para um arquivo chamado myimage.gif.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill o:althref="myimage.gif"/>
   </v:shape>
```



 

 