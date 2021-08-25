---
title: Atributo de origem (sombra) (VML)
description: Atributo de origem (sombra) (VML)
ms.assetid: acef5134-dad6-4ba6-9d70-a9f56cd8c5ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1776b0d8a857a3247543eae13d280d023585229d27c04a576420003ea53920
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959176"
---
# <a name="origin-attribute-shadowvml"></a>Atributo de origem (sombra) (VML)

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Define o centro da sombra. Leitura/gravação. **VgVector2D**.

**Aplica-se a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxe de marca**

<v: *elemento* Origin = " *expressão* " >

**Sintaxe do script**

*elemento* . Origin = "*expressão*"

*expressão* = de *elemento*. Origin

**Comentários**

Um par de valores fracionários da forma, variando de 50% a-50%. O valor padrão é 0,0.

*Atributo padrão da VML*

**Exemplo**

A sombra tem uma origem que está de 20% abaixo e 20% à direita da origem da forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" origin="20%,20%"/>
   </v:shape>
```



 

 