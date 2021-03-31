---
title: Atributo src (Stroke) (VML)
description: Atributo src (Stroke) (VML)
ms.assetid: dac6b5b7-2038-4534-97e9-a1340102777e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5833b24abf0f16c6e17fa3319931565ee6c232
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641160"
---
# <a name="src-attribute-strokevml"></a>Atributo src (Stroke) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define a imagem de origem a ser carregada para um preenchimento de traço. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Pincel](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *Element* src = " *expressão* " >

**Sintaxe do script**

*Element* . src = "*expressão*"

*expressão* = de *elemento*. src

**Comentários**

URL para uma imagem a ser carregada para preenchimentos de imagem e padrão. Esse atributo sempre deve estar presente e apontar para dados de imagem válidos para que uma imagem apareça. Se esse atributo aparecer sozinho, ou seja, não **href** ou **title**, a imagem será vinculada.

*Atributo padrão da VML*

**Exemplo**

O traço é criado com a imagem especificada pelo arquivo de cylinder.gif.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke src="cylinder.gif" filltype="tile" width="10pt"/>
   </v:shape>
```





 

 