---
title: Atributo de opacidade (Fill) (VML)
description: Atributo de opacidade (Fill) (VML)
ms.assetid: abd2fe4d-6391-4413-80f0-549bcc74f42e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b913498705e65fa7211db4b4cef039894d573a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641808"
---
# <a name="opacity-attribute-fillvml"></a>Atributo de opacidade (Fill) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define a transparência de um preenchimento. Leitura/gravação. [VgFraction](msdn-online-vml-vgfraction-data-type.md).

**Aplica-se a**

[Preencher](msdn-online-vml-fill-element.md)

**Sintaxe de marca**

<v: *elemento* Opacity = " *expressão* " >

**Sintaxe do script**

*elemento* . Opacity = "*expressão*"

*expressão* = de *elemento*. Opacity

**Comentários**

O valor padrão é 1.0.

*Atributo padrão da VML*

**Exemplo**

O preenchimento da forma será de 50% transparente.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill opacity="50%" color="red"/>
   </v:shape>
```



 

 