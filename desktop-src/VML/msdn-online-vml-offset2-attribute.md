---
title: Atributo Offset2 de VML
description: Atributo Offset2 de VML
ms.assetid: a2792992-71a1-4932-8180-82ca38bd6dd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b5253e1a27ce8292ee5fc4ce49259db9512a5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499132"
---
# <a name="vml-offset2-attribute"></a>Atributo Offset2 de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina um segundo deslocamento. Leitura/gravação. **VgVector2D**.

**Aplica-se a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxe de marca**

<v: *Element* offset2 = " *expressão* " >

**Sintaxe do script**

*Element* . offset2 = "*expressão*"

*expressão* = de *elemento*. offset2

**Comentários**

O padrão para um segundo deslocamento para o valor x é 0 e o padrão para o valor y é 0. Os valores são uma medida absoluta ou um valor fracionário de Shape. Se fracionários, os valores variam de 50% a-50%.

Use um segundo deslocamento para criar efeitos de sombra especiais. Consulte o atributo [Type](type-attribute--shadow--vml.md) para obter mais informações sobre os segundos deslocamentos.

*Atributo padrão da VML*

**Exemplo**

Uma sombra dupla é criada para a forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="red" color2="blue"
   offset="50%" offset2="-20%" type="double"/>
   </v:shape>
```



 

 