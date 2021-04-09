---
title: Atributo ForceDash de VML
description: Atributo ForceDash de VML
ms.assetid: 659e99bb-16d9-425a-97b1-7767c065ec41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bcec4a694a6449412aa07ec69aa9a817aa917c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007858"
---
# <a name="vml-forcedash-attribute"></a>Atributo ForceDash de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se um contorno tracejado é usado para desenhar uma forma quando uma forma não tem linha ou preenchimento. Leitura/gravação. **VgTriState**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* o:forcedash = " *expressão* " >

**Comentários**

Usado pelos espaços reservados do Microsoft PowerPoint para desenhar um contorno tracejado quando não há nenhuma linha e nenhum preenchimento para uma forma. O padrão é **False**. Se **for true**, um contorno tracejado será usado para indicar um espaço reservado.

*Atributo de extensões de Microsoft Office*

**Exemplo**

Uma linha tracejada será usada para renderizar a forma se não houver nenhuma linha ou preenchimento.


```HTML
   <v:rect id=myrect fillcolor="red" o:forcedash="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 