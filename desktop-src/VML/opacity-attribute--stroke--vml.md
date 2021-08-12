---
title: Atributo de opacidade (traço) (VML)
description: Atributo de opacidade (traço) (VML)
ms.assetid: 8f1968ba-0d0b-4cd6-9332-74755e891783
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2f457ee73ffdccd589f5ab3b4d89c5ce4c05f871a71572c1f04b2ddef5de4a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596767"
---
# <a name="opacity-attribute-strokevml"></a>Atributo de opacidade (traço) (VML)

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Define a quantidade de transparência de um traço. Leitura/gravação. **VgFraction**.

**Aplica-se a**

[Pincel](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *elemento* Opacity = " *expressão* " >

**Sintaxe do script**

*elemento* . Opacity = "*expressão*"

*expressão* = de *elemento*. Opacity

**Comentários**

O valor padrão é 1.0.

*Atributo padrão da VML*

**Exemplo**

O traço é de 50% transparente.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke opacity="50%"/>
   </v:shape>
```



 

 