---
title: Atributo de classe VML
description: Atributo de classe VML
ms.assetid: 4030b8b7-fcc9-4153-8004-81935a347a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ada95b56430dacd09801a9aaa200c92abab064bbbb5732b369372de63c34de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602174"
---
# <a name="vml-class-attribute"></a>Atributo de classe VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Refere-se a uma definição de um estilo CSS. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *element* class=" *expressão* ">

**Sintaxe do script**

*expressão element* .classname=""

*expressão* = *elemento*.classname

**Comentários**

O **atributo** de classe é semelhante ao atributo de **classe** HTML padrão usado com folhas de estilos CSS.

Observe que **classname** é usado em vez da **classe** para scripts. Observe também que, para scripts, **o nome de classe** só pode ser lido; alterar o valor de **classname** não alterará a renderização da forma.

*Atributo padrão VML*

**Consulte também**

[Forma](shape-element--vml.md)

**Exemplo**

Uma classe para **largura** é criada com o estilo


```HTML
   .narrowstyle {width:50;height:100}
```



Em seguida, a largura é referenciada incluindo o estilo . Observe que width andheight não está definido no atributo **de estilo,** mas será definido pelo estilo.


```HTML
   <v:shape id="rect01" class="narrowstyle"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



Observe que **Class só** se aplica a atributos do tipo CSS.

 

 