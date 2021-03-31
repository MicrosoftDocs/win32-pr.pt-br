---
title: Atributo de classe VML
description: Atributo de classe VML
ms.assetid: 4030b8b7-fcc9-4153-8004-81935a347a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94bdc723ba9be335afc43023ab89b88834c55474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917468"
---
# <a name="vml-class-attribute"></a>Atributo de classe VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Refere-se a uma definição de um estilo CSS. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* Class = " *expression* " >

**Sintaxe do script**

*Element* . ClassName = "*expressão*"

*expressão* = de *Element*. ClassName

**Comentários**

O atributo de **classe** é semelhante ao atributo de **classe** HTML padrão usado com folhas de estilo CSS.

Observe que **ClassName** é usado em vez de **Class** para scripts. Observe também que para scripts, o **ClassName** só pode ser lido; a alteração do valor de **ClassName** não alterará a renderização da forma.

*Atributo padrão da VML*

**Consulte também**

[Forma](shape-element--vml.md)

**Exemplo**

Uma classe para **largura** é criada com o estilo


```HTML
   .narrowstyle {width:50;height:100}
```



Em seguida, a largura é referenciada incluindo o estilo. Observe que a largura andheight não está definida no atributo **Style** , mas será definida pelo estilo.


```HTML
   <v:shape id="rect01" class="narrowstyle"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



Observe que a **classe** se aplica somente aos atributos do tipo CSS.

 

 